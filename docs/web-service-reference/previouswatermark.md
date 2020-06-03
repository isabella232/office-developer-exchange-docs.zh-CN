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
description: PreviousWatermark 元素表示成功传递给订阅客户端的最新事件的水印。
ms.openlocfilehash: 1b26a645a5ec6dbbd2874b118f968866aadc32af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461651"
---
# <a name="previouswatermark"></a><span data-ttu-id="01af0-103">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="01af0-103">PreviousWatermark</span></span>

<span data-ttu-id="01af0-104">**PreviousWatermark**元素表示成功传递给订阅客户端的最新事件的水印。</span><span class="sxs-lookup"><span data-stu-id="01af0-104">The **PreviousWatermark** element represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span> 
  
```xml
<PreviousWatermark/>
```

 <span data-ttu-id="01af0-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="01af0-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01af0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01af0-106">Attributes and elements</span></span>

<span data-ttu-id="01af0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01af0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01af0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="01af0-108">Attributes</span></span>

<span data-ttu-id="01af0-109">无。</span><span class="sxs-lookup"><span data-stu-id="01af0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01af0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="01af0-110">Child elements</span></span>

<span data-ttu-id="01af0-111">无。</span><span class="sxs-lookup"><span data-stu-id="01af0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01af0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="01af0-112">Parent elements</span></span>

|<span data-ttu-id="01af0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="01af0-113">**Element**</span></span>|<span data-ttu-id="01af0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="01af0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01af0-115">通知</span><span class="sxs-lookup"><span data-stu-id="01af0-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="01af0-116">包含有关订阅以及上次通知之后发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="01af0-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01af0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="01af0-117">Text value</span></span>

<span data-ttu-id="01af0-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="01af0-118">A text value is required.</span></span> <span data-ttu-id="01af0-119">该文本值表示最新的水印。</span><span class="sxs-lookup"><span data-stu-id="01af0-119">The text value represents the latest watermark.</span></span> <span data-ttu-id="01af0-120">文本值不能为空字符串。</span><span class="sxs-lookup"><span data-stu-id="01af0-120">The text value cannot be an empty string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01af0-121">备注</span><span class="sxs-lookup"><span data-stu-id="01af0-121">Remarks</span></span>

<span data-ttu-id="01af0-122">**PreviousWatermark**属性对确定最后一个成功通知的客户端很有用。</span><span class="sxs-lookup"><span data-stu-id="01af0-122">The **PreviousWatermark** property is useful to the client in determining the last successful notification.</span></span> <span data-ttu-id="01af0-123">例如，如果订阅包含具有水印1、2和3的三个事件，并且下一个通知发送的**PreviousWatermark**值为3，则客户端可以将此值与接收到的最后一条通知的水位线值进行比较。</span><span class="sxs-lookup"><span data-stu-id="01af0-123">For example, if a subscription has three events with watermarks 1, 2, and 3, and the next notification is sent with a **PreviousWatermark** value of 3, the client can compare this value to the Watermark value of the last notification received.</span></span> <span data-ttu-id="01af0-124">这使客户端能够确保事件的连续性。</span><span class="sxs-lookup"><span data-stu-id="01af0-124">This enables the client to ensure the continuity of events.</span></span> 
  
<span data-ttu-id="01af0-125">对于推送客户端，将**PreviousWatermark**与本地的客户端最后一个已知的水印进行比较。</span><span class="sxs-lookup"><span data-stu-id="01af0-125">For push clients, the **PreviousWatermark** is compared to the local, client-side last known watermark.</span></span> <span data-ttu-id="01af0-126">如果值不同，客户端将错过事件通知，应使用最新的本地水印重新建立订阅。</span><span class="sxs-lookup"><span data-stu-id="01af0-126">If the values are different, the client has missed an event notification and should reestablish a subscription by using the latest local watermark.</span></span> <span data-ttu-id="01af0-127">例如，如果推送客户端接收到具有水印1、2和3的订阅的三个事件，并且下一个通知的**PreviousWatermark**值为5，则客户端已错过至少一次通知，应创建一个新的订阅，并将3作为水印进行传递。</span><span class="sxs-lookup"><span data-stu-id="01af0-127">For example, if a push client receives three events for a subscription with watermarks 1, 2, and 3, and the next notification comes with a **PreviousWatermark** value of 5, the client has missed at least one notification and should create a new subscription, passing a 3 as the watermark.</span></span> 
  
<span data-ttu-id="01af0-128">对于 pull 客户端， **PreviousWatermark**的值将与 GetEvents 调用中的客户端所包含的[水印](watermark.md)相同。</span><span class="sxs-lookup"><span data-stu-id="01af0-128">In the case of a pull client, the value of **PreviousWatermark** will be the same as the [Watermark](watermark.md) included by the client in the GetEvents call.</span></span> 
  
<span data-ttu-id="01af0-129">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="01af0-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01af0-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="01af0-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01af0-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="01af0-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01af0-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="01af0-132">Schema Name</span></span>  <br/> |<span data-ttu-id="01af0-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="01af0-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="01af0-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="01af0-134">Validation File</span></span>  <br/> |<span data-ttu-id="01af0-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01af0-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01af0-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="01af0-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="01af0-137">False</span><span class="sxs-lookup"><span data-stu-id="01af0-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01af0-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01af0-138">See also</span></span>



[<span data-ttu-id="01af0-139">订阅操作</span><span class="sxs-lookup"><span data-stu-id="01af0-139">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="01af0-140">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="01af0-140">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="01af0-141">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="01af0-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

