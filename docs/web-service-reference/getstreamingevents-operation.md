---
title: GetStreamingEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: 8da95423-72bc-4034-90a8-162eedcd059b
description: 查找有关 GetStreamingEvents EWS 操作的信息。
ms.openlocfilehash: 27744ec40d7c7cb551f35ed5f6fcb726f23d4865
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530167"
---
# <a name="getstreamingevents-operation"></a><span data-ttu-id="a9787-103">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="a9787-103">GetStreamingEvents operation</span></span>

<span data-ttu-id="a9787-104">查找有关**GetStreamingEvents** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="a9787-104">Find information about the **GetStreamingEvents** EWS operation.</span></span> 
  
<span data-ttu-id="a9787-105">流式订阅客户端使用**GetStreamingEvents**操作从客户端访问服务器中请求通知。</span><span class="sxs-lookup"><span data-stu-id="a9787-105">The **GetStreamingEvents** operation is used by streaming subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="a9787-106">**GetStreamingEvents**响应返回自上次通知以来在邮箱中发生的项和事件的数组。</span><span class="sxs-lookup"><span data-stu-id="a9787-106">The **GetStreamingEvents** response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
## <a name="getstreamingevents-request-example"></a><span data-ttu-id="a9787-107">GetStreamingEvents 请求示例</span><span class="sxs-lookup"><span data-stu-id="a9787-107">GetStreamingEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="a9787-108">Description</span><span class="sxs-lookup"><span data-stu-id="a9787-108">Description</span></span>

<span data-ttu-id="a9787-109">下面的**GetStreamingEvents**操作示例演示如何请求与订阅标识符标识的订阅相关联的事件和项目。</span><span class="sxs-lookup"><span data-stu-id="a9787-109">The following example of a **GetStreamingEvents** operation shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9787-110">代码</span><span class="sxs-lookup"><span data-stu-id="a9787-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
  xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Body>
    <GetStreamingEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <ConnectionTimeout>30</ConnectionTimeout>
    </GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getstreamingevents-request-elements"></a><span data-ttu-id="a9787-111">GetStreamingEvents 请求元素</span><span class="sxs-lookup"><span data-stu-id="a9787-111">GetStreamingEvents request elements</span></span>

<span data-ttu-id="a9787-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a9787-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a9787-113">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="a9787-113">GetStreamingEvents</span></span>](getstreamingevents.md)
    
- [<span data-ttu-id="a9787-114">SubscriptionId （GetStreamingEvents）</span><span class="sxs-lookup"><span data-stu-id="a9787-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
- [<span data-ttu-id="a9787-115">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="a9787-115">ConnectionTimeout</span></span>](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a><span data-ttu-id="a9787-116">成功的 GetStreamingEvents 响应示例</span><span class="sxs-lookup"><span data-stu-id="a9787-116">Successful GetStreamingEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="a9787-117">Description</span><span class="sxs-lookup"><span data-stu-id="a9787-117">Description</span></span>

<span data-ttu-id="a9787-118">下面的**GetStreamingEvents**响应示例显示收到新电子邮件时发送给客户端的通知。</span><span class="sxs-lookup"><span data-stu-id="a9787-118">The following example of a **GetStreamingEvents** response shows the notifications that are sent to the client when a new email message is received.</span></span> <span data-ttu-id="a9787-119">它包括针对以下事件的通知： CreatedEvent、NewMail 和 ModifiedEvent。</span><span class="sxs-lookup"><span data-stu-id="a9787-119">It includes notifications for the following events: CreatedEvent, NewMail, and ModifiedEvent.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9787-120">代码</span><span class="sxs-lookup"><span data-stu-id="a9787-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <ServerVersionInfo xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
</soap:Header>
<soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
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

### <a name="getstreamingevents-response-elements"></a><span data-ttu-id="a9787-121">GetStreamingEvents 响应元素</span><span class="sxs-lookup"><span data-stu-id="a9787-121">GetStreamingEvents response elements</span></span>

<span data-ttu-id="a9787-122">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a9787-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a9787-123">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="a9787-123">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
    
- [<span data-ttu-id="a9787-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a9787-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="a9787-125">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a9787-125">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md)
    
- [<span data-ttu-id="a9787-126">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="a9787-126">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md)
    
- [<span data-ttu-id="a9787-127">通知</span><span class="sxs-lookup"><span data-stu-id="a9787-127">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="a9787-128">SubscriptionId （GetStreamingEvents）</span><span class="sxs-lookup"><span data-stu-id="a9787-128">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
<span data-ttu-id="a9787-129">若要查找**GetStreamingEvents**操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="a9787-129">To find other options for the response message of the **GetStreamingEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="a9787-130">从[通知](notification-ex15websvcsotherref.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="a9787-130">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getstreamingevents-error-response-example"></a><span data-ttu-id="a9787-131">GetStreamingEvents 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="a9787-131">GetStreamingEvents error response example</span></span>

### <a name="description"></a><span data-ttu-id="a9787-132">Description</span><span class="sxs-lookup"><span data-stu-id="a9787-132">Description</span></span>

<span data-ttu-id="a9787-133">下面的示例演示对**GetStreamingEvents**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="a9787-133">The following example shows an error response to a **GetStreamingEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a9787-134">代码</span><span class="sxs-lookup"><span data-stu-id="a9787-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetStreamingEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetStreamingEventsResponseMessage ResponseClass="Error">
        <m:MessageText></m:MessageText>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        <m:ResponseCode>ErrorInvalidSubscription</m:ResponseCode>
        <m:ConnectionStatus>Closed</m:ConnectionStatus>
      </m:ResponseMessages>
    </GetStreamingEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a><span data-ttu-id="a9787-135">备注</span><span class="sxs-lookup"><span data-stu-id="a9787-135">Remarks</span></span>

<span data-ttu-id="a9787-136">在处理**GetStreamingEvents**请求时，客户端访问服务器将执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a9787-136">When processing a **GetStreamingEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="a9787-137">将请求的[SubscriptionId （GetStreamingEvents）](subscriptionid-getstreamingevents.md)确认为在客户端访问服务器上承载的有效订阅。</span><span class="sxs-lookup"><span data-stu-id="a9787-137">The [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="a9787-138">如果不是，则**GetStreamingEvents**调用将失败。</span><span class="sxs-lookup"><span data-stu-id="a9787-138">If it is not, the **GetStreamingEvents** call fails.</span></span> 
    
2. <span data-ttu-id="a9787-139">对请求的经过身份验证的用户的 SMTP 地址进行验证，以获得模拟权限。</span><span class="sxs-lookup"><span data-stu-id="a9787-139">The SMTP address of the authenticated user for the request is validated to have impersonation rights.</span></span> <span data-ttu-id="a9787-140">如果不是，则**GetStreamingEvents**请求将失败。</span><span class="sxs-lookup"><span data-stu-id="a9787-140">If they do not, the **GetStreamingEvents** request fails.</span></span> 
    
3. <span data-ttu-id="a9787-141">将查询订阅队列中等待发送到客户端的事件。</span><span class="sxs-lookup"><span data-stu-id="a9787-141">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="a9787-142">如果队列不为空，则会从队列中提取队列中的前50个事件并将其编码到通知中。</span><span class="sxs-lookup"><span data-stu-id="a9787-142">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="a9787-143">如果队列中未找到任何事件，则会生成[StatusEvent](statusevent.md)并将其编码到通知响应中。</span><span class="sxs-lookup"><span data-stu-id="a9787-143">If no events are found in the queue, a [StatusEvent](statusevent.md) is generated and encoded into a notification response.</span></span> 
    
5. <span data-ttu-id="a9787-144">通知响应将返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="a9787-144">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="a9787-145">通知中包含的事件将从订阅队列中删除，并且客户端访问服务器-订阅的本地最后的水印将设置为返回的最后一个事件的水印。</span><span class="sxs-lookup"><span data-stu-id="a9787-145">The events that are included in the notification are removed from the subscription queue and the Client Access server-local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="a9787-146">订阅的超时计时器将重置。</span><span class="sxs-lookup"><span data-stu-id="a9787-146">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9787-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9787-147">See also</span></span>



[<span data-ttu-id="a9787-148">订阅操作</span><span class="sxs-lookup"><span data-stu-id="a9787-148">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="a9787-149">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="a9787-149">Unsubscribe operation</span></span>](unsubscribe-operation.md)

