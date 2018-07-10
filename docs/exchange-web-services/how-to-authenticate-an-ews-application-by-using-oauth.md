---
title: EWS 应用程序通过使用 OAuth 进行身份验证
manager: sethgros
ms.date: 1/15/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何使用 EWS 托管 API 应用程序的 OAuth 身份验证。
ms.openlocfilehash: 66bbc0525ecf78407e853da0c8dcdec92791ca56
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752745"
---
# <a name="authenticate-an-ews-application-by-using-oauth"></a><span data-ttu-id="1c0d5-103">EWS 应用程序通过使用 OAuth 进行身份验证</span><span class="sxs-lookup"><span data-stu-id="1c0d5-103">Authenticate an EWS application by using OAuth</span></span>

<span data-ttu-id="1c0d5-104">了解如何使用 EWS 托管 API 应用程序的 OAuth 身份验证。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-104">Learn how to use OAuth authentication with your EWS Managed API applications.</span></span>
  
<span data-ttu-id="1c0d5-105">您可以使用 Azure Active Directory 所提供的 OAuth 身份验证服务与 Office 365 REST Api 使用的相同的身份验证模型集成 EWS 托管 API 应用程序。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-105">You can use the OAuth authentication service provided by Azure Active Directory to integrate your EWS Managed API applications with the same authentication model used by the Office 365 REST APIs.</span></span> <span data-ttu-id="1c0d5-106">若要使用 OAuth 在应用程序，您将需要：</span><span class="sxs-lookup"><span data-stu-id="1c0d5-106">To use OAuth with your application you will need to:</span></span>
  
1. <span data-ttu-id="1c0d5-107">与 Azure Active Directory 中[注册您的应用程序](#bk_register)。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-107">[Register your application](#bk_register) with Azure Active Directory.</span></span> 
    
2. <span data-ttu-id="1c0d5-108">[添加代码以获取身份验证令牌](#bk_getToken)以从令牌服务器获取身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-108">[Add code to get an authentication token](#bk_getToken) to get an authentication token from a token server.</span></span> 
    
3. <span data-ttu-id="1c0d5-109">[添加身份验证令牌 EWS 请求](#bk_useToken)所发送。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-109">[Add an authentication token to EWS requests](#bk_useToken) that you send.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1c0d5-110">EWS 的 OAuth 身份验证在 Exchange 中的 Office 365 一部分才可用。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-110">OAuth authentication for EWS is only available in Exchange as part of Office 365.</span></span> <span data-ttu-id="1c0d5-111">EWS 应用程序要求"完全访问用户邮箱"权限。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-111">EWS applications require the "Full access to user's mailbox" permission.</span></span> 
  
<span data-ttu-id="1c0d5-112">若要使用本文中的代码，您将需要有权访问以下：</span><span class="sxs-lookup"><span data-stu-id="1c0d5-112">To use the code in this article, you will need to have access to the following:</span></span>
  
- <span data-ttu-id="1c0d5-113">[Office 365 开发人员帐户](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-113">An [Office 365 developer account](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx.aspx).</span></span> <span data-ttu-id="1c0d5-114">您可以使用试用帐户来测试您的应用程序</span><span class="sxs-lookup"><span data-stu-id="1c0d5-114">You can use a trial account to test your application</span></span>
    
- <span data-ttu-id="1c0d5-115">[用于.NET 的 Azure AD 身份验证库](http://msdn.microsoft.com/zh-cn/library/office/jj573266.aspx.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-115">The [Azure AD Authentication Library for .NET](http://msdn.microsoft.com/zh-cn/library/office/jj573266.aspx.aspx).</span></span>
    
- <span data-ttu-id="1c0d5-116">[EWS 托管 API](https://github.com/officedev/ews-managed-api.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-116">[The EWS Managed API](https://github.com/officedev/ews-managed-api.aspx).</span></span>

<span data-ttu-id="1c0d5-117"><a name="bk_register"> </a></span><span class="sxs-lookup"><span data-stu-id="1c0d5-117"></span></span>

## <a name="register-your-application"></a><span data-ttu-id="1c0d5-118">注册您的应用程序</span><span class="sxs-lookup"><span data-stu-id="1c0d5-118">Register your application</span></span>

<span data-ttu-id="1c0d5-119">若要使用 OAuth，应用程序必须具有一个客户端标识符和应用程序标识应用程序的 URI。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-119">To use OAuth, an application must have a client identifier and an application URI that identifies the application.</span></span> <span data-ttu-id="1c0d5-120">如果您尚未尚未注册您的应用程序与 Azure Active Directory 服务，您将需要手动将您的应用程序添加按照下[注册您的应用程序](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)的步骤。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-120">If you have not yet registered your application with Azure Active Directory Services, you'll need to manually add your application by following the steps under [Register you app](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx).</span></span>

<span data-ttu-id="1c0d5-121"><a name="bk_getToken"> </a></span><span class="sxs-lookup"><span data-stu-id="1c0d5-121"></span></span>

## <a name="add-code-to-get-an-authentication-token"></a><span data-ttu-id="1c0d5-122">添加代码以获取身份验证令牌</span><span class="sxs-lookup"><span data-stu-id="1c0d5-122">Add code to get an authentication token</span></span>

<span data-ttu-id="1c0d5-123">用于.NET 的 Azure AD 身份验证库简化了从 Azure Active Directory 获取身份验证令牌，以便您可以在您的应用程序中使用令牌。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-123">The Azure AD Authentication Library for .NET simplifies getting an authentication token from Azure Active Directory so that you can use the token in your application.</span></span> <span data-ttu-id="1c0d5-124">您需要提供的信息获取令牌的四个部分：</span><span class="sxs-lookup"><span data-stu-id="1c0d5-124">You need to provide four pieces of information to get the token:</span></span>
  
1. <span data-ttu-id="1c0d5-125">令牌的服务器的 URI。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-125">The URI of the token server.</span></span> <span data-ttu-id="1c0d5-126">令牌的服务器是对用户进行身份验证并返回您的应用程序可用于访问 EWS 的令牌**颁发机构**。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-126">The token server is the **authority** that authenticates the user and returns a token that your application can use to access EWS.</span></span> 
    
2. <span data-ttu-id="1c0d5-127">使用 Azure Active Directory 中注册您的应用程序时创建应用程序客户端 ID。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-127">The application client ID created when you registered your application with Azure Active Directory.</span></span>
    
3. <span data-ttu-id="1c0d5-128">应用程序客户端与 Azure Active Directory 中注册您的应用程序时创建的 URI。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-128">The application client URI created when you registered your application with Azure Active Directory.</span></span>
    
4. <span data-ttu-id="1c0d5-129">EWS 服务器的 URI 和的 EWS 终结点 URI。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-129">The URI of the EWS server and the URI of the EWS endpoint.</span></span> <span data-ttu-id="1c0d5-130">对于 Exchange 作为 Office 365 的一部分，这将为`https://<server name>/ews/exchange.asmx`。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-130">For Exchange as part of Office 365, this will be  `https://<server name>/ews/exchange.asmx`.</span></span>
    
<span data-ttu-id="1c0d5-131">下面的代码演示如何使用 Azure AD 身份验证库获取身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-131">The following code shows how to use the Azure AD Authentication Library to get an authentication token.</span></span> <span data-ttu-id="1c0d5-132">该示例假定在 App.config 文件中的应用程序的存储进行身份验证请求所需的信息。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-132">It assumes that the information required to make the authentication request is stored in the application's App.config file.</span></span> <span data-ttu-id="1c0d5-133">本示例不包括错误检查，请参阅[代码示例](#bk_codeSample)的完整代码。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-133">This example does not include error checking, see the [Code sample](#bk_codeSample) for the complete code.</span></span> 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<span data-ttu-id="1c0d5-134"><a name="bk_useToken"> </a></span><span class="sxs-lookup"><span data-stu-id="1c0d5-134"></span></span>

## <a name="add-an-authentication-token-to-ews-requests"></a><span data-ttu-id="1c0d5-135">将身份验证令牌添加到 EWS 请求</span><span class="sxs-lookup"><span data-stu-id="1c0d5-135">Add an authentication token to EWS requests</span></span>

<span data-ttu-id="1c0d5-136">已收到的**AuthenticationResult**对象后可以使用**AccessToken**属性获取令牌颁发的令牌服务。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-136">After you've received the **AuthenticationResult** object you can use the **AccessToken** property to get the token issued by the token service.</span></span> 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<span data-ttu-id="1c0d5-137"><a name="bk_codeSample"> </a></span><span class="sxs-lookup"><span data-stu-id="1c0d5-137"></span></span>

## <a name="code-sample"></a><span data-ttu-id="1c0d5-138">代码示例</span><span class="sxs-lookup"><span data-stu-id="1c0d5-138">Code sample</span></span>

<span data-ttu-id="1c0d5-139">以下是完整代码示例，演示如何使 OAuth 身份验证 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="1c0d5-139">The following is the complete code sample that demonstrates making an OAuth-authenticated EWS request.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Configuration;
using System.Globalization;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;
using System.Web.Script.Serialization;
using Microsoft.Exchange.WebServices.Autodiscover;
using Microsoft.Exchange.WebServices.Data;
using Microsoft.IdentityModel.Clients.ActiveDirectory;
namespace TestV1App
{
    class Program
    {
        static void Main(string[] args)
        {
            var t = new Thread(Run);
            t.SetApartmentState(ApartmentState.STA);
            t.Start();
            t.Join();
        }
        static void Run()
        {
           string authority = ConfigurationManager.AppSettings["authority"];
           string clientID = ConfigurationManager.AppSettings["clientID"];
           Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
           string serverName = ConfigurationManager.AppSettings["serverName"];
            AuthenticationResult authenticationResult = null;
            AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
            
            string errorMessage = null;
            try
            {
                Console.WriteLine("Trying to acquire token");
                authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);
            }
                catch (AdalException ex)
            {
                errorMessage = ex.Message;
                if (ex.InnerException != null)
                {
                    errorMessage += "\nInnerException : " + ex.InnerException.Message;
                }
            }
            catch (ArgumentException ex)
            {
                errorMessage = ex.Message;
            }
            if (!string.IsNullOrEmpty(errorMessage))
            {
                Console.WriteLine("Failed: {0}" + errorMessage);
                return;
            }
            Console.WriteLine("\nMaking the protocol call\n");
            ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
            exchangeService.Url = new Uri(resource + "ews/exchange.asmx");
            exchangeService.TraceEnabled = true;
            exchangeService.TraceFlags = TraceFlags.All;
            exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken);
            exchangeService.FindFolders(WellKnownFolderName.Root, new FolderView(10));
        }
    }
}

```

<span data-ttu-id="1c0d5-140">示例代码需要以下条目 App.config 文件：</span><span class="sxs-lookup"><span data-stu-id="1c0d5-140">The sample code requires an App.config file with the following entries:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <startup>
    <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
  </startup>
  <appSettings>
    <add key="authority" value="http://login.windows.net/<devAccountName>.onmicrosoft.com" />
    <add key="clientId" value="<ID generated by Azure Active Directory"/>
    <add key="clientAppUri" value="<URI registered with Azure Active Directory"/>
    <add key="serverName" value="outlook.office365.com" />
  </appSettings>
</configuration>
```

## <a name="see-also"></a><span data-ttu-id="1c0d5-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1c0d5-141">See also</span></span>

- [<span data-ttu-id="1c0d5-142">身份验证和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="1c0d5-142">Authentication and EWS in Exchange</span></span>](authentication-and-ews-in-exchange.md)    
- [<span data-ttu-id="1c0d5-143">测试和部署 Office 365 应用程序</span><span class="sxs-lookup"><span data-stu-id="1c0d5-143">Test and deploy Office 365 apps</span></span>](http://msdn.microsoft.com/en-us/office/office365/howto/test-and-deploy-apps.aspx)
    

