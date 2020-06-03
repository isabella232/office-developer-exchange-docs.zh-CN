---
title: GetEvents 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: 请求订阅客户端使用 GetEvents 操作从客户端访问服务器中请求通知。 GetEvents 操作响应返回自上次通知以来在邮箱中发生的项和事件的数组。
ms.openlocfilehash: 9258fd003c242911866aa7abbca5eba2b9582223
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462512"
---
# <a name="getevents-operation"></a><span data-ttu-id="5f991-104">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="5f991-104">GetEvents operation</span></span>

<span data-ttu-id="5f991-105">请求订阅客户端使用**GetEvents**操作从客户端访问服务器中请求通知。</span><span class="sxs-lookup"><span data-stu-id="5f991-105">The **GetEvents** operation is used by pull subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="5f991-106">**GetEvents**操作响应返回自上次通知以来在邮箱中发生的项和事件的数组。</span><span class="sxs-lookup"><span data-stu-id="5f991-106">The **GetEvents** operation response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5f991-107">**DeleteUserConfiguration**操作将触发事件通知系统的移动事件。</span><span class="sxs-lookup"><span data-stu-id="5f991-107">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="5f991-108">用户配置对象将被移动到转储程序。</span><span class="sxs-lookup"><span data-stu-id="5f991-108">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5f991-109">备注</span><span class="sxs-lookup"><span data-stu-id="5f991-109">Remarks</span></span>

<span data-ttu-id="5f991-110">对日历项目所做的更改可能会导致生成多个事件。</span><span class="sxs-lookup"><span data-stu-id="5f991-110">Changes to Calendar items may result in the generation of multiple events.</span></span> <span data-ttu-id="5f991-111">这些事件是在邮箱、忙/闲数据存储项目被更改为常规日历操作的一部分或同时在这两者中创建的临时项目的结果。</span><span class="sxs-lookup"><span data-stu-id="5f991-111">These events are the result of temporary items being created in the mailbox, free/busy data storage items being changed as part of the normal Calendar operations, or both.</span></span> <span data-ttu-id="5f991-112">项目类 "IPM." 的事件。Web 服务客户端应忽略 FreeBusy。 SchedulePlus。</span><span class="sxs-lookup"><span data-stu-id="5f991-112">Events for item class "IPM.SchedulePlus.FreeBusy.BinaryData" should be ignored by Web service clients.</span></span> <span data-ttu-id="5f991-113">这些临时项目在创建后将被删除;因此，如果尝试检索这些项，则将返回错误，指出找不到该项目。</span><span class="sxs-lookup"><span data-stu-id="5f991-113">These temporary items are deleted after they are created; therefore, if an attempt is made to retrieve these items, an error will be returned that states that the item was not found.</span></span>
  
## <a name="getevents-request-example"></a><span data-ttu-id="5f991-114">GetEvents 请求示例</span><span class="sxs-lookup"><span data-stu-id="5f991-114">GetEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="5f991-115">Description</span><span class="sxs-lookup"><span data-stu-id="5f991-115">Description</span></span>

<span data-ttu-id="5f991-116">下面的示例演示如何请求与订阅标识符和水印标识的订阅相关联的事件和项目。</span><span class="sxs-lookup"><span data-stu-id="5f991-116">The following example shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier and watermark.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f991-117">代码</span><span class="sxs-lookup"><span data-stu-id="5f991-117">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a><span data-ttu-id="5f991-118">GetEvents 请求元素</span><span class="sxs-lookup"><span data-stu-id="5f991-118">GetEvents Request Elements</span></span>

<span data-ttu-id="5f991-119">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f991-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5f991-120">GetEvents</span><span class="sxs-lookup"><span data-stu-id="5f991-120">GetEvents</span></span>](getevents.md)
    
- [<span data-ttu-id="5f991-121">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="5f991-121">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="5f991-122">Watermark</span><span class="sxs-lookup"><span data-stu-id="5f991-122">Watermark</span></span>](watermark.md)
    
## <a name="successful-getevents-response-example"></a><span data-ttu-id="5f991-123">成功的 GetEvents 响应示例</span><span class="sxs-lookup"><span data-stu-id="5f991-123">Successful GetEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="5f991-124">Description</span><span class="sxs-lookup"><span data-stu-id="5f991-124">Description</span></span>

<span data-ttu-id="5f991-125">下面的响应示例显示通知，自上次通知请求发送到服务器后，存在两封新邮件。</span><span class="sxs-lookup"><span data-stu-id="5f991-125">The following example of a response shows a notification of the existence of two new mail messages since the last notification request was sent to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f991-126">代码</span><span class="sxs-lookup"><span data-stu-id="5f991-126">Code</span></span>

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
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="5f991-127">备注</span><span class="sxs-lookup"><span data-stu-id="5f991-127">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="5f991-128">项目和文件夹标识符已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="5f991-128">The item and folder identifiers have been shortened to preserve readability.</span></span> 
  
### <a name="getevents-response-elements"></a><span data-ttu-id="5f991-129">GetEvents 响应元素</span><span class="sxs-lookup"><span data-stu-id="5f991-129">GetEvents response elements</span></span>

<span data-ttu-id="5f991-130">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f991-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5f991-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5f991-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5f991-132">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="5f991-132">GetEventsResponse</span></span>](geteventsresponse.md)
    
- [<span data-ttu-id="5f991-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f991-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5f991-134">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f991-134">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md)
    
- [<span data-ttu-id="5f991-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5f991-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5f991-136">通知</span><span class="sxs-lookup"><span data-stu-id="5f991-136">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="5f991-137">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="5f991-137">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="5f991-138">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="5f991-138">PreviousWatermark</span></span>](previouswatermark.md)
    
- [<span data-ttu-id="5f991-139">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="5f991-139">MoreEvents</span></span>](moreevents.md)
    
- [<span data-ttu-id="5f991-140">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="5f991-140">NewMailEvent</span></span>](newmailevent.md)
    
- [<span data-ttu-id="5f991-141">Watermark</span><span class="sxs-lookup"><span data-stu-id="5f991-141">Watermark</span></span>](watermark.md)
    
- [<span data-ttu-id="5f991-142">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="5f991-142">TimeStamp</span></span>](timestamp.md)
    
- [<span data-ttu-id="5f991-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f991-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="5f991-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="5f991-144">ParentFolderId</span></span>](parentfolderid.md)
    
<span data-ttu-id="5f991-145">若要查找**GetEvents**操作的响应邮件的其他选项，请浏览架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="5f991-145">To find other options for the response message of the **GetEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5f991-146">从[通知](notification-ex15websvcsotherref.md)元素开始。</span><span class="sxs-lookup"><span data-stu-id="5f991-146">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getevents-error-response-example"></a><span data-ttu-id="5f991-147">GetEvents 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5f991-147">GetEvents Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5f991-148">Description</span><span class="sxs-lookup"><span data-stu-id="5f991-148">Description</span></span>

<span data-ttu-id="5f991-149">下面的示例演示对**GetEvents**请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="5f991-149">The following example shows an error response to a **GetEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5f991-150">代码</span><span class="sxs-lookup"><span data-stu-id="5f991-150">Code</span></span>

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
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a><span data-ttu-id="5f991-151">备注</span><span class="sxs-lookup"><span data-stu-id="5f991-151">Remarks</span></span>

<span data-ttu-id="5f991-152">在处理**GetEvents**请求时，客户端访问服务器将执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="5f991-152">When processing a **GetEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="5f991-153">将请求的 SubscriptionID 确认为在客户端访问服务器上承载的有效订阅。</span><span class="sxs-lookup"><span data-stu-id="5f991-153">The SubscriptionID of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="5f991-154">如果不是，则**GetEvents**调用将失败。</span><span class="sxs-lookup"><span data-stu-id="5f991-154">If it is not, the **GetEvents** call fails.</span></span> 
    
2. <span data-ttu-id="5f991-155">将请求的已通过身份验证的用户的 SMTP 地址与创建订阅的用户的 SMTP 地址进行比较。</span><span class="sxs-lookup"><span data-stu-id="5f991-155">The SMTP address of the authenticated user for the request is compared to the SMTP address of the user who created the subscription.</span></span> <span data-ttu-id="5f991-156">如果不匹配， **GetEvents**请求将失败。</span><span class="sxs-lookup"><span data-stu-id="5f991-156">If they do not match, the **GetEvents** request fails.</span></span> 
    
3. <span data-ttu-id="5f991-157">将查询订阅队列中等待发送到客户端的事件。</span><span class="sxs-lookup"><span data-stu-id="5f991-157">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="5f991-158">如果队列不为空，则会从队列中提取队列中的前50个事件并将其编码到通知中。</span><span class="sxs-lookup"><span data-stu-id="5f991-158">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="5f991-159">如果队列中未找到任何事件，则会生成 StatusEvent 并将其编码到通知响应中。</span><span class="sxs-lookup"><span data-stu-id="5f991-159">If no events are found in the queue, a StatusEvent is generated and encoded into a notification response.</span></span>
    
5. <span data-ttu-id="5f991-160">通知响应将返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="5f991-160">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="5f991-161">通知中包含的事件将从订阅队列中删除，并且订阅的客户端访问服务器本地最后的水印将设置为返回的最后一个事件的水印。</span><span class="sxs-lookup"><span data-stu-id="5f991-161">The events that are included in the notification are removed from the subscription queue and the Client Access server local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="5f991-162">订阅的超时计时器将重置。</span><span class="sxs-lookup"><span data-stu-id="5f991-162">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f991-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f991-163">See also</span></span>



[<span data-ttu-id="5f991-164">订阅操作</span><span class="sxs-lookup"><span data-stu-id="5f991-164">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="5f991-165">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="5f991-165">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="5f991-166">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="5f991-166">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

