---
title: EventTypes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventTypes
api_type:
- schema
ms.assetid: 29ded9e5-f191-4aa3-bc3e-500de2fc8818
description: EventTypes 元素包含用于创建订阅事件通知类型的集合。
ms.openlocfilehash: f4c622376f6b607ed390511d7bb5f0f723889420
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754164"
---
# <a name="eventtypes"></a><span data-ttu-id="a2399-103">EventTypes</span><span class="sxs-lookup"><span data-stu-id="a2399-103">EventTypes</span></span>

<span data-ttu-id="a2399-104">**EventTypes**元素包含用于创建订阅事件通知类型的集合。</span><span class="sxs-lookup"><span data-stu-id="a2399-104">The **EventTypes** element contains a collection of event notification types that are used to create a subscription.</span></span> 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 <span data-ttu-id="a2399-105">**NonEmptyArrayOfNotificationEventTypesType**</span><span class="sxs-lookup"><span data-stu-id="a2399-105">**NonEmptyArrayOfNotificationEventTypesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a2399-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a2399-106">Attributes and elements</span></span>

<span data-ttu-id="a2399-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a2399-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a2399-108">属性</span><span class="sxs-lookup"><span data-stu-id="a2399-108">Attributes</span></span>

<span data-ttu-id="a2399-109">无。</span><span class="sxs-lookup"><span data-stu-id="a2399-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a2399-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a2399-110">Child elements</span></span>

|<span data-ttu-id="a2399-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2399-111">**Element**</span></span>|<span data-ttu-id="a2399-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2399-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2399-113">EventType</span><span class="sxs-lookup"><span data-stu-id="a2399-113">EventType</span></span>](eventtype.md) <br/> |<span data-ttu-id="a2399-114">表示用于创建订阅请求的事件通知类型。</span><span class="sxs-lookup"><span data-stu-id="a2399-114">Represents a requested event notification type that is used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a2399-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a2399-115">Parent elements</span></span>

|<span data-ttu-id="a2399-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a2399-116">**Element**</span></span>|<span data-ttu-id="a2399-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a2399-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a2399-118">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a2399-118">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="a2399-119">代表对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="a2399-119">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="a2399-120">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a2399-120">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="a2399-121">代表对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="a2399-121">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="a2399-122">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a2399-122">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="a2399-123">代表对流式处理的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="a2399-123">Represents a subscription to a streaming event notification subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a2399-124">文本值</span><span class="sxs-lookup"><span data-stu-id="a2399-124">Text value</span></span>

<span data-ttu-id="a2399-125">无。</span><span class="sxs-lookup"><span data-stu-id="a2399-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2399-126">备注</span><span class="sxs-lookup"><span data-stu-id="a2399-126">Remarks</span></span>

<span data-ttu-id="a2399-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a2399-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a2399-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="a2399-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a2399-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="a2399-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a2399-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="a2399-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a2399-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="a2399-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a2399-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="a2399-132">Validation File</span></span>  <br/> |<span data-ttu-id="a2399-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a2399-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a2399-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="a2399-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a2399-135">False</span><span class="sxs-lookup"><span data-stu-id="a2399-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2399-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a2399-136">See also</span></span>



[<span data-ttu-id="a2399-137">订阅操作</span><span class="sxs-lookup"><span data-stu-id="a2399-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="a2399-138">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="a2399-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="a2399-139">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="a2399-139">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="a2399-140">取消操作</span><span class="sxs-lookup"><span data-stu-id="a2399-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)

