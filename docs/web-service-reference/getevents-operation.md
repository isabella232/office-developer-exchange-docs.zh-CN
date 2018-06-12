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
description: GetEvents 操作使用拉订阅客户端请求通知从客户端访问服务器。 GetEvents 操作响应返回的数组项和发生的事件的邮箱中上次通知。
ms.openlocfilehash: 1a23a9d570a4554e54becb7927f25dff89888c74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754531"
---
# <a name="getevents-operation"></a><span data-ttu-id="b78fd-104">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="b78fd-104">GetEvents operation</span></span>

<span data-ttu-id="b78fd-105">**GetEvents**操作使用拉订阅客户端请求通知从客户端访问服务器。</span><span class="sxs-lookup"><span data-stu-id="b78fd-105">The **GetEvents** operation is used by pull subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="b78fd-106">**GetEvents**操作响应返回的数组项和发生的事件的邮箱中上次通知。</span><span class="sxs-lookup"><span data-stu-id="b78fd-106">The **GetEvents** operation response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b78fd-107">**DeleteUserConfiguration**操作将触发事件通知系统移动的事件。</span><span class="sxs-lookup"><span data-stu-id="b78fd-107">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="b78fd-108">用户配置对象将移至转储程序。</span><span class="sxs-lookup"><span data-stu-id="b78fd-108">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b78fd-109">备注</span><span class="sxs-lookup"><span data-stu-id="b78fd-109">Remarks</span></span>

<span data-ttu-id="b78fd-110">对日历项目的更改可能会导致生成的多个事件。</span><span class="sxs-lookup"><span data-stu-id="b78fd-110">Changes to Calendar items may result in the generation of multiple events.</span></span> <span data-ttu-id="b78fd-111">这些事件是正在更改为正常的日历操作中，或两者的一部分的忙/闲数据存储项在邮箱中创建的临时项目的结果。</span><span class="sxs-lookup"><span data-stu-id="b78fd-111">These events are the result of temporary items being created in the mailbox, free/busy data storage items being changed as part of the normal Calendar operations, or both.</span></span> <span data-ttu-id="b78fd-112">项目的事件类"IPM。Web 服务客户端应忽略 SchedulePlus.FreeBusy.BinaryData"。</span><span class="sxs-lookup"><span data-stu-id="b78fd-112">Events for item class "IPM.SchedulePlus.FreeBusy.BinaryData" should be ignored by Web service clients.</span></span> <span data-ttu-id="b78fd-113">在创建; 后删除临时项目因此，如果尝试检索这些项，将返回错误，指出找不到该项目。</span><span class="sxs-lookup"><span data-stu-id="b78fd-113">These temporary items are deleted after they are created; therefore, if an attempt is made to retrieve these items, an error will be returned that states that the item was not found.</span></span>
  
## <a name="getevents-request-example"></a><span data-ttu-id="b78fd-114">GetEvents 请求示例</span><span class="sxs-lookup"><span data-stu-id="b78fd-114">GetEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="b78fd-115">说明</span><span class="sxs-lookup"><span data-stu-id="b78fd-115">Description</span></span>

<span data-ttu-id="b78fd-116">下面的示例演示如何请求的事件和订阅的订阅标识符和水印标识与关联的项目。</span><span class="sxs-lookup"><span data-stu-id="b78fd-116">The following example shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier and watermark.</span></span>
  
### <a name="code"></a><span data-ttu-id="b78fd-117">代码</span><span class="sxs-lookup"><span data-stu-id="b78fd-117">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a><span data-ttu-id="b78fd-118">GetEvents 请求元素</span><span class="sxs-lookup"><span data-stu-id="b78fd-118">GetEvents Request Elements</span></span>

<span data-ttu-id="b78fd-119">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b78fd-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b78fd-120">GetEvents</span><span class="sxs-lookup"><span data-stu-id="b78fd-120">GetEvents</span></span>](getevents.md)
    
- [<span data-ttu-id="b78fd-121">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="b78fd-121">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="b78fd-122">水印</span><span class="sxs-lookup"><span data-stu-id="b78fd-122">Watermark</span></span>](watermark.md)
    
## <a name="successful-getevents-response-example"></a><span data-ttu-id="b78fd-123">成功 GetEvents 响应示例</span><span class="sxs-lookup"><span data-stu-id="b78fd-123">Successful GetEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="b78fd-124">说明</span><span class="sxs-lookup"><span data-stu-id="b78fd-124">Description</span></span>

<span data-ttu-id="b78fd-125">下面的示例响应的显示存在两个新邮件通知自从最后一个通知请求发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="b78fd-125">The following example of a response shows a notification of the existence of two new mail messages since the last notification request was sent to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="b78fd-126">代码</span><span class="sxs-lookup"><span data-stu-id="b78fd-126">Code</span></span>

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
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="b78fd-127">注释</span><span class="sxs-lookup"><span data-stu-id="b78fd-127">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="b78fd-128">项目和文件夹标识符具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="b78fd-128">The item and folder identifiers have been shortened to preserve readability.</span></span> 
  
### <a name="getevents-response-elements"></a><span data-ttu-id="b78fd-129">GetEvents 响应元素</span><span class="sxs-lookup"><span data-stu-id="b78fd-129">GetEvents response elements</span></span>

<span data-ttu-id="b78fd-130">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="b78fd-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b78fd-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="b78fd-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="b78fd-132">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="b78fd-132">GetEventsResponse</span></span>](geteventsresponse.md)
    
- [<span data-ttu-id="b78fd-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b78fd-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="b78fd-134">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b78fd-134">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md)
    
- [<span data-ttu-id="b78fd-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b78fd-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="b78fd-136">通知</span><span class="sxs-lookup"><span data-stu-id="b78fd-136">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="b78fd-137">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="b78fd-137">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="b78fd-138">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="b78fd-138">PreviousWatermark</span></span>](previouswatermark.md)
    
- [<span data-ttu-id="b78fd-139">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="b78fd-139">MoreEvents</span></span>](moreevents.md)
    
- [<span data-ttu-id="b78fd-140">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="b78fd-140">NewMailEvent</span></span>](newmailevent.md)
    
- [<span data-ttu-id="b78fd-141">水印</span><span class="sxs-lookup"><span data-stu-id="b78fd-141">Watermark</span></span>](watermark.md)
    
- [<span data-ttu-id="b78fd-142">时间戳</span><span class="sxs-lookup"><span data-stu-id="b78fd-142">TimeStamp</span></span>](timestamp.md)
    
- [<span data-ttu-id="b78fd-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="b78fd-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="b78fd-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b78fd-144">ParentFolderId</span></span>](parentfolderid.md)
    
<span data-ttu-id="b78fd-145">若要查找的响应消息**GetEvents**操作的其他选项，浏览的架构层次结构。</span><span class="sxs-lookup"><span data-stu-id="b78fd-145">To find other options for the response message of the **GetEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="b78fd-146">启动[通知](notification-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b78fd-146">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getevents-error-response-example"></a><span data-ttu-id="b78fd-147">GetEvents 错误响应示例</span><span class="sxs-lookup"><span data-stu-id="b78fd-147">GetEvents Error response example</span></span>

### <a name="description"></a><span data-ttu-id="b78fd-148">说明</span><span class="sxs-lookup"><span data-stu-id="b78fd-148">Description</span></span>

<span data-ttu-id="b78fd-149">下面的示例演示对**GetEvents**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="b78fd-149">The following example shows an error response to a **GetEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b78fd-150">代码</span><span class="sxs-lookup"><span data-stu-id="b78fd-150">Code</span></span>

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
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="remarks"></a><span data-ttu-id="b78fd-151">备注</span><span class="sxs-lookup"><span data-stu-id="b78fd-151">Remarks</span></span>

<span data-ttu-id="b78fd-152">当处理**GetEvents**请求，客户端访问服务器将执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b78fd-152">When processing a **GetEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="b78fd-153">确认请求的 SubscriptionID 是有效的订阅的客户端访问服务器上承载。</span><span class="sxs-lookup"><span data-stu-id="b78fd-153">The SubscriptionID of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="b78fd-154">如果不存在，则**GetEvents**调用将失败。</span><span class="sxs-lookup"><span data-stu-id="b78fd-154">If it is not, the **GetEvents** call fails.</span></span> 
    
2. <span data-ttu-id="b78fd-155">创建订阅的用户的 SMTP 地址进行比较的请求身份验证的用户的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="b78fd-155">The SMTP address of the authenticated user for the request is compared to the SMTP address of the user who created the subscription.</span></span> <span data-ttu-id="b78fd-156">如果不匹配， **GetEvents**请求失败。</span><span class="sxs-lookup"><span data-stu-id="b78fd-156">If they do not match, the **GetEvents** request fails.</span></span> 
    
3. <span data-ttu-id="b78fd-157">订阅队列中等待要发送给客户端的事件查询。</span><span class="sxs-lookup"><span data-stu-id="b78fd-157">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="b78fd-158">如果不为空队列，从队列的前 50 个事件是从队列中拉取和编码到通知。</span><span class="sxs-lookup"><span data-stu-id="b78fd-158">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="b78fd-159">如果在队列中不发现的任何事件，StatusEvent 生成，且编码到通知响应。</span><span class="sxs-lookup"><span data-stu-id="b78fd-159">If no events are found in the queue, a StatusEvent is generated and encoded into a notification response.</span></span>
    
5. <span data-ttu-id="b78fd-160">通知响应将返回到客户端。</span><span class="sxs-lookup"><span data-stu-id="b78fd-160">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="b78fd-161">从订阅队列中删除包含在的通知的事件和客户端访问服务器本地最后一个水印订阅设置为返回的最后一个事件水印。</span><span class="sxs-lookup"><span data-stu-id="b78fd-161">The events that are included in the notification are removed from the subscription queue and the Client Access server local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="b78fd-162">订阅超时计时器重置。</span><span class="sxs-lookup"><span data-stu-id="b78fd-162">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b78fd-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b78fd-163">See also</span></span>



[<span data-ttu-id="b78fd-164">订阅操作</span><span class="sxs-lookup"><span data-stu-id="b78fd-164">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b78fd-165">取消操作</span><span class="sxs-lookup"><span data-stu-id="b78fd-165">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="b78fd-166">使用请求订阅</span><span class="sxs-lookup"><span data-stu-id="b78fd-166">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

