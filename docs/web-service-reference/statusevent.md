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
description: StatusEvent 元素表示在邮箱中未发生任何新活动的通知。
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468255"
---
# <a name="statusevent"></a><span data-ttu-id="46ac5-103">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="46ac5-103">StatusEvent</span></span>

<span data-ttu-id="46ac5-104">**StatusEvent**元素表示在邮箱中未发生任何新活动的通知。</span><span class="sxs-lookup"><span data-stu-id="46ac5-104">The **StatusEvent** element represents a notification that no new activity has occurred in the mailbox.</span></span> 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 <span data-ttu-id="46ac5-105">**BaseNotificationEventType**</span><span class="sxs-lookup"><span data-stu-id="46ac5-105">**BaseNotificationEventType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46ac5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="46ac5-106">Attributes and elements</span></span>

<span data-ttu-id="46ac5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="46ac5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46ac5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="46ac5-108">Attributes</span></span>

<span data-ttu-id="46ac5-109">无。</span><span class="sxs-lookup"><span data-stu-id="46ac5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46ac5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="46ac5-110">Child elements</span></span>

|<span data-ttu-id="46ac5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="46ac5-111">**Element**</span></span>|<span data-ttu-id="46ac5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="46ac5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46ac5-113">Watermark</span><span class="sxs-lookup"><span data-stu-id="46ac5-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="46ac5-114">表示订阅的最后一个有效的水印。</span><span class="sxs-lookup"><span data-stu-id="46ac5-114">Represents the last valid watermark for a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46ac5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="46ac5-115">Parent elements</span></span>

|<span data-ttu-id="46ac5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="46ac5-116">**Element**</span></span>|<span data-ttu-id="46ac5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="46ac5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46ac5-118">通知</span><span class="sxs-lookup"><span data-stu-id="46ac5-118">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="46ac5-119">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="46ac5-119">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46ac5-120">备注</span><span class="sxs-lookup"><span data-stu-id="46ac5-120">Remarks</span></span>

<span data-ttu-id="46ac5-121">由于以下原因之一，在通知中返回**StatusEvent**元素：</span><span class="sxs-lookup"><span data-stu-id="46ac5-121">The **StatusEvent** element is returned in a notification for one of the following reasons:</span></span> 
  
- <span data-ttu-id="46ac5-122">"拉" 客户端在没有活动的订阅上发出 GetEvents 请求。</span><span class="sxs-lookup"><span data-stu-id="46ac5-122">A pull client issues a GetEvents request on a subscription that has no activity.</span></span>
    
- <span data-ttu-id="46ac5-123">当已到达[StatusFrequency](statusfrequency.md)时，推送客户端在队列中没有事件。</span><span class="sxs-lookup"><span data-stu-id="46ac5-123">A push client has no events in the queue when the [StatusFrequency](statusfrequency.md) has been reached.</span></span> 
    
<span data-ttu-id="46ac5-124">客户端应用程序使用**StatusEvent**[水印](watermark.md)的方式与其他事件类型的水印的使用方式相同。</span><span class="sxs-lookup"><span data-stu-id="46ac5-124">The **StatusEvent**[Watermark](watermark.md) is used by a client application in the same manner as the other event type watermarks.</span></span> <span data-ttu-id="46ac5-125">但是， **StatusEvent**的水印与用于其他事件的水印不同。</span><span class="sxs-lookup"><span data-stu-id="46ac5-125">However, the watermark for the **StatusEvent** is not the same as the watermarks used for other events.</span></span> <span data-ttu-id="46ac5-126">例如，订阅具有水印1、2和3的事件，并且这些事件已在通知中成功传递。</span><span class="sxs-lookup"><span data-stu-id="46ac5-126">For example, a subscription has events with watermarks 1, 2, and 3 and those events have been successfully communicated in a notification.</span></span> <span data-ttu-id="46ac5-127">发生不活动的一段时间，并发送**GetEvents**请求。</span><span class="sxs-lookup"><span data-stu-id="46ac5-127">A period of inactivity occurs and a **GetEvents** request is sent.</span></span> <span data-ttu-id="46ac5-128">客户端访问服务器（CAS）返回一个状态事件，并包括最后一个水印3，作为[PreviousWatermark](previouswatermark.md)和当前的[水印](watermark.md)。</span><span class="sxs-lookup"><span data-stu-id="46ac5-128">The Client Access server (CAS) returns a status event and includes the last watermark, 3, as both the [PreviousWatermark](previouswatermark.md) and the current [Watermark](watermark.md).</span></span>
  
<span data-ttu-id="46ac5-129">在所有情况下，水印不会保持相同。</span><span class="sxs-lookup"><span data-stu-id="46ac5-129">The watermark will not remain the same in all cases.</span></span> <span data-ttu-id="46ac5-130">事件条目的维护时间为30天。</span><span class="sxs-lookup"><span data-stu-id="46ac5-130">Event entries are maintained for 30 days.</span></span> <span data-ttu-id="46ac5-131">为了维护活动订阅，CAS 会定期更新订阅队列的水印。</span><span class="sxs-lookup"><span data-stu-id="46ac5-131">To maintain an active subscription, the CAS periodically updates the watermarks for subscription queues.</span></span> <span data-ttu-id="46ac5-132">更新的水印将发送到客户端，以维护活动订阅。</span><span class="sxs-lookup"><span data-stu-id="46ac5-132">The updated watermarks are sent to clients to maintain an active subscription.</span></span>
  
<span data-ttu-id="46ac5-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="46ac5-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46ac5-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="46ac5-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46ac5-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="46ac5-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46ac5-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="46ac5-136">Schema name</span></span>  <br/> |<span data-ttu-id="46ac5-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="46ac5-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="46ac5-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="46ac5-138">Validation file</span></span>  <br/> |<span data-ttu-id="46ac5-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46ac5-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46ac5-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="46ac5-140">Can be empty</span></span>  <br/> |<span data-ttu-id="46ac5-141">False</span><span class="sxs-lookup"><span data-stu-id="46ac5-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46ac5-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46ac5-142">See also</span></span>



[<span data-ttu-id="46ac5-143">订阅操作</span><span class="sxs-lookup"><span data-stu-id="46ac5-143">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="46ac5-144">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="46ac5-144">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="46ac5-145">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="46ac5-145">Unsubscribe operation</span></span>](unsubscribe-operation.md)

