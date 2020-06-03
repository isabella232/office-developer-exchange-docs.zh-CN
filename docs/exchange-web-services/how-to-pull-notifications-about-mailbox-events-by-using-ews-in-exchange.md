---
title: 使用 Exchange 中的 EWS 获取有关邮箱事件的通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: 了解如何使用 EWS 托管 API 或 EWS 订阅拉取通知和获取事件。
ms.openlocfilehash: 3d77c0d4efb8fc853eea64ff2429af5c3dbead27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456726"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 获取有关邮箱事件的通知

了解如何使用 EWS 托管 API 或 EWS 订阅拉取通知和获取事件。
  
Exchange 中的 EWS 使用拉取通知，使客户端能够请求（或拉取）对邮箱的更改通知到客户端。
  
如果你正在订阅使用 EWS 托管 API 请求获取通知，请使用[SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法[订阅并获取拉取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma)。 然后，通过使用[GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx)方法从服务器获取事件。 
  
若要使用 EWS 订阅拉取通知，请使用[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)[创建订阅](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews)，分析响应，然后使用[GetEvents 操作](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)[获取通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull)。
  
在客户端收到在服务器上发生更改或创建的项目的通知后，它便可以[同步更改](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 订阅和获取拉取通知
<a name="bk_cepullewsma"> </a>

下面的代码示例演示如何使用[SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法为 "收件箱" 文件夹中的所有事件订阅 pull 通知。 然后，该示例使用[GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx)方法从服务器检索事件。 在此示例中，我们假定**服务**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)绑定。 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

从服务器接收到事件后，可以[将这些更改与服务器同步](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。 使用在 "[如何取消订阅通知？](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) " 中指定的取消订阅方法之一，以便在不再需要订阅时结束与服务器的订阅。 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>使用 EWS 订阅拉取通知
<a name="bk_cepullews"> </a>

下面的示例演示使用[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)发送到服务器以订阅 "收件箱" 文件夹中所有[EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx)的 XML 请求。 这也是在通过使用[SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法订阅拉取通知时，EWS 托管 API 发送的 XML 请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="https://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

下面的 XML 示例显示从服务器发送到客户端以响应**订阅**操作请求的[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息。 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的 NoError 值的包含意味着已成功创建订阅。 [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)元素唯一标识服务器上的拉取通知订阅。 [水印](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx)元素表示邮箱事件队列中的书签。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

创建订阅后，您现在可以使用**SubscribeResponse**邮件中返回的**SubscriptionId**获取事件。 
  
## <a name="get-pull-notifications-by-using-ews"></a>使用 EWS 获取拉取通知
<a name="bk_getpull"> </a>

下面的 XML 示例显示从客户端发送到服务器的[GetEvents 操作](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)请求消息，以获取[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)邮件中返回的[SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)的通知。 对于第一个**GetEvents**请求，使用**订阅**响应中返回的[水印](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx)。 对于后续的**GetEvents**请求，请使用上一**GetEvents**请求中返回的最后一个**水印**。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

下面的 XML 示例展示了从服务器发送到客户端的**GetEvents**响应消息。 每个**GetEvents**响应都包含有关一个或多个事件的信息。 为每个事件返回一个**水印**。 必须保存最后一个**水印**并将其用于下一个**GetEvents**请求。 如果自上次**GetEvents**请求以来未发生任何存储事件，则返回一个 status 事件。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="https://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

从服务器接收到事件后，[将更改同步到客户端](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。 当不再需要订阅时，使用[取消订阅操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx)可在服务器上结束订阅。 
  
## <a name="next-steps"></a>后续步骤
<a name="bk_nextsteps"> </a>

收到通知后，可以[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)或[同步已更改的文件夹的内容](how-to-synchronize-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [在 Exchange 中使用 EWS 流式处理有关邮箱事件的通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

