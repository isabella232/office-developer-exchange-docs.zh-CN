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
description: 查找信息 GetStreamingEvents EWS 操作。
ms.openlocfilehash: 0e93be7b14cb1ca6a2a9821b016f7bdc0e8d7772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825673"
---
# <a name="getstreamingevents-operation"></a><span data-ttu-id="42d9a-103">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="42d9a-103">GetStreamingEvents operation</span></span>

<span data-ttu-id="42d9a-104">查找有关**GetStreamingEvents** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="42d9a-104">Find information about the **GetStreamingEvents** EWS operation.</span></span> 
  
<span data-ttu-id="42d9a-105">流式处理订阅客户端使用**GetStreamingEvents**操作从客户端访问服务器请求通知。</span><span class="sxs-lookup"><span data-stu-id="42d9a-105">The **GetStreamingEvents** operation is used by streaming subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="42d9a-106">**GetStreamingEvents**响应中返回的数组项和发生的事件的邮箱中上次通知。</span><span class="sxs-lookup"><span data-stu-id="42d9a-106">The **GetStreamingEvents** response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
## <a name="getstreamingevents-request-example"></a><span data-ttu-id="42d9a-107">GetStreamingEvents 请求示例</span><span class="sxs-lookup"><span data-stu-id="42d9a-107">GetStreamingEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="42d9a-108">说明</span><span class="sxs-lookup"><span data-stu-id="42d9a-108">Description</span></span>

<span data-ttu-id="42d9a-109">**GetStreamingEvents**操作的下面的示例演示如何请求的事件和订阅的订阅标识符标识与关联的项目。</span><span class="sxs-lookup"><span data-stu-id="42d9a-109">The following example of a **GetStreamingEvents** operation shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42d9a-110">代码</span><span class="sxs-lookup"><span data-stu-id="42d9a-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
  xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Body>
    <GetStreamingEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <ConnectionTimeout>30</ConnectionTimeout>
    </GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getstreamingevents-request-elements"></a><span data-ttu-id="42d9a-111">GetStreamingEvents 请求元素</span><span class="sxs-lookup"><span data-stu-id="42d9a-111">GetStreamingEvents request elements</span></span>

<span data-ttu-id="42d9a-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="42d9a-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="42d9a-113">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="42d9a-113">GetStreamingEvents</span></span>](getstreamingevents.md)
    
- [<span data-ttu-id="42d9a-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="42d9a-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
- [<span data-ttu-id="42d9a-115">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="42d9a-115">ConnectionTimeout</span></span>](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a><span data-ttu-id="42d9a-116">成功 GetStreamingEvents 响应示例</span><span class="sxs-lookup"><span data-stu-id="42d9a-116">Successful GetStreamingEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="42d9a-117">说明</span><span class="sxs-lookup"><span data-stu-id="42d9a-117">Description</span></span>

<span data-ttu-id="42d9a-118">**GetStreamingEvents**响应的下面的示例演示时收到新的电子邮件发送到客户端的通知。</span><span class="sxs-lookup"><span data-stu-id="42d9a-118">The following example of a **GetStreamingEvents** response shows the notifications that are sent to the client when a new email message is received.</span></span> <span data-ttu-id="42d9a-119">它包括下面的事件通知： CreatedEvent、 NewMail 和 ModifiedEvent。</span><span class="sxs-lookup"><span data-stu-id="42d9a-119">It includes notifications for the following events: CreatedEvent, NewMail, and ModifiedEvent.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42d9a-120">代码</span><span class="sxs-lookup"><span data-stu-id="42d9a-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <ServerVersionInfo xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
</soap:Header>
<soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="getstreamingevents-response-elements"></a><span data-ttu-id="42d9a-121">GetStreamingEvents 响应元素</span><span class="sxs-lookup"><span data-stu-id="42d9a-121">GetStreamingEvents response elements</span></span>

<span data-ttu-id="42d9a-122">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="42d9a-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="42d9a-123">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="42d9a-123">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
    
- [<span data-ttu-id="42d9a-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="42d9a-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="42d9a-125">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="42d9a-125">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md)
    
- [<span data-ttu-id="42d9a-126">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="42d9a-126">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md)
    
- [<span data-ttu-id="42d9a-127">通知</span><span class="sxs-lookup"><span data-stu-id="42d9a-127">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="42d9a-128">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="42d9a-128">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
<span data-ttu-id="42d9a-129">若要查找的响应消息**GetStreamingEvents**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="42d9a-129">To find other options for the response message of the **GetStreamingEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="42d9a-130">启动[通知](notification-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="42d9a-130">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getstreamingevents-error-response-example"></a><span data-ttu-id="42d9a-131">GetStreamingEvents 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="42d9a-131">GetStreamingEvents error response example</span></span>

### <a name="description"></a><span data-ttu-id="42d9a-132">说明</span><span class="sxs-lookup"><span data-stu-id="42d9a-132">Description</span></span>

<span data-ttu-id="42d9a-133">下面的示例演示对**GetStreamingEvents**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="42d9a-133">The following example shows an error response to a **GetStreamingEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="42d9a-134">代码</span><span class="sxs-lookup"><span data-stu-id="42d9a-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetStreamingEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="remarks"></a><span data-ttu-id="42d9a-135">备注</span><span class="sxs-lookup"><span data-stu-id="42d9a-135">Remarks</span></span>

<span data-ttu-id="42d9a-136">当处理**GetStreamingEvents**请求，客户端访问服务器将执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="42d9a-136">When processing a **GetStreamingEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="42d9a-137">确认请求的[SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md)是有效的订阅的客户端访问服务器上承载。</span><span class="sxs-lookup"><span data-stu-id="42d9a-137">The [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="42d9a-138">如果不存在，则**GetStreamingEvents**调用将失败。</span><span class="sxs-lookup"><span data-stu-id="42d9a-138">If it is not, the **GetStreamingEvents** call fails.</span></span> 
    
2. <span data-ttu-id="42d9a-139">验证请求身份验证的用户的 SMTP 地址拥有模拟权限。</span><span class="sxs-lookup"><span data-stu-id="42d9a-139">The SMTP address of the authenticated user for the request is validated to have impersonation rights.</span></span> <span data-ttu-id="42d9a-140">如果未显示，请**GetStreamingEvents**请求失败。</span><span class="sxs-lookup"><span data-stu-id="42d9a-140">If they do not, the **GetStreamingEvents** request fails.</span></span> 
    
3. <span data-ttu-id="42d9a-141">订阅队列中等待要发送给客户端的事件查询。</span><span class="sxs-lookup"><span data-stu-id="42d9a-141">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="42d9a-142">如果不为空队列，从队列的前 50 个事件是从队列中拉取和编码到通知。</span><span class="sxs-lookup"><span data-stu-id="42d9a-142">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="42d9a-143">如果在队列中不发现的任何事件， [StatusEvent](statusevent.md)生成，且编码到通知响应。</span><span class="sxs-lookup"><span data-stu-id="42d9a-143">If no events are found in the queue, a [StatusEvent](statusevent.md) is generated and encoded into a notification response.</span></span> 
    
5. <span data-ttu-id="42d9a-144">通知响应将返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="42d9a-144">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="42d9a-145">从订阅队列中删除包含在的通知的事件和客户端访问服务器本地最后一个水印订阅设置为返回的最后一个事件水印。</span><span class="sxs-lookup"><span data-stu-id="42d9a-145">The events that are included in the notification are removed from the subscription queue and the Client Access server-local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="42d9a-146">订阅超时计时器重置。</span><span class="sxs-lookup"><span data-stu-id="42d9a-146">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42d9a-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="42d9a-147">See also</span></span>



[<span data-ttu-id="42d9a-148">订阅操作</span><span class="sxs-lookup"><span data-stu-id="42d9a-148">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="42d9a-149">取消操作</span><span class="sxs-lookup"><span data-stu-id="42d9a-149">Unsubscribe operation</span></span>](unsubscribe-operation.md)

