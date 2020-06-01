---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: PushSubscriptionRequest 元素表示对基于推送的事件通知订阅的订阅。
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465511"
---
# <a name="pushsubscriptionrequest"></a><span data-ttu-id="ec3a9-103">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ec3a9-103">PushSubscriptionRequest</span></span>

<span data-ttu-id="ec3a9-104">**PushSubscriptionRequest**元素表示对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-104">The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription.</span></span> 
  
[<span data-ttu-id="ec3a9-105">订阅</span><span class="sxs-lookup"><span data-stu-id="ec3a9-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="ec3a9-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="ec3a9-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 <span data-ttu-id="ec3a9-107">**PushSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-107">**PushSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec3a9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec3a9-108">Attributes and elements</span></span>

<span data-ttu-id="ec3a9-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec3a9-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="ec3a9-110">Attributes</span></span>

|<span data-ttu-id="ec3a9-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-111">**Attribute**</span></span>|<span data-ttu-id="ec3a9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec3a9-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="ec3a9-114">指示是否订阅所有可用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="ec3a9-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ec3a9-116">子元素</span><span class="sxs-lookup"><span data-stu-id="ec3a9-116">Child elements</span></span>

|<span data-ttu-id="ec3a9-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-117">**Element**</span></span>|<span data-ttu-id="ec3a9-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec3a9-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ec3a9-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="ec3a9-120">包含用于标识要监视其事件通知的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="ec3a9-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="ec3a9-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="ec3a9-122">包含用于创建订阅的事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="ec3a9-123">Watermark</span><span class="sxs-lookup"><span data-stu-id="ec3a9-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="ec3a9-124">表示邮箱事件表中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="ec3a9-125">这用于创建从水印所代表的事件开始的订阅。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-125">This is used to create a subscription starting at an event represented by the watermark.</span></span> <span data-ttu-id="ec3a9-126">如果找不到订阅请求中的水印，将向客户端返回错误响应。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="ec3a9-127">如果水印的时间超过30天或者水印从未出现在邮箱中，则可能会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-127">This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ec3a9-128">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="ec3a9-128">StatusFrequency</span></span>](statusfrequency.md) <br/> |<span data-ttu-id="ec3a9-129">表示在没有事件发生时，通知邮件将发送到客户端的频率（以分钟为单位）。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-129">Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.</span></span>  <br/> |
|[<span data-ttu-id="ec3a9-130">Url</span><span class="sxs-lookup"><span data-stu-id="ec3a9-130">Url </span></span>](url-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ec3a9-131">表示用于推送通知的客户端 Web 服务的位置。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-131">Represents the location of the client Web service for push notifications.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec3a9-132">父元素</span><span class="sxs-lookup"><span data-stu-id="ec3a9-132">Parent elements</span></span>

|<span data-ttu-id="ec3a9-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-133">**Element**</span></span>|<span data-ttu-id="ec3a9-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec3a9-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec3a9-135">订阅</span><span class="sxs-lookup"><span data-stu-id="ec3a9-135">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="ec3a9-136">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-136">Contains the properties used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec3a9-137">文本值</span><span class="sxs-lookup"><span data-stu-id="ec3a9-137">Text value</span></span>

<span data-ttu-id="ec3a9-138">无。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec3a9-139">说明</span><span class="sxs-lookup"><span data-stu-id="ec3a9-139">Remarks</span></span>

<span data-ttu-id="ec3a9-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec3a9-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec3a9-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec3a9-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec3a9-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec3a9-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec3a9-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec3a9-143">Schema name</span></span>  <br/> |<span data-ttu-id="ec3a9-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="ec3a9-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec3a9-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec3a9-145">Validation file</span></span>  <br/> |<span data-ttu-id="ec3a9-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec3a9-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec3a9-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec3a9-147">Can be empty</span></span>  <br/> |<span data-ttu-id="ec3a9-148">False</span><span class="sxs-lookup"><span data-stu-id="ec3a9-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec3a9-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec3a9-149">See also</span></span>



[<span data-ttu-id="ec3a9-150">订阅操作</span><span class="sxs-lookup"><span data-stu-id="ec3a9-150">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ec3a9-151">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="ec3a9-151">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ec3a9-152">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="ec3a9-152">Unsubscribe operation</span></span>](unsubscribe-operation.md)

