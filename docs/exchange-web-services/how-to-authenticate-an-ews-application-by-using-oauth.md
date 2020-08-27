---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。
localization_priority: Priority
ms.openlocfilehash: 795cbcc3dd1c895850086ebf0e23da905c1c99b7
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254963"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>使用 OAuth 对 EWS 应用程序进行身份验证
<!-- markdownlint-enable MD025 -->

了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。

可使用 Azure Active Directory 提供的 OAuth 身份验证服务来启用 EWS 托管 API 应用程序，以便在 Office 365 中访问 Exchange Online。 若要将 OAuth 用于你的应用程序，需要执行以下操作：

1. 使用 Azure Active Directory [注册应用程序](#register-your-application)。

2. [添加代码以获取身份验证令牌](#add-code-to-get-an-authentication-token)，以获取来自令牌服务器的身份验证令牌。

3. 对你发送的[ EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。

> [!NOTE]
> 对 EWS 的 OAuth 身份验证仅在作为 Office 365 一部分的 Exchange 中可用。 使用 OAuth 的 EWS 应用程序必须通过 Azure Active Directory 注册。

若要使用本文中的代码，你需要以下访问权限：

- 具有 Exchange Online 邮箱的 Office 365 帐户。 如果没有 Office 365 帐户，可 [注册 Office 365 开发人员计划](https://developer.microsoft.com/office/dev-program)，以获取免费的 Office 365 订阅。

- [.NET 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client?view=azure-dotnet)。

- [EWS Managed API](https://github.com/officedev/ews-managed-api)。


可以用于访问 Exchange Online 中的 EWS API 的 OAuth 权限类型分为两种。 继续教程前，需要选择要使用的特定权限类型。

* **委派权限**供已有用户登录的应用使用。 对于这些应用，用户或管理员同意应用请求的权限，并且应用可在调用 API 时充当已登录的用户。 
* **应用程序权限**由无需用户登录即可运行的应用使用；例如，作为后台服务或守护程序运行的应用，并且可以访问多个邮箱。

## <a name="register-your-application"></a>注册应用程序

若要使用 OAuth，应用程序必须具有由 Azure Active Directory 发布的应用程序 ID。 在本教程中，我们假定应用程序是一个控制台应用程序，因此需要通过 Azure Active Directory 将应用程序注册为公共客户端。

1. 打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用**个人帐户**（亦称为“Microsoft 帐户”）或**工作或学校帐户**登录。

1. 选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。

1. 选择“新注册”****。 在“注册应用”**** 页上，按如下方式设置值。

    - 将 **名称** 设置为应用的友好名称。
    - 将 **受支持的帐户类型** 设置为对你的方案有意义的选择。
    - 若要 **重定向 URI**，请将下拉列表更改为 **公共客户端（移动 & 桌面）** 并将值设置为 “`urn:ietf:wg:oauth:2.0:oob`”。

1. 选择 **“注册”**。 在下一页，复制“**应用（客户端）ID**”的值，然后保存，你将在下一步中用到它。

1. 在“**管理**”下的左侧导航中，选择 “**API 权限**”。 

1. 选择 “**添加权限**”。 在 “** 请求 API 权限**”页面上，选择“**受支持的旧版 API**” 下的 **Exchange**。 

1. 若要使用委派权限，请选择“**委派权限**”，然后选择 **EWS** 下的 **EWS.AccessAsUser.All**。 点击“**添加权限**”。 

若要使用“应用程序权限”，请执行以下额外步骤。

1. 选择“**应用程序权限**”， 然后选择 **full_access_as_app**。 点击“**添加权限**”。

1. 选择“**对组织授予管理员许可**”，并接受许可对话框。 

1. 在“**管理**”下的左侧导航中，选择“**证书 & 机密**”。 

1. 选择“**新建客户端机密**”，并输入简短说明，然后选择“**添加**”。

1. 复制新添加客户端机密的“**值**”并保存，你等下会用到它。 

## <a name="add-code-to-get-an-authentication-token"></a>添加代码以获取身份验证令牌

以下的代码片段显示了如何使用 Microsoft 身份验证库获取代理权限和应用程序权限的身份验证令牌。 这些片段假定执行身份验证请求所需的信息都存储在了应用程序的 **App.config** 文件中。 这些示例不包括错误检查，请参阅“[代码示例](#code-samples)”，查看完整代码。

### <a name="delegated-permissions"></a>委派权限

```cs
// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="application-permissions"></a>应用程序权限

```cs
// Configure the MSAL client to get tokens
var app = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"]).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/.default" };

//Make the token request
AuthenticationResult authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();

```

## <a name="add-an-authentication-token-to-ews-requests"></a>向 EWS 请求添加身份验证令牌

收到 **AuthenticationResult** 对象后，可以使用 **AccessToken** 属性来获取令牌服务发出的令牌。

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

若要使用“应用程序权限”，还需要显式模拟想要访问的邮箱。 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>代码示例

### <a name="delegated-permissions"></a>委派权限

下面是完整的代码示例，该示例演示了如何使用“委派权限”，构建被 OAuth 身份验证通过的 EWS 请求。

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }

        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            var ewsScopes = new string[] { "https://outlook.office.com/EWS.AccessAsUser.All" };

            try
            {
                // Make the interactive token request
                var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

### <a name="application-permissions"></a>应用程序权限

下面是完整的代码示例，该示例演示了如何使用“应用程序权限”，构建被 OAuth 身份验证通过的 EWS 请求。

> [!NOTE]
> 使用模拟时，必须始终使用 X-AnchorMailbox 请求页眉，该页眉应设置为模拟邮箱的 SMTP。

```cs
using System;
using System.Configuration;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;

namespace ews_oauth_samples
{
    class Program
    {
        static void Main(string[] args)
        {
            MainAsync(args).Wait();

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
        
        static async System.Threading.Tasks.Task MainAsync(string[] args)
        {
            // Configure the MSAL client to get tokens
            var ewsScopes = new string[] { "https://outlook.office.com/.default" };

            var app = ConfidentialClientApplicationBuilder.Create(ConfigurationManager.AppSettings["appId"])
                .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .Build();

            AuthenticationResult result = null;

            try
            {
                // Make the interactive token request
                result = await app.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(result.AccessToken);

                //Impersonate the mailbox you'd like to access.
                ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "test@demotenant.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach (var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex.ToString()}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex.ToString()}");
            }
        }
    }
}
```

两种情况下的示例代码都需要 **App.config** 文件，其中包含以下条目：

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.7.2" />
  </startup>
  <appSettings>
    <!-- The application ID from your app registration -->
    <add key="appId" value="YOUR_APP_ID_HERE" />
    <!-- If you registered your app to support only users in your organization, change the value
           of this key to your tenant ID -->
    <add key="tenantId" value="common"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>另请参阅

- [在 Exchange 中的身份验证和 EWS](authentication-and-ews-in-exchange.md)
