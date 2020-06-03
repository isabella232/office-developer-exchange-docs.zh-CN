---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: PullSubscriptionRequest 元素表示对基于请求的事件通知订阅的订阅。
ms.openlocfilehash: fb9712c9e1481678c2821ee344052783d5c25bf9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468864"
---
# <a name="pullsubscriptionrequest"></a><span data-ttu-id="28a1e-103">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="28a1e-103">PullSubscriptionRequest</span></span>

<span data-ttu-id="28a1e-104">**PullSubscriptionRequest**元素表示对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="28a1e-104">The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription.</span></span> 
  
[<span data-ttu-id="28a1e-105">订阅</span><span class="sxs-lookup"><span data-stu-id="28a1e-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="28a1e-106">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="28a1e-106">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 <span data-ttu-id="28a1e-107">**PullSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="28a1e-107">**PullSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28a1e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="28a1e-108">Attributes and elements</span></span>

<span data-ttu-id="28a1e-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="28a1e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28a1e-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="28a1e-110">Attributes</span></span>

|<span data-ttu-id="28a1e-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="28a1e-111">**Attribute**</span></span>|<span data-ttu-id="28a1e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="28a1e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28a1e-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="28a1e-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="28a1e-114">指示是否订阅所有可用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="28a1e-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="28a1e-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="28a1e-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28a1e-116">子元素</span><span class="sxs-lookup"><span data-stu-id="28a1e-116">Child elements</span></span>

|<span data-ttu-id="28a1e-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="28a1e-117">**Element**</span></span>|<span data-ttu-id="28a1e-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="28a1e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a1e-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="28a1e-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="28a1e-120">包含用于标识要监视其事件通知的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="28a1e-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="28a1e-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="28a1e-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="28a1e-122">包含用于创建订阅的事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="28a1e-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="28a1e-123">Watermark</span><span class="sxs-lookup"><span data-stu-id="28a1e-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="28a1e-124">表示邮箱事件表中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="28a1e-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="28a1e-125">这用于创建在由水印表示的事件处启动的订阅。</span><span class="sxs-lookup"><span data-stu-id="28a1e-125">This is used to create a subscription that starts at an event that is represented by the watermark.</span></span> <span data-ttu-id="28a1e-126">如果找不到订阅请求中的水印，将向客户端返回错误响应。</span><span class="sxs-lookup"><span data-stu-id="28a1e-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="28a1e-127">如果水印的时间超过30天或者水印从未出现在邮箱中，则可能会出现此错误。</span><span class="sxs-lookup"><span data-stu-id="28a1e-127">This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="28a1e-128">Timeout</span><span class="sxs-lookup"><span data-stu-id="28a1e-128">Timeout</span></span>](timeout.md) <br/> |<span data-ttu-id="28a1e-129">表示订阅可以保持空闲状态的持续时间（以分钟为单位），而无需客户端的 GetEvents 请求。</span><span class="sxs-lookup"><span data-stu-id="28a1e-129">Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28a1e-130">父元素</span><span class="sxs-lookup"><span data-stu-id="28a1e-130">Parent elements</span></span>

|<span data-ttu-id="28a1e-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="28a1e-131">**Element**</span></span>|<span data-ttu-id="28a1e-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="28a1e-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28a1e-133">订阅</span><span class="sxs-lookup"><span data-stu-id="28a1e-133">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="28a1e-134">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="28a1e-134">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="28a1e-135">文本值</span><span class="sxs-lookup"><span data-stu-id="28a1e-135">Text value</span></span>

<span data-ttu-id="28a1e-136">无。</span><span class="sxs-lookup"><span data-stu-id="28a1e-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28a1e-137">说明</span><span class="sxs-lookup"><span data-stu-id="28a1e-137">Remarks</span></span>

<span data-ttu-id="28a1e-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="28a1e-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28a1e-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="28a1e-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28a1e-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="28a1e-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="28a1e-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="28a1e-141">Schema name</span></span>  <br/> |<span data-ttu-id="28a1e-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="28a1e-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="28a1e-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="28a1e-143">Validation file</span></span>  <br/> |<span data-ttu-id="28a1e-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="28a1e-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="28a1e-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="28a1e-145">Can be empty</span></span>  <br/> |<span data-ttu-id="28a1e-146">False</span><span class="sxs-lookup"><span data-stu-id="28a1e-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28a1e-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28a1e-147">See also</span></span>



[<span data-ttu-id="28a1e-148">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="28a1e-148">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="28a1e-149">订阅操作</span><span class="sxs-lookup"><span data-stu-id="28a1e-149">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="28a1e-150">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="28a1e-150">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="28a1e-151">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="28a1e-151">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="28a1e-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="28a1e-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

