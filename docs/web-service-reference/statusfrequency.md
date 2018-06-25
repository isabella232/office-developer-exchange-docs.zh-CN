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
description: StatusFrequency 元素表示最大超时值，以分钟为单位，由服务器尝试重试。
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827589"
---
# <a name="statusfrequency"></a><span data-ttu-id="de0e5-103">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="de0e5-103">StatusFrequency</span></span>

<span data-ttu-id="de0e5-104">**StatusFrequency**元素表示最大超时值，以分钟为单位，由服务器尝试重试。</span><span class="sxs-lookup"><span data-stu-id="de0e5-104">The **StatusFrequency** element represents the maximum timeout value, in minutes, in which retries are attempted by the server.</span></span> 
  
[<span data-ttu-id="de0e5-105">订阅</span><span class="sxs-lookup"><span data-stu-id="de0e5-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="de0e5-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="de0e5-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="de0e5-107">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="de0e5-107">StatusFrequency</span></span>](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 <span data-ttu-id="de0e5-108">**SubscriptionStatusFrequencyType**</span><span class="sxs-lookup"><span data-stu-id="de0e5-108">**SubscriptionStatusFrequencyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de0e5-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="de0e5-109">Attributes and elements</span></span>

<span data-ttu-id="de0e5-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="de0e5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de0e5-111">属性</span><span class="sxs-lookup"><span data-stu-id="de0e5-111">Attributes</span></span>

<span data-ttu-id="de0e5-112">无。</span><span class="sxs-lookup"><span data-stu-id="de0e5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de0e5-113">子元素</span><span class="sxs-lookup"><span data-stu-id="de0e5-113">Child elements</span></span>

<span data-ttu-id="de0e5-114">无。</span><span class="sxs-lookup"><span data-stu-id="de0e5-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de0e5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="de0e5-115">Parent elements</span></span>

|<span data-ttu-id="de0e5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="de0e5-116">**Element**</span></span>|<span data-ttu-id="de0e5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="de0e5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de0e5-118">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="de0e5-118">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="de0e5-119">代表对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="de0e5-119">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de0e5-120">文本值</span><span class="sxs-lookup"><span data-stu-id="de0e5-120">Text value</span></span>

<span data-ttu-id="de0e5-121">如果使用此元素，则需要表示一个整数的文本值。</span><span class="sxs-lookup"><span data-stu-id="de0e5-121">A text value that represents an integer is required if this element is used.</span></span> <span data-ttu-id="de0e5-122">此元素的可能值是 1 到 1440 之间，非独占。</span><span class="sxs-lookup"><span data-stu-id="de0e5-122">The possible values for this element are 1 to 1440, inclusive.</span></span> <span data-ttu-id="de0e5-123">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="de0e5-123">This element is optional.</span></span> <span data-ttu-id="de0e5-124">默认值为 30 分钟。</span><span class="sxs-lookup"><span data-stu-id="de0e5-124">The default value is 30 minutes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de0e5-125">注解</span><span class="sxs-lookup"><span data-stu-id="de0e5-125">Remarks</span></span>

<span data-ttu-id="de0e5-126">服务器使用**StatusFrequency**值时不会收到来自客户端的推送通知或状态 ping 响应重试推送通知。</span><span class="sxs-lookup"><span data-stu-id="de0e5-126">The **StatusFrequency** value is used by the server to retry a push notification when it does not receive a response to a push notification or status ping from the client.</span></span> <span data-ttu-id="de0e5-127">如果服务器未收到响应，它重试停止发送通知前几次发送通知。</span><span class="sxs-lookup"><span data-stu-id="de0e5-127">If the server does not receive a response, it retries sending the notification several times before it stops sending the notification.</span></span> <span data-ttu-id="de0e5-128">Ews，默认重试时间间隔为 30 秒，并且后续重试次数总是 double 最后一个重试时间间隔的时间。</span><span class="sxs-lookup"><span data-stu-id="de0e5-128">In EWS, the default retry interval is 30 seconds and subsequent retries are always double the time of the last retry interval.</span></span> <span data-ttu-id="de0e5-129">重试次数并不精确，与他们可以延迟由于服务器上的其他负载。</span><span class="sxs-lookup"><span data-stu-id="de0e5-129">Retry times are not exact as they can be delayed due to other loads on the server.</span></span> <span data-ttu-id="de0e5-130">下表显示了如何分配的默认**StatusFrequency**值 （假定服务器不会遇到任何延迟） 在 30 分钟内发生的重试间隔。</span><span class="sxs-lookup"><span data-stu-id="de0e5-130">The following table shows how the retry intervals occur in the 30 minutes allotted by the default **StatusFrequency** value (assuming the server did not encounter any delays).</span></span> 
  
|<span data-ttu-id="de0e5-131">**重试**</span><span class="sxs-lookup"><span data-stu-id="de0e5-131">**Retry**</span></span>|<span data-ttu-id="de0e5-132">**秒**</span><span class="sxs-lookup"><span data-stu-id="de0e5-132">**Seconds**</span></span>|<span data-ttu-id="de0e5-133">**Time**</span><span class="sxs-lookup"><span data-stu-id="de0e5-133">**Time**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de0e5-134">0</span><span class="sxs-lookup"><span data-stu-id="de0e5-134">0</span></span>  <br/> |<span data-ttu-id="de0e5-135">0</span><span class="sxs-lookup"><span data-stu-id="de0e5-135">0</span></span>  <br/> |<span data-ttu-id="de0e5-136">初始同步</span><span class="sxs-lookup"><span data-stu-id="de0e5-136">Initial sync</span></span>  <br/> |
|<span data-ttu-id="de0e5-137">1</span><span class="sxs-lookup"><span data-stu-id="de0e5-137">1</span></span>  <br/> |<span data-ttu-id="de0e5-138">30</span><span class="sxs-lookup"><span data-stu-id="de0e5-138">30</span></span>  <br/> |<span data-ttu-id="de0e5-139">00:30</span><span class="sxs-lookup"><span data-stu-id="de0e5-139">00:30</span></span>  <br/> |
|<span data-ttu-id="de0e5-140">2</span><span class="sxs-lookup"><span data-stu-id="de0e5-140">2</span></span>  <br/> |<span data-ttu-id="de0e5-141">60</span><span class="sxs-lookup"><span data-stu-id="de0e5-141">60</span></span>  <br/> |<span data-ttu-id="de0e5-142">01:00</span><span class="sxs-lookup"><span data-stu-id="de0e5-142">01:00</span></span>  <br/> |
|<span data-ttu-id="de0e5-143">3</span><span class="sxs-lookup"><span data-stu-id="de0e5-143">3</span></span>  <br/> |<span data-ttu-id="de0e5-144">120</span><span class="sxs-lookup"><span data-stu-id="de0e5-144">120</span></span>  <br/> |<span data-ttu-id="de0e5-145">02:00</span><span class="sxs-lookup"><span data-stu-id="de0e5-145">02:00</span></span>  <br/> |
|<span data-ttu-id="de0e5-146">4</span><span class="sxs-lookup"><span data-stu-id="de0e5-146">4</span></span>  <br/> |<span data-ttu-id="de0e5-147">240</span><span class="sxs-lookup"><span data-stu-id="de0e5-147">240</span></span>  <br/> |<span data-ttu-id="de0e5-148">04:00</span><span class="sxs-lookup"><span data-stu-id="de0e5-148">04:00</span></span>  <br/> |
|<span data-ttu-id="de0e5-149">5</span><span class="sxs-lookup"><span data-stu-id="de0e5-149">5</span></span>  <br/> |<span data-ttu-id="de0e5-150">480</span><span class="sxs-lookup"><span data-stu-id="de0e5-150">480</span></span>  <br/> |<span data-ttu-id="de0e5-151">08:00</span><span class="sxs-lookup"><span data-stu-id="de0e5-151">08:00</span></span>  <br/> |
|<span data-ttu-id="de0e5-152">6</span><span class="sxs-lookup"><span data-stu-id="de0e5-152">6</span></span>  <br/> |<span data-ttu-id="de0e5-153">960</span><span class="sxs-lookup"><span data-stu-id="de0e5-153">960</span></span>  <br/> |<span data-ttu-id="de0e5-154">16:00</span><span class="sxs-lookup"><span data-stu-id="de0e5-154">16:00</span></span>  <br/> |
|<span data-ttu-id="de0e5-155">7</span><span class="sxs-lookup"><span data-stu-id="de0e5-155">7</span></span>  <br/> |<span data-ttu-id="de0e5-156">1920</span><span class="sxs-lookup"><span data-stu-id="de0e5-156">1920</span></span>  <br/> |<span data-ttu-id="de0e5-157">32:00- **StatusFrequency**默认值为 30 超过，未发送的重试</span><span class="sxs-lookup"><span data-stu-id="de0e5-157">32:00 - **StatusFrequency** default value of 30 exceeded, retry not sent</span></span>  <br/> |
   
<span data-ttu-id="de0e5-158">如果客户端未收到通知消息从服务器的一段时间超过两次**StatusFrequency**指定的时间，客户端应采取的操作，如重新创建订阅。</span><span class="sxs-lookup"><span data-stu-id="de0e5-158">If the client does not receive notification messages from the server for a period of time that exceeds twice the time specified by **StatusFrequency**, the client should take an action such as recreating the subscription.</span></span> 
  
<span data-ttu-id="de0e5-159">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="de0e5-159">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de0e5-160">元素信息</span><span class="sxs-lookup"><span data-stu-id="de0e5-160">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de0e5-161">命名空间</span><span class="sxs-lookup"><span data-stu-id="de0e5-161">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de0e5-162">架构名称</span><span class="sxs-lookup"><span data-stu-id="de0e5-162">Schema name</span></span>  <br/> |<span data-ttu-id="de0e5-163">类型架构</span><span class="sxs-lookup"><span data-stu-id="de0e5-163">Types schema</span></span>  <br/> |
|<span data-ttu-id="de0e5-164">验证文件</span><span class="sxs-lookup"><span data-stu-id="de0e5-164">Validation file</span></span>  <br/> |<span data-ttu-id="de0e5-165">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de0e5-165">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de0e5-166">可以为空</span><span class="sxs-lookup"><span data-stu-id="de0e5-166">Can be empty</span></span>  <br/> |<span data-ttu-id="de0e5-167">False</span><span class="sxs-lookup"><span data-stu-id="de0e5-167">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de0e5-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de0e5-168">See also</span></span>



[<span data-ttu-id="de0e5-169">订阅操作</span><span class="sxs-lookup"><span data-stu-id="de0e5-169">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="de0e5-170">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="de0e5-170">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="de0e5-171">取消操作</span><span class="sxs-lookup"><span data-stu-id="de0e5-171">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="de0e5-172">水印</span><span class="sxs-lookup"><span data-stu-id="de0e5-172">Watermark</span></span>](watermark.md)

