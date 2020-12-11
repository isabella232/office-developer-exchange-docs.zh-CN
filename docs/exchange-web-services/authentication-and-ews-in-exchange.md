---
title: 在 Exchange 中的身份验证和 EWS
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: 查找更多信息，帮助你为面向 Exchange 的 EWS 应用程序选择正确的身份验证标准。
localization_priority: Priority
ms.openlocfilehash: 0b35921f33b935f9a5a490e15d4e76d1a3e3c9dc
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603832"
---
# <a name="authentication-and-ews-in-exchange"></a>在 Exchange 中的身份验证和 EWS

查找更多信息，帮助你为面向 Exchange 的 EWS 应用程序选择正确的身份验证标准。
  
身份验证是 Exchange Web 服务 (EWS) 应用程序中的一个关键部分。 Exchange Online、Exchange Online 作为 Office 365 的一部分以及从 Exchange Server 2013 开始的本地版 Exchange 支持标准版 Web 身份验证 协议，以帮助保护应用和 Exchange Server 之间的通讯。
  
如果你面向 Exchange Online，那么你选择的身份验证方法必须使用 HTTPS 加密应用发出的请求和响应。 即使你可以在 Exchange 本地服务器上使用HTTP，我们建议你使用 HTTPS 加密任何应用发送到 EWS 终结点的请求，以帮助保护应用和 Exchange Server 之间的通讯。
  
Exchange 提供下列身份验证选项供你选择： 
  
- OAuth 2.0 （仅Exchange Online）
    
- NTLM （仅本地 Exchange）
    
- 基本（不在推荐）
    
你选择的身份验证方法取决于你组织的安全要求，取决于你在使用 Exchange Online 还是本地 Exchange，以及你是否有权限访问可以提供 OAuth 令牌的第三方提供商。 这篇文章提供相关信息，帮助你选择适合你应用的身份验证标准。
  
## <a name="oauth-authentication"></a>OAuth 身份验证

我们推荐所有新应用使用 OAuth 标准连接 Exchange Online 服务。 它在安全性方面优于基本身份验证，所以值得花额外的必需精力将 OAuth 应用到你的应用。 但是，郑重声明，这也存在一些你需要注意的缺点。
  
**表 1. 使用 OAuth 的优缺点**

|**优点**|**缺点**|
|:-----|:-----|
| OAuth 是行业标准的身份验证协议。<br/><br/>身份验证由第三方提供商管理。 你的应用程序不需要收集和存储 Exchange 凭据。<br/><br/>你的烦恼减少了，因为你的应用只会从身份验证提供商处收到一个不透明的令牌，因此，你的应用中的安全漏洞只会暴露此令牌，而不是用户的 Exchange 凭据。  <br/> | OAuth 依赖第三方身份验证提供商。 这会增加你组织或客户的成本。<br/><br/>OAuth 标准比基本身份验证更难实施。<br/><br/>要实施 OAuth，你需要将你的应用与身份验证提供商和 Exchange 服务器进行整合。  <br/> |
   
为帮助最小化缺点，你可以使用 [Azure AD 身份验证库](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) 来在云或本地验证用户使用 Active Directory 域服务 (AD DS)，然后获取到 Exchange 服务器的保护通话的访问令牌。 Exchange Online 要求 Microsoft Azure Active Directory 服务颁发的令牌，该令牌由 ADAL 支持。但是，你也可以使用任何第三方库。 
  
了解更多关于如何在你的 EWS 应用中使用 OAuth 身份验证的信息，参与以下资源：
  
- [Office 365 试用版](https://docs.microsoft.com/office/developer-program/office-365-developer-program)，设置 Exchange 服务器来使用测试你的客户端应用程序。
    
- [适用于 .NET 的 Azure AD 身份验证库](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [配置 Azure Active Directory](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)，让你的应用可以使用 OAuth 令牌进行身份验证。
    
- 在“[使用 OAuth 验证 EWS 应用](how-to-authenticate-an-ews-application-by-using-oauth.md)”中使用 OAuth 检查示例代码，比如你可以 研究的代码。 
    
## <a name="ntlm-authentication"></a>NTLM 身份验证

NTLM 身份验证仅对 Exchange 本地服务器可用。 对用在公司防火墙内运行的应用，NTLM 身份验证和 .NET Framework 的结合可以通过内嵌的方式验证你的应用。 
  
**表 2. 使用 NTLM 身份验证的优缺点**

|**优点**|**缺点**|
|:-----|:-----|
| 以创新方法在你的 Exchange 服务器上工作。 你可以通过使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置对 Exchange 服务的访问。<br/><br/>使用 .NET Framework [CredentialCache](https://msdn2.microsoft.com/library/615e0wsd) 对象自动获取用户的凭据。<br/><br/>[代码示例可用](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)，使用登陆用户的凭据验证到本地 Exchange 服务器。  <br/> | 用户必须登陆到域来使用 NTLM 身份验证。<br/><br/>要访问和用户的域账号不关联的电子邮件账号可能会很困难。<br/><br/>服务应用程序必须有域账号来利用 NTLM 身份验证的优势。  <br/> |

   
## <a name="basic-authentication"></a>基本身份验证

基本身份验证提供了你的客户端应用程序基本的安全性。 我们建议所有新应用使用 NTLM 或 OAuth 协议进行身份验证，但是基本身份验证也在某些情况下可行。
  
**表 3. 使用基本身份验证的优缺点**

|**优点**|**缺点**|
|:-----|:-----|
| 以创新方法在你的 Exchange 服务器上工作。 你可以通过使用[Exchange 命令行管理程序 cmdlet](how-to-control-access-to-ews-in-exchange.md)配置对 Exchange 服务的访问。<br/><br/>Windows 应用可以使用登陆用户的默认凭据。<br/><br/>很多 [代码示例可用](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c)，它们向你展示如何用基本身份验证调用 EWS。  <br/> | 需要你的应用收集和存储用户的凭据。<br/><br/>如果你想要强制所有用户使用基本身份验证，你必须关闭 NTLM 身份验证。<br/><br/>如果你的应用出现安全漏洞，你的用户的电子邮件地址和密码可能会暴露给入侵者。  <br/> |
   
你需要决定基本身份验证是否满足你的组织和用户的要求。 如果你想避免过多的设置，比如示例测试或演示应用，基本身份验证是合适的选择。

> [!NOTE]
> 基本身份验证不在受 EWS 支持，无法连接 Exchange Online。 在你的新的或现有的 EWS 应用上使用 OAuth 身份验证来连接Exchange Online。 对 EWS 的 OAuth 身份验证仅在作为 Microsoft 365 一部分的 Exchange Online 中可用。 使用 OAuth 的 EWS 应用程序必须先通过 Azure Active Directory 注册。
  
## <a name="see-also"></a>另请参阅
- [使用 OAuth 对 EWS 应用程序进行身份验证](how-to-authenticate-an-ews-application-by-using-oauth.md)
- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [使用 Microsoft Azure AD 添加到你的 Web 应用的登陆](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [在 Exchange 中控制对 EWS 的访问](how-to-control-access-to-ews-in-exchange.md)    
- [在 Exchange 中控制客户端应用对 EWS 的访问](controlling-client-application-access-to-ews-in-exchange.md)   
- [支持的令牌和声明类型](https://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
 
