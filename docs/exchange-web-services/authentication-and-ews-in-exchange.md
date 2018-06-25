---
title: 身份验证和 Exchange 中的 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: 查找可帮助您选择您的 Exchange 的 EWS 应用程序的正确的身份验证标准的信息。
ms.openlocfilehash: c81b29cbe9aa3c658a8f776876366fd0875b2669
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752704"
---
# <a name="authentication-and-ews-in-exchange"></a>身份验证和 Exchange 中的 EWS

查找可帮助您选择您的 Exchange 的 EWS 应用程序的正确的身份验证标准的信息。
  
身份验证是 Exchange Web Services (EWS) 应用程序的关键部分。 Exchange Online、 Exchange Online 作为 Office 365 的一部分和本地版本的开头 Exchange Server 2013 的 Exchange 支持标准 web 身份验证协议，以帮助保护您的应用程序和 Exchange 服务器之间的通信。
  
如果您正在面向 Exchange Online，您选择的身份验证方法必须使用 HTTPS 进行加密的请求和应用程序发送的响应。 尽管您可以与 Exchange 本地服务器使用 HTTP，我们建议您的应用程序将发送到 EWS 终结点可帮助您的应用程序和 Exchange 服务器之间的安全通信任何请求使用 HTTPS。
  
Exchange 提供了您可供选择的以下身份验证选项： 
  
- OAuth 2.0 (Exchange Online 仅)
    
- NTLM （Exchange 内部部署仅）
    
- Basic （不再推荐）
    
您选择的身份验证方法取决于您的组织，您使用的 Exchange Online 或 Exchange 的本地和您是否有权访问可以发出 OAuth 令牌的第三方提供程序的安全要求。 本文提供了将帮助您选择适合您的应用程序的身份验证标准的信息。
  
## <a name="oauth-authentication"></a>OAuth 身份验证

我们建议所有新应用程序使用此 OAuth 标准能够连接到 Exchange Online 服务。 基本身份验证安全性优于值得应用程序中实现 OAuth 所需的其他工作。 对于该记录，但是，有还应注意的一些缺点。
  
**表 1。使用 OAuth 的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| OAuth 是行业标准身份验证协议。<br/><br/>第三方提供程序管理身份验证。 您的应用程序没有收集和存储 Exchange 凭据。<br/><br/>更少担心，因为您的应用程序将不透明的令牌仅接收身份验证提供程序;因此，在您的应用程序安全性遭到破坏仅可以公开令牌，而不是用户的 Exchange 凭据。  <br/> | OAuth 依赖于第三方身份验证提供程序。 这可以施加额外的成本，在您的组织或您的客户。<br/><br/>此 OAuth 标准是更加难以实现比基本身份验证。<br/><br/>若要实现 OAuth，您需要将您的应用程序与身份验证提供程序和 Exchange 服务器集成。  <br/> |
   
为了帮助减少缺点，您可以使用[Microsoft Azure AD 身份验证库](http://msdn.microsoft.com/library/a03f39fa-7ba4-4182-a98e-55562a64b8f3%28Office.15%29.aspx)(ADAL) 为在云中还是内部部署 Active Directory 域服务 (AD DS) 的用户进行身份验证，然后获取访问令牌的保护呼叫到Exchange 服务器。 Exchange Online 要求由受支持的 ADAL; Azure Active Directory 服务颁发的令牌但是，您可以使用任何第三方库。 
  
若要了解有关 EWS 应用程序中使用 OAuth 身份验证的详细信息，请参阅以下资源：
  
- [Office 365 试用版](http://office.microsoft.com/compare-office-365-for-business-plans-FX102918419.aspx?CR_CC=200061904&amp;WT.srch=1&amp;WT.mc_ID=PS_bing_O365Comm_office%20365%20trial_Text)，设置要用于测试客户端应用程序的 Exchange 服务器。
    
- [适用于.NET的Azure AD身份验证库](http://msdn.microsoft.com/library/a03f39fa-7ba4-4182-a98e-55562a64b8f3%28Office.15%29.aspx)
    
- [配置 Azure Active Directory](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)，若要启用应用程序使用 OAuth 令牌的身份验证。
    
- 查看[Authenticate EWS 应用程序使用 OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md)例如可以研究的代码中的示例代码。 
    
## <a name="ntlm-authentication"></a>NTLM 身份验证

NTLM 身份验证功能仅适用于 Exchange 内部部署服务器。 对于运行在企业防火墙内部的应用程序，NTLM 身份验证和.NET Framework 之间的集成提供内置意味着您的应用程序进行身份验证。 
  
**表 2。使用 NTLM 身份验证的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| "开"适用于您的 Exchange 服务器。 您可以使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置 Exchange 服务的访问权限。<br/><br/>使用.NET Framework [CredentialCache](http://msdn2.microsoft.com/EN-US/library/615e0wsd)对象以自动获取用户的凭据。<br/><br/>[代码示例都可用](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)，使用了已登录用户的凭据进行身份验证内部部署 Exchange 服务器。  <br/> | 用户必须登录到要使用 NTLM 身份验证的域。<br/><br/>很难访问未与用户的域帐户关联的电子邮件帐户。<br/><br/>服务应用程序必须具有充分利用 NTLM 身份验证的域帐户。  <br/> |
   
## <a name="basic-authentication"></a>基本身份验证

基本身份验证提供一个很基本级别的客户端应用程序的安全性。 我们建议所有新应用程序进行身份验证; 使用 NTLM 或 OAuth 协议但是，基本身份验证可以是在某些情况下应用程序的正确选择。
  
**表 3。使用基本身份验证的优点和缺点**

|**优点**|**缺点**|
|:-----|:-----|
| "开"适用于您的 Exchange 服务器。 您可以使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置 Exchange 服务的访问权限。<br/><br/>Windows 应用程序可以使用登录的用户的默认凭据。<br/><br/>多个[代码示例可](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)向您演示如何调用 EWS 使用基本身份验证。  <br/> | 需要您的应用程序，以收集和存储用户的凭据。<br/><br/>您必须关闭所有用户使用基本身份验证的 NTLM 身份验证。<br/><br/>如果您的应用程序中发生安全性遭到破坏，它可以公开用户的电子邮件地址和密码攻击者。  <br/> |
   
您需要确定基本身份验证是否符合您的组织和客户的安全要求。 基本身份验证可以正确的选择，如果您想要避免广泛安装任务，例如对于简单的测试或演示应用程序。
  
## <a name="see-also"></a>另请参阅

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)   
- [单一登录添加到 Web 应用程序使用 Microsoft Azure AD](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [在 Exchange 控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)    
- [在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)    
- [支持的令牌和声明类型](http://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
    

