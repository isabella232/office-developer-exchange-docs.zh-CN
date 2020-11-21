---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 11/19/2020
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。
localization_priority: Priority
ms.openlocfilehash: c52b254f14cadd287a709bb68f8464e7cfe1837a
ms.sourcegitcommit: 2d16ba247a8cb4b6c8ca9941cb079f75202aae1e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/19/2020
ms.locfileid: "49356491"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a>使用 OAuth 对 EWS 应用程序进行身份验证
<!-- markdownlint-enable MD025 -->

了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。

可使用 Azure Active Directory 提供的 OAuth 身份验证服务来启用 EWS 托管 API 应用程序，以便在 Office 365 中访问 Exchange Online。 若要将 OAuth 用于你的应用程序，需要执行以下操作：

1. 使用 Azure Active Directory [注册应用程序](#register-your-application)。
1. [添加代码以获取身份验证令牌](#add-code-to-get-an-authentication-token)，以获取来自令牌服务器的身份验证令牌。
1. 对你发送的[ EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。

> [!NOTE]
> 对 EWS 的 OAuth 身份验证仅在作为 Microsoft 365 一部分的 Exchange Online 中可用。 使用 OAuth 的 EWS 应用程序必须通过 Azure Active Directory 注册。

若要使用本文中的代码，你需要以下访问权限：

- 具有 Exchange Online 邮箱的 Office 365 帐户。 如果没有 Office 365 帐户，可 [注册 Office 365 开发人员计划](https://developer.microsoft.com/microsoft-365/dev-program)，以获取免费的 Office 365 订阅。
- [.NET 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client)。
- [EWS Managed API](https://github.com/officedev/ews-managed-api)。

可以用于访问 Exchange Online 中的 EWS API 的 OAuth 权限类型分为两种。 继续教程前，需要选择要使用的特定权限类型。

- **委派权限** 供已有用户登录的应用使用。 对于这些应用，用户或管理员同意应用请求的权限，并且应用可在调用 API 时充当已登录的用户。
- **应用程序权限** 由无需用户登录即可运行的应用使用；例如，作为后台服务或守护程序运行的应用，并且可以访问多个邮箱。

## <a name="register-your-application"></a>注册应用程序

若要使用 OAuth，应用程序必须具有由 Azure Active Directory 发布的应用程序 ID。 在本教程中，我们假定应用程序是一个控制台应用程序，因此需要通过 Azure Active Directory 将应用程序注册为公共客户端。 可在 Azure Active Directory 管理中心或使用 Microsoft Graph 注册应用程序。

1. 打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用 **个人帐户**（亦称为“Microsoft 帐户”）或 **工作或学校帐户** 登录。

1. 选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。

1. 选择“新注册”。 在“注册应用”页上，按如下方式设置值。

    - 将 **名称** 设置为应用的友好名称。
    - 将 **受支持的帐户类型** 设置为对你的方案有意义的选择。
    - 若要 **重定向 URI**，请将下拉列表更改为 **公共客户端（移动 & 桌面）** 并将值设置为 “`urn:ietf:wg:oauth:2.0:oob`”。

1. 选择 **“注册”**。 在下一页，复制“**应用（客户端）ID**”和 **目录（租户）ID** 的值，然后保存，你将在下一步中用到它们。

### <a name="configure-for-delegated-authentication"></a>配置以进行委派身份验证

如果应用程序使用委派的身份验证，则无需进行进一步配置。 [Microsoft 标识平台] 允许应用动态请求权限，因此无需预配置应用注册的权限。 但是，在某些情况下（例如 [流代表](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)）预配置权限是必需的。 使用以下步骤预配置 EWS 权限。

1. 在“**管理**”下的左侧导航中，选择 “**清单**”。

1. 找到清单中的“`requiredResourceAccess`”属性，然后在方括号内添加以下内容（`[]`）：

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
                "type": "Scope"
            }
        ]
    }
    ```

1. 选择“**保存**”。

1. 在“**管理**”下选择 “**API 权限**”。 确认列出了 **EWS.AccessAsUser.All** 权限。

### <a name="configure-for-app-only-authentication"></a>配置仅应用身份验证

若要使用“应用程序权限”，请执行以下额外步骤。

1. 在“**管理**”下的左侧导航中，选择 “**清单**”。

1. 找到清单中的“`requiredResourceAccess`”属性，然后在方括号内添加以下内容（`[]`）：

    ```json
    {
        "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
        "resourceAccess": [
            {
                "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
                "type": "Role"
            }
        ]
    }
    ```

1. 选择“**保存**”。

1. 在“**管理**”下选择 “**API 权限**”。 确认列出了 **full_access_as_app** 权限。

1. 选择“**对组织授予管理员许可**”，并接受许可对话框。

1. 在“**管理**”下的左侧导航中，选择“**证书 & 机密**”。

1. 选择“**新建客户端机密**”，并输入简短说明，然后选择“**添加**”。

1. 复制新添加客户端机密的“**值**”并保存，你等下会用到它。

## <a name="add-code-to-get-an-authentication-token"></a>添加代码以获取身份验证令牌

以下的代码片段显示了如何使用 Microsoft 身份验证库获取代理权限和应用程序权限的身份验证令牌。 这些片段假定执行身份验证请求所需的信息都存储在了应用程序的 **App.config** 文件中。 这些示例不包括错误检查，请参阅“[代码示例](#code-samples)”，查看完整代码。

### <a name="get-a-token-with-delegated-auth"></a>获取委派身份验证的令牌

```cs
// Using Microsoft.Identity.Client 4.22.0
var pca = PublicClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="get-a-token-with-app-only-auth"></a>获取仅限应用的身份验证令牌

```cs
// Using Microsoft.Identity.Client 4.22.0
var cca = ConfidentialClientApplicationBuilder
    .Create(ConfigurationManager.AppSettings["appId"])
    .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
    .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
    .Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

//Make the token request
var authResult = await app.AcquireTokenForClient(ewsScopes).ExecuteAsync();
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

### <a name="delegated-authentication"></a>委派身份验证

下面是完整的代码示例，该示例演示了如何使用“委派身份验证”，构建被 OAuth 身份验证通过的 EWS 请求。

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0
            var pca = PublicClientApplicationBuilder
                .Create(ConfigurationManager.AppSettings["appId"])
                .Build();

            var ewsScopes = new string[] { "EWS.AccessAsUser.All" };

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
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
            }
        }
    }
}
```

### <a name="app-only-authentication"></a>仅限应用的身份验证

仅限应用的身份验证”，构建被 OAuth 身份验证通过的 EWS 请求。

> [!NOTE]
> 使用模拟时，必须始终使用 X-AnchorMailbox 请求页眉，该页眉应设置为模拟邮箱的 SMTP 地址。

```cs
using Microsoft.Exchange.WebServices.Data;
using Microsoft.Identity.Client;
using System;
using System.Configuration;

namespace EwsOAuth
{
    class Program
    {
        static async System.Threading.Tasks.Task Main(string[] args)
        {
            // Using Microsoft.Identity.Client 4.22.0
            var cca = ConfidentialClientApplicationBuilder
                .Create(ConfigurationManager.AppSettings["appId"])
                .WithClientSecret(ConfigurationManager.AppSettings["clientSecret"])
                .WithTenantId(ConfigurationManager.AppSettings["tenantId"])
                .Build();

            var ewsScopes = new string[] { "https://outlook.office365.com/.default" };

            try
            {
                var authResult = await cca.AcquireTokenForClient(ewsScopes)
                    .ExecuteAsync();

                // Configure the ExchangeService with the access token
                var ewsClient = new ExchangeService();
                ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
                ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
                ewsClient.ImpersonatedUserId =
                    new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "meganb@contoso.onmicrosoft.com");

                //Include x-anchormailbox header
                ewsClient.HttpHeaders.Add("X-AnchorMailbox", "meganb@contoso.onmicrosoft.com");

                // Make an EWS call
                var folders = ewsClient.FindFolders(WellKnownFolderName.MsgFolderRoot, new FolderView(10));
                foreach(var folder in folders)
                {
                    Console.WriteLine($"Folder: {folder.DisplayName}");
                }
            }
            catch (MsalException ex)
            {
                Console.WriteLine($"Error acquiring access token: {ex}");
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Error: {ex}");
            }

            if (System.Diagnostics.Debugger.IsAttached)
            {
                Console.WriteLine("Hit any key to exit...");
                Console.ReadKey();
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
    <!-- The tenant ID copied from your app registration -->
    <add key="tenantId" value="YOUR_TENANT_ID_HERE"/>
    <!-- The application's client secret from your app registration. Needed for application permission access -->
    <add key="clientSecret" value="YOUR_CLIENT_SECRET_HERE"/>
  </appSettings>
</configuration>
```

## <a name="see-also"></a>另请参阅

- [在 Exchange 中的身份验证和 EWS](authentication-and-ews-in-exchange.md)
