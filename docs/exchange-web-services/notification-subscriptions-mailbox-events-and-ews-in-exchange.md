---
title: Notification subscriptions, mailbox events, and EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 76136f28-0dad-4ecc-9dd7-a45a1861e4b0
description: 了解 Exchange 中的 EWS 通知订阅和邮箱事件。
localization_priority: Priority
ms.openlocfilehash: 2a99b1922e021a8f5f221381d7f2965c3e1ab504
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459346"
---
# <a name="notification-subscriptions-mailbox-events-and-ews-in-exchange"></a>Notification subscriptions, mailbox events, and EWS in Exchange

了解 Exchange 中的 EWS 通知订阅和邮箱事件。
  
您可以使用 EWS 托管 API 和 Exchange Web 服务（EWS）在邮箱中发生事件时，或者在邮箱中的一个或多个文件夹中的一个或多个文件夹中，订阅接收通知。 可以使用三种订阅类型：流式通知、请求通知和推送通知。 这些订阅类型中的每一种都使用不同的技术来接收或检索通知。
  
## <a name="getting-notifications---what-are-my-options"></a>获取通知-什么是我的选项？
<a name="bk_notiftypes"> </a>

EWS 包括三种单独工作的订阅类型，用于将服务器上的更改通知客户端。 无论您选择哪种订阅类型，最终都有权访问所有相同的通知事件，这就是您如何获取它们的问题。
  
**表1。订阅类型**

|**选项**|**说明**|**适合我吗？**|
|:-----|:-----|:-----|
|流式处理通知  <br/> |由服务器通过在指定时间段内保持打开状态的连接发送的通知。  <br/> |通常，大多数应用程序都建议使用流式通知。 它们类似于请求和推送通知，并提供了这两个方面的最佳优势。 建立通知订阅后，连接将保持打开状态达30分钟，以允许服务器将通知推送回客户端。 无需请求更新，就像使用请求订阅一样，无需像使用推送订阅那样创建 web 服务侦听器应用程序。  <br/> |
|请求通知  <br/> |客户端请求（或请求）的通知。  <br/> |"拉" 通知通常最适用于松散耦合客户端，其中客户端不可靠地连接到网络。 由于客户端向服务器发送频繁的请求以检索通知，并且并非所有请求都会检索通知，因此请求通知可以在客户端和服务器之间创建多余的流量。  <br/> |
|推送通知  <br/> |通过回调地址将服务器发送（或推送）到客户端 web 服务的通知。  <br/> |通常，推送通知提供比 pull 通知更小的通知延迟，并且适用于服务器具有可靠访问权限且客户端为 IP 可寻址的紧密耦合客户端。 但是，由于 Exchange 2010 中出现流式通知，因此推送通知已停止。 如果可能，我们建议使用流式通知，而不是将推送通知转发。 推送通知要求您编写侦听器应用程序，即将通知推送到的位置。 这对 "拉" 通知略有好处，因为它可减少线路流量，但会因需要单独的应用程序而增加开销。  <br/> |
   
## <a name="what-ews-events-can-i-subscribe-to"></a>我可以订阅哪些 EWS 事件？
<a name="bk_eventtypes"> </a>

客户端订阅的 EWS 事件的类型由 EWS 托管 API 的[事件](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx)类型枚举或 Ews 的[事件](https://msdn.microsoft.com/library/04b70f9e-c226-4130-958e-0db0275cf58b%28Office.15%29.aspx)类型元素定义。 以下 EWS 事件可用于订阅： 
  
- NewMail —到达收件箱中的新邮件。
    
- 已删除—从收件箱中硬删除邮件。 若要了解有关已删除邮件通知的详细信息，请参阅[使用 exchange 中的 Ews 删除项目](deleting-items-by-using-ews-in-exchange.md)和[获取 EXCHANGE 中与 ews 删除相关邮箱事件的通知](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)。
    
- 已修改-项目或文件夹已更改。
    
- 已移动-项目或文件夹已移动。 
    
- 复制-项目或文件夹已复制。
    
- 已创建-项目或文件夹已创建。 
    
- FreeBusyChanged —用户的忙/闲信息已更改。
    
另一个 EWS 事件类型（状态事件）由[事件](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.eventtype%28v=exchg.80%29.aspx)类型元素定义，但您不订阅此事件。 相反，它由服务器发送，以检查客户端的状态以进行流式传输和推送通知。 客户端需要响应此事件的需要，否则客户端将超时。 
  
单个用户操作通常会导致创建多个通知。 为了说明这一点，下图显示了一些常见方案以及为每个方案创建的通知。 客户端设置会影响收到的通知，因此这并不是所有配置选项和生成的通知的详尽列表。
  
**图1。通知订阅返回的事件类型**

![此表格显示在常见用户情境下发送的通知，例如收到新的电子邮件、创建新的文件夹、移动某个文件夹等。](media/Exchange2013_Notifications_Events.png)
  
图1简化了通知过程。 实际上，可以为单个用户操作创建多个通知（甚至相同类型的多个通知）。 例如，在文件夹移动操作中，将创建三个文件夹事件：一个用于要修改的文件夹，一个用于旧父文件夹，一个用于新的父文件夹。 由于可能会触发单个操作的多个事件，因此我们建议您在[同步操作中构建几秒的等待时间](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)，以便仅在操作完成时进行同步，而不是中途通过操作进行同步。
  
还要认识的是，每个用户选择的配置设置会影响创建哪些通知。 例如，某些用户的忙/闲数据会自动更新，并且在收到新的会议请求（即使他们已阅读项目之前），将创建 FreeBusyChanged 事件。 对于其他用户，不会更新忙闲数据，也不会在接受会议后再创建 FreeBusyChanged 事件。 这些设置会对服务器所创建的通知产生重大影响。
  
## <a name="how-do-ews-notifications-work"></a>EWS 通知的工作原理是什么？
<a name="bk_howwork"> </a>

EWS 通知在订阅基础上进行处理。 通常每个邮箱有一个订阅，在邮箱订阅中，您可以订阅部分或所有文件夹。 您可以决定要订阅的通知类型（流、拉取或推送）以及要接收的事件类型（NewMail、已创建、已删除、已修改等），然后创建订阅。 然后，将 EWS 事件从邮箱服务器异步发送到客户端。 （历史记录课程：事件是 Exchange 2007 中的同步-并且事件存储在 Exchange 2010 中的客户端访问服务器上，而不是更多！）。
  
根据您拥有的订阅类型，将通知发送到客户端的方式会有所不同。 本节介绍了每种类型的订阅如何更详细地工作。
  
### <a name="ews-streaming-notifications"></a>EWS 流通知
<a name="bk_streamnotif"> </a>

流式通知依赖于服务器上的挂起 get 请求，以保持流式订阅连接处于打开状态，这样，在连接处于活动状态时发生的任何事件都将立即流式传输到客户端。 可以在单个连接的过程中发送多个通知，并且该连接将保持打开状态，直到间隔时间到期，或最多为30分钟。 连接过期后，客户端将再次发送挂起的 get 请求。 图2显示流式处理订阅和流式处理通知的工作原理。
  
**图2。流式通知概述**

![此插图显示流通知的工作原理。设置流通知的步骤：1. 订阅；2. 打开连接；3. 等待事件；4. 接收事件，重复 3 和 4；5. 关闭或保留连接；6. 取消订阅或超时。](media/Exchange2013_Notifications_StreamSub.png)
  
有关创建流式通知的信息，请参阅[使用 Exchange 中的 EWS 流式处理有关邮箱事件的通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-pull-notifications"></a>EWS 拉取通知
<a name="bk_pullnotif"> </a>

"拉" 通知依赖客户端要求在客户端管理的时间间隔内发出通知。 这可能会导致无通知的 GetEvents 响应。 图3显示了请求订阅和请求通知的工作原理。
  
**图3。拉取通知概述**

![此插图显示拉取通知的工作原理。设置拉取通知的步骤：1. 订阅；2. 发送 GetEvents；3. 接收答复，重复 2 和 3；4. 关闭或保留连接；5. 取消订阅或超时。](media/Exchange2013_Notifications_PullSub.png)
  
有关创建请求通知的信息，请参阅[使用 Exchange 中的 EWS 在邮箱事件中提取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。
  
### <a name="ews-push-notifications"></a>EWS 推送通知
<a name="bk_pushnotif"> </a>

推送通知依赖于将通知推送回客户端的服务器。 如果有通知，则只有流量。 图4显示了推送订阅和推送通知的工作原理。
  
**图4。推送通知概述**

![此插图显示推送通知的工作原理。设置推送通知的步骤：1. 创建侦听器；2. 订阅；3. 等待事件；4. 接收事件；5. 发送“确定”答复，重复 3、4、和 5；6. 取消订阅或超时。](media/Exchange2013_Notifications_PushSub.png)

如果要将[推送通知与 Exchange 2010 一起](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)使用，请考虑将应用程序升级为[使用流式通知](https://code.msdn.microsoft.com/exchange/Exchange-2013-Set-push-82738cc5)，以便不需要单独的应用程序即可接收事件。

  
## <a name="how-do-i-subscribe-to-notifications"></a>如何订阅通知？
<a name="bk_notifoperations"> </a>

根据要创建的订阅类型，有许多选项可供选择，以便订阅通知。
  
**表2。订阅通知的操作和方法**

|**订阅类型**|**EWS 操作**|**EWS 托管 API 方法**|**功能**|
|:-----|:-----|:-----|:-----|
|媒体  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetostreamingnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) <br/> |创建订阅流式通知的请求。  <br/> |
|超类  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) <br/> [ExchangeService 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建订阅请求通知的请求。  <br/> |
|子类  <br/> |[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) <br/> |[BeginSubscribeToPushNotifications 重载方法 ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [BeginSubscribeToPushNotificationsOnAllFolders 重载方法 ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsubscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> [SubscribeToPushNotifications 重载方法 ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx) <br/> [SubscribeToPushNotificationsOnAllFolders 重载方法 ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotificationsonallfolders%28v=exchg.80%29.aspx) <br/> |创建订阅推送通知的请求。  <br/> |
   
## <a name="how-do-i-get-ews-events"></a>如何获取 EWS 事件？
<a name="bk_getevents"> </a>

创建订阅后，将实际事件发送到客户端的方式取决于订阅类型。 
  
对于流式通知，必须创建流式订阅连接，然后将订阅添加到该连接中。 您可以[通过使用 Exchange 中的 EWS 在有关邮箱事件的流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)中阅读有关此过程的详细信息。 
  
对于拉取通知，在创建订阅时初始化订阅对象，因此您只需调用**GetEvent**方法或操作来从服务器检索事件。 您可以[使用 Exchange 中的 EWS 在关于邮箱事件的 Pull 通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)中阅读有关此信息的详细信息。 
  
下表列出了检索事件所需的操作和类。 
  
**表3。用于创建连接和获取事件的元素和类**

|**订阅类型**|**EWS 操作**|**EWS 托管的 API 方法**|**功能**|
|:-----|:-----|:-----|:-----|
|媒体  <br/> |[GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) <br/> |[StreamingSubscriptionConnection 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.addsubscription%28v=exchg.80%29.aspx) <br/> |在服务器上创建一个挂起的 get 请求，该请求在事件发生时对其做出响应。  <br/> |
|超类  <br/> |[GetEvents 操作](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) <br/> |[PullSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) <br/> |从服务器获取请求通知事件。  <br/> |
|子类  <br/> |不适用。  <br/> |不适用。  <br/> |推送通知会自动发送到 web 服务侦听器（订阅请求中指定的回调 URL）。 不需要调用其他方法或操作。  <br/> |
   
## <a name="how-do-i-unsubscribe-to-notifications"></a>如何取消订阅通知？
<a name="bk_notifunsubscribe"> </a>

下表列出了可取消订阅每种类型的订阅的方法。
  
**表4。取消订阅通知的操作和方法**

|**订阅类型**|**EWS**|**EWS Managed API**||
|:-----|:-----|:-----|:-----|
|媒体  <br/> |[取消订阅操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[StreamingSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [StreamingSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|超类  <br/> |[取消订阅操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) <br/> |[PullSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.beginunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.endunsubscribe%28v=exchg.80%29.aspx) <br/> [PullSubscription 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.unsubscribe%28v=exchg.80%29.aspx) <br/> ||
|子类  <br/> |在[SendNotificationResponseMessage](https://msdn.microsoft.com/library/2c6d681b-67ac-4331-bc6b-a2e709b638e3%28Office.15%29.aspx)的[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)元素中返回**取消订阅** <br/> |不适用。 改为让订阅超时。  <br/> ||
   
或者，可以让每个订阅超时。 
  
**表5。订阅超时**

|**订阅类型**|**以 EWS 为单位的超时值**|**EWS 托管 API 中的超时值**|**超时处理**|
|:-----|:-----|:-----|:-----|
|媒体  <br/> |[ConnectionTimeout](https://msdn.microsoft.com/library/14da68a0-bcca-4281-a774-47644baa4ee9%28Office.15%29.aspx)元素  <br/> | [StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)构造函数的*生存期*参数  <br/> |对于 EWS 托管 API，在超时值过期后，将引发[OnDisconnect](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.ondisconnect%28v=exchg.80%29.aspx)事件。 如果未调用[StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.open%28v=exchg.80%29.aspx)方法，则关闭该连接。  <br/> 对于 EWS，在超时值过期后， [GetUserConfigurationResponse](https://msdn.microsoft.com/library/5e418c91-c836-4de0-a80d-f0dad0c684d7%28Office.15%29.aspx)消息将返回[ConnectionStatus](https://msdn.microsoft.com/library/4300f9d6-8bf9-48c2-9f07-d80197864e17%28Office.15%29.aspx)的关闭值。  <br/> |
|超类  <br/> |[Timeout](https://msdn.microsoft.com/library/c2e1ca5a-6667-4f6f-aac4-89de33bddc54%28Office.15%29.aspx)元素  <br/> | [SubscribeToPullNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法的*timeout*参数  <br/> |超时值过期后，服务器将删除订阅。  <br/> |
|子类  <br/> |[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)元素  <br/> | [SubscribeToPushNotification](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopushnotifications%28v=exchg.80%29.aspx)方法的*frequency*参数  <br/> |如果服务器未收到对推送通知或状态 ping 的响应，则它会在停止发送通知之前多次重试发送通知。 有关详细信息，请参阅[StatusFrequency](https://msdn.microsoft.com/library/917474e2-a426-4166-b825-53783a41dad4%28Office.15%29.aspx)。  <br/> |
   
## <a name="can-i-limit-subscriptions"></a>我可以限制订阅吗？
<a name="bk_limitsubs"> </a>

在本地部署中，可以使用限制策略的[EwsMaxSubscriptions 限制参数](ews-throttling-in-exchange.md)限制每个用户的订阅数。 该策略可应用于所有用户或仅适用于特定用户。 Exchange Online 的**EwsMaxSubscriptions**限制策略不可配置。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_limitsubs"> </a>

- [在 Exchange 中使用 EWS 流式处理有关邮箱事件的通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取有关邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
- [Exchange web 服务引用](../web-service-reference/web-services-reference-for-exchange.md)
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
- [推送通知示例应用程序](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
    

