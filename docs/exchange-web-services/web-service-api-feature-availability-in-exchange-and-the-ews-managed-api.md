---
title: Web 服务 API 功能在 Exchange 和 EWS 托管 API 中的可用性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: 了解每个版本的网站和 EWS 托管 API 中可用的 EWS Exchange Web 服务 API 功能。
ms.openlocfilehash: 6fc0c40410be543b149885c7b0785a2c6c8828af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544470"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Web 服务 API 功能在 Exchange 和 EWS 托管 API 中的可用性

了解每个版本的网站和 EWS 托管 API 中可用的 EWS Exchange Web 服务 API 功能。
  
Exchange客户端应用程序通常面向许多版本的 Exchange。 因此，您可能需要设计应用程序，以便您可以根据托管用户邮箱的 Exchange 版本启用和禁用[EWS](ews-client-design-overview-for-exchange.md#EWSFeatures)客户端功能。 本文提供有关哪些服务 API 功能可用于不同版本的 Exchange 和 EWS 托管 API 的信息。 使用此信息设计应用程序，以广泛应用于运行多个版本 Exchange。 
  
有关版本之间的差异的详细信息，Exchange EWS 架构文件和关联的[参考文档](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)。
  
## <a name="api-features-by-exchange-version"></a>按版本Exchange API 功能
<a name="bk_apifeatures"> </a>

开发 Exchange Web 服务 API（包括 EWS 和自动发现）时考虑多版本兼容性。 因此，面向 Exchange 2007 的应用程序还适用于从 Exchange 2013 开始版本的 Exchange，包括 Exchange Online 和 Exchange Online 作为 Office 365 的一部分。 
  
下表指示从版本 2.0 开始，每个 Exchange EWS 托管 API 版本中可用的 API 功能。 由于应用程序可能面向多个版本的 Exchange，因此了解哪些版本支持客户端实现的功能将很有帮助。 可以使用自动发现服务发现客户端面向的 Exchange 版本，以便根据功能是否可供用户使用来启用和关闭功能。
  
**表 1.Web 服务功能在 Exchange 和 EWS 托管 API 中的可用性**

|API 功能|Exchange Online (Office 365) |EWS 托管 API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|不明确的名称解析  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Outlook管理的应用  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[存档邮箱访问](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[自动发现 (POX) ](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[自动发现 (SOAP) ](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|OOF (自动)   <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|可用性  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|会议室 (可用性)   <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|批量传输  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|联系人组  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|对话管理  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|DateTime 精度  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|委派管理  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|通讯组列表扩展  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[垃圾站访问](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[电子数据展示](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|增强的时区  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|文件夹权限  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[标识符转换](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[收件箱管理](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[项和文件夹访问权限](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[拉式 (推送邮件的邮箱) ](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[流式传输 (邮箱) ](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|邮件提示  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|密码有效期  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Personas](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|发布项目  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[公用文件夹访问](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|保留策略  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[搜索 (索引) ](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[搜索 (存储) ](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[同步](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[统一联系人存储](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[统一消息 Web 服务](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|基于 EWS (统一消息)   <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户配置对象](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户照片](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
有关不同版本的 Exchange 中可用的 Web 服务功能的详细信息，请参阅有关[EWS](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)操作、自动发现服务和[](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)[ExchangeService 方法的信息](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx)。
  
## <a name="to-learn-more"></a>了解更多信息
<a name="bk_apifeatures"> </a>

如果你想要更深入地了解不同版本之间的特定Exchange，可以执行下列任一操作：
  
- 浏览 [EWS 架构以](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) 更详细地研究每个 EWS 版本之间的差异。 
    
- 下载 [EWSEditor](http://ewseditor.codeplex.com/)。 您可以使用 EWSEditor 指定不同的目标架构版本并提交基于目标架构版本的查询。
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md) 
- [EWS 和其他 Web 服务中的新增Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

