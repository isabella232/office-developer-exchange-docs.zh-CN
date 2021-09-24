---
title: 在 Exchange 中使用 EWS 时处理通知相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 519e1e52-5f1f-4f06-931e-8c20a586a563
description: 了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与通知Exchange。
ms.openlocfilehash: 7b49a57b7236318e08cb70ac2ac00edc4cf86363
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520211"
---
# <a name="handling-notification-related-errors-in-ews-in-exchange"></a>在 Exchange 中使用 EWS 时处理通知相关的错误

了解如何在应用程序中使用 EWS 托管 API 或 EWS 在应用程序中处理与通知Exchange。

如果应用程序订阅并获取通知，可能必须处理与通知相关的错误。 您可以处理这些错误在运行时，或者开发 EWS 应用程序时。

**表 1.与通知相关的错误以及如何处理它们**

|错误|在尝试...|处理它的...|
|:-----|:-----|:-----|
|**ErrorExceededConnectionCount** |打开连接，在帐户达到开放流连接的连接限制时获取事件。 | <ul><li>使用[模拟打开](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)[连接](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>使用更少的连接获取事件。 通过使用相关性，并在同一组中放置最多[](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)[200](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howdoimaintain)个订阅 ID，最大程度地增加每个连接中的订阅数。 然后，可以使用同一连接检索整个组的事件，从而减少所需的连接数。</li><li>  在本地更改 web.config 文件中 HangingConnectionLimit Exchange以覆盖三个打开的连接的默认值。 Exchange Online的 HangingConnectionLimit 的默认值为 10，这是不可配置的。</li></ul> |
|**ErrorExceededSubscriptionCount** |创建过多订阅。 [EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)限制策略参数确定帐户可以创建的最大订阅数。 | <ul><li>使用[模拟](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)[创建订阅](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling)。</li><li>减少订阅数。</li></ul> |
|**ErrorInvalidSubscriptionRequest** |从单个请求创建多个邮箱或多个文件夹的订阅。  |为单个公用文件夹或单个请求中的单个邮箱创建订阅。|
|**ErrorInvalid使用Mark** |使用无效水印获取事件。| <ul><li>检查上一响应中返回的订阅 ID。</li><li>确保发送正确的 **ExchangeService** 对象的订阅 ID。</li><li>[创建新订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**ErrorMissedNotificationEvents** |获取一些之前错过的事件。   |比较扩展文件夹PR_LOCAL_COMMIT_TIME_MAX (0x670a) 和PR_DELETED_COUNT_TOTAL (0x670b) ，以确定遗漏了哪些更改，[并创建新的订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。  |
|**ErrorProxyRequestNotAllowed** |订阅用户邮箱已移动到其他网站的批处理请求中的事件。   |使用 [自动发现](autodiscover-for-exchange.md) 重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新订阅。  |
|**ErrorReadEventsFailed** |从找不到的订阅获取事件。  |使用 [自动发现](autodiscover-for-exchange.md) 重新发现 ExternalEwsUrl 或 EwsPartnerUrl，并创建新订阅。  |
|**ErrorServerBusy** | 超过 [限制](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) 。 请注意以下有关限制的事项：<ul><li>[EwsMaxSubscriptions](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxsubscriptions%28v=exchg.150%29.aspx)限制标识可同时处于活动状态的推送、拉取或流式处理通知订阅的最大数量。 这是邮箱订阅的值，而不是邮箱订阅中单个文件夹订阅的数量。 从服务邮箱版本 14.16.0135 和 14.15.0057.000 开始，Exchange Online 或 Exchange Online 作为 Office 365 的一部分托管的邮箱可具有最多 20 个订阅，目标 Exchange 2013 本地邮箱最多具有 5000 个订阅。</li><li>[EwsMaxConcurrency](https://msdn.microsoft.com/library/microsoft.exchange.data.directory.systemconfiguration.throttlingpolicy.ewsmaxconcurrency%28v=exchg.150%29.aspx)限制标识非流式连接的最大活动请求数，默认值为 27。</li><li>开放流连接的默认限制为 10 个。</li></ul> |<ul><li>[考虑通知相关](ews-throttling-in-exchange.md#throttling-considerations-for-ews-notification-applications) 限制策略的影响，并限制活动订阅和活动连接的数量，以便应用程序不会受到限制。</li><li>使用更少的连接获取事件。 通过将最多 [200](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)个订阅 ID 置于同一组中，最大程度地增加每个连接中的订阅数。 然后，可以使用同一连接检索整个组的事件，从而减少所需的连接数。</li><li>更改项目文件中 HangingConnectionLimit web.config以覆盖 10 个打开的流式连接的默认值。</li></ul>|
|**ErrorSubscriptionNotFound** |获取找不到的订阅的事件。 订阅可能已过期，EWS 进程可能已重新启动，或者传递了无效的订阅。 | <ul><li>验证你使用的订阅 ID 是否与上一响应中返回的订阅 ID 相同。</li><li>确保发送正确的 **ExchangeService** 对象的订阅 ID。</li><li> [创建新订阅](handling-notification-related-errors-in-ews-in-exchange.md#bk_recover)。</li></ul> |
|**[ServiceLocalException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |当订阅连接在另一个文件夹上打开时，将订阅添加到新文件夹。  |更改订阅以订阅邮箱中所有文件夹，而不是特定文件夹。  |
|**[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)** |获取无法位于应用商店中的订阅Exchange事件。  | <ul><li>验证你使用的订阅 ID 是否与上一响应中返回的订阅 ID 相同。</li><li>确保发送正确的 **ExchangeService** 对象的订阅 ID。</li></ul> |

## <a name="recovering-from-lost-subscriptions"></a>从丢失的订阅中恢复
<a name="bk_recover"> </a>

订阅丢失或无法再访问时，最好创建新订阅，并且不要将旧水印包括在新订阅中。 重新订阅旧水印会导致对事件的线性扫描，这非常昂贵。 相反，创建新的订阅并比较文件夹属性，以查找丢失的订阅和新订阅之间发生的内容更改。 建议检查的扩展文件夹属性 **PR_LOCAL_COMMIT_TIME_MAX (0x670a0040) PR_DELETED_COUNT_TOTAL (0x670b0003) 。**  您可以通过创建扩展 [的属性定义 来这样做](properties-and-extended-properties-in-ews-in-exchange.md)。

## <a name="see-also"></a>另请参阅

- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [在 Exchange 上使用 EWS 时关于邮箱事件的流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [在 Exchange 上使用 EWS 时关于邮箱事件的拉取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [在 Exchange 中保持一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)


