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
description: Subscribe 元素包含用于创建订阅的属性。
ms.openlocfilehash: 9f23f566f9105c655b289ed9b434c5e7b917207f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827618"
---
# <a name="subscribe"></a><span data-ttu-id="a23f7-103">订阅</span><span class="sxs-lookup"><span data-stu-id="a23f7-103">Subscribe</span></span>

<span data-ttu-id="a23f7-104">**Subscribe**元素包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="a23f7-104">The **Subscribe** element contains the properties used to create subscriptions.</span></span> 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 <span data-ttu-id="a23f7-105">**SubscribeType**</span><span class="sxs-lookup"><span data-stu-id="a23f7-105">**SubscribeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a23f7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a23f7-106">Attributes and elements</span></span>

<span data-ttu-id="a23f7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a23f7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a23f7-108">属性</span><span class="sxs-lookup"><span data-stu-id="a23f7-108">Attributes</span></span>

<span data-ttu-id="a23f7-109">无。</span><span class="sxs-lookup"><span data-stu-id="a23f7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a23f7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a23f7-110">Child elements</span></span>

|<span data-ttu-id="a23f7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a23f7-111">**Element**</span></span>|<span data-ttu-id="a23f7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a23f7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a23f7-113">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a23f7-113">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="a23f7-114">代表对基于请求的事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="a23f7-114">Represents a subscription to a pull-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="a23f7-115">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a23f7-115">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="a23f7-116">代表对基于推送的事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="a23f7-116">Represents a subscription to a push-based event notification.</span></span>  <br/> |
|[<span data-ttu-id="a23f7-117">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="a23f7-117">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md) <br/> |<span data-ttu-id="a23f7-118">代表对流式处理的事件通知的订阅。</span><span class="sxs-lookup"><span data-stu-id="a23f7-118">Represents a subscription to a streaming event notification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a23f7-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a23f7-119">Parent elements</span></span>

<span data-ttu-id="a23f7-120">无。</span><span class="sxs-lookup"><span data-stu-id="a23f7-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a23f7-121">备注</span><span class="sxs-lookup"><span data-stu-id="a23f7-121">Remarks</span></span>

<span data-ttu-id="a23f7-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a23f7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a23f7-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a23f7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a23f7-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a23f7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a23f7-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a23f7-125">Schema name</span></span>  <br/> |<span data-ttu-id="a23f7-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="a23f7-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a23f7-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a23f7-127">Validation file</span></span>  <br/> |<span data-ttu-id="a23f7-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a23f7-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a23f7-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a23f7-129">Can be empty</span></span>  <br/> |<span data-ttu-id="a23f7-130">False</span><span class="sxs-lookup"><span data-stu-id="a23f7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a23f7-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a23f7-131">See also</span></span>



[<span data-ttu-id="a23f7-132">订阅操作</span><span class="sxs-lookup"><span data-stu-id="a23f7-132">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="a23f7-133">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="a23f7-133">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="a23f7-134">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="a23f7-134">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="a23f7-135">取消操作</span><span class="sxs-lookup"><span data-stu-id="a23f7-135">Unsubscribe operation</span></span>](unsubscribe-operation.md)

