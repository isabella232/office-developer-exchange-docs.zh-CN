---
title: Exchange 中的身份验证和 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: 查找信息，以帮助您为面向 Exchange 的 EWS 应用程序选择正确的身份验证标准。
localization_priority: Priority
ms.openlocfilehash: 69018b6f88fc80e1e18edd96ed0e16d52064572d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528480"
---
# <a name="authentication-and-ews-in-exchange"></a>Exchange 中的身份验证和 EWS

查找信息，以帮助您为面向 Exchange 的 EWS 应用程序选择正确的身份验证标准。
  
身份验证是 Exchange Web 服务（EWS）应用程序的关键部分。 Exchange Online、Exchange Online （作为 Office 365 的一部分）和本地版本的 Exchange 以 Exchange Server 2013 开头。支持标准 web 身份验证协议，以帮助保护应用程序和 Exchange 服务器之间的通信。
  
如果您针对的是 Exchange Online，则您选择的身份验证方法必须使用 HTTPS 加密您的应用程序发送的请求和响应。 虽然您可以将 HTTP 与 Exchange 本地服务器结合使用，但我们建议对应用程序发送到 EWS 终结点的任何请求使用 HTTPS，以帮助确保应用程序与 Exchange 服务器之间的通信安全。
  
Exchange 提供了以下身份验证选项供您选择： 
  
- OAuth 2.0 （仅限 Exchange Online）
    
- NTLM （仅限本地 Exchange）
    
- 基本（不再推荐）
    
您选择的身份验证方法取决于您的组织的安全要求、是使用 Exchange Online 还是本地 Exchange，以及您是否有权访问可颁发 OAuth 令牌的第三方提供程序。 本文提供的信息可帮助您选择适合您的应用程序的身份验证标准。
  
## <a name="oauth-authentication"></a>OAuth 身份验证

我们建议所有新应用程序都使用 OAuth 标准连接到 Exchange Online services。 安全性优于基本身份验证的优点是，在应用程序中实现 OAuth 所需的额外工作。 但对于记录而言，还有一些应注意的缺点。
  
**表1。使用 OAuth 的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| OAuth 是行业标准的身份验证协议。<br/><br/>身份验证由第三方提供程序进行管理。 您的应用程序不需要收集和存储 Exchange 凭据。<br/><br/>由于您的应用程序仅从身份验证提供程序接收到不透明令牌，因此为你提供了更少的照管。因此，应用程序中的安全破坏只能公开令牌，而不是用户的 Exchange 凭据。  <br/> | OAuth 依赖于第三方身份验证提供程序。 这可能会给你的组织或客户带来额外的成本。<br/><br/>与基本身份验证相比，OAuth 标准更难实现。<br/><br/>若要实现 OAuth，您需要将您的应用程序与身份验证提供程序和 Exchange 服务器集成。  <br/> |
   
为了帮助最大限度地降低缺点，可以使用[Microsoft AZURE AD 身份验证库](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries)（ADAL）对用户进行身份验证，以便在云中或内部部署中对 Active Directory 域服务（AD DS）进行身份验证，然后获取访问令牌以保护对 Exchange 服务器的呼叫。 Exchange Online 需要由受 ADAL 支持的 Azure Active Directory 服务颁发的令牌;不过，您可以使用任何第三方库。 
  
若要了解有关在 EWS 应用程序中使用 OAuth 身份验证的详细信息，请参阅以下资源：
  
- [Office 365 试用版](https://docs.microsoft.com/office/developer-program/office-365-developer-program)，用于设置用于测试客户端应用程序的 Exchange 服务器。
    
- [适用于.NET的Azure AD身份验证库](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [配置 Azure Active Directory](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)，以使应用程序能够使用 OAuth 令牌进行身份验证。
    
- 通过使用可研究的示例代码的 OAuth，查看[对 EWS 应用程序进行身份验证](how-to-authenticate-an-ews-application-by-using-oauth.md)的示例代码。 
    
## <a name="ntlm-authentication"></a>NTLM 身份验证

NTLM 身份验证仅适用于 Exchange 本地服务器。 对于在企业防火墙内部运行的应用程序，在 NTLM 身份验证和 .NET Framework 之间集成提供了对应用程序进行身份验证的内置方法。 
  
**表2。使用 NTLM 身份验证的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| 与 Exchange 服务器配合使用 "开箱即用"。 您可以使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置对 Exchange 服务的访问权限。<br/><br/>使用 .NET Framework [CredentialCache](https://msdn2.microsoft.com/library/615e0wsd)对象自动获取用户的凭据。<br/><br/>可以使用已登录用户的凭据进行本地 Exchange server 身份验证的[代码示例](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)。  <br/> | 用户必须登录到域才能使用 NTLM 身份验证。<br/><br/>很难访问与用户的域帐户不关联的电子邮件帐户。<br/><br/>服务应用程序必须具有域帐户才能充分利用 NTLM 身份验证。  <br/> |

   
## <a name="basic-authentication"></a>基本身份验证

基本身份验证为客户端应用程序提供了一种基本的安全级别。 我们建议所有新应用程序都使用 NTLM 或 OAuth 协议进行身份验证;但是，在某些情况下，基本身份验证可能是应用程序的正确选择。
  
**表3。使用基本身份验证的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| 与 Exchange 服务器配合使用 "开箱即用"。 您可以使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置对 Exchange 服务的访问权限。<br/><br/>Windows 应用程序可以使用已登录用户的默认凭据。<br/><br/>提供了许多[代码示例](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)，向您展示了如何使用基本身份验证来调用 EWS。  <br/> | 要求您的应用程序收集和存储用户的凭据。<br/><br/>如果您希望强制所有用户使用基本身份验证，则必须关闭 NTLM 身份验证。<br/><br/>如果应用程序中发生安全破坏，它可以向攻击者公开用户的电子邮件地址和密码。  <br/> |
   
您需要确定基本身份验证是否符合组织和客户的安全要求。 如果您想要避免大量的设置任务（例如简单的测试或演示应用程序），则基本身份验证可能是正确的选择。
  
## <a name="see-also"></a>另请参阅

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [使用 Microsoft Azure AD 将登录添加到 Web 应用程序](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [在 Exchange 中控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)    
- [控制对 Exchange 中的 EWS 的客户端应用程序访问](controlling-client-application-access-to-ews-in-exchange.md)   
- [支持的令牌和声明类型](https://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
 