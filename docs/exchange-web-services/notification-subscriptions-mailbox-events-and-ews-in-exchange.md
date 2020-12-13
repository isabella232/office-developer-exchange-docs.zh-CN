---
title: Exchange 中的通知订阅、邮箱事件和 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 76136f28-0dad-4ecc-9dd7-a45a1861e4b0
description: 查找更多关于在 Exchange中的 EWS 中的通知订阅和邮箱时间的信息。
localization_priority: Priority
ms.openlocfilehash: 00a0941e615f35a46bb77c00648b75fcd2a45286
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603839"
---
# <a name="notification-subscriptions-mailbox-events-and-ews-in-exchange"></a>Exchange 中的通知订阅、邮箱事件和 EWS

查找更多关于在 Exchange中的 EWS 中的通知订阅和邮箱时间的信息。
  
你可以使用 EWS 托管 API 和Exchange Web 服务 (EWS) 订阅，以便当邮箱或邮箱中的一个或多个文件夹中的事件发生时接收通知。 这些订阅类型可用：流式通知、拉取通知和推送通知。 每个订阅类型使用不同的技术收取或检索通知。
  
## <a name="getting-notifications---what-are-my-options"></a>获取通知 - 我有哪些选择？
<a name="bk_notiftypes"> </a>

EWS 包含三种订阅类型，它们可以独立工作，通知服务器上的客户端任何发生的改变。 不管你选择哪种订阅，你将可以访问所有相同的通知事件 - 不同的只是你获取它们的方式。
  
**表 1. 订阅类型**

|**选项**|**说明**|**它适合我吗？**|
|:-----|:-----|:-----|
|流式通知  <br/> |通过连接由服务器发送的通知，该连接在特定时间内保持开放。  <br/> |流式通知一般适合大多数应用程序。 它们类似于拉取和推送通知，并结合了这两种的优点。 在你确定了通知订阅后，连接将会保持开放 30 分钟，以允许服务器向客户端推送通知。 不像拉取订阅那样需要请求更新，也不需要像推送订阅那样创建 Web 服务侦听器应用。  <br/> |
|拉取通知  <br/> |由客户端请求（拉）的通知。  <br/> |拉取通知一般来说适用于大多数松散的客户端，即它们并没有持续地连接到网络。 拉取通知可能在客户端和服务器之间创造过多的流量，因为客户端会向服务器频繁地请求检索通知，且不是所有请求都能取回通知。  <br/> |
|推送通知  <br/> |由服务器通过回拨地址向客户端 Web 服务发送的通知。  <br/> |一般来说，推送通知比拉取通知延迟较小，且适合重度用户，即有稳定访问权限且 IP 可查址的用户。 但是，自从流式通知于 2010 年来到 Exchange 后，推送通知就失去了宠爱。 如果可能的话，我们建议你以后使用流式通知而不是推送通知。 推送通知要求你写一个侦听器应用，也就是通知被推到的地方。 与拉取通知相比，这有一个小的好处，就是它可以减少线路流量，但是由于要求额外的应用，它也增加了开销。  <br/> |
   
## <a name="what-ews-events-can-i-subscribe-to"></a>我可以订阅什么 EWS 事件？
<a name="bk_eventtypes"> </a>

客户端订阅的 EWS 事件类型由 EWS 托管 API 的 [EventType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) 枚举或 EWS 的 [EventType](https://msdn.microsoft.com/library/04b70f9e-c226-4130-958e-0db0275cf58b%28Office.15%29.aspx)元素定义。 以下 EWS 事件可订阅： 
  
- NewMail - 新邮件抵达收件箱。
    
- Deleted - 邮件从收件箱中硬删除。 了解更多关于删除项通知，请参阅[在 Exchange 中使用 EWS 删除项](deleting-items-by-using-ews-in-exchange.md) 以及 [在 Exchange 中与 EWS 删除相关的邮箱事件拉取通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)。
    
- Modified - 项或文件夹有更改。
    
- Moved - 项或文件夹移动。 
    
- Copied - 项或文件夹被复制。
    
- Created - 项或文件夹被创建。 
    
- FreeBusyChanged - 用户的空闲忙碌信息更改。
    
另一个 EWS 事件类型，状态事件，由 [EventType](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx) 元素定义，但你无需订阅此事件。 状态事件仅在流式和推送通知中由服务器发送，以检查客户端的状态。 用户需要响应此事件或用户超时。 
  
单一用户操作经常导致多个通知的建立。 为阐释这一点，下文的图显示了一些常见的应用场景以及每个场景中创建的通知。 用户设置对所收通知有影响，所以此列表不能穷尽所有配置选项和最终通知。
  
**图 1. 通知订阅返回的事件类型**

![此表格显示在常见用户情境下发送的通知，例如收到新的电子邮件、创建新的文件夹、移动某个文件夹等。](media/Exchange2013_Notifications_Events.png)
  
图 1 简化了通知过程。 现实中，多个通知（甚至是多个同类型的通知）可以由单一用户操作创建。 比如，在文件夹移动操作的情况中，三个文件夹事件被创建：一个关于文件夹修改，一个关于旧文件夹，还有一个关于新文件夹。 因为单一操作可以出现多个事件，我们建议你[构建一个几秒长的等待事件到你的同步操作中](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)，这样同步只有在操作完成时才会进行，而不是在操作中多次进行。
  
另外很重要的是，每个用户选择的配置设置会影响最终创建的通知。 比如，一些用户的空闲忙碌数据是自动更新的，当收到新的会议请求时 FreeBusyChanged 事件就会被创建，这甚至早于他们阅读此请求的时间。 对于其他用户来说，空闲忙碌时间、FreeBusyChanged 事件在他们接受会议请求之前都不会更新或创建。 这些设置可能会对服务器创建的通知产生极大的影响。
  
## <a name="how-do-ews-notifications-work"></a>EWS 通知的原理是什么？
<a name="bk_howwork"> </a>

EWS 通知以订阅的形式进行。 通常，每个邮箱一个订阅，在邮箱订阅内你还可以订阅一些或所有文件夹。 你可以决定订阅什么种类的通知（流式、拉取、推送）以及接收什么种类的事件（NewMail、Created、Deleted、Modified等），然后可以创建订阅。 然后 EWS 事件会非同步地从邮箱服务器发送到客户端。 （历史经验：事件在 Exchange 2007 上是同步的 - 事件在 Exchange 2010 存储在 Client Access 服务器上，但现在已经不是了！）
  
取决于你的订阅类型，通知发送到客户端的方式不一。 本节介绍了每种订阅类型的具体工作原理。
  
### <a name="ews-streaming-notifications"></a>EWS 流式通知
<a name="bk_streamnotif"> </a>

流式通知依赖于一个在服务器挂起的 get 请求来保持流式订阅连接打开，这样任何在连接活动时发生的事件都会马上流给客户端。 多个通知可以在单个连接周期内发送，在至多 30 分钟的间隔期过期前，连接都会保持打开。 连接过期后，客户端再次发送 get 请求。 图 2 显示了流式订阅和流式通知工作的原理。
  
**图 2. 流式通知概述**

![此插图显示流通知的工作原理。设置流通知的步骤：1. 订阅；2. 打开连接；3. 等待事件；4. 接收事件，重复 3 和 4；5. 关闭或保留连接；6. 取消订阅或超时。](media/Exchange2013_Notifications_StreamSub.png)
  
更多关于创建流式通知的信息，请参阅[在 Exchange 上使用 EWS 时关于邮箱事件的流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-pull-notifications"></a>EWS 拉取通知
<a name="bk_pullnotif"> </a>

拉取通知依靠客户端以一定间隔请求客户端管理的通知。 这可能会在获得 GetEvents 响应时未收到通知。 图 3 显示了拉取订阅和拉取通知工作的原理。
  
**图 3. 拉取通知概述**

![此插图显示拉取通知的工作原理。设置拉取通知的步骤：1. 订阅；2. 发送 GetEvents；3. 接收答复，重复 2 和 3；4. 关闭或保留连接；5. 取消订阅或超时。](media/Exchange2013_Notifications_PullSub.png)
  
更多关于创建拉取通知的信息，请参阅[在 Exchange 上使用 EWS 时关于邮箱事件的拉取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-push-notifications"></a>EWS 推送通知
<a name="bk_pushnotif"> </a>

推送通知依靠服务区将通知推回到客户端。 只有在有通知时才会有流量。 图 4 显示了推送订阅和推送通知工作的原理。
  
**图 4. 推送通知概述**

![此插图显示推送通知的工作原理。设置推送通知的步骤：1. 创建侦听器；2. 订阅；3. 等待事件；4. 接收事件；5. 发送“确定”答复，重复 3、4、和 5；6. 取消订阅或超时。](media/Exchange2013_Notifications_PushSub.png)

如果你在使用 [Exchange 2010 和推送通知](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)，请考虑升级你的应用[使用流式通知](https://code.msdn.microsoft.com/exchange/Exchange-2013-Set-push-82738cc5)，这样你就不用一个额外的应用程序来收取事件了。

  
## <a name="how-do-i-subscribe-to-notifications"></a>我如何订阅通知？
<a name="bk_notifoperations"> </a>

取决于你想要创建的订阅类型，你有一些订阅通知的选项。
  
**表 2. 订阅通知的操作和方法**

|**订阅类型**|**EWS 操作**|**EWS 托管 API**|**功能**|
|:-----|:-----|:-----|:-----|
|流式  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToStreamingNotifications 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToStreamingNotificationsOnAllFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToStreamingNotificationsOnAllFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> |创建请求以订阅流式通知。  <br/> |
|拉取  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPullNotifications 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPullNotificationsOnAllFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotifications 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotificationsOnAllFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建请求以订阅流式通知。  <br/> |
|推送  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPullNotifications 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPushNotificationsOnAllFolders overload 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotifications overloaded 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPushNotificationsOnAllFolders overload 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建请求以订阅推送通知。  <br/> |
   
## <a name="how-do-i-get-ews-events"></a>如何获取 EWS 事件？
<a name="bk_getevents"> </a>

创建订阅后，实际事件发送到客户端的方式取决于订阅类型。 
  
对于流式通知而言，流式订阅连接必须创建，然后订阅会加到连接上。 你可以在[在 Exchange 上使用 EWS 时关于邮箱事件的流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)中了解更多有关此过程的信息。 
  
对于推送通知而言，订阅对象在订阅创建时初始化，这样你只需调用 **GetEvent** 方法或操作来从服务器检索事件。 你可以在[在 Exchange 上使用 EWS 时关于邮箱事件的推送通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)中了解更多有关信息。 
  
接下来的表列出了检索事件所需的操作和类。 
  
**表 3. 创建连接和获取事件的元素和类**

|**订阅类型**|**EWS 操作**|**EWS 托管 API 方法**|**功能**|
|:-----|:-----|:-----|:-----|
|流式  <br/> |[GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) <br/> |[StreamingSubscriptionConnection.AddSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.addsubscription%28v=exchg.80%29.aspx) <br/> |在服务器上创建一个挂起的 get 请求，当事件发生时，该请求会被响应。  <br/> |
|拉取  <br/> |[GetEvents 操作](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) <br/> |[PullSubscription.GetEvents 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) <br/> |从服务器获取拉取通知事件。  <br/> |
|推送  <br/> |不适用。  <br/> |不适用。  <br/> |推送通知自动发送到 Web 服务倾听器（订阅请求中指定的回拨 URL）。 无额外的方法或操作需要被调用。  <br/> |
   
## <a name="how-do-i-unsubscribe-to-notifications"></a>我如何取消订阅通知？
<a name="bk_notifunsubscribe"> </a>

下列表格列出了你取消退订每一种订阅的方法。
  
**表 4. 取消订阅通知的操作和方法**

|**订阅类型**|**EWS**|**EWS 托管 API**||
|:-----|:-----|:-----|:-----|
|流式  <br/> |[Unsubscribe 操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[StreamingSubscription.BeginUnsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.EndUnsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.Unsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|拉取  <br/> |[Unsubscribe 操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[PullSubscription.BeginUnsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.EndUnsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.Unsubscribe 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|推送  <br/> |在 [SendNotificationResponseMessage](https://msdn.microsoft.com/library/2c6d681b-67ac-4331-bc6b-a2e709b638e3%28Office.15%29.aspx) 的元素 [StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx) 中返回 **Unsubscribe** <br/> |不适用 让订阅超时。  <br/> ||
   
或者，你可以让每个订阅超时。 
  
**表 5. 订阅超时**

|**订阅类型**|**EWS 中的超时值**|**EWS 托管 API 中的超时值**|**处理超时**|
|:-----|:-----|:-----|:-----|
|流式  <br/> |[ConnectionTimeout](https://msdn.microsoft.com/library/14da68a0-bcca-4281-a774-47644baa4ee9%28Office.15%29.aspx) 元素  <br/> | [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)构造函数的 *生存期*  <br/> |对于 EWS 托管 API，超时值走完后，会引发 [OnDisconnect](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.ondisconnect%28v=exchg.80%29.aspx) 事件。 如果 [StreamingSubscriptionConnection.Open](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.open%28v=exchg.80%29.aspx) 方法未被调用，连接将关闭。  <br/> 对于 EWS，超时值走完后，[GetUserConfigurationResponse](https://msdn.microsoft.com/library/5e418c91-c836-4de0-a80d-f0dad0c684d7%28Office.15%29.aspx) 消息会返回一个 [ConnectionStatus](https://msdn.microsoft.com/library/4300f9d6-8bf9-48c2-9f07-d80197864e17%28Office.15%29.aspx)的关闭值。  <br/> |
|拉取  <br/> |[超时](https://msdn.microsoft.com/library/c2e1ca5a-6667-4f6f-aac4-89de33bddc54%28Office.15%29.aspx)元素  <br/> | [SubscribeToPullNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) 方法的 *超时* 参数  <br/> |超时值走完后，服务器会删除订阅。  <br/> |
|推送  <br/> |[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx) 元素  <br/> | [SubscribeToPushNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) 方法的 *频率* 参数  <br/> |如果服务器没有收到对推送通知或状态 ping 的响应，它会重新尝试发送通知几次，然后才停止发送通知。 有关详细信息，请参阅[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)  <br/> |
   
## <a name="can-i-limit-subscriptions"></a>我可以限制订阅吗？
<a name="bk_limitsubs"> </a>

在本地部署中，你可以用[EwsMaxSubscriptions 限制参数](ews-throttling-in-exchange.md)限制每个用户的订阅数量限制。 该策略可以应用到全部用户或仅具体用户。 **EwsMaxSubscriptions** 限制策略对 Exchange Online 不可配置。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_limitsubs"> </a>

- [在 Exchange 上使用 EWS 时关于邮箱事件的流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 上使用 EWS 时关于邮箱事件的拉取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 中保持一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 中使用 EWS 时处理通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
- [Exchange Web 服务参考](../web-service-reference/web-services-reference-for-exchange.md)
- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
- [邮箱同步和 Exchange 中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
- [推送通知示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
    

