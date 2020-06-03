---
title: 在 Exchange 中使用 EWS 流式处理有关邮箱事件的通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: fe9bde1e-da0e-413c-a109-077f399f67a3
description: 了解如何使用 EWS 托管 API 或 EWS 订阅流式通知和获取事件。
localization_priority: Priority
ms.openlocfilehash: 97784be8ab13509f950355f532f97167e9b6f43e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527717"
---
# <a name="stream-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 流式处理有关邮箱事件的通知

了解如何使用 EWS 托管 API 或 EWS 订阅流式通知和获取事件。
  
Exchange 中的 EWS 使用流式通知通过在指定时间段内仍处于打开状态的连接来接收由服务器发送的通知。
  
如果要使用 EWS 托管 API 订阅流式通知，请使用[SubscribeToStreamingNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx)方法[订阅和获取流式处理](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamewsma)通知。 然后，使用[StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象创建到订阅的连接。 
  
若要使用 EWS 订阅流式通知，请使用[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)[创建订阅](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamews)，分析响应，然后使用[GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求[获取流式处理通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews)。 
  
客户端在服务器上收到已更改或已创建的项目的通知后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是同步这些更改。 
  
## <a name="subscribe-to-and-get-streaming-notifications-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 订阅和获取流式处理通知
<a name="bk_cestreamewsma"> </a>

下面的代码示例演示如何使用[SubscribeToStreamingNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx)方法来订阅 "收件箱" 文件夹中所有事件的流通知。 然后，它通过创建[StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象为订阅创建连接。 在此示例中，我们假定**服务**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)绑定。 
  
```cs
// Subscribe to streaming notifications in the Inbox. 
StreamingSubscription = service.SubscribeToStreamingNotifications(
    new FolderId[] { WellKnownFolderName.Inbox },
    EventType.NewMail,
    EventType.Created,
    EventType.Deleted,
    EventType.Modified,
    EventType.Moved,
    EventType.Copied,
    EventType.FreeBusyChanged);
// Create a streaming connection to the service object, over which events are returned to the client.
// Keep the streaming connection open for 30 minutes.
StreamingSubscriptionConnection connection = new StreamingSubscriptionConnection(service, 30);
connection.AddSubscription(StreamingSubscription);
connection.OnNotificationEvent += OnNotificationEvent;
connection.OnDisconnect += OnDisconnect;
connection.Open();
```

从服务器接收到事件后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是将这些更改与服务器同步。 当不再需要订阅时，使用[表 4](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe)中列出的其中一个取消订阅方法可结束与服务器的订阅。 
  
## <a name="subscribe-to-streaming-notifications-by-using-ews"></a>使用 EWS 订阅流式通知
<a name="bk_cestreamews"> </a>

下面的示例演示当客户端调用[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)以订阅 "收件箱" 文件夹中的所有[EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx)时，客户端向服务器发送的 XML 请求。 这也是在使用[SubscribeToStreamingNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx)方法订阅流式通知时，EWS 托管 API 发送的 XML 请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>CreatedEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
          <t:EventType>ModifiedEvent</t:EventType>
          <t:EventType>MovedEvent</t:EventType>
          <t:EventType>CopiedEvent</t:EventType>
          <t:EventType>FreeBusyChangedEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

下面的 XML 示例显示从服务器发送到客户端以响应[订阅操作](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)请求的[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息。 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的 NoError 值的包含意味着已成功创建订阅。 [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)元素唯一标识服务器上的流式通知订阅。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
          <m:SubscribeResponseMessage ResponseClass="Success">
            <m:ResponseCode>NoError</m:ResponseCode>
            <m:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</m:SubscriptionId>
          </m:SubscribeResponseMessage>
        </m:ResponseMessages>
      </m:SubscribeResponse>
    </s:Body>
  </s:Envelope>
```

创建订阅后，您现在可以使用[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)邮件中返回的[SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) [获取流式处理事件](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews)。 
  
## <a name="get-streaming-events-by-using-ews"></a>使用 EWS 获取流式处理事件
<a name="bk_cegetnotifsews"> </a>

下面的 XML 示例显示客户端向服务器发送的[GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求消息，以获取[SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)邮件中返回的[订阅](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)的通知。 [GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求指示连接的长度为30分钟长。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>30</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

下面的 XML 示例展示了从服务器发送到客户端以响应[GetStreamingEvents 操作](https://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求的[GetStreamingEventsResponse](https://msdn.microsoft.com/library/ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2%28Office.15%29.aspx)消息。 它包含项目的 CreatedEvent 和 NewMailEvent，以及该文件夹的 ModifiedEvent，这是在收到新邮件时发生的。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <soap:Body xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>JgBibjFwcjAzbWIyMDIubmFtcHJkMDMucHJvZC5vdXRsb29rLmNvbRAAAADwXxVesOnHS5BxUHKwAW88SHjwd1iB0Ag=</t:SubscriptionId>
            <t:CreatedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:CreatedEvent>
            <t:NewMailEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:ModifiedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:FolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgEJAAAA" ChangeKey="AQAAAA==" />
              <t:UnreadCount>1</t:UnreadCount>
            </t:ModifiedEvent>
          </m:Notification>
        </m:Notifications>
      </m:GetStreamingEventsResponseMessage>
    </m:ResponseMessages>
  </m:GetStreamingEventsResponse>
</soap:Body>
```

从服务器接收到事件后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是将这些更改与服务器同步。 当不再需要订阅时，使用[取消订阅操作](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx)可在服务器上结束订阅。 
  
## <a name="next-steps"></a>后续步骤
<a name="bk_nextsteps"> </a>

收到通知后，可以[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)或[同步已更改的文件夹的内容](how-to-synchronize-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取有关邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [维护 Exchange 中的一组订阅和邮箱服务器之间的相关性](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

