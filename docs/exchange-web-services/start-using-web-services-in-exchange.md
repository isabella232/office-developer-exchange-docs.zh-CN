---
title: 开始 Exchange 中使用 web 服务
manager: sethgros
ms.date: 2/27/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b07a92-0595-4bf1-bd6b-c07e66a8c923
description: 查找可帮助您开始使用 EWS 和其他 web 服务在 Exchange 中的信息。
ms.openlocfilehash: 2f203c5634c29105feb39220c3ebdd9624bb49ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753011"
---
# <a name="start-using-web-services-in-exchange"></a>开始 Exchange 中使用 web 服务

查找可帮助您开始使用 EWS 和其他 web 服务在 Exchange 中的信息。
  
[在 Exchange web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)提供访问邮箱数据存储在 Exchange Online，Exchange Online 作为 Office 365 的一部分和本地版本的 Exchange 开头 Exchange Server 2007，并使您能够创建自定义应用程序可以使用管理根据组织的要求的信息。 从实际的角度是无限 EWS 和 web 服务应用程序，您可以创建的范围时，一些基本概念适用于任何类型的应用程序中。 本节提供有关的基本概念您需要熟悉以开始在 Exchange 使用 EWS 和其他 web 服务的信息。 
  
## <a name="build-your-knowledge"></a>构建您的知识
<a name="bk_Knowledge"> </a>

是否使用.NET Framework 或另一个平台开发 web 服务应用程序，您需要了解一些重要的概念，您开始开发项目。 
  
**表 1。Web 服务概念**

|**概念**|**摘要**|
|:-----|:-----|
|[体系结构](ews-applications-and-the-exchange-architecture.md) <br/> |了解 EWS Exchange 体系结构和它使用的协议中的工作方式。  <br/> |
|[EWS 应用程序类型](ews-application-types.md) <br/> |了解有关您可以使用 EWS 在 Exchange 中创建的应用程序的最常见类型。  <br/> |
|[EWS 访问](controlling-client-application-access-to-ews-in-exchange.md) <br/> |Exchange 管理员可以限制对 EWS 全局性针对整个组织，为各个用户，以及各个应用程序的访问。 找出最适合您的访问级别。  <br/> |
|[设置](setting-up-your-ews-application.md) <br/> |查找有关的任务所需完成才能创建使用 EWS 托管 API 或 EWS 与 Exchange 通信的应用程序的信息。  <br/> |
|[身份验证](authentication-and-ews-in-exchange.md) <br/> |了解用于连接到 Exchange Online 和 Exchange 内部部署的身份验证选项。  <br/> |
|[自动发现](autodiscover-for-exchange.md) <br/> |了解可用于发现的 URL 终结点用户的帐户可以在其中访问通过 EWS 的信息的服务集。  <br/> |
|[邮箱服务器](http://technet.microsoft.com/en-us/library/jj150491%28v=exchg.150%29.aspx) <br/> |查找有关的信息可用于 EWS 客户端的主存储库。 EWS 有权有限设置 Active Directory 域服务 (AD DS) 中存储的信息。  <br/> |
|[面向 Outlook 和 EWS 的邮件应用程序](mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |查找有关邮件应用程序的 Outlook 和如何使用 EWS 在 Exchange 中的信息。  <br/> |
|[Office 365 REST Api 的邮件、 日历和联系人](office-365-rest-apis-for-mail-calendars-and-contacts.md) <br/> |了解 Office 365 Api 可用于访问邮件、 日历和联系人在 Exchange Online 作为 Office 365 的一部分。  <br/> |
|[EWS 托管的 API](get-started-with-ews-managed-api-client-applications.md) <br/> |查找面向.NET Framework 开发人员的首选的客户端 API 的信息。  <br/> |
|[EWS](get-started-with-ews-client-applications.md) <br/> |查找有关使用 EWS XML 请求和响应创建首个应用程序的信息。  <br/> |
|[Exchange 产品版本中的 EWS 功能](ews-functionality-in-exchange-product-versions.md) <br/> |找出哪些 EWS 功能是可用的 Exchange 版本中。  <br/> |
|[跟踪和疑难解答](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md) <br/> |找出如何跟踪以便解决 EWS 托管 API 应用程序中的错误的 EWS 请求和响应。  <br/> |
   
## <a name="create-your-first-application"></a>创建首个应用程序
<a name="create"> </a>

如果您已准备好开始编写您的第一个.NET Framework 或 EWS 客户端应用程序的工作，请参阅[入门 EWS 托管 API 客户端应用程序](get-started-with-ews-managed-api-client-applications.md)或[入门 EWS 客户端应用程序](get-started-with-ews-client-applications.md)。
  
## <a name="get-code-samples"></a>获取代码示例
<a name="samples"> </a>

若要找到代码示例和演示如何在 Exchange 使用 EWS 和其他 web 服务的示例，请参阅以下资源：
  
- [Exchange 代码示例](http://code.msdn.microsoft.com/exchange)
    
- [CodePlex](http://www.codeplex.com/)
    
- [Exchange API 文档](develop-web-service-clients-for-exchange.md)
    
- [Exchange 开发论坛 （英文)](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)
    
中博客 （英文）、 代码演示网站和论坛提供了许多其他示例。 我们还建议您下载[EWSEditor](http://ewseditor.codeplex.com/)。 此项目实现的大多数 EWS 功能;您可以找到的所有核心 EWS 功能下面的示例。
  
如果您不是.NET Framework 开发人员，您可以使用 Java、 Python、 PHP 和其他语言的 EWS 开发出有找到多个客户端库。 
  
## <a name="ask-questions-and-solve-problems"></a>提出问题和解决问题
<a name="questions"> </a>

是否需要帮助完成任务并不找到答案？ 您可以搜索[Exchange 开发论坛](http://social.technet.microsoft.com/Forums/exchange/en-US/home?forum=exchangesvrdevelopment)以找出人具有是否遇到和解决了相同的问题。 参与者社区应答数百有关 Exchange 开发的问题。 您还可以找到第三方网站、 论坛和博客的覆盖 Exchange 开发并可能具有您要寻找的解决方案。 
  
如果您需要其他帮助，请联系[Microsoft 支持](https://support.microsoft.com/)。 Exchange 开发人员支持团队配备经验丰富的专业人员可帮助您回答有关 Exchange 开发的影响。 
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) 
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md) 
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md) 
- [Exchange web 服务引用](../web-service-reference/web-services-reference-for-exchange.md)
    

