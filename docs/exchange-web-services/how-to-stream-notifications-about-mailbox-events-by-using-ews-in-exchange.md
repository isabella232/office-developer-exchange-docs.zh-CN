---
title: 有关在 Exchange 中使用 EWS 邮箱事件流通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe9bde1e-da0e-413c-a109-077f399f67a3
description: 了解如何使用 EWS 托管 API 或 EWS 订阅流式处理通知并获取事件。
ms.openlocfilehash: aad7604511687d1482914183979e954f79572af9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752880"
---
# <a name="stream-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="98aa7-103">有关在 Exchange 中使用 EWS 邮箱事件流通知</span><span class="sxs-lookup"><span data-stu-id="98aa7-103">Stream notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="98aa7-104">了解如何使用 EWS 托管 API 或 EWS 订阅流式处理通知并获取事件。</span><span class="sxs-lookup"><span data-stu-id="98aa7-104">Find out how to use the EWS Managed API or EWS to subscribe to streaming notifications and get events.</span></span>
  
<span data-ttu-id="98aa7-105">EWS 在 Exchange 使用流式处理通知，以接收由服务器通过保持连接发送的通知打开指定的时间段。</span><span class="sxs-lookup"><span data-stu-id="98aa7-105">EWS in Exchange uses streaming notifications to receive notifications that are sent by the server through a connection that remains open for a specified period of time.</span></span>
  
<span data-ttu-id="98aa7-106">如果您正在订阅通知流使用 EWS 托管 API，您[订阅和获取流式处理通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamewsma)使用[SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="98aa7-106">If you're subscribing to streaming notifications by using the EWS Managed API, you [subscribe and get streaming notifications](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamewsma) by using the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.subscribetostreamingnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="98aa7-107">您随后可以通过使用[StreamingSubscriptionConnection](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象创建与订阅的连接。</span><span class="sxs-lookup"><span data-stu-id="98aa7-107">You then create a connection to the subscription by using the [StreamingSubscriptionConnection](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="98aa7-108">若要使用 EWS 订阅流式通知，通过使用[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)，您[创建订阅](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamews)响应，然后[获取流式通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews)使用分析[GetStreamingEvents 操作](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="98aa7-108">To subscribe to streaming notifications by using EWS, you [create a subscription](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cestreamews) by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the streaming notifications](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) by using the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request.</span></span> 
  
<span data-ttu-id="98aa7-109">客户端接收通知的更改，或在服务器上创建项目后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是将更改同步。</span><span class="sxs-lookup"><span data-stu-id="98aa7-109">After the client receives notifications of items changed or created on the server, the [next step](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) is to synchronize the changes.</span></span> 
  
## <a name="subscribe-to-and-get-streaming-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="98aa7-110">订阅并获取使用 EWS 托管 API 流通知</span><span class="sxs-lookup"><span data-stu-id="98aa7-110">Subscribe to and get streaming notifications by using the EWS Managed API</span></span>
<span data-ttu-id="98aa7-111"><a name="bk_cestreamewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="98aa7-111"></span></span>

<span data-ttu-id="98aa7-112">下面的代码示例演示如何使用[SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx)方法订阅流式处理的收件箱文件夹中的所有事件通知。</span><span class="sxs-lookup"><span data-stu-id="98aa7-112">The following code example shows how to use the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) method to subscribe to streaming notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="98aa7-113">通过创建[StreamingSubscriptionConnection](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx)对象然后创建订阅的连接。</span><span class="sxs-lookup"><span data-stu-id="98aa7-113">It then creates a connection for the subscription by creating a [StreamingSubscriptionConnection](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection.streamingsubscriptionconnection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="98aa7-114">本示例中，我们假定该**服务**是一个有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)绑定。</span><span class="sxs-lookup"><span data-stu-id="98aa7-114">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
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

<span data-ttu-id="98aa7-115">已从服务器接收事件后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是与服务器同步这些更改。</span><span class="sxs-lookup"><span data-stu-id="98aa7-115">After you have received events from the server, the [next step](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) is to synchronize those changes with the server.</span></span> <span data-ttu-id="98aa7-116">使用[表 4](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe)中列出的 unsubscribe 方法之一结束与服务器的订阅，当不再需要订阅。</span><span class="sxs-lookup"><span data-stu-id="98aa7-116">Use one of the unsubscribe methods listed in [Table 4](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-streaming-notifications-by-using-ews"></a><span data-ttu-id="98aa7-117">使用 EWS 流通知订阅</span><span class="sxs-lookup"><span data-stu-id="98aa7-117">Subscribe to streaming notifications by using EWS</span></span>
<span data-ttu-id="98aa7-118"><a name="bk_cestreamews"> </a></span><span class="sxs-lookup"><span data-stu-id="98aa7-118"></span></span>

<span data-ttu-id="98aa7-119">下面的示例演示 XML 请求发送的客户端到服务器时客户端调用[Subscribe 操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)以订阅收件箱文件夹中的所有[EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="98aa7-119">The following example shows an XML request that is sent by the client to the server when the client calls the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) to subscribe to all [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder.</span></span> <span data-ttu-id="98aa7-120">这也是使用[SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx)方法订阅流式通知时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="98aa7-120">This is also the XML request that the EWS Managed API sends when you use the [SubscribeToStreamingNotifications](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.endsubscribetostreamingnotifications%28v=exchg.80%29.aspx) method to subscribe to streaming notifications.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="98aa7-121">下面的 XML 示例演示从服务器发送到客户端对[订阅操作](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)请求响应中的[SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="98aa7-121">The following XML example shows the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="98aa7-122">包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的 NoError 值意味着已成功创建订阅。</span><span class="sxs-lookup"><span data-stu-id="98aa7-122">The inclusion of the NoError value for the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="98aa7-123">[SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)元素唯一地标识的服务器上的流式通知订阅。</span><span class="sxs-lookup"><span data-stu-id="98aa7-123">The [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the streaming notification subscription on the server.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="98aa7-124">创建订阅后, 您可以立即[获取流式的事件](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews)使用[SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)邮件中返回。</span><span class="sxs-lookup"><span data-stu-id="98aa7-124">After creating the subscription, you can now [get the streamed events](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cegetnotifsews) by using the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> 
  
## <a name="get-streaming-events-by-using-ews"></a><span data-ttu-id="98aa7-125">使用 EWS 获取流事件</span><span class="sxs-lookup"><span data-stu-id="98aa7-125">Get streaming events by using EWS</span></span>
<span data-ttu-id="98aa7-126"><a name="bk_cegetnotifsews"> </a></span><span class="sxs-lookup"><span data-stu-id="98aa7-126"></span></span>

<span data-ttu-id="98aa7-127">下面的 XML 示例演示客户端发送到服务器以获得的[SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx)通知[GetStreamingEvents 操作](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求消息[SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx)邮件中返回。</span><span class="sxs-lookup"><span data-stu-id="98aa7-127">The following XML example shows the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request message that the client sends to the server to get notifications for the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="98aa7-128">[GetStreamingEvents 操作](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求指示连接的长度是长 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="98aa7-128">The [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request indicates that the length of the connection is 30 minutes long.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="98aa7-129">下面的 XML 示例演示从服务器发送到客户端以响应[GetStreamingEvents 操作](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx)请求[GetStreamingEventsResponse](http://msdn.microsoft.com/library/ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="98aa7-129">The following XML example shows the [GetStreamingEventsResponse](http://msdn.microsoft.com/library/ea1e7e7e-1b19-4e07-ba42-5dbd888c6db2%28Office.15%29.aspx) message that is sent from the server to the client in response to the [GetStreamingEvents operation](http://msdn.microsoft.com/library/8da95423-72bc-4034-90a8-162eedcd059b%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="98aa7-130">它包含 CreatedEvent 和项 NewMailEvent ModifiedEvent 文件夹，所有这些时发生收到新邮件。</span><span class="sxs-lookup"><span data-stu-id="98aa7-130">It contains a CreatedEvent and a NewMailEvent for the item, and a ModifiedEvent for the folder, all of which occur when a new message is received.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

已从服务器接收事件后，[下一步](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)是与服务器同步这些更改。 <span data-ttu-id="98aa7-132">使用[取消操作](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx)结束与服务器的订阅，当不再需要订阅。</span><span class="sxs-lookup"><span data-stu-id="98aa7-132">Use the [Unsubscribe operation](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="98aa7-133">后续步骤</span><span class="sxs-lookup"><span data-stu-id="98aa7-133">Next steps</span></span>
<span data-ttu-id="98aa7-134"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="98aa7-134"></span></span>

<span data-ttu-id="98aa7-135">已收到通知后，您可以[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)或[同步的文件夹的更改的内容](how-to-synchronize-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="98aa7-135">After you've received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98aa7-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98aa7-136">See also</span></span>


- [<span data-ttu-id="98aa7-137">Notification subscriptions, mailbox events, and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="98aa7-137">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="98aa7-138">在 Exchange 使用 EWS 提取有关邮箱事件的通知</span><span class="sxs-lookup"><span data-stu-id="98aa7-138">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="98aa7-139">在 Exchange 维护一组订阅和邮箱服务器之间的关联</span><span class="sxs-lookup"><span data-stu-id="98aa7-139">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="98aa7-140">在 Exchange 处理与通知相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="98aa7-140">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="98aa7-141">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="98aa7-141">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

