---
title: Exchange 和 EWS 托管 API 中的 Web 服务 API 功能可用性
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: 了解每个版本的 Exchange 和 EWS 托管 API 中提供了哪些 EWS 和 web 服务 API 功能。
ms.openlocfilehash: f15cf4784a59c18d1bb9ae20af378baed084acc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529845"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Exchange 和 EWS 托管 API 中的 Web 服务 API 功能可用性

了解每个版本的 Exchange 和 EWS 托管 API 中提供了哪些 EWS 和 web 服务 API 功能。
  
Exchange 客户端应用程序通常面向许多 Exchange 版本。 出于此原因，您可能需要设计应用程序，以便根据托管用户邮箱的 Exchange 版本来打开和关闭[EWS 客户端功能](ews-client-design-overview-for-exchange.md#EWSFeatures)。 本文提供了有关不同版本的 Exchange 和 EWS 托管 API 中可用的服务 API 功能的信息。 使用此信息可将您的应用程序设计为广泛应用于运行多个 Exchange 版本的客户。 
  
有关 Exchange 版本之间的差异的详细信息，请参阅 EWS 架构文件和关联的[参考文档](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)。
  
## <a name="api-features-by-exchange-version"></a>由 Exchange 版本提供的 API 功能
<a name="bk_apifeatures"> </a>

Exchange web 服务 Api （包括 EWS 和自动发现）在编写时考虑到了多版本兼容性。 因此，针对 exchange 2007 的应用程序也适用于从 Exchange 2013 开始的 Exchange 版本，包括 Exchange Online 和 Exchange Online （作为 Office 365 的一部分）。 
  
下表显示了每个 Exchange 版本和从版本2.0 开始的 EWS 托管 API 版本中可用的 API 功能。 由于您的应用程序可能以多个版本的 Exchange 为目标，因此您知道哪些版本支持您的客户端实现的功能将非常有帮助。 您可以使用自动发现服务发现用户的哪种版本的 Exchange 是客户端目标，以便您可以打开和关闭这些功能，具体取决于您的用户是否可以使用它们。
  
**表1。Exchange 和 EWS 托管 API 的版本中的 Web 服务功能可用性**

|API 功能|Exchange Online （Office 365）|EWS 托管 API|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|不明确的名称解析  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Outlook 相关应用程序管理  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[存档邮箱访问](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[自动发现（POX）](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[自动发现（SOAP）](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|自动答复（OOF）  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|供应情况  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|可用性（会议室）  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|批量转移  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|联系人组  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|会话管理  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|日期时间精度  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|委派管理  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|通讯组列表扩展  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[转储程序访问](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[电子数据展示](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|增强的时区  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|文件夹权限  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[标识符转换](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[收件箱管理](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[项目和文件夹访问](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[邮箱事件（拉取和推送）](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[邮箱事件（流）](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|邮件  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|密码有效期  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[人数](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|发布项目  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[公用文件夹访问](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|保留策略  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[搜索（编入索引）](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[搜索（存储）](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[同步](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[统一联系人存储](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[统一消息 Web 服务](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|统一消息（基于 EWS）  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户配置对象](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[用户照片](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
您可以通过阅读关于[EWS 操作](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)、[自动发现服务](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)和[ExchangeService 方法](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx)，找到有关不同 Exchange 版本中可用的 web 服务功能的详细信息。
  
## <a name="to-learn-more"></a>若要了解详细信息
<a name="bk_apifeatures"> </a>

如果要深入了解 Exchange 版本之间的具体区别，可以执行以下任一操作：
  
- 浏览[ews 架构](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)，以详细了解每个 ews 版本之间的差异。 
    
- 下载[EWSEditor](http://ewseditor.codeplex.com/)。 您可以使用 EWSEditor 指定不同的目标架构版本，并根据目标架构版本提交查询。
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md) 
- [Exchange 中的 EWS 和其他 web 服务中的新增功能](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

