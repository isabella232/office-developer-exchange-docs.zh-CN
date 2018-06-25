---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: PreviousWatermark 元素均表示水印成功传到用于订阅的客户端的最新事件。
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826886"
---
# <a name="previouswatermark"></a><span data-ttu-id="db475-103">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="db475-103">PreviousWatermark</span></span>

<span data-ttu-id="db475-104">**PreviousWatermark**元素均表示水印成功传到用于订阅的客户端的最新事件。</span><span class="sxs-lookup"><span data-stu-id="db475-104">The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span> 
  
```xml
<PreviousWatermark/>
```

 <span data-ttu-id="db475-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="db475-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db475-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db475-106">Attributes and elements</span></span>

<span data-ttu-id="db475-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db475-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db475-108">属性</span><span class="sxs-lookup"><span data-stu-id="db475-108">Attributes</span></span>

<span data-ttu-id="db475-109">无。</span><span class="sxs-lookup"><span data-stu-id="db475-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db475-110">子元素</span><span class="sxs-lookup"><span data-stu-id="db475-110">Child elements</span></span>

<span data-ttu-id="db475-111">无。</span><span class="sxs-lookup"><span data-stu-id="db475-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="db475-112">父元素</span><span class="sxs-lookup"><span data-stu-id="db475-112">Parent elements</span></span>

|<span data-ttu-id="db475-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="db475-113">**Element**</span></span>|<span data-ttu-id="db475-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="db475-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db475-115">通知</span><span class="sxs-lookup"><span data-stu-id="db475-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="db475-116">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="db475-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="db475-117">文本值</span><span class="sxs-lookup"><span data-stu-id="db475-117">Text value</span></span>

<span data-ttu-id="db475-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="db475-118">A text value is required.</span></span> <span data-ttu-id="db475-119">文本值表示最新的水印。</span><span class="sxs-lookup"><span data-stu-id="db475-119">The text value represents the latest watermark.</span></span> <span data-ttu-id="db475-120">文本值不能为空字符串。</span><span class="sxs-lookup"><span data-stu-id="db475-120">The text value cannot be an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="db475-121">注解</span><span class="sxs-lookup"><span data-stu-id="db475-121">Remarks</span></span>

<span data-ttu-id="db475-122">**PreviousWatermark**属性可确定上次成功通知客户端。</span><span class="sxs-lookup"><span data-stu-id="db475-122">The **PreviousWatermark** property is useful to the client in determining the last successful notification.</span></span> <span data-ttu-id="db475-123">例如，如果订阅具有三个事件水印 1、 2 和 3，并将下一个通知发送**PreviousWatermark**值为 3，客户端可以进行比较此值为水印值接收的最后一个通知。</span><span class="sxs-lookup"><span data-stu-id="db475-123">For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received.</span></span> <span data-ttu-id="db475-124">这样，客户端以确保事件的连续性。</span><span class="sxs-lookup"><span data-stu-id="db475-124">This enables the client to ensure the continuity of events.</span></span> 
  
<span data-ttu-id="db475-125">对于推送客户端， **PreviousWatermark**将与本地、 客户端的最后一个已知水印进行比较。</span><span class="sxs-lookup"><span data-stu-id="db475-125">For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark.</span></span> <span data-ttu-id="db475-126">如果值不同，客户端错过了事件通知，以及如何应使用最新的本地水印重建订阅。</span><span class="sxs-lookup"><span data-stu-id="db475-126">If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark.</span></span> <span data-ttu-id="db475-127">例如，如果推送客户端接收水印 1、 2 和 3，与订阅的三个事件和下一个通知附带**PreviousWatermark**值 5，则客户端将错过了至少一个通知，应创建新的订阅，将作为水印传递 3。</span><span class="sxs-lookup"><span data-stu-id="db475-127">For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark.</span></span> 
  
<span data-ttu-id="db475-128">对于提取客户端的**PreviousWatermark**值将由客户端 GetEvents 呼叫中包含[水印](watermark.md)相同。</span><span class="sxs-lookup"><span data-stu-id="db475-128">In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call.</span></span> 
  
<span data-ttu-id="db475-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db475-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db475-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="db475-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db475-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="db475-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db475-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="db475-132">Schema Name</span></span>  <br/> |<span data-ttu-id="db475-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="db475-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="db475-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="db475-134">Validation File</span></span>  <br/> |<span data-ttu-id="db475-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db475-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db475-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="db475-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="db475-137">False</span><span class="sxs-lookup"><span data-stu-id="db475-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db475-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db475-138">See also</span></span>



[<span data-ttu-id="db475-139">订阅操作</span><span class="sxs-lookup"><span data-stu-id="db475-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="db475-140">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="db475-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="db475-141">取消操作</span><span class="sxs-lookup"><span data-stu-id="db475-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

