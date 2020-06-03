---
title: 在 Exchange 中处理 EWS 中与通知相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: 了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中通知相关的错误。
ms.openlocfilehash: 60edb1344e6b0499ef6d2ed2aefaebde723b42cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528312"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a>在 Exchange 中处理 EWS 中与通知相关的错误

了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中通知相关的错误。

如果应用程序订阅并获取通知，则可能需要处理与通知相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。

**表1。通知相关错误以及如何处理这些错误**

|错误|当您尝试 .。。|处理它的...|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |打开一个连接，以便在帐户达到其开放流连接的连接限制时获取事件。 | <ul><li>使用[模拟](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)[打开连接](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>使用较少的连接获取事件。 [使用相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)将每个连接中的订阅数最大化，并将[最多为200个订阅 id 放在同一组中](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain)。 然后，可以使用相同的连接来检索整个组的事件，从而减少所需的连接数。</li><li>  更改 Exchange 本地的 web.config 文件中 HangingConnectionLimit 的值，以覆盖三个打开的连接的默认值。 Exchange Online 的默认 HangingConnectionLimit 为10，不可配置。</li></ul> |
|**ErrorExceededSubscriptionCount** |创建的订阅过多。 [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)限制策略参数确定帐户可以创建的最大订阅数。 | <ul><li>使用[模拟](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)[创建订阅](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>减少订阅的数量。</li></ul> |
|**ErrorInvalidSubscriptionRequest** |通过单个请求为多个邮箱或多个文件夹创建订阅。  |在单个请求中为单个公用文件夹或单个邮箱创建订阅。|
|**ErrorInvalidWatermark** |使用无效的水印获取事件。| <ul><li>检查在之前的响应中返回的订阅 ID。</li><li>确保您正在为正确的**ExchangeService**对象发送订阅 ID。</li><li>[创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**ErrorMissedNotificationEvents** |在缺少一些以前的事件时获取事件。   |将扩展文件夹属性与**PR_LOCAL_COMMIT_TIME_MAX** （0x670a）和**PR_DELETED_COUNT_TOTAL** （0x670b）进行比较，以确定丢失了哪些更改，并[创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。  |
|**ErrorProxyRequestNotAllowed** |在邮箱已移动到其他网站的批处理请求中订阅用户的事件。   |使用[自动发现](autodiscover-for-exchange.md)重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新的订阅。  |
|**ErrorReadEventsFailed** |从无法找到的订阅中获取事件。  |使用[自动发现](autodiscover-for-exchange.md)重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新的订阅。  |
|**ErrorServerBusy** | 超过[限制](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications)限制。 请注意以下相关限制：<ul><li>[EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)限制限制标识可一次活动的最大推送、请求或流式通知订阅数。 这是邮箱订阅的值，而不是邮箱订阅中的单个文件夹订阅的数量。 从服务邮箱版本14.16.0135 和14.15.0057.000 中开始，Exchange Online 或 Exchange Online 作为 Office 365 的一部分托管的邮箱最长可包含20个订阅，而目标 Exchange 2013 本地邮箱最长可有5000个订阅。</li><li>[限制](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx)限制限制标识非流式连接的活动请求的最大数量，其默认值为27。</li><li>打开的流式连接的默认限制为10个。</li></ul> |<ul><li>[考虑与通知相关的限制策略的含义](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications)，并限制活动订阅和活动连接数，使应用程序不会受到限制。</li><li>使用较少的连接获取事件。 [将最多200个订阅 id 放在同一组中](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)，以最大限度地提高每个连接中的订阅数。 然后，可以使用相同的连接来检索整个组的事件，从而减少所需的连接数。</li><li>在 web.config 文件中更改 HangingConnectionLimit 的值，以替代10个打开的流式连接的默认值。</li></ul>|
|**ErrorSubscriptionNotFound** |获取找不到的订阅的事件。 订阅可能已过期，EWS 进程可能已重新启动，或者传入了无效的订阅。 | <ul><li>验证您使用的订阅 ID 与以前的响应中返回的订阅 ID 相同。</li><li>确保您正在为正确的**ExchangeService**对象发送订阅 ID。</li><li> [创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**[ServiceLocalException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |在另一个文件夹上打开订阅连接时，将订阅添加到新文件夹。  |将订阅更改为订阅邮箱中的所有文件夹，而不是特定文件夹。  |
|**[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |获取无法位于 Exchange 存储中的订阅的事件。  | <ul><li>验证您使用的订阅 ID 与以前的响应中返回的订阅 ID 相同。</li><li>确保您正在为正确的**ExchangeService**对象发送订阅 ID。</li></ul> |

## <a name="recovering-from-lost-subscriptions"></a>从丢失的订阅恢复
<a name="bk_recover"> </a>

当订阅丢失或无法再访问时，最好创建一个新的订阅，而不在新订阅中包含旧的水印。 使用旧水印的 Resubscribing 会导致对事件进行线性扫描，这会导致成本高昂。 而是创建一个新的订阅，并比较文件夹属性以查找在丢失的订阅和新订阅之间发生的内容更改。 我们建议您检查的扩展文件夹属性**PR_LOCAL_COMMIT_TIME_MAX** （0x670a0040）和**PR_DELETED_COUNT_TOTAL** （0x670b0003）。 您可以通过[创建扩展属性定义](properties-and-extended-properties-in-ews-in-exchange.md)来执行此操作。

## <a name="see-also"></a>另请参阅

- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [在 Exchange 中使用 EWS 流式处理有关邮箱事件的通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [使用 Exchange 中的 EWS 获取有关邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)


