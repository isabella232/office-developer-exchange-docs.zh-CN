---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 05/17/2019
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何将 OAuth 身份验证与您的 EWS 托管 API 应用程序结合使用。
localization_priority: Priority
ms.openlocfilehash: 0375095faac918859354da026118ea4ccfd6792b
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012564"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="9741d-103">使用 OAuth 对 EWS 应用程序进行身份验证</span><span class="sxs-lookup"><span data-stu-id="9741d-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="9741d-104">了解如何将 OAuth 身份验证与您的 EWS 托管 API 应用程序结合使用。</span><span class="sxs-lookup"><span data-stu-id="9741d-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="9741d-105">您可以使用 Azure Active Directory 提供的 OAuth 身份验证服务，以便您的 EWS 托管 API 应用程序能够访问 Office 365 中的 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="9741d-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="9741d-106">若要将 OAuth 与您的应用程序一起使用，您需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="9741d-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="9741d-107">向 Azure Active Directory[注册应用程序](#register-your-application)。</span><span class="sxs-lookup"><span data-stu-id="9741d-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>

2. <span data-ttu-id="9741d-108">[添加代码以获取](#add-code-to-get-an-authentication-token)用于从令牌服务器获取身份验证令牌的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="9741d-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>

3. <span data-ttu-id="9741d-109">向您发送的[EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。</span><span class="sxs-lookup"><span data-stu-id="9741d-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="9741d-110">EWS 的 OAuth 身份验证仅在 Exchange 中作为 Office 365 的一部分提供。</span><span class="sxs-lookup"><span data-stu-id="9741d-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="9741d-111">使用 OAuth 的 EWS 应用程序必须注册到 Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="9741d-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="9741d-112">若要使用本文中的代码，您需要具有以下权限：</span><span class="sxs-lookup"><span data-stu-id="9741d-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="9741d-113">包含 Exchange Online 邮箱的 Office 365 帐户。</span><span class="sxs-lookup"><span data-stu-id="9741d-113">An Office 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="9741d-114">如果没有 Office 365 帐户，可以[注册 office 365 开发人员计划](https://developer.microsoft.com/office/dev-program)以获取免费的 office 365 订阅。</span><span class="sxs-lookup"><span data-stu-id="9741d-114">If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

- <span data-ttu-id="9741d-115">[适用于 .net 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client?view=azure-dotnet)。</span><span class="sxs-lookup"><span data-stu-id="9741d-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span></span>

- <span data-ttu-id="9741d-116">[EWS 托管 API](https://github.com/officedev/ews-managed-api)。</span><span class="sxs-lookup"><span data-stu-id="9741d-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>


<span data-ttu-id="9741d-117">有两种类型的 OAuth 权限可用于访问 Exchange Online 中的 EWS Api。</span><span class="sxs-lookup"><span data-stu-id="9741d-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="9741d-118">在继续使用教程之前，您需要选择要使用的特定权限类型。</span><span class="sxs-lookup"><span data-stu-id="9741d-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

* <span data-ttu-id="9741d-119">**委派权限**供已有用户登录的应用使用。</span><span class="sxs-lookup"><span data-stu-id="9741d-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="9741d-120">对于这些应用程序，用户或管理员同意应用程序请求的权限，并且应用可以在进行 API 调用时充当登录用户。</span><span class="sxs-lookup"><span data-stu-id="9741d-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span> 
* <span data-ttu-id="9741d-121">**应用程序权限**由在没有登录用户的情况下运行的应用程序使用;例如，作为后台服务或守护程序运行的应用程序，可以访问多个邮箱。</span><span class="sxs-lookup"><span data-stu-id="9741d-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="9741d-122">注册应用程序</span><span class="sxs-lookup"><span data-stu-id="9741d-122">Register your application</span></span>

<span data-ttu-id="9741d-123">若要使用 OAuth，应用程序必须具有由 Azure Active Directory 颁发的应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="9741d-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="9741d-124">在本教程中，假定应用程序是一个控制台应用程序，因此您需要将应用程序注册为具有 Azure Active Directory 的公共客户端。</span><span class="sxs-lookup"><span data-stu-id="9741d-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span>

1. <span data-ttu-id="9741d-125">打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用**个人帐户**（亦称为“Microsoft 帐户”）或**工作或学校帐户**登录。</span><span class="sxs-lookup"><span data-stu-id="9741d-125">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="9741d-126">选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。</span><span class="sxs-lookup"><span data-stu-id="9741d-126">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="9741d-127">选择“新注册”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9741d-127">Select **New registration**.</span></span> <span data-ttu-id="9741d-128">在“注册应用”\*\*\*\* 页上，按如下方式设置值。</span><span class="sxs-lookup"><span data-stu-id="9741d-128">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="9741d-129">将**名称**设置为您的应用程序的友好名称。</span><span class="sxs-lookup"><span data-stu-id="9741d-129">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="9741d-130">将**支持的帐户类型**设置为适合您的方案的选项。</span><span class="sxs-lookup"><span data-stu-id="9741d-130">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="9741d-131">对于 "**重定向 URI**"，将 dropdown 更改为 "**公用客户端（移动 & 桌面）** "，并将值设置为 `urn:ietf:wg:oauth:2.0:oob` 。</span><span class="sxs-lookup"><span data-stu-id="9741d-131">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="9741d-132">选择“注册”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="9741d-132">Choose **Register**.</span></span> <span data-ttu-id="9741d-133">在下一页上，复制**应用程序（客户端） ID**的值并将其保存，稍后将需要它。</span><span class="sxs-lookup"><span data-stu-id="9741d-133">On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.</span></span>

1. <span data-ttu-id="9741d-134">在 "**管理**" 下的左侧导航栏中选择 " **API 权限**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-134">Select **API permissions** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="9741d-135">选择 "**添加权限**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-135">Select **Add a permission**.</span></span> <span data-ttu-id="9741d-136">在 "**请求 API 权限**" 页面上，选择 "**受支持的旧版 api**" 下的**Exchange** 。</span><span class="sxs-lookup"><span data-stu-id="9741d-136">On the **Request API permissions** page, select **Exchange** under **Supported legacy APIs**.</span></span> 

1. <span data-ttu-id="9741d-137">若要使用委派权限，请选择 "**委派权限**"，然后选择 " **EWS"。Directory.accessasuser.all**在**EWS**下。</span><span class="sxs-lookup"><span data-stu-id="9741d-137">To use Delegated permissions, select **Delegated permissions** and then select **EWS.AccessAsUser.All** under **EWS**.</span></span> <span data-ttu-id="9741d-138">单击 "**添加权限**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-138">Click on **Add permissions**.</span></span> 

<span data-ttu-id="9741d-139">若要使用应用程序权限，请执行以下附加步骤。</span><span class="sxs-lookup"><span data-stu-id="9741d-139">To use Application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="9741d-140">选择 "**应用程序权限**"，然后选择 " **full_access_as_app**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-140">Select **Application permissions** and then select **full_access_as_app**.</span></span> <span data-ttu-id="9741d-141">单击 "**添加权限**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-141">Click on **Add permissions**.</span></span>

1. <span data-ttu-id="9741d-142">选择 "**授予对组织的管理员同意**" 并接受 "同意" 对话框。</span><span class="sxs-lookup"><span data-stu-id="9741d-142">Select **Grant admin consent for org** and accept the consent dialog.</span></span> 

1. <span data-ttu-id="9741d-143">在 "**管理**" 下的左侧导航栏中选择 "**证书 & 密码**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-143">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="9741d-144">选择 "**新建客户端密码**"，输入简短说明，然后选择 "**添加**"。</span><span class="sxs-lookup"><span data-stu-id="9741d-144">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="9741d-145">复制新添加的客户端密码的**值**并将其保存，稍后将需要它。</span><span class="sxs-lookup"><span data-stu-id="9741d-145">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span> 

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="9741d-146">添加代码以获取身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="9741d-146">Add code to get an authentication token</span></span>

<span data-ttu-id="9741d-147">下面的代码段演示如何使用 Microsoft 身份验证库获取委派权限和应用程序权限的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="9741d-147">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="9741d-148">这些代码片段假定进行身份验证请求所需的信息存储在应用程序的**App.config**文件中。</span><span class="sxs-lookup"><span data-stu-id="9741d-148">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="9741d-149">这些示例不包括错误检查，请参阅完整代码的[代码示例](#code-samples)。</span><span class="sxs-lookup"><span data-stu-id="9741d-149">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="9741d-150">委派权限</span><span class="sxs-lookup"><span data-stu-id="9741d-150">Delegated permissions</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="9741d-151">应用权限</span><span class="sxs-lookup"><span data-stu-id="9741d-151">Application permissions</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="9741d-152">向 EWS 请求添加身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="9741d-152">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="9741d-153">在收到**AuthenticationResult**对象之后，可以使用**AccessToken**属性获取令牌服务所颁发的令牌。</span><span class="sxs-lookup"><span data-stu-id="9741d-153">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="9741d-154">若要使用应用程序权限，您还需要明确模拟您要访问的邮箱。</span><span class="sxs-lookup"><span data-stu-id="9741d-154">To use Application permissions, you will also need to explictly impersonate a mailbox that you would like to access.</span></span> 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="9741d-155">代码示例</span><span class="sxs-lookup"><span data-stu-id="9741d-155">Code samples</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="9741d-156">委派权限</span><span class="sxs-lookup"><span data-stu-id="9741d-156">Delegated permissions</span></span>

<span data-ttu-id="9741d-157">下面是完整的代码示例，该示例演示如何使用委派权限创建通过 OAuth 身份验证的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="9741d-157">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Delegated permissions.</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="9741d-158">应用权限</span><span class="sxs-lookup"><span data-stu-id="9741d-158">Application permissions</span></span>

<span data-ttu-id="9741d-159">下面是完整的代码示例，演示如何使用应用程序权限创建通过 OAuth 身份验证的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="9741d-159">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Application permissions.</span></span>

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

<span data-ttu-id="9741d-160">两种情况下的示例代码都需要具有以下条目的**App.config**文件：</span><span class="sxs-lookup"><span data-stu-id="9741d-160">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9741d-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9741d-161">See also</span></span>

- [<span data-ttu-id="9741d-162">Exchange 中的身份验证和 EWS</span><span class="sxs-lookup"><span data-stu-id="9741d-162">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
