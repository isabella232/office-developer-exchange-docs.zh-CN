---
title: Start using web services in Exchange
manager: sethgros
ms.date: 2/26/2019
ms.audience: Developer
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: 查找信息，以帮助你开始使用 EWS 和 Exchange 中的其他 web 服务。
localization_priority: Priority
ms.openlocfilehash: 5980e22599585aa376890a414e0e8e7c7c5c707a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463753"
---
# <a name="start-using-web-services-in-exchange"></a>Start using web services in Exchange

查找信息，以帮助你开始使用 EWS 和 Exchange 中的其他 web 服务。
  
[Exchange 中的 web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)提供对存储在 exchange online 中的邮箱数据、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 exchange Server 2007 开始）的访问权限，并使您能够创建自定义应用程序，以根据组织的要求管理信息。 虽然您可以创建的 EWS 和 web 服务应用程序的范围几乎是无限的，但某些基本概念适用于任何类型的应用程序。 本节提供有关您需要熟悉的基本概念的信息，以便开始在 Exchange 中使用 EWS 和其他 web 服务。 
  
## <a name="build-your-knowledge"></a>构建你的知识
<a name="bk_Knowledge"> </a>

无论您是使用 .NET Framework 还是其他平台开发 web 服务应用程序，您都需要先了解一些重要概念，然后再开始开发项目。 
  
**表1。Web 服务概念**

|**概念**|**摘要**|
|:-----|:-----|
|[体系结构](ews-applications-and-the-exchange-architecture.md) <br/> |了解 EWS 在 Exchange 体系结构中的工作方式以及它使用的协议。  <br/> |
|[EWS 应用程序类型](ews-application-types.md) <br/> |了解您可以使用 Exchange 中的 EWS 创建的最常见的应用程序类型。  <br/> |
|[EWS 访问](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Exchange 管理员可以限制整个组织、单个用户和各个应用程序对 EWS 的全局访问。 了解哪种访问级别适合您。  <br/> |
|[Setup](setting-up-your-ews-application.md) <br/> |查找有关您需要完成的任务的信息，以便创建使用 EWS 托管 API 或 EWS 与 Exchange 进行通信的应用程序。  <br/> |
|[身份验证](authentication-and-ews-in-exchange.md) <br/> |了解用于连接到 Exchange Online 和本地 Exchange 的身份验证选项。  <br/> |
|[自动发现](autodiscover-for-exchange.md) <br/> |了解您可以用来发现 URL 终结点的一组服务，用户的帐户可以通过 EWS 访问信息。  <br/> |
|[邮箱服务器](https://technet.microsoft.com/library/jj150491%28v=exchg.150%29.aspx) <br/> |了解对 EWS 客户端提供的信息的主要存储库。 EWS 可以访问存储在 Active Directory 域服务（AD DS）中的一组有限的信息。  <br/> |
|[Outlook 和 EWS 的邮件应用程序](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |查找有关 Outlook 相关邮件应用程序及其在 Exchange 中如何使用 EWS 的信息。  <br/> |
|[Office 365 REST Api 的邮件、 日历和联系人](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |了解可用于将 Exchange Online 中的邮件、日历和联系人作为 Office 365 的一部分进行访问的 Office 365 Api。  <br/> |
|[EWS Managed API](get-started-with-ews-managed-api-client-applications.md) <br/> |查找有关适用于 .NET Framework 开发人员的首选客户端 API 的信息。  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |查找有关使用 EWS XML 请求和响应创建您的第一个应用程序的信息。  <br/> |
|[Exchange 产品版本中的 EWS 功能](ews-functionality-in-exchange-product-versions.md) <br/> |了解 Exchange 版本中提供了哪些 EWS 功能。  <br/> |
|[跟踪和故障排除](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |了解如何跟踪 EWS 请求和响应，以便解决 EWS 托管 API 应用程序中的错误。  <br/> |
   
## <a name="create-your-first-application"></a>创建您的第一个应用程序
<a name="create"> </a>

如果你已准备好了解编写你的第一个 .NET Framework 或 EWS 客户端应用程序的业务，请参阅[开始使用 Ews 托管 API 客户端应用程序](get-started-with-ews-managed-api-client-applications.md)或[开始使用 ews 客户端](get-started-with-ews-client-applications.md)应用程序。
  
## <a name="get-code-samples"></a>获取代码示例
<a name="samples"> </a>

若要查找介绍如何使用 EWS 和 Exchange 中的其他 web 服务的代码示例和示例，请参阅以下资源：
  
- [Exchange 代码示例](https://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Exchange API 文档](develop-web-service-clients-for-exchange.md)
    
- [Exchange 开发论坛](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)
    
博客、代码演示网站和论坛中提供了许多其他示例。 此外，我们还建议您下载[EWSEditor](http://ewseditor.codeplex.com/)。 此项目实现大部分 EWS 功能;你可以在此处找到所有核心 EWS 功能的示例。
  
如果您不是 .NET Framework 开发人员，则可以找到多个客户端库，其中包含使用 Java、Python、PHP 和其他语言的 EWS 开发。 
  
## <a name="ask-questions-and-solve-problems"></a>提出问题并解决问题
<a name="questions"> </a>

是否需要帮助才能完成操作，但未找到答案？ 您可以搜索[Exchange 开发论坛](https://social.technet.microsoft.com/Forums/exchange/home?forum=exchangesvrdevelopment)，了解是否有人遇到并解决了相同的问题。 一社区参与者回答了有关 Exchange 开发的数百个问题。 您还可以查找第三方网站、论坛和博客，其中包含 Exchange 开发，并且可能具有您要查找的解决方案。 
  
如果你需要其他帮助，请联系[Microsoft 支持](https://support.microsoft.com/)部门。 Exchange 开发人员支持团队为经验丰富的专业人员配备了可帮助回答有关 Exchange 开发的问题的人员。 
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md) 
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md) 
- [Exchange web 服务引用](../web-service-reference/web-services-reference-for-exchange.md)
    

