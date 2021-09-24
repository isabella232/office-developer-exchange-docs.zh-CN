---
title: 在 Exchange 上使用 EWS 时关于邮箱事件的拉取通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: 了解如何使用 EWS 托管 API 或 EWS 订阅拉取通知和获取事件。
ms.openlocfilehash: eb694eddd16567e42ccc43b2854f0432c54dc6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513099"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>在 Exchange 上使用 EWS 时关于邮箱事件的拉取通知

了解如何使用 EWS 托管 API 或 EWS 订阅拉取通知和获取事件。
  
EWS in Exchange uses pull notifications to enable clients to request (or pull) notifications about changes to the mailbox from the server to the client.
  
如果要使用 EWS 托管 API 订阅拉取通知，可以使用[SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx)方法订阅并获取拉取通知。 [](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) 然后，使用 [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) 方法从服务器获取事件。 
  
若要使用 EWS 订阅拉取通知，[](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews)可以使用[Subscribe](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)操作创建订阅，分析响应，然后使用[GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)操作获取通知。 [](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull)
  
客户端收到服务器上更改或创建的项目通知后，可以 [同步更改](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 订阅和获取拉取通知
<a name="bk_cepullewsma"> </a>

以下代码示例演示如何使用 [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) 方法订阅"收件箱"文件夹中所有事件的拉取通知。 然后，该示例使用 [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) 方法从服务器检索事件。 在此例中，我们假定 **服务** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 绑定。 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

从服务器接收事件后，可以将 [这些更改与服务器同步](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。 使用如何取消订阅通知 [？](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) 中指定的取消订阅方法之一，在不再需要订阅时终止服务器订阅。 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>使用 EWS 订阅拉取通知
<a name="bk_cepullews"> </a>

以下示例显示通过使用 Subscribe 操作发送到服务器以订阅收件箱文件夹中的所有 [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) 的 XML [请求](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)。 这也是 EWS 托管 API 在订阅使用 [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) 方法拉取通知时发送的 XML 请求。 
  
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

以下 XML 示例显示了为响应 Subscribe 操作请求而从服务器发送到客户端的[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息。  包含 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 元素的 NoError 值意味着订阅已成功创建。 [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)元素唯一标识服务器上拉取通知订阅。 [Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx)元素表示邮箱事件队列中的书签。 
  
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

创建订阅后，你现在可以使用 **SubscribeResponse** 消息中返回的 **SubscriptionId** 获取事件。 
  
## <a name="get-pull-notifications-by-using-ews"></a>使用 EWS 获取拉取通知
<a name="bk_getpull"> </a>

以下 XML 示例显示[GetEvents](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)操作请求消息，该消息从客户端发送到服务器，用于获取[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息中返回的[SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)的通知。 对于第一 **个 GetEvents** 请求，请使用 Subscribe 响应中返回 **的 Watermark。** [](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) 对于后续 **GetEvents** 请求，请使用上一个 **GetEvents** 请求中返回的最后一个 **Watermark。** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

以下 XML 示例显示从服务器发送到客户端的 **GetEvents** 响应消息。 每个 **GetEvents** 响应包含有关一个或多个事件的信息。 将 **返回** 每个事件水印。 必须在下一个 **GetEvents** 请求中保存并使用最后一个 **Watermark。** 如果自上次 **GetEvents** 请求以来未发生存储事件，则返回状态事件。 
  
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

从服务器接收事件后， [将更改同步到客户端](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)。 使用 ["取消订阅](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) "操作在不再需要订阅时终止服务器订阅。 
  
## <a name="next-steps"></a>后续步骤
<a name="bk_nextsteps"> </a>

收到通知后，可以同步文件夹层次结构或[](how-to-synchronize-folders-by-using-ews-in-exchange.md)[同步已更改的文件夹的内容](how-to-synchronize-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [在 Exchange 上使用 EWS 时关于邮箱事件的流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [在 Exchange 中保持一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 中使用 EWS 时处理通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [邮箱同步和 Exchange 中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

