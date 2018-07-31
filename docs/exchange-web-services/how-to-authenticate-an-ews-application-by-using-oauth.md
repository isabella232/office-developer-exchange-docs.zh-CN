---
title: 使用 OAuth 对 EWS 应用程序进行身份验证
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1d8d57f9-4df5-4f21-9bbb-a89e0e259052
description: 了解如何使用 EWS 托管 API 应用程序的 OAuth 身份验证。
ms.openlocfilehash: 8b6a3fd72e42a36e31f261205292de28ef341270
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353579"
---
# <a name="authenticate-an-ews-application-by-using-oauth"></a>使用 OAuth 对 EWS 应用程序进行身份验证

了解如何使用 EWS 托管 API 应用程序的 OAuth 身份验证。
  
您可以使用 Azure Active Directory 所提供的 OAuth 身份验证服务与 Office 365 REST Api 使用的相同的身份验证模型集成 EWS 托管 API 应用程序。 若要使用 OAuth 在应用程序，您将需要：
  
1. 与 Azure Active Directory 中[注册您的应用程序](#bk_register)。 
    
2. [添加代码以获取身份验证令牌](#bk_getToken)以从令牌服务器获取身份验证令牌。 
    
3. [添加身份验证令牌 EWS 请求](#bk_useToken)所发送。 
    
> [!NOTE]
> EWS 的 OAuth 身份验证在 Exchange 中的 Office 365 一部分才可用。 EWS 应用程序要求"完全访问用户邮箱"权限。 
  
若要使用本文中的代码，您将需要有权访问以下：
  
- [Office 365 开发人员帐户](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program)。 试用帐户可用于测试您的应用程序。
    
- [用于.NET 的 Azure AD 身份验证库](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries)。
    
- [EWS 托管 API](https://github.com/officedev/ews-managed-api.aspx)。

<a name="bk_register"> </a>

## <a name="register-your-application"></a>注册您的应用程序

若要使用 OAuth，应用程序必须具有一个客户端标识符和应用程序标识应用程序的 URI。 如果您尚未尚未注册您的应用程序与 Azure Active Directory 服务，您将需要手动将您的应用程序添加按照在[注册您的应用程序](https://apps.dev.microsoft.com/#/appList)的步骤。

<a name="bk_getToken"> </a>

## <a name="add-code-to-get-an-authentication-token"></a>添加代码以获取身份验证令牌

用于.NET 的 Azure AD 身份验证库简化了从 Azure Active Directory 获取身份验证令牌，以便您可以在您的应用程序中使用令牌。 您需要提供的信息获取令牌的四个部分：
  
1. 令牌的服务器的 URI。 令牌的服务器是对用户进行身份验证并返回您的应用程序可用于访问 EWS 的令牌**颁发机构**。 
    
2. 使用 Azure Active Directory 中注册您的应用程序时创建应用程序客户端 ID。
    
3. 应用程序客户端与 Azure Active Directory 中注册您的应用程序时创建的 URI。
    
4. EWS 服务器的 URI 和的 EWS 终结点 URI。 对于 Exchange 作为 Office 365 的一部分，这将为`https://<server name>/ews/exchange.asmx`。
    
下面的代码演示如何使用 Azure AD 身份验证库获取身份验证令牌。 该示例假定在 App.config 文件中的应用程序的存储进行身份验证请求所需的信息。 本示例不包括错误检查，请参阅[代码示例](#bk_codeSample)的完整代码。 
  
```cs
string authority = ConfigurationManager.AppSettings["authority"];
string clientID = ConfigurationManager.AppSettings["clientID"];
Uri clientAppUri = new Uri(ConfigurationManager.AppSettings["clientAppUri"];
string serverName = ConfigurationManager.AppSettings["serverName"];
AuthenticationContext authenticationContext = new AuthenticationContext(authority, false);
AuthenticationResult authenticationResult = authenticationContext.AcquireToken(serverName, clientId, clientAppUri);

```

<a name="bk_useToken"> </a>

## <a name="add-an-authentication-token-to-ews-requests"></a>将身份验证令牌添加到 EWS 请求

已收到的**AuthenticationResult**对象后可以使用**AccessToken**属性获取令牌颁发的令牌服务。 
  
```cs
ExchangeService exchangeService = new ExchangeService(ExchangeVersion.Exchange2013);
exchangeService.Url = new Uri(ConfigurationManager.AppSettings["serverName"]+"ews/exchange.asmx");
exchangeService.TraceEnabled = true;
exchangeService.TraceFlags = TraceFlags.All;
exchangeService.Credentials = new OAuthCredentials(authenticationResult.AccessToken));
exchangeService.FindFolders(WellKnownFolderName.Root, new Folderview(10));
```

<a name="bk_codeSample"> </a>

## <a name="code-sample"></a>代码示例

以下是完整代码示例，演示如何使 OAuth 身份验证 EWS 请求。
  
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

示例代码需要以下条目 App.config 文件：
  
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

## <a name="see-also"></a>另请参阅

- [身份验证和 Exchange 中的 EWS](authentication-and-ews-in-exchange.md)    

    

