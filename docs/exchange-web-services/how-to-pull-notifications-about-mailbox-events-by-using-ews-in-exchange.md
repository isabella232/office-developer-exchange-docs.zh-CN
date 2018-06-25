---
title: 在 Exchange 使用 EWS 提取有关邮箱事件的通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: 了解如何使用 EWS 托管 API 或 EWS 订阅拉通知并获取事件。
ms.openlocfilehash: 6a04aaf0102c149691a30c2bd2f499e03265bce8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752869"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 提取有关邮箱事件的通知

了解如何使用 EWS 托管 API 或 EWS 订阅拉通知并获取事件。
  
Exchange 中的 EWS 使用拉通知启用客户端请求 （或请求） 有关从服务器到客户端对邮箱的更改的通知。
  
如果您正在使用 EWS 托管 API，您[订阅并获取拉通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma)使用[SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法订阅出现通知。 您然后事件从服务器获取使用[GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx)方法。 
  
要通过使用 EWS 订阅出现通知，请使用[Subscribe 操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)，您[创建订阅](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews)响应，然后[获取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull)使用分析[GetEvents 操作](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)。
  
客户端接收通知的已更改或在服务器上创建项目后，它可以然后[同步所做的更改](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>订阅并使用 EWS 托管 API 获取拉通知
<a name="bk_cepullewsma"> </a>

下面的代码示例演示如何使用[SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法订阅收件箱文件夹中的所有事件的出现通知。 该示例然后使用[GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx)方法从服务器中检索事件。 本示例中，我们假定该**服务**是一个有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)绑定。 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

从服务器接收事件后，您可以[将这些更改与服务器同步](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。 使用一种 unsubscribe 方法中指定[如何我执行取消订阅通知？](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe)结束与服务器的订阅，当不再需要订阅。 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>使用 EWS 订阅拉通知
<a name="bk_cepullews"> </a>

下面的示例演示 XML 请求发送到服务器可以订阅通过使用[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)的收件箱文件夹中的所有[EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) 。 这也是 XML 请求 EWS 托管 API 发送时使用[SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法订阅出现通知。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="http://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

下面的 XML 示例演示从服务器发送到客户端对**订阅**操作请求的响应的[SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息。 包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的 NoError 值意味着已成功创建订阅。 [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)元素唯一地标识的服务器上的请求通知订阅。 [水印](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx)元素均表示邮箱事件队列中的书签。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

创建订阅后, 现在可以通过使用**SubscribeResponse**邮件中返回**SubscriptionId**获取事件。 
  
## <a name="get-pull-notifications-by-using-ews"></a>通过使用 EWS 获取拉通知
<a name="bk_getpull"> </a>

下面的 XML 示例演示[GetEvents 操作](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)请求发送的邮件是从客户端到服务器以获得的[SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)返回[SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息的通知。 第一个**GetEvents**请求，使用[水印](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) **Subscribe**响应中返回。 对于后续**GetEvents**请求，使用所返回以前**GetEvents**请求中的最后一个**水印**。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

下面的 XML 示例演示从服务器发送到客户端**GetEvents**响应消息。 每个**GetEvents**响应，包括有关一个或多个事件的信息。 **水印**将返回每个事件。 最后一个**水印**必须保存，并在下一个**GetEvents**请求中使用。 如果自上次**GetEvents**请求以来不发生任何存储事件，则返回的状态事件。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="http://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Watermark>AAAAAHMhAAAAAAAAAQ==</Watermark>
          <TimeStamp>2013-09-15T21:37:01Z</TimeStamp>
          <ItemId Id="AAAtA=" ChangeKey="CQAAAA==" />
          <ParentFolderId Id="AQAtAEFkbWA==" ChangeKey="AQAAAA==" />
        </NewMailEvent>
      </Notification>
    </GetEventsResponseMessage>
  </ResponseMessages>
</GetEventsResponse>
```

后从服务器中，[将更改同步到客户端](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)接收事件。 使用[取消操作](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx)结束与服务器的订阅，当不再需要订阅。 
  
## <a name="next-steps"></a>后续步骤
<a name="bk_nextsteps"> </a>

正在接收后通知，您可以[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)或[同步的文件夹的更改的内容](how-to-synchronize-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [有关在 Exchange 中使用 EWS 邮箱事件流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 维护一组订阅和邮箱服务器之间的关联](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 处理与通知相关 EWS 中的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

