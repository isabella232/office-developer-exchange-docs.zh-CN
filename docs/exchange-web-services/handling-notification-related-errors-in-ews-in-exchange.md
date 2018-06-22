---
title: 在 Exchange 处理与通知相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: 了解如何处理与通知相关的您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发应用程序中的错误。
ms.openlocfilehash: cb0c16a74e68b5a16ef0f2011f65b22675950f58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752723"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a>在 Exchange 处理与通知相关 EWS 中的错误

了解如何处理与通知相关的您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发应用程序中的错误。
  
如果您的应用程序订阅并获取通知，您可能需要处理与通知相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。
  
**表 1。与通知相关的错误和如何处理它们**

|Error|您尝试对时发生...|处理由...|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |打开要获取事件时达到的连接限制的帐户打开流式连接的连接。 | <ul><li>使用[模拟](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)到[打开连接](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>使用较少的连接可获取事件。 通过[使用关联](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)和[放置 200 订阅 Id 同一组中的最大](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain)最大化中每个连接的订阅数。 然后可以使用相同的连接以检索整个组，从而减少了所需的连接数的事件。</li><li>  更改 HangingConnectionLimit Exchange 内部部署的 web.config 文件中覆盖三个打开的连接的默认值的值。 Exchange Online 有默认的 10，HangingConnectionLimit 不可配置。</li></ul> |
|**ErrorExceededSubscriptionCount** |创建订阅过多。 [EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)限制策略参数确定帐户可以创建的订阅的最大的数目。 | <ul><li>使用[模拟](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)为[创建订阅](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>减少的订阅数。</li></ul> |
|**ErrorInvalidSubscriptionRequest** |从单个请求创建多个邮箱或多个文件夹的订阅。  |在单个请求中创建一个公用文件夹或对单个邮箱订阅。| 
|**ErrorInvalidWatermark** |通过使用无效水印获取事件。| <ul><li>检查的订阅 ID 的以前的响应中返回。</li><li>确保您发送正确的**ExchangeService**对象的订阅 ID。</li><li>[创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**ErrorMissedNotificationEvents** |获取时出现遗漏某些以前的事件的事件。   |比较**PR_LOCAL_COMMIT_TIME_MAX** (0x670a) and **PR_DELETED_COUNT_TOTAL** (0x670b)，以确定哪些更改已错过了，扩展的文件夹属性并[创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。  |
|**ErrorProxyRequestNotAllowed** |订阅批处理请求其邮箱已移动到另一个网站中的用户的事件。   |使用[自动发现](autodiscover-for-exchange.md)重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新的订阅。  |
|**ErrorReadEventsFailed** |获得找不到订阅事件。  |使用[自动发现](autodiscover-for-exchange.md)重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新的订阅。  |
|**ErrorServerBusy** | 超过[带宽限制](ews-throttling-in-exchange.md#bk_ThrottlingNotifications)的限制。 注意以下相关限制：<ul><li>限制限制[EwsMaxSubscriptions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)标识推送、 请求或流式处理可同时处于活动状态的通知订阅的最大数量。 这是邮箱订阅，不邮箱订阅中的单个文件夹订阅数的值。 启动与服务邮箱版本 14.16.0135 和 14.15.0057.000 承载的 Exchange Online 或 Exchange Online 作为 Office 365 的一部分邮箱可以具有最多为 20 订阅，并且目标 Exchange 2013 内部部署邮箱可以具有最多 5000 位订阅。</li><li>限制限制[EwsMaxConcurrency](http://msdn.microsoft.com/en-us/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx)标识的非流式连接的活动请求的最大数量具有默认值为 27。</li><li>打开的流连接的默认限制为 10。</li></ul> |<ul><li>[考虑与通知相关的限制策略的含义](ews-throttling-in-exchange.md#bk_ThrottlingNotifications)和限制的活动订阅和活动的连接数，以便应用程序不会限制。</li><li>使用较少的连接可获取事件。 通过[发出 200 订阅 Id 同一组中的最大](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)最大化中每个连接的订阅数。 然后可以使用相同的连接以检索整个组，从而减少了所需的连接数的事件。</li><li>更改 HangingConnectionLimit web.config 文件中，若要覆盖的十个打开的流连接的默认值的值。</li></ul>|
|**ErrorSubscriptionNotFound** |获得找不到订阅事件。 订阅可能已到期、 EWS 过程可能具有已重新启动，或传递了无效的订阅。 | <ul><li>确认正在使用相同的以前的响应中返回的订阅 ID。</li><li>确保您发送正确的**ExchangeService**对象的订阅 ID。</li><li> [创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**[ServiceLocalException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |订阅连接上另一个文件夹中打开时，将订阅添加到新文件夹。  |更改您的订阅订阅的邮箱，而不是特定文件夹中的所有文件夹。  |
|**[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |事件获得找不到订阅 Exchange 存储中。  | <ul><li>确认正在使用相同的以前的响应中返回的订阅 ID。</li><li>确保您发送正确的**ExchangeService**对象的订阅 ID。</li></ul> |
   
## <a name="recovering-from-lost-subscriptions"></a>从丢失订阅恢复
<a name="bk_recover"> </a>

当订阅将会丢失，或将不再可访问时，最好创建新的订阅并不包括新的订阅中的旧水印。 与旧水印 resubscribing 使线性扫描的事件，即代价高昂。 相反，创建新的订阅并比较文件夹属性查找的内容的更改，丢失的订阅和新的订阅之间发生。 我们建议您查看扩展的文件夹属性是**PR_LOCAL_COMMIT_TIME_MAX** (0x670a0040) 和**PR_DELETED_COUNT_TOTAL** (0x670b0003)。 您可以通过[创建扩展的属性定义](properties-and-extended-properties-in-ews-in-exchange.md)来执行此操作。
  
## <a name="see-also"></a>另请参阅

- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [有关在 Exchange 中使用 EWS 邮箱事件流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)    
- [在 Exchange 使用 EWS 提取有关邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)    
- [在 Exchange 维护一组订阅和邮箱服务器之间的关联](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    

