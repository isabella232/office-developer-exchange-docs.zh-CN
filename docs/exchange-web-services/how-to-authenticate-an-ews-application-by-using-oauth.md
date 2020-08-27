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
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="3f241-103">使用 OAuth 对 EWS 应用程序进行身份验证</span><span class="sxs-lookup"><span data-stu-id="3f241-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="3f241-104">了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。</span><span class="sxs-lookup"><span data-stu-id="3f241-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="3f241-105">可使用 Azure Active Directory 提供的 OAuth 身份验证服务来启用 EWS 托管 API 应用程序，以便在 Office 365 中访问 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="3f241-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="3f241-106">若要将 OAuth 用于你的应用程序，需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="3f241-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="3f241-107">使用 Azure Active Directory [注册应用程序](#register-your-application)。</span><span class="sxs-lookup"><span data-stu-id="3f241-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>

2. <span data-ttu-id="3f241-108">[添加代码以获取身份验证令牌](#add-code-to-get-an-authentication-token)，以获取来自令牌服务器的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="3f241-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>

3. <span data-ttu-id="3f241-109">对你发送的[ EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。</span><span class="sxs-lookup"><span data-stu-id="3f241-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="3f241-110">对 EWS 的 OAuth 身份验证仅在作为 Office 365 一部分的 Exchange 中可用。</span><span class="sxs-lookup"><span data-stu-id="3f241-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="3f241-111">使用 OAuth 的 EWS 应用程序必须通过 Azure Active Directory 注册。</span><span class="sxs-lookup"><span data-stu-id="3f241-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="3f241-112">若要使用本文中的代码，你需要以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="3f241-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="3f241-113">具有 Exchange Online 邮箱的 Office 365 帐户。</span><span class="sxs-lookup"><span data-stu-id="3f241-113">An Office 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="3f241-114">如果没有 Office 365 帐户，可 [注册 Office 365 开发人员计划](https://developer.microsoft.com/office/dev-program)，以获取免费的 Office 365 订阅。</span><span class="sxs-lookup"><span data-stu-id="3f241-114">If you do not have an Office 365 account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

- <span data-ttu-id="3f241-115">[.NET 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client?view=azure-dotnet)。</span><span class="sxs-lookup"><span data-stu-id="3f241-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client?view=azure-dotnet).</span></span>

- <span data-ttu-id="3f241-116">[EWS Managed API](https://github.com/officedev/ews-managed-api)。</span><span class="sxs-lookup"><span data-stu-id="3f241-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>


<span data-ttu-id="3f241-117">可以用于访问 Exchange Online 中的 EWS API 的 OAuth 权限类型分为两种。</span><span class="sxs-lookup"><span data-stu-id="3f241-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="3f241-118">继续教程前，需要选择要使用的特定权限类型。</span><span class="sxs-lookup"><span data-stu-id="3f241-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

* <span data-ttu-id="3f241-119">**委派权限**供已有用户登录的应用使用。</span><span class="sxs-lookup"><span data-stu-id="3f241-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="3f241-120">对于这些应用，用户或管理员同意应用请求的权限，并且应用可在调用 API 时充当已登录的用户。</span><span class="sxs-lookup"><span data-stu-id="3f241-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span> 
* <span data-ttu-id="3f241-121">**应用程序权限**由无需用户登录即可运行的应用使用；例如，作为后台服务或守护程序运行的应用，并且可以访问多个邮箱。</span><span class="sxs-lookup"><span data-stu-id="3f241-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="3f241-122">注册应用程序</span><span class="sxs-lookup"><span data-stu-id="3f241-122">Register your application</span></span>

<span data-ttu-id="3f241-123">若要使用 OAuth，应用程序必须具有由 Azure Active Directory 发布的应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="3f241-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="3f241-124">在本教程中，我们假定应用程序是一个控制台应用程序，因此需要通过 Azure Active Directory 将应用程序注册为公共客户端。</span><span class="sxs-lookup"><span data-stu-id="3f241-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span>

1. <span data-ttu-id="3f241-125">打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用**个人帐户**（亦称为“Microsoft 帐户”）或**工作或学校帐户**登录。</span><span class="sxs-lookup"><span data-stu-id="3f241-125">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="3f241-126">选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-126">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="3f241-127">选择“新注册”\*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="3f241-127">Select **New registration**.</span></span> <span data-ttu-id="3f241-128">在“注册应用”\*\*\*\* 页上，按如下方式设置值。</span><span class="sxs-lookup"><span data-stu-id="3f241-128">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="3f241-129">将 **名称** 设置为应用的友好名称。</span><span class="sxs-lookup"><span data-stu-id="3f241-129">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="3f241-130">将 **受支持的帐户类型** 设置为对你的方案有意义的选择。</span><span class="sxs-lookup"><span data-stu-id="3f241-130">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="3f241-131">若要 **重定向 URI**，请将下拉列表更改为 **公共客户端（移动 & 桌面）** 并将值设置为 “`urn:ietf:wg:oauth:2.0:oob`”。</span><span class="sxs-lookup"><span data-stu-id="3f241-131">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="3f241-132">选择 **“注册”**。</span><span class="sxs-lookup"><span data-stu-id="3f241-132">Choose **Register**.</span></span> <span data-ttu-id="3f241-133">在下一页，复制“**应用（客户端）ID**”的值，然后保存，你将在下一步中用到它。</span><span class="sxs-lookup"><span data-stu-id="3f241-133">On the next page, copy the value of the **Application (client) ID** and save it, you will need it later.</span></span>

1. <span data-ttu-id="3f241-134">在“**管理**”下的左侧导航中，选择 “**API 权限**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-134">Select **API permissions** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="3f241-135">选择 “**添加权限**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-135">Select **Add a permission**.</span></span> <span data-ttu-id="3f241-136">在 “\*\* 请求 API 权限**”页面上，选择“**受支持的旧版 API\*\*” 下的 **Exchange**。</span><span class="sxs-lookup"><span data-stu-id="3f241-136">On the **Request API permissions** page, select **Exchange** under **Supported legacy APIs**.</span></span> 

1. <span data-ttu-id="3f241-137">若要使用委派权限，请选择“**委派权限**”，然后选择 **EWS** 下的 **EWS.AccessAsUser.All**。</span><span class="sxs-lookup"><span data-stu-id="3f241-137">To use Delegated permissions, select **Delegated permissions** and then select **EWS.AccessAsUser.All** under **EWS**.</span></span> <span data-ttu-id="3f241-138">点击“**添加权限**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-138">Click on **Add permissions**.</span></span> 

<span data-ttu-id="3f241-139">若要使用“应用程序权限”，请执行以下额外步骤。</span><span class="sxs-lookup"><span data-stu-id="3f241-139">To use Application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="3f241-140">选择“**应用程序权限**”， 然后选择 **full_access_as_app**。</span><span class="sxs-lookup"><span data-stu-id="3f241-140">Select **Application permissions** and then select **full_access_as_app**.</span></span> <span data-ttu-id="3f241-141">点击“**添加权限**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-141">Click on **Add permissions**.</span></span>

1. <span data-ttu-id="3f241-142">选择“**对组织授予管理员许可**”，并接受许可对话框。</span><span class="sxs-lookup"><span data-stu-id="3f241-142">Select **Grant admin consent for org** and accept the consent dialog.</span></span> 

1. <span data-ttu-id="3f241-143">在“**管理**”下的左侧导航中，选择“**证书 & 机密**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-143">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span> 

1. <span data-ttu-id="3f241-144">选择“**新建客户端机密**”，并输入简短说明，然后选择“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="3f241-144">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="3f241-145">复制新添加客户端机密的“**值**”并保存，你等下会用到它。</span><span class="sxs-lookup"><span data-stu-id="3f241-145">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span> 

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="3f241-146">添加代码以获取身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="3f241-146">Add code to get an authentication token</span></span>

<span data-ttu-id="3f241-147">以下的代码片段显示了如何使用 Microsoft 身份验证库获取代理权限和应用程序权限的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="3f241-147">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="3f241-148">这些片段假定执行身份验证请求所需的信息都存储在了应用程序的 **App.config** 文件中。</span><span class="sxs-lookup"><span data-stu-id="3f241-148">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="3f241-149">这些示例不包括错误检查，请参阅“[代码示例](#code-samples)”，查看完整代码。</span><span class="sxs-lookup"><span data-stu-id="3f241-149">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="3f241-150">委派权限</span><span class="sxs-lookup"><span data-stu-id="3f241-150">Delegated permissions</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="3f241-151">应用程序权限</span><span class="sxs-lookup"><span data-stu-id="3f241-151">Application permissions</span></span>

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

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="3f241-152">向 EWS 请求添加身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="3f241-152">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="3f241-153">收到 **AuthenticationResult** 对象后，可以使用 **AccessToken** 属性来获取令牌服务发出的令牌。</span><span class="sxs-lookup"><span data-stu-id="3f241-153">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="3f241-154">若要使用“应用程序权限”，还需要显式模拟想要访问的邮箱。</span><span class="sxs-lookup"><span data-stu-id="3f241-154">To use Application permissions, you will also need to explictly impersonate a mailbox that you would like to access.</span></span> 

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="3f241-155">代码示例</span><span class="sxs-lookup"><span data-stu-id="3f241-155">Code samples</span></span>

### <a name="delegated-permissions"></a><span data-ttu-id="3f241-156">委派权限</span><span class="sxs-lookup"><span data-stu-id="3f241-156">Delegated permissions</span></span>

<span data-ttu-id="3f241-157">下面是完整的代码示例，该示例演示了如何使用“委派权限”，构建被 OAuth 身份验证通过的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="3f241-157">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Delegated permissions.</span></span>

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

### <a name="application-permissions"></a><span data-ttu-id="3f241-158">应用程序权限</span><span class="sxs-lookup"><span data-stu-id="3f241-158">Application permissions</span></span>

<span data-ttu-id="3f241-159">下面是完整的代码示例，该示例演示了如何使用“应用程序权限”，构建被 OAuth 身份验证通过的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="3f241-159">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using Application permissions.</span></span>

> [!NOTE]
> <span data-ttu-id="3f241-160">使用模拟时，必须始终使用 X-AnchorMailbox 请求页眉，该页眉应设置为模拟邮箱的 SMTP。</span><span class="sxs-lookup"><span data-stu-id="3f241-160">When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP of the impersonated mailbox.</span></span>

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

<span data-ttu-id="3f241-161">两种情况下的示例代码都需要 **App.config** 文件，其中包含以下条目：</span><span class="sxs-lookup"><span data-stu-id="3f241-161">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3f241-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f241-162">See also</span></span>

- [<span data-ttu-id="3f241-163">在 Exchange 中的身份验证和 EWS</span><span class="sxs-lookup"><span data-stu-id="3f241-163">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
