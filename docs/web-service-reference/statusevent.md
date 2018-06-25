---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: StatusEvent 元素均表示没有新的活动发生的邮箱中的通知。
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827592"
---
# <a name="statusevent"></a><span data-ttu-id="b50f2-103">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="b50f2-103">StatusEvent</span></span>

<span data-ttu-id="b50f2-104">**StatusEvent**元素均表示没有新的活动发生的邮箱中的通知。</span><span class="sxs-lookup"><span data-stu-id="b50f2-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="b50f2-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="b50f2-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b50f2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b50f2-106">Attributes and elements</span></span>

<span data-ttu-id="b50f2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b50f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b50f2-108">属性</span><span class="sxs-lookup"><span data-stu-id="b50f2-108">Attributes</span></span>

<span data-ttu-id="b50f2-109">无。</span><span class="sxs-lookup"><span data-stu-id="b50f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b50f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b50f2-110">Child elements</span></span>

|<span data-ttu-id="b50f2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b50f2-111">**Element**</span></span>|<span data-ttu-id="b50f2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b50f2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b50f2-113">水印</span><span class="sxs-lookup"><span data-stu-id="b50f2-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="b50f2-114">表示订阅的最后一个有效水印。</span><span class="sxs-lookup"><span data-stu-id="b50f2-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b50f2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b50f2-115">Parent elements</span></span>

|<span data-ttu-id="b50f2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b50f2-116">**Element**</span></span>|<span data-ttu-id="b50f2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b50f2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b50f2-118">通知</span><span class="sxs-lookup"><span data-stu-id="b50f2-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b50f2-119">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="b50f2-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b50f2-120">注解</span><span class="sxs-lookup"><span data-stu-id="b50f2-120">Remarks</span></span>

<span data-ttu-id="b50f2-121">**StatusEvent**元素返回在通知中的以下原因之一：</span><span class="sxs-lookup"><span data-stu-id="b50f2-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="b50f2-122">提取客户端发出 GetEvents 请求上订阅处于不活动状态。</span><span class="sxs-lookup"><span data-stu-id="b50f2-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="b50f2-123">已达到[StatusFrequency](statusfrequency.md)时，推送客户端在队列中具有没有事件。</span><span class="sxs-lookup"><span data-stu-id="b50f2-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="b50f2-124">客户端应用程序中其他事件类型水印相同的方式使用**StatusEvent**[水印](watermark.md)。</span><span class="sxs-lookup"><span data-stu-id="b50f2-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="b50f2-125">但是， **StatusEvent**的水印不是用于其他事件水印相同。</span><span class="sxs-lookup"><span data-stu-id="b50f2-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="b50f2-126">例如，订阅已事件水印 1，2，3 和这些事件已成功指出在通知中。</span><span class="sxs-lookup"><span data-stu-id="b50f2-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="b50f2-127">停止活动一段时间，发生此事件，并发送一个**GetEvents**请求。</span><span class="sxs-lookup"><span data-stu-id="b50f2-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="b50f2-128">客户端访问服务器 (CAS) 返回状态事件，并包括最后一个水印，3，为[PreviousWatermark](previouswatermark.md)和当前[水印](watermark.md)。</span><span class="sxs-lookup"><span data-stu-id="b50f2-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="b50f2-129">水印将保持不变在所有情况下。</span><span class="sxs-lookup"><span data-stu-id="b50f2-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="b50f2-130">30 天维护事件项。</span><span class="sxs-lookup"><span data-stu-id="b50f2-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="b50f2-131">若要维护的活动订阅，CAS 定期更新订阅队列的水印。</span><span class="sxs-lookup"><span data-stu-id="b50f2-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="b50f2-132">更新的水印发送到客户端，以维护的活动订阅。</span><span class="sxs-lookup"><span data-stu-id="b50f2-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="b50f2-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b50f2-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b50f2-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="b50f2-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b50f2-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="b50f2-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b50f2-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="b50f2-136">Schema name</span></span>  <br/> |<span data-ttu-id="b50f2-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="b50f2-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="b50f2-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="b50f2-138">Validation file</span></span>  <br/> |<span data-ttu-id="b50f2-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b50f2-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b50f2-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="b50f2-140">Can be empty</span></span>  <br/> |<span data-ttu-id="b50f2-141">False</span><span class="sxs-lookup"><span data-stu-id="b50f2-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b50f2-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b50f2-142">See also</span></span>



[<span data-ttu-id="b50f2-143">订阅操作</span><span class="sxs-lookup"><span data-stu-id="b50f2-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b50f2-144">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="b50f2-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b50f2-145">取消操作</span><span class="sxs-lookup"><span data-stu-id="b50f2-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

