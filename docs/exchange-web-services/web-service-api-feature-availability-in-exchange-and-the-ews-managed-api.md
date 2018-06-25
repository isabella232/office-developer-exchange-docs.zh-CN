---
title: Exchange 和 EWS 托管 API 中的 web 服务 API 功能可用性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: 了解哪些 EWS 和 web 服务的 API 功能在每个版本的 Exchange 和 EWS 托管 API 中可用。
ms.openlocfilehash: d19ab062c8d418e373e8268b1ab039e5436e71bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753018"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Exchange 和 EWS 托管 API 中的 web 服务 API 功能可用性

了解哪些 EWS 和 web 服务的 API 功能在每个版本的 Exchange 和 EWS 托管 API 中可用。
  
Exchange 客户端应用程序通常针对多个 Exchange 版本。 因此，您可能想要设计您的应用程序，以便您可以禁用[EWS 客户端功能](ews-client-design-overview-for-exchange.md#EWSFeatures)在打开和关闭基于的承载用户邮箱的 Exchange 版本。 本文提供了有关哪些服务的 API 功能有不同版本的 Exchange 和 EWS 托管 API 的信息。 使用此信息来设计您的应用程序广泛应用于运行多个版本的 Exchange 的客户。 
  
有关 Exchange 版本之间的差异的详细信息，查看 EWS 架构文件和相关的[参考文档](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)。
  
## <a name="api-features-by-exchange-version"></a>通过 Exchange 版本的 API 功能
<a name="bk_apifeatures"> </a>

Exchange web 服务 Api，包括 EWS 和自动发现，具有多版本兼容性记住开发。 因此，面向 Exchange 2007 应用程序还适用于针对开头 Exchange 2013，包括 Exchange Online 和 Exchange Online 作为 Office 365 的一部分的 Exchange 版本。 
  
下表指示每个版本的 Exchange 和版本的 EWS 托管 API 开头 2.0 版中可用的 API 功能。 因为您的应用程序可能针对多个版本的 Exchange，它将有助于您了解哪些版本支持您的客户端实现的功能。 您可以使用自动发现服务发现哪个版本的 Exchange 客户端目标的用户，以便您可以打开和关闭功能取决于是否对用户可用。
  
**表 1。版本的 Exchange 和 EWS 托管 API 中的 web 服务功能可用性**

|API 功能|Exchange Online (Office 365)|EWS 托管 API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|模糊名称解析  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|适用于 Outlook 管理应用程序  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[存档邮箱访问](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[自动发现 (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[自动发现 (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|自动答复 (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|可用性  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|可用性 （聊天室）  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|批量传输  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|联系人组  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|会话管理  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime 精度  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|管理工作委派给  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|通讯组列表扩展  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[转储程序访问](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[电子数据展示](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|增强的时区  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|文件夹权限  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[标识符转换](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[收件箱管理](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[项目和文件夹的访问](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[邮箱事件 （拉和推送）](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[邮箱事件 （流视频）](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|邮件提示  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|密码过期  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[角色](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|发布项目  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[公用文件夹访问](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|保留策略  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[搜索 （索引）](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[搜索 （存储）](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[同步](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[统一的联系人存储库](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[统一消息 Web 服务](http://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|统一消息 （基于 EWS）  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户配置对象](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户照片](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
您可以找到有关 web 的详细信息，请参阅[EWS 操作](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)、[自动发现服务](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)和[ExchangeService 方法](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx)可在不同版本的 Exchange 的服务功能。
  
## <a name="to-learn-more"></a>若要了解详细信息
<a name="bk_apifeatures"> </a>

如果您希望深入了解 Exchange 版本之间的特定差异，您可以执行以下任一操作：
  
- 了解[EWS 架构](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)调查中的 EWS 中更多详细信息的每个版本之间的差异。 
    
- 下载[EWSEditor](http://ewseditor.codeplex.com/)。 您可以使用 EWSEditor 来指定不同的目标架构版本和提交查询基于目标架构版本。
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md) 
- [What's new in EWS 和其他 web 服务在 Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

