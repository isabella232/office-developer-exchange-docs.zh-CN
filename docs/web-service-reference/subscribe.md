---
title: 订阅
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: 6c2ee57d-e216-4a94-92db-faa3cb0e244a
description: 订阅元素包含用于创建订阅的属性。
ms.openlocfilehash: f60e67654fb6af76e8081036a3463f5be401862d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530956"
---
# <a name="subscribe"></a><span data-ttu-id="eb4c3-103">订阅</span><span class="sxs-lookup"><span data-stu-id="eb4c3-103">Subscribe</span></span>

<span data-ttu-id="eb4c3-104">**订阅**元素包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="eb4c3-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="eb4c3-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb4c3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb4c3-106">Attributes and elements</span></span>

<span data-ttu-id="eb4c3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb4c3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="eb4c3-108">Attributes</span></span>

<span data-ttu-id="eb4c3-109">无。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb4c3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eb4c3-110">Child elements</span></span>

|<span data-ttu-id="eb4c3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="eb4c3-111">**Element**</span></span>|<span data-ttu-id="eb4c3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="eb4c3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb4c3-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="eb4c3-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="eb4c3-114">表示对基于请求的事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="eb4c3-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="eb4c3-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="eb4c3-116">表示对基于推送的事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="eb4c3-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="eb4c3-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="eb4c3-118">表示对流式事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb4c3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="eb4c3-119">Parent elements</span></span>

<span data-ttu-id="eb4c3-120">无。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb4c3-121">说明</span><span class="sxs-lookup"><span data-stu-id="eb4c3-121">Remarks</span></span>

<span data-ttu-id="eb4c3-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb4c3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb4c3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb4c3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb4c3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb4c3-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb4c3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb4c3-125">Schema name</span></span>  <br/> |<span data-ttu-id="eb4c3-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="eb4c3-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb4c3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb4c3-127">Validation file</span></span>  <br/> |<span data-ttu-id="eb4c3-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb4c3-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb4c3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb4c3-129">Can be empty</span></span>  <br/> |<span data-ttu-id="eb4c3-130">False</span><span class="sxs-lookup"><span data-stu-id="eb4c3-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb4c3-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb4c3-131">See also</span></span>



[<span data-ttu-id="eb4c3-132">订阅操作</span><span class="sxs-lookup"><span data-stu-id="eb4c3-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="eb4c3-133">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="eb4c3-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="eb4c3-134">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="eb4c3-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="eb4c3-135">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="eb4c3-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

