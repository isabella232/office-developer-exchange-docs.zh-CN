---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何将 OAuth 身份验证与您的 EWS 托管 API 应用程序结合使用。
localization_priority: Priority
ms.openlocfilehash: e2bcb339ddac51b888660b6f982a8377591b1a29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528249"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>使用 OAuth 对 EWS 应用程序进行身份验证
<!-- markdownlint-enable MD025 -->

了解如何将 OAuth 身份验证与您的 EWS 托管 API 应用程序结合使用。

您可以使用 Azure Active Directory 提供的 OAuth 身份验证服务，以便您的 EWS 托管 API 应用程序能够访问 Office 365 中的 Exchange Online。 若要将 OAuth 与您的应用程序一起使用，您需要执行以下操作：

1. 向 Azure Active Directory[注册应用程序](#register-your-application)。

2. [添加代码以获取](#add-code-to-get-an-authentication-token)用于从令牌服务器获取身份验证令牌的身份验证令牌。

3. 向您发送的[EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。

> [!NOTE]
> EWS 的 OAuth 身份验证仅在 Exchange 中作为 Office 365 的一部分提供。 使用 OAuth 的 EWS 应用程序必须注册到 Azure Active Directory。

若要使用本文中的代码，您需要具有以下权限：

- 包含 Exchange Online 邮箱的 Office 365 帐户。 如果没有 Office 365 帐户，可以[注册 office 365 开发人员计划](https://developer.microsoft.com/office/dev-program)以获取免费的 office 365 订阅。

- [适用于 .net 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client?view=azure-dotnet)。

- [EWS 托管 API](https://github.com/officedev/ews-managed-api)。


有两种类型的 OAuth 权限可用于访问 Exchange Online 中的 EWS Api。 在继续使用教程之前，您需要选择要使用的特定权限类型。

* **委派权限**供已有用户登录的应用使用。 对于这些应用程序，用户或管理员同意应用程序请求的权限，并且应用可以在进行 API 调用时充当登录用户。 
* **应用程序权限**由在没有登录用户的情况下运行的应用程序使用;例如，作为后台服务或守护程序运行的应用程序，可以访问多个邮箱。

## <a name="register-your-application"></a>注册应用程序

若要使用 OAuth，应用程序必须具有由 Azure Active Directory 颁发的应用程序 ID。 在本教程中，假定应用程序是一个控制台应用程序，因此您需要将应用程序注册为具有 Azure Active Directory 的公共客户端。

1. 打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用**个人帐户**（亦称为“Microsoft 帐户”）或**工作或学校帐户**登录。

1. 选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。

1. 选择“新注册”****。 在“注册应用”**** 页上，按如下方式设置值。

    - 将**名称**设置为您的应用程序的友好名称。
    - 将**支持的帐户类型**设置为适合您的方案的选项。
    - 对于 "**重定向 URI**"，将 dropdown 更改为 "**公用客户端（移动 & 桌面）** "，并将值设置为 `urn:ietf:wg:oauth:2.0:oob` 。

1. 选择“注册”****。 在下一页上，复制**应用程序（客户端） ID**的值并将其保存，稍后将需要它。

1. 在 "**管理**" 下的左侧导航栏中选择 " **API 权限**"。 

1. 选择 "**添加权限**"。 在 "**请求 API 权限**" 页面上，选择 "**受支持的旧版 api**" 下的**Exchange** 。 

1. 若要使用委派权限，请选择 "**委派权限**"，然后选择 " **EWS"。Directory.accessasuser.all**在**EWS**下。 单击 "**添加权限**"。 

若要使用应用程序权限，请执行以下附加步骤。

1. 选择 "**应用程序权限**"，然后选择 " **full_access_as_app**"。 单击 "**添加权限**"。

1. 选择 "**授予对组织的管理员同意**" 并接受 "同意" 对话框。 

1. 在 "**管理**" 下的左侧导航栏中选择 "**证书 & 密码**"。 

1. 选择 "**新建客户端密码**"，输入简短说明，然后选择 "**添加**"。

1. 复制新添加的客户端密码的**值**并将其保存，稍后将需要它。 

## <a name="add-code-to-get-an-authentication-token"></a>添加代码以获取身份验证令牌

下面的代码段演示如何使用 Microsoft 身份验证库获取委派权限和应用程序权限的身份验证令牌。 这些代码片段假定进行身份验证请求所需的信息存储在应用程序的 app.config**文件中。** 这些示例不包括错误检查，请参阅完整代码的[代码示例](#code-samples)。

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

### <a name="application-permissions"></a>应用权限

```cs
// Configure the MSAL client to get tokens
var app = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithAuthority(AzureCloudInstance.AzurePublic, ConfigurationManager.AppSettings["tenantId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"]).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office.com/.default" };

//Make the toekn request
AuthenticationResult authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();

```

## <a name="add-an-authentication-token-to-ews-requests"></a>向 EWS 请求添加身份验证令牌

在收到**AuthenticationResult**对象之后，可以使用**AccessToken**属性获取令牌服务所颁发的令牌。

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

若要使用应用程序权限，您还需要明确模拟您要访问的邮箱。 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a>代码示例

### <a name="delegated-permissions"></a>委派权限

下面是完整的代码示例，该示例演示如何使用委派权限创建通过 OAuth 身份验证的 EWS 请求。

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

### <a name="application-permissions"></a>应用权限

下面是完整的代码示例，演示如何使用应用程序权限创建通过 OAuth 身份验证的 EWS 请求。

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

两种情况下的示例代码都需要具有以下条目的**app.config**文件：

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

- [Exchange 中的身份验证和 EWS](authentication-and-ews-in-exchange.md)
