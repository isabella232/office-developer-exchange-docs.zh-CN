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
description: PushSubscriptionRequest 元素均表示对基于推送的事件通知订阅的订阅。
ms.openlocfilehash: 34717d37b8e5bb50c927e57088299fbcb18a2514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826929"
---
# <a name="pushsubscriptionrequest"></a><span data-ttu-id="b2d92-103">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="b2d92-103">PushSubscriptionRequest</span></span>

<span data-ttu-id="b2d92-104">**PushSubscriptionRequest**元素均表示对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="b2d92-104">The **PushSubscriptionRequest** element represents a subscription to a push-based event notification subscription.</span></span> 
  
[<span data-ttu-id="b2d92-105">订阅</span><span class="sxs-lookup"><span data-stu-id="b2d92-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="b2d92-106">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="b2d92-106">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 <span data-ttu-id="b2d92-107">**PushSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="b2d92-107">**PushSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2d92-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b2d92-108">Attributes and elements</span></span>

<span data-ttu-id="b2d92-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b2d92-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2d92-110">属性</span><span class="sxs-lookup"><span data-stu-id="b2d92-110">Attributes</span></span>

|<span data-ttu-id="b2d92-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="b2d92-111">**Attribute**</span></span>|<span data-ttu-id="b2d92-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2d92-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2d92-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="b2d92-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="b2d92-114">指示是否订阅所有可用文件夹。</span><span class="sxs-lookup"><span data-stu-id="b2d92-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="b2d92-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2d92-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b2d92-116">子元素</span><span class="sxs-lookup"><span data-stu-id="b2d92-116">Child elements</span></span>

|<span data-ttu-id="b2d92-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2d92-117">**Element**</span></span>|<span data-ttu-id="b2d92-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2d92-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2d92-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="b2d92-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="b2d92-120">包含用于标识要监视的事件通知文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="b2d92-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="b2d92-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="b2d92-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="b2d92-122">包含用于创建订阅事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="b2d92-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="b2d92-123">水印</span><span class="sxs-lookup"><span data-stu-id="b2d92-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="b2d92-124">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="b2d92-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="b2d92-125">这用于创建订阅开始由水印事件。</span><span class="sxs-lookup"><span data-stu-id="b2d92-125">This is used to create a subscription starting at an event represented by the watermark.</span></span> <span data-ttu-id="b2d92-126">如果找不到订阅请求从水印，向客户端将返回错误响应。</span><span class="sxs-lookup"><span data-stu-id="b2d92-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="b2d92-127">如果水印已超过 30 天或水印从未存在的邮箱中，可能会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="b2d92-127">This may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b2d92-128">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="b2d92-128">StatusFrequency</span></span>](statusfrequency.md) <br/> |<span data-ttu-id="b2d92-129">代表指定以分钟为单位，在的通知邮件将被发送到客户端时没有发生任何事件的频率。</span><span class="sxs-lookup"><span data-stu-id="b2d92-129">Represents the frequency, specified in minutes, at which notification messages will be sent to the client when no events have occurred.</span></span>  <br/> |
|[<span data-ttu-id="b2d92-130">Url</span><span class="sxs-lookup"><span data-stu-id="b2d92-130">Url </span></span>](url-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b2d92-131">表示客户端推送通知的 Web 服务的位置。</span><span class="sxs-lookup"><span data-stu-id="b2d92-131">Represents the location of the client Web service for push notifications.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2d92-132">父元素</span><span class="sxs-lookup"><span data-stu-id="b2d92-132">Parent elements</span></span>

|<span data-ttu-id="b2d92-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2d92-133">**Element**</span></span>|<span data-ttu-id="b2d92-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2d92-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2d92-135">订阅</span><span class="sxs-lookup"><span data-stu-id="b2d92-135">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="b2d92-136">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="b2d92-136">Contains the properties used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b2d92-137">文本值</span><span class="sxs-lookup"><span data-stu-id="b2d92-137">Text value</span></span>

<span data-ttu-id="b2d92-138">无。</span><span class="sxs-lookup"><span data-stu-id="b2d92-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2d92-139">备注</span><span class="sxs-lookup"><span data-stu-id="b2d92-139">Remarks</span></span>

<span data-ttu-id="b2d92-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b2d92-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2d92-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="b2d92-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2d92-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="b2d92-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2d92-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="b2d92-143">Schema name</span></span>  <br/> |<span data-ttu-id="b2d92-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="b2d92-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b2d92-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="b2d92-145">Validation file</span></span>  <br/> |<span data-ttu-id="b2d92-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2d92-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2d92-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="b2d92-147">Can be empty</span></span>  <br/> |<span data-ttu-id="b2d92-148">False</span><span class="sxs-lookup"><span data-stu-id="b2d92-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2d92-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2d92-149">See also</span></span>



[<span data-ttu-id="b2d92-150">订阅操作</span><span class="sxs-lookup"><span data-stu-id="b2d92-150">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b2d92-151">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="b2d92-151">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b2d92-152">取消操作</span><span class="sxs-lookup"><span data-stu-id="b2d92-152">Unsubscribe operation</span></span>](unsubscribe-operation.md)

