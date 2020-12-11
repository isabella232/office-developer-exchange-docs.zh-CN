---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 11/25/2020
ms.audience: Developer
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。
localization_priority: Priority
ms.openlocfilehash: a7b1d2a099cf5f3c95f8453605363de12ff33c54
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603825"
---
<!-- markdownlint-disable MD025 -->
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="41803-103">使用 OAuth 对 EWS 应用程序进行身份验证</span><span class="sxs-lookup"><span data-stu-id="41803-103">Authenticate an EWS application by using OAuth</span></span>
<!-- markdownlint-enable MD025 -->

<span data-ttu-id="41803-104">了解如何一起使用 OAuth 身份验证和 EWS 托管 API 应用程序。</span><span class="sxs-lookup"><span data-stu-id="41803-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>

<span data-ttu-id="41803-105">可使用 Azure Active Directory 提供的 OAuth 身份验证服务来启用 EWS 托管 API 应用程序，以便在 Office 365 中访问 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="41803-105">You can use the OAuth authentication service provided by Azure Active Directory to enable your EWS Managed API applications to access Exchange Online in Office 365.</span></span> <span data-ttu-id="41803-106">若要将 OAuth 用于你的应用程序，需要执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="41803-106">To use OAuth with your application you will need to:</span></span>

1. <span data-ttu-id="41803-107">使用 Azure Active Directory [注册应用程序](#register-your-application)。</span><span class="sxs-lookup"><span data-stu-id="41803-107">[Register your application](#register-your-application) with Azure Active Directory.</span></span>
1. <span data-ttu-id="41803-108">[添加代码以获取身份验证令牌](#add-code-to-get-an-authentication-token)，以获取来自令牌服务器的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="41803-108">[Add code to get an authentication token](#add-code-to-get-an-authentication-token) to get an authentication token from a token server.</span></span>
1. <span data-ttu-id="41803-109">对你发送的[ EWS 请求添加身份验证令牌](#add-an-authentication-token-to-ews-requests)。</span><span class="sxs-lookup"><span data-stu-id="41803-109">[Add an authentication token to EWS requests](#add-an-authentication-token-to-ews-requests) that you send.</span></span>

> [!NOTE]
> <span data-ttu-id="41803-110">对 EWS 的 OAuth 身份验证仅在作为 Microsoft 365 一部分的 Exchange Online 中可用。</span><span class="sxs-lookup"><span data-stu-id="41803-110">OAuth authentication for EWS is only available in Exchange Online as part of Microsoft 365.</span></span> <span data-ttu-id="41803-111">使用 OAuth 的 EWS 应用程序必须通过 Azure Active Directory 注册。</span><span class="sxs-lookup"><span data-stu-id="41803-111">EWS applications that use OAuth must be registered with Azure Active Directory.</span></span>

<span data-ttu-id="41803-112">若要使用本文中的代码，你需要以下访问权限：</span><span class="sxs-lookup"><span data-stu-id="41803-112">To use the code in this article, you will need to have access to the following:</span></span>

- <span data-ttu-id="41803-113">具有 Exchange Online 邮箱的 Office 365 帐户。</span><span class="sxs-lookup"><span data-stu-id="41803-113">A Microsoft 365 account with an Exchange Online mailbox.</span></span> <span data-ttu-id="41803-114">如果没有 Office 365 帐户，可 [注册 Office 365 开发人员计划](https://developer.microsoft.com/microsoft-365/dev-program)，以获取免费的 Office 365 订阅。</span><span class="sxs-lookup"><span data-stu-id="41803-114">If you do not have a Microsoft 365 account, you can [sign up for the Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) to get a free Microsoft 365 subscription.</span></span>
- <span data-ttu-id="41803-115">[.NET 的 Microsoft 身份验证库](/dotnet/api/microsoft.identity.client)。</span><span class="sxs-lookup"><span data-stu-id="41803-115">The [Microsoft Authentication Library for .NET](/dotnet/api/microsoft.identity.client).</span></span>
- <span data-ttu-id="41803-116">[EWS Managed API](https://github.com/officedev/ews-managed-api)。</span><span class="sxs-lookup"><span data-stu-id="41803-116">The [EWS Managed API](https://github.com/officedev/ews-managed-api).</span></span>

<span data-ttu-id="41803-117">可以用于访问 Exchange Online 中的 EWS API 的 OAuth 权限类型分为两种。</span><span class="sxs-lookup"><span data-stu-id="41803-117">There are two types of OAuth permissions that can be used to access EWS APIs in Exchange Online.</span></span> <span data-ttu-id="41803-118">继续教程前，需要选择要使用的特定权限类型。</span><span class="sxs-lookup"><span data-stu-id="41803-118">Before you proceed with the tutorial, you will need to choose the specific permission type to use.</span></span>

- <span data-ttu-id="41803-119">**委派权限** 供已有用户登录的应用使用。</span><span class="sxs-lookup"><span data-stu-id="41803-119">**Delegated permissions** are used by apps that have a signed-in user present.</span></span> <span data-ttu-id="41803-120">对于这些应用，用户或管理员同意应用请求的权限，并且应用可在调用 API 时充当已登录的用户。</span><span class="sxs-lookup"><span data-stu-id="41803-120">For these apps, either the user or an administrator consents to the permissions that the app requests and the app can act as the signed-in user when making API calls.</span></span>
- <span data-ttu-id="41803-121">**应用程序权限** 由无需用户登录即可运行的应用使用；例如，作为后台服务或守护程序运行的应用，并且可以访问多个邮箱。</span><span class="sxs-lookup"><span data-stu-id="41803-121">**Application permissions** are used by apps that run without a signed-in user present; for example, apps that run as background services or daemons and can access multiple mailboxes.</span></span>

## <a name="register-your-application"></a><span data-ttu-id="41803-122">注册应用程序</span><span class="sxs-lookup"><span data-stu-id="41803-122">Register your application</span></span>

<span data-ttu-id="41803-123">若要使用 OAuth，应用程序必须具有由 Azure Active Directory 发布的应用程序 ID。</span><span class="sxs-lookup"><span data-stu-id="41803-123">To use OAuth, an application must have an application ID issued by Azure Active Directory.</span></span> <span data-ttu-id="41803-124">在本教程中，我们假定应用程序是一个控制台应用程序，因此需要通过 Azure Active Directory 将应用程序注册为公共客户端。</span><span class="sxs-lookup"><span data-stu-id="41803-124">In this tutorial, it is assumed that the application is a console application, so you need to register your application as a public client with Azure Active Directory.</span></span> <span data-ttu-id="41803-125">可在 Azure Active Directory 管理中心或使用 Microsoft Graph 注册应用程序。</span><span class="sxs-lookup"><span data-stu-id="41803-125">You can register an application in the Azure Active Directory admin center or by using Microsoft Graph.</span></span>

1. <span data-ttu-id="41803-126">打开浏览器，并转到 [Azure Active Directory 管理中心](https://aad.portal.azure.com)。然后，使用 **个人帐户**（亦称为“Microsoft 帐户”）或 **工作或学校帐户** 登录。</span><span class="sxs-lookup"><span data-stu-id="41803-126">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="41803-127">选择左侧导航栏中的“**Azure Active Directory**”，再选择“**管理**”下的“**应用注册**”。</span><span class="sxs-lookup"><span data-stu-id="41803-127">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

1. <span data-ttu-id="41803-128">选择“新注册”。</span><span class="sxs-lookup"><span data-stu-id="41803-128">Select **New registration**.</span></span> <span data-ttu-id="41803-129">在“注册应用”页上，按如下方式设置值。</span><span class="sxs-lookup"><span data-stu-id="41803-129">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="41803-130">将 **名称** 设置为应用的友好名称。</span><span class="sxs-lookup"><span data-stu-id="41803-130">Set **Name** to a friendly name for your app.</span></span>
    - <span data-ttu-id="41803-131">将 **受支持的帐户类型** 设置为对你的方案有意义的选择。</span><span class="sxs-lookup"><span data-stu-id="41803-131">Set **Supported account types** to the choice that makes sense for your scenario.</span></span>
    - <span data-ttu-id="41803-132">若要 **重定向 URI**，请将下拉列表更改为 **公共客户端（移动 & 桌面）** 并将值设置为 “`urn:ietf:wg:oauth:2.0:oob`”。</span><span class="sxs-lookup"><span data-stu-id="41803-132">For **Redirect URI**, change the dropdown to **Public client (mobile & desktop)** and set the value to `urn:ietf:wg:oauth:2.0:oob`.</span></span>

1. <span data-ttu-id="41803-133">选择 **“注册”**。</span><span class="sxs-lookup"><span data-stu-id="41803-133">Choose **Register**.</span></span> <span data-ttu-id="41803-134">在下一页，复制“**应用（客户端）ID**”和 **目录（租户）ID** 的值，然后保存，你将在下一步中用到它们。</span><span class="sxs-lookup"><span data-stu-id="41803-134">On the next page, copy the values of the **Application (client) ID** and **Directory (tenant) ID** and save them, you will need them later.</span></span>

### <a name="configure-for-delegated-authentication"></a><span data-ttu-id="41803-135">配置以进行委派身份验证</span><span class="sxs-lookup"><span data-stu-id="41803-135">Configure for delegated authentication</span></span>

<span data-ttu-id="41803-136">如果应用程序使用委派的身份验证，则无需进行进一步配置。</span><span class="sxs-lookup"><span data-stu-id="41803-136">If your application uses delegated authentication, no further configuration is required.</span></span> <span data-ttu-id="41803-137">[Microsoft 标识平台](/azure/active-directory/develop/v2-overview) 允许应用动态请求权限，因此无需预配置应用注册的权限。</span><span class="sxs-lookup"><span data-stu-id="41803-137">The [Microsoft identity platform](/azure/active-directory/develop/v2-overview) allows apps to request permissions dynamically, so you do not have to pre-configure permissions on the app registration.</span></span> <span data-ttu-id="41803-138">但是，在某些情况下（例如 [流代表](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)）预配置权限是必需的。</span><span class="sxs-lookup"><span data-stu-id="41803-138">However, in some scenarios (like the [on-behalf-of flow](/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow)) pre-configuring permissions is required.</span></span> <span data-ttu-id="41803-139">使用以下步骤预配置 EWS 权限。</span><span class="sxs-lookup"><span data-stu-id="41803-139">Use the following steps to pre-configure EWS permissions.</span></span>

1. <span data-ttu-id="41803-140">在“**管理**”下的左侧导航中，选择 “**清单**”。</span><span class="sxs-lookup"><span data-stu-id="41803-140">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="41803-141">找到清单中的“`requiredResourceAccess`”属性，然后在方括号内添加以下内容（`[]`）：</span><span class="sxs-lookup"><span data-stu-id="41803-141">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="41803-142">选择“**保存**”。</span><span class="sxs-lookup"><span data-stu-id="41803-142">Select **Save**.</span></span>

1. <span data-ttu-id="41803-143">在“**管理**”下选择 “**API 权限**”。</span><span class="sxs-lookup"><span data-stu-id="41803-143">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="41803-144">确认列出了 **EWS.AccessAsUser.All** 权限。</span><span class="sxs-lookup"><span data-stu-id="41803-144">Confirm that the **EWS.AccessAsUser.All** permission is listed.</span></span>

### <a name="configure-for-app-only-authentication"></a><span data-ttu-id="41803-145">配置仅应用身份验证</span><span class="sxs-lookup"><span data-stu-id="41803-145">Configure for app-only authentication</span></span>

<span data-ttu-id="41803-146">若要使用“应用程序权限”，请执行以下额外步骤。</span><span class="sxs-lookup"><span data-stu-id="41803-146">To use application permissions, follow these additional steps.</span></span>

1. <span data-ttu-id="41803-147">在“**管理**”下的左侧导航中，选择 “**清单**”。</span><span class="sxs-lookup"><span data-stu-id="41803-147">Select **Manifest** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="41803-148">找到清单中的“`requiredResourceAccess`”属性，然后在方括号内添加以下内容（`[]`）：</span><span class="sxs-lookup"><span data-stu-id="41803-148">Locate the `requiredResourceAccess` property in the manifest, and add the following inside the square brackets (`[]`):</span></span>

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

1. <span data-ttu-id="41803-149">选择“**保存**”。</span><span class="sxs-lookup"><span data-stu-id="41803-149">Select **Save**.</span></span>

1. <span data-ttu-id="41803-150">在“**管理**”下选择 “**API 权限**”。</span><span class="sxs-lookup"><span data-stu-id="41803-150">Select **API permissions** under **Manage**.</span></span> <span data-ttu-id="41803-151">确认列出了 **full_access_as_app** 权限。</span><span class="sxs-lookup"><span data-stu-id="41803-151">Confirm that the **full_access_as_app** permission is listed.</span></span>

1. <span data-ttu-id="41803-152">选择“**对组织授予管理员许可**”，并接受许可对话框。</span><span class="sxs-lookup"><span data-stu-id="41803-152">Select **Grant admin consent for org** and accept the consent dialog.</span></span>

1. <span data-ttu-id="41803-153">在“**管理**”下的左侧导航中，选择“**证书 & 机密**”。</span><span class="sxs-lookup"><span data-stu-id="41803-153">Select **Certificates & Secrets** in the left-hand navigation under **Manage**.</span></span>

1. <span data-ttu-id="41803-154">选择“**新建客户端机密**”，并输入简短说明，然后选择“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="41803-154">Select **New client secret**, enter a short description and select **Add**.</span></span>

1. <span data-ttu-id="41803-155">复制新添加客户端机密的“**值**”并保存，你等下会用到它。</span><span class="sxs-lookup"><span data-stu-id="41803-155">Copy the **Value** of the newly added client secret and save it, you will need it later.</span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="41803-156">添加代码以获取身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="41803-156">Add code to get an authentication token</span></span>

<span data-ttu-id="41803-157">以下的代码片段显示了如何使用 Microsoft 身份验证库获取代理权限和应用程序权限的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="41803-157">The following code snippets show how to use the Microsoft Authentication Library to get authentication tokens for delegated permissions and application permissions.</span></span> <span data-ttu-id="41803-158">这些片段假定执行身份验证请求所需的信息都存储在了应用程序的 **App.config** 文件中。</span><span class="sxs-lookup"><span data-stu-id="41803-158">These snippets assume that the information required to make the authentication request is stored in the application's **App.config** file.</span></span> <span data-ttu-id="41803-159">这些示例不包括错误检查，请参阅“[代码示例](#code-samples)”，查看完整代码。</span><span class="sxs-lookup"><span data-stu-id="41803-159">These examples do not include error checking, see the [Code samples](#code-samples) for the complete code.</span></span>

### <a name="get-a-token-with-delegated-auth"></a><span data-ttu-id="41803-160">获取委派身份验证的令牌</span><span class="sxs-lookup"><span data-stu-id="41803-160">Get a token with delegated auth</span></span>

```cs
// Using Microsoft.Identity.Client 4.22.0

// Configure the MSAL client to get tokens
var pcaOptions = new PublicClientApplicationOptions
{
    ClientId = ConfigurationManager.AppSettings["appId"],
    TenantId = ConfigurationManager.AppSettings["tenantId"]
};

var pca = PublicClientApplicationBuilder
    .CreateWithApplicationOptions(pcaOptions).Build();

// The permission scope required for EWS access
var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

// Make the interactive token request
var authResult = await pca.AcquireTokenInteractive(ewsScopes).ExecuteAsync();
```

### <a name="get-a-token-with-app-only-auth"></a><span data-ttu-id="41803-161">获取仅限应用的身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="41803-161">Get a token with app-only auth</span></span>

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
var authResult = await cca.AcquireTokenForClient(ewsScopes).ExecuteAsync();
```

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="41803-162">向 EWS 请求添加身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="41803-162">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="41803-163">收到 **AuthenticationResult** 对象后，可以使用 **AccessToken** 属性来获取令牌服务发出的令牌。</span><span class="sxs-lookup"><span data-stu-id="41803-163">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span>

```cs
// Configure the ExchangeService with the access token
var ewsClient = new ExchangeService();
ewsClient.Url = new Uri("https://outlook.office365.com/EWS/Exchange.asmx");
ewsClient.Credentials = new OAuthCredentials(authResult.AccessToken);
```

<span data-ttu-id="41803-164">若要使用“应用程序权限”，还需要显式模拟想要访问的邮箱。</span><span class="sxs-lookup"><span data-stu-id="41803-164">To use application permissions, you will also need to explicitly impersonate a mailbox that you would like to access.</span></span>

```cs
//Impersonate the mailbox you'd like to access.
ewsClient.ImpersonatedUserId = new ImpersonatedUserId(ConnectingIdType.SmtpAddress, "test@demotenant.onmicrosoft.com");
```

## <a name="code-samples"></a><span data-ttu-id="41803-165">代码示例</span><span class="sxs-lookup"><span data-stu-id="41803-165">Code samples</span></span>

### <a name="delegated-authentication"></a><span data-ttu-id="41803-166">委派身份验证</span><span class="sxs-lookup"><span data-stu-id="41803-166">Delegated authentication</span></span>

<span data-ttu-id="41803-167">下面是完整的代码示例，该示例演示了如何使用“委派身份验证”，构建被 OAuth 身份验证通过的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="41803-167">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using delegated authentication.</span></span>

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

            // Configure the MSAL client to get tokens
            var pcaOptions = new PublicClientApplicationOptions
            {
                ClientId = ConfigurationManager.AppSettings["appId"],
                TenantId = ConfigurationManager.AppSettings["tenantId"]
            };

            var pca = PublicClientApplicationBuilder
                .CreateWithApplicationOptions(pcaOptions).Build();

            // The permission scope required for EWS access
            var ewsScopes = new string[] { "https://outlook.office365.com/EWS.AccessAsUser.All" };

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

### <a name="app-only-authentication"></a><span data-ttu-id="41803-168">仅限应用的身份验证</span><span class="sxs-lookup"><span data-stu-id="41803-168">App-only authentication</span></span>

<span data-ttu-id="41803-169">仅限应用的身份验证”，构建被 OAuth 身份验证通过的 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="41803-169">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request using app-only authentication.</span></span>

> [!NOTE]
> <span data-ttu-id="41803-170">使用模拟时，必须始终使用 X-AnchorMailbox 请求页眉，该页眉应设置为模拟邮箱的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="41803-170">When using impersonation you must always use the X-AnchorMailbox request header, which should be set to the SMTP address of the impersonated mailbox.</span></span>

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

<span data-ttu-id="41803-171">两种情况下的示例代码都需要 **App.config** 文件，其中包含以下条目：</span><span class="sxs-lookup"><span data-stu-id="41803-171">The sample code in both cases requires an **App.config** file with the following entries:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="41803-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41803-172">See also</span></span>

- [<span data-ttu-id="41803-173">在 Exchange 中的身份验证和 EWS</span><span class="sxs-lookup"><span data-stu-id="41803-173">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)
