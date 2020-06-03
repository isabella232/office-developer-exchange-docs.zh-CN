---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: StatusFrequency 元素表示服务器尝试重试的最大超时值（以分钟为单位）。
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468241"
---
# <a name="statusfrequency"></a><span data-ttu-id="22b50-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="22b50-103">StatusFrequency</span></span>

<span data-ttu-id="22b50-104">**StatusFrequency**元素表示服务器尝试重试的最大超时值（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="22b50-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="22b50-105">订阅</span><span class="sxs-lookup"><span data-stu-id="22b50-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="22b50-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="22b50-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="22b50-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="22b50-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="22b50-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="22b50-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22b50-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22b50-109">Attributes and elements</span></span>

<span data-ttu-id="22b50-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22b50-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22b50-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="22b50-111">Attributes</span></span>

<span data-ttu-id="22b50-112">无。</span><span class="sxs-lookup"><span data-stu-id="22b50-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22b50-113">子元素</span><span class="sxs-lookup"><span data-stu-id="22b50-113">Child elements</span></span>

<span data-ttu-id="22b50-114">无。</span><span class="sxs-lookup"><span data-stu-id="22b50-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22b50-115">父元素</span><span class="sxs-lookup"><span data-stu-id="22b50-115">Parent elements</span></span>

|<span data-ttu-id="22b50-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="22b50-116">**Element**</span></span>|<span data-ttu-id="22b50-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="22b50-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22b50-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="22b50-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="22b50-119">表示对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="22b50-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22b50-120">文本值</span><span class="sxs-lookup"><span data-stu-id="22b50-120">Text value</span></span>

<span data-ttu-id="22b50-121">如果使用此元素，则需要一个表示整数的文本值。</span><span class="sxs-lookup"><span data-stu-id="22b50-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="22b50-122">此元素的可能值为1到1440（包含这两个值）。</span><span class="sxs-lookup"><span data-stu-id="22b50-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="22b50-123">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="22b50-123">This element is optional.</span></span> <span data-ttu-id="22b50-124">默认值为 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="22b50-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22b50-125">备注</span><span class="sxs-lookup"><span data-stu-id="22b50-125">Remarks</span></span>

<span data-ttu-id="22b50-126">当服务器未收到对推送通知或来自客户端的状态 ping 的响应时，服务器使用**StatusFrequency**值重试推送通知。</span><span class="sxs-lookup"><span data-stu-id="22b50-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="22b50-127">如果服务器没有收到响应，则在停止发送通知之前，它会多次重试发送通知。</span><span class="sxs-lookup"><span data-stu-id="22b50-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="22b50-128">在 EWS 中，默认重试间隔为30秒，随后重试次数始终为上次重试间隔的时间的两倍。</span><span class="sxs-lookup"><span data-stu-id="22b50-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="22b50-129">重试次数并不完全取决于服务器上的其他负载是否会延迟。</span><span class="sxs-lookup"><span data-stu-id="22b50-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="22b50-130">下表显示了在由默认**StatusFrequency**值（假定服务器未遇到任何延迟）分配的30分钟内重试间隔的发生方式。</span><span class="sxs-lookup"><span data-stu-id="22b50-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="22b50-131">**重试**</span><span class="sxs-lookup"><span data-stu-id="22b50-131">**Retry**</span></span>|<span data-ttu-id="22b50-132">**秒**</span><span class="sxs-lookup"><span data-stu-id="22b50-132">**Seconds**</span></span>|<span data-ttu-id="22b50-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="22b50-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="22b50-134">0</span><span class="sxs-lookup"><span data-stu-id="22b50-134">0</span></span>  <br/> |<span data-ttu-id="22b50-135">0</span><span class="sxs-lookup"><span data-stu-id="22b50-135">0</span></span>  <br/> |<span data-ttu-id="22b50-136">初始同步</span><span class="sxs-lookup"><span data-stu-id="22b50-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="22b50-137">1 </span><span class="sxs-lookup"><span data-stu-id="22b50-137">1</span></span>  <br/> |<span data-ttu-id="22b50-138">30</span><span class="sxs-lookup"><span data-stu-id="22b50-138">30</span></span>  <br/> |<span data-ttu-id="22b50-139">00:30</span><span class="sxs-lookup"><span data-stu-id="22b50-139">00:30</span></span>  <br/> |
|<span data-ttu-id="22b50-140">双面</span><span class="sxs-lookup"><span data-stu-id="22b50-140">2</span></span>  <br/> |<span data-ttu-id="22b50-141">60</span><span class="sxs-lookup"><span data-stu-id="22b50-141">60</span></span>  <br/> |<span data-ttu-id="22b50-142">01:00</span><span class="sxs-lookup"><span data-stu-id="22b50-142">01:00</span></span>  <br/> |
|<span data-ttu-id="22b50-143">第三章</span><span class="sxs-lookup"><span data-stu-id="22b50-143">3</span></span>  <br/> |<span data-ttu-id="22b50-144">120</span><span class="sxs-lookup"><span data-stu-id="22b50-144">120</span></span>  <br/> |<span data-ttu-id="22b50-145">02:00</span><span class="sxs-lookup"><span data-stu-id="22b50-145">02:00</span></span>  <br/> |
|<span data-ttu-id="22b50-146">4 </span><span class="sxs-lookup"><span data-stu-id="22b50-146">4</span></span>  <br/> |<span data-ttu-id="22b50-147">240</span><span class="sxs-lookup"><span data-stu-id="22b50-147">240</span></span>  <br/> |<span data-ttu-id="22b50-148">04:00</span><span class="sxs-lookup"><span data-stu-id="22b50-148">04:00</span></span>  <br/> |
|<span data-ttu-id="22b50-149">5 </span><span class="sxs-lookup"><span data-stu-id="22b50-149">5</span></span>  <br/> |<span data-ttu-id="22b50-150">480</span><span class="sxs-lookup"><span data-stu-id="22b50-150">480</span></span>  <br/> |<span data-ttu-id="22b50-151">08:00</span><span class="sxs-lookup"><span data-stu-id="22b50-151">08:00</span></span>  <br/> |
|<span data-ttu-id="22b50-152">6 </span><span class="sxs-lookup"><span data-stu-id="22b50-152">6</span></span>  <br/> |<span data-ttu-id="22b50-153">960</span><span class="sxs-lookup"><span data-stu-id="22b50-153">960</span></span>  <br/> |<span data-ttu-id="22b50-154">16:00</span><span class="sxs-lookup"><span data-stu-id="22b50-154">16:00</span></span>  <br/> |
|<span data-ttu-id="22b50-155">7 </span><span class="sxs-lookup"><span data-stu-id="22b50-155">7</span></span>  <br/> |<span data-ttu-id="22b50-156">1920</span><span class="sxs-lookup"><span data-stu-id="22b50-156">1920</span></span>  <br/> |<span data-ttu-id="22b50-157">32:00-超过**StatusFrequency**的默认值30，不发送重试</span><span class="sxs-lookup"><span data-stu-id="22b50-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="22b50-158">如果客户端在超过**StatusFrequency**指定时间的一段时间内未收到来自服务器的通知消息，客户端应执行重新创建订阅等操作。</span><span class="sxs-lookup"><span data-stu-id="22b50-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="22b50-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22b50-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22b50-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="22b50-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22b50-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="22b50-161">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22b50-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="22b50-162">Schema name</span></span>  <br/> |<span data-ttu-id="22b50-163">类型架构</span><span class="sxs-lookup"><span data-stu-id="22b50-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="22b50-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="22b50-164">Validation file</span></span>  <br/> |<span data-ttu-id="22b50-165">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22b50-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22b50-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="22b50-166">Can be empty</span></span>  <br/> |<span data-ttu-id="22b50-167">False</span><span class="sxs-lookup"><span data-stu-id="22b50-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22b50-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22b50-168">See also</span></span>



[<span data-ttu-id="22b50-169">订阅操作</span><span class="sxs-lookup"><span data-stu-id="22b50-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="22b50-170">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="22b50-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="22b50-171">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="22b50-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="22b50-172">Watermark</span><span class="sxs-lookup"><span data-stu-id="22b50-172">Watermark</span></span>](watermark.md)

