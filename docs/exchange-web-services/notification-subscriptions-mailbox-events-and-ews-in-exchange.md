---
title: 通知订阅、 邮箱事件和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 76136f28-0dad-4ecc-9dd7-a45a1861e4b0
description: 了解有关通知订阅和 EWS 中的邮箱事件在 Exchange。
ms.openlocfilehash: 4f466c6cc01af410807948a9fec40c2af399c3e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753007"
---
# <a name="notification-subscriptions-mailbox-events-and-ews-in-exchange"></a>通知订阅、 邮箱事件和 Exchange 中的 EWS

了解有关通知订阅和 EWS 中的邮箱事件在 Exchange。
  
您可以使用 EWS 托管 API 和 Exchange Web Services (EWS) 订阅事件发生在邮箱，或在一个或多个邮箱中的一个文件夹中时收到通知。 有三个订阅类型： 流式传输通知，拉通知和推送通知。 每个订阅类型使用不同的技术来接收或检索通知。
  
## <a name="getting-notifications---what-are-my-options"></a>获取通知-我的选项什么？
<a name="bk_notiftypes"> </a>

EWS 包括三个独立工作向客户端的服务器上更改通知的订阅类型。 预订类型选择，您将有权访问所有相同通知事件最终-无论它是只需如何获取它们。
  
**表 1。预订类型**

|**选项**|**说明**|**适合它为我？**|
|:-----|:-----|:-----|
|流式处理通知  <br/> |由服务器通过指定时间内保持打开状态的连接发送的通知。  <br/> |流式通知通常建议对于大多数应用程序中。 它们类似于拉和推送通知，并提供这两个领域的优势。 在建立通知订阅之后，连接将保持打开的最多 30 分钟，以便向客户端的推送通知的服务器。 像即可与请求订阅，并且您无需创建 web 侦听器应用程序强制订阅像请求更新，无需。  <br/> |
|提取通知  <br/> |所请求 （或中拉取） 由客户端的通知。  <br/> |拉通知是通常最适合松散耦合客户端，其中客户端不可靠地连接到网络。 拉通知可以创建客户端和服务器之间的多余流量，因为客户端将频繁请求发送到服务器以检索通知，并且不是所有请求所都产生的检索的通知。  <br/> |
|推送通知  <br/> |通知要发送 （或推送） 客户端到服务器的 web 服务通过回调地址。  <br/> |通常，推送通知提供比拉通知的较小通知延迟，并且适合紧密耦合的客户端到服务器具有可靠地访问和客户端是 IP 寻址。 但是，推送通知已弃用不以来的流通知在 Exchange 2010 一起工作。 如果可能，我们建议您使用流式通知，而不是循序的推送通知。 推送通知要求您编写侦听器应用程序，它是其中推送通知到。 它可以减少网络通信，但它需要单独的应用程序添加开销，这会通过拉通知有少许收益。  <br/> |
   
## <a name="what-ews-events-can-i-subscribe-to"></a>可以订阅的 EWS 中的哪些事件？
<a name="bk_eventtypes"> </a>

由 EWS 托管 API 的[EventType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx)枚举或 EWS 的[EventType](http://msdn.microsoft.com/library/04b70f9e-c226-4130-958e-0db0275cf58b%28Office.15%29.aspx)元素定义的客户端订阅的 EWS 事件的类型。 以下 EWS 事件供订阅： 
  
- NewMail — 新消息到达收件箱中。
    
- 删除 — 一条消息，很难从收件箱中删除。 若要了解有关已删除的邮件通知的详细信息，请参阅[使用 EWS 在 Exchange 中删除项目](deleting-items-by-using-ews-in-exchange.md)并[在 Exchange 拉 EWS 删除相关邮箱事件通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)。
    
- 修改 — 项目或文件夹已更改。
    
- 移动 — 项目或文件夹已移动。 
    
- 复制 — 项目或文件夹已复制。
    
- 创建 — 项目或文件夹的创建。 
    
- FreeBusyChanged — 已更改用户的忙/闲信息。
    
另一种 EWS 事件类型，状态事件中，定义[EventType](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx)元素，但不订阅此事件。 相反，它是发送服务器检查客户端的流式传输和推送通知的状态。 客户端需要响应这个事件需求或客户端将超时时间。 
  
通常的单个用户操作导致的多个通知创建。 为了说明这一点下, 图显示了一些常见方案和为每个创建的通知。 客户端设置会影响收到，通知，因此这不是所有配置选项和生成通知的详尽列表。
  
**图 1。返回的通知订阅的事件类型**

![此表格显示在常见用户情境下发送的通知，例如收到新的电子邮件、创建新的文件夹、移动某个文件夹等。](media/Exchange2013_Notifications_Events.png)
  
图 1 简化了通知过程。 实际上，可以为单个用户操作创建多个通知 （甚至相同类型的多个通知）。 例如，对于文件夹移动操作，三个文件夹创建事件： 一个用于要修改的文件夹、 旧的父文件夹，和新的父文件夹。 因为许多事件可以为单个操作而触发，我们建议您[构建一个几秒钟到同步操作的等待时间](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)，以便仅同步操作完成后，而不是通过操作的一部分。
  
也很重要认识到，每个用户选择的配置设置会影响创建的通知。 例如，某些用户的忙/闲数据将被自动更新和时收到新会议请求，甚至他们已经阅读该项目之前创建的 FreeBusyChanged 事件。 和其他用户的忙/闲数据不更新接受会议之后，直到创建不 FreeBusyChanged 事件。 这些设置会对由服务器创建通知相当大的影响。
  
## <a name="how-do-ews-notifications-work"></a>EWS 通知的工作方式？
<a name="bk_howwork"> </a>

EWS 通知订阅逐个处理。 通常没有有一个订阅每个邮箱，并且内的邮箱订阅您可以订阅的部分或所有文件夹。 您决定哪种类型的通知订阅 （流视频、 请求或推送） 和哪种类型的事件您想要接收 （NewMail、 创建、 删除、 修改时间等），然后创建订阅。 EWS 事件是然后异步从邮箱服务器发送到客户端。 (历史记录课： 事件都是在 Exchange 2007-同步和事件都存储在 Exchange 2010 客户端访问服务器上，但没有更多 ！)。
  
根据已的订阅的类型，其中通知发送到客户端的方式会有所不同。 本节介绍每种类型的订阅中更多详细信息的方式。
  
### <a name="ews-streaming-notifications"></a>EWS 流式通知
<a name="bk_streamnotif"> </a>

流式通知依赖悬挂 get 请求的服务器上的流式订阅连接保持打开状态，以便连接处于活动状态时出现的任何事件流式传输到客户端立即。 可以通过单个连接，并连接保持打开，直到间隔过期，或者最多 30 分钟的课程发送多个通知。 客户端连接过期后，发送溢出再次 get 请求。 图 2 显示了如何工作流订阅和流式处理通知。
  
**图 2。流式处理通知概述 （英文）**

![此插图显示流通知的工作原理。设置流通知的步骤：1. 订阅；2. 打开连接；3. 等待事件；4. 接收事件，重复 3 和 4；5. 关闭或保留连接；6. 取消订阅或超时。](media/Exchange2013_Notifications_StreamSub.png)
  
有关创建流式通知的信息，请参阅[有关使用 EWS 在 Exchange 邮箱事件的流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-pull-notifications"></a>EWS 拉通知
<a name="bk_pullnotif"> </a>

拉通知依赖于客户端上，客户端管理间隔要求通知。 这会导致 GetEvents 响应与任何通知。 图 3 显示请求订阅和拉通知的工作方式。
  
**图 3。提取通知概述 （英文）**

![此插图显示拉取通知的工作原理。设置拉取通知的步骤：1. 订阅；2. 发送 GetEvents；3. 接收答复，重复 2 和 3；4. 关闭或保留连接；5. 取消订阅或超时。](media/Exchange2013_Notifications_PullSub.png)
  
有关创建拉通知的信息，请参阅[有关使用 EWS 在 Exchange 邮箱事件出现通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-push-notifications"></a>EWS 推送通知
<a name="bk_pushnotif"> </a>

推送通知依赖于服务器返回到客户端推送通知。 没有通知时仅流量。 图 4 显示强制订阅和推送通知的工作方式。
  
**图 4。推送通知概述 （英文)**

![此插图显示推送通知的工作原理。设置推送通知的步骤：1. 创建侦听器；2. 订阅；3. 等待事件；4. 接收事件；5. 发送“确定”答复，重复 3、4、和 5；6. 取消订阅或超时。](media/Exchange2013_Notifications_PushSub.png)
  
如果您使用[与 Exchange 2010 的推送通知](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)，请考虑升级应用程序[使用流式通知](http://code.msdn.microsoft.com/exchange/Exchange-2013-Set-push-82738cc5)，以便您无需单独的应用程序以接收事件。
  
## <a name="how-do-i-subscribe-to-notifications"></a>如何订阅通知？
<a name="bk_notifoperations"> </a>

根据您想要创建的订阅的类型，您有多种选项可供选择的订阅通知。
  
**表 2。操作和用于订阅通知的方法**

|**预订类型**|**EWS 操作**|**EWS 托管 API 方法**|**它的用途**|
|:-----|:-----|:-----|:-----|
|流式处理  <br/> |[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToStreamingNotifications 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToStreamingNotificationsOnAllFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToStreamingNotificationsOnAllFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> |创建订阅通知流式处理的请求。  <br/> |
|提取  <br/> |[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPullNotifications 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPullNotificationsOnAllFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotifications 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPullNotificationsOnAllFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建订阅拉通知的请求。  <br/> |
|推送  <br/> |[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService.BeginSubscribeToPushNotifications 重载方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSubscribeToPushNotificationsOnAllFolders 重载方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotifications 重载方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService.SubscribeToPushNotificationsOnAllFolders 重载方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建订阅推送通知的请求。  <br/> |
   
## <a name="how-do-i-get-ews-events"></a>如何获取 EWS 事件？
<a name="bk_getevents"> </a>

创建订阅后，在其中的实际事件发送到客户端的方式取决于预订类型。 
  
进行流式处理通知，必须先创建传输的订阅连接，然后订阅添加到该连接。 您可以阅读更多有关此过程中[使用 EWS 在 Exchange 邮箱事件有关的流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。 
  
出现通知订阅对象已初始化时创建订阅，因此只需调用**GetEvent**方法或要从服务器中检索事件的操作。 您可以阅读更多有关此中[提取有关使用 EWS 在 Exchange 邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。 
  
下表列出的操作和检索事件所需的类。 
  
**表 3。元素和类可用于创建连接和获取事件**

|**预订类型**|**EWS 操作**|**EWS 托管的 API 方法**|**它的用途**|
|:-----|:-----|:-----|:-----|
|流式处理  <br/> |[GetStreamingEvents 操作](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) <br/> |[StreamingSubscriptionConnection.AddSubscription 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.addsubscription%28v=exchg.80%29.aspx) <br/> |创建悬挂事件发生时做出响应的服务器上的 get 请求。  <br/> |
|提取  <br/> |[GetEvents 操作](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) <br/> |[PullSubscription.GetEvents 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) <br/> |获取从服务器中请求通知事件。  <br/> |
|推送  <br/> |不适用。  <br/> |不适用。  <br/> |推送通知会自动发送给 web 服务侦听器 (订阅请求中指定的回调 URL)。 没有其他方法或操作需要调用。  <br/> |
   
## <a name="how-do-i-unsubscribe-to-notifications"></a>如何取消订阅通知？
<a name="bk_notifunsubscribe"> </a>

下表列出了您可以在其中取消订阅的每种类型的方式。
  
**表 4。操作和通知取消订阅的方法**

|**预订类型**|**EWS**|**EWS Managed API**||
|:-----|:-----|:-----|:-----|
|流式处理  <br/> |[取消操作](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[StreamingSubscription.BeginUnsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.EndUnsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription.Unsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|提取  <br/> |[取消操作](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[PullSubscription.BeginUnsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.EndUnsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription.Unsubscribe 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|推送  <br/> |[SendNotificationResponseMessage](http://msdn.microsoft.com/library/2c6d681b-67ac-4331-bc6b-a2e709b638e3%28Office.15%29.aspx)的[StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)元素中返回**取消订阅** <br/> |不可用。 而是让订阅超时。  <br/> ||
   
此外，您可以让每个订阅超时。 
  
**表 5。订阅超时**

|**预订类型**|**Ews 的超时值**|**EWS 托管 API 中的超时值**|**超时处理**|
|:-----|:-----|:-----|:-----|
|流式处理  <br/> |[ConnectionTimeout](http://msdn.microsoft.com/library/14da68a0-bcca-4281-a774-47644baa4ee9%28Office.15%29.aspx)元素  <br/> | *生存期* [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)构造函数参数  <br/> |对于 EWS 托管 API 后经过的超时值， [OnDisconnect](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.ondisconnect%28v=exchg.80%29.aspx)事件引发。 如果未调用[StreamingSubscriptionConnection.Open](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.open%28v=exchg.80%29.aspx)方法，则连接已关闭。  <br/> 对于 EWS 后经过的超时值，, [GetUserConfigurationResponse](http://msdn.microsoft.com/library/5e418c91-c836-4de0-a80d-f0dad0c684d7%28Office.15%29.aspx)消息返回[ConnectionStatus](http://msdn.microsoft.com/library/4300f9d6-8bf9-48c2-9f07-d80197864e17%28Office.15%29.aspx)值的已关闭。  <br/> |
|提取  <br/> |[超时](http://msdn.microsoft.com/library/c2e1ca5a-6667-4f6f-aac4-89de33bddc54%28Office.15%29.aspx)元素  <br/> | *timeout*参数的[SubscribeToPullNotification](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法  <br/> |回拨此前的超时值后，服务器中删除订阅。  <br/> |
|推送  <br/> |[StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)元素  <br/> | *频率* [SubscribeToPushNotification](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx)方法参数  <br/> |如果服务器未收到对推送通知或状态 ping 的响应，它重试停止发送通知前几次发送通知。 有关详细信息，请参阅[StatusFrequency](http://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)。  <br/> |
   
## <a name="can-i-limit-subscriptions"></a>可以将限制订阅？
<a name="bk_limitsubs"> </a>

在本地部署中，您可以限制的每个用户的订阅数的限制策略的[EwsMaxSubscriptions 限制参数](ews-throttling-in-exchange.md)。 可以将该策略应用于所有用户还是仅特定用户。 限制策略**EwsMaxSubscriptions**不可用于 Exchange Online 配置。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_limitsubs"> </a>

- [有关在 Exchange 中使用 EWS 邮箱事件流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 提取有关邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 维护一组订阅和邮箱服务器之间的关联](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 处理与通知相关 EWS 中的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
- [Exchange web 服务引用](../web-service-reference/web-services-reference-for-exchange.md)
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
- [推送通知示例应用程序](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
    

