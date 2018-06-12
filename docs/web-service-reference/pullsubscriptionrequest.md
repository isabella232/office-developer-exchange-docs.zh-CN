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
description: PullSubscriptionRequest 元素均表示对基于请求的事件通知订阅的订阅。
ms.openlocfilehash: 5f757bf1f79f7e2a00fb886db50e6ea0eaed1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826932"
---
# <a name="pullsubscriptionrequest"></a><span data-ttu-id="2ebca-103">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="2ebca-103">PullSubscriptionRequest</span></span>

<span data-ttu-id="2ebca-104">**PullSubscriptionRequest**元素均表示对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="2ebca-104">The **PullSubscriptionRequest** element represents a subscription to a pull-based event notification subscription.</span></span> 
  
[<span data-ttu-id="2ebca-105">订阅</span><span class="sxs-lookup"><span data-stu-id="2ebca-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="2ebca-106">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="2ebca-106">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 <span data-ttu-id="2ebca-107">**PullSubscriptionRequestType**</span><span class="sxs-lookup"><span data-stu-id="2ebca-107">**PullSubscriptionRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ebca-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ebca-108">Attributes and elements</span></span>

<span data-ttu-id="2ebca-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ebca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ebca-110">属性</span><span class="sxs-lookup"><span data-stu-id="2ebca-110">Attributes</span></span>

|<span data-ttu-id="2ebca-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="2ebca-111">**Attribute**</span></span>|<span data-ttu-id="2ebca-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ebca-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ebca-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="2ebca-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="2ebca-114">指示是否订阅所有可用文件夹。</span><span class="sxs-lookup"><span data-stu-id="2ebca-114">Indicates whether to subscribe to all available folders.</span></span> <span data-ttu-id="2ebca-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="2ebca-115">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2ebca-116">子元素</span><span class="sxs-lookup"><span data-stu-id="2ebca-116">Child elements</span></span>

|<span data-ttu-id="2ebca-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ebca-117">**Element**</span></span>|<span data-ttu-id="2ebca-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ebca-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebca-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="2ebca-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="2ebca-120">包含用于标识要监视的事件通知文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="2ebca-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="2ebca-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="2ebca-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="2ebca-122">包含用于创建订阅事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="2ebca-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
|[<span data-ttu-id="2ebca-123">水印</span><span class="sxs-lookup"><span data-stu-id="2ebca-123">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="2ebca-124">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="2ebca-124">Represents an event bookmark in the mailbox events table.</span></span> <span data-ttu-id="2ebca-125">这用于在由水印事件创建启动订阅。</span><span class="sxs-lookup"><span data-stu-id="2ebca-125">This is used to create a subscription that starts at an event that is represented by the watermark.</span></span> <span data-ttu-id="2ebca-126">如果找不到订阅请求从水印，向客户端将返回错误响应。</span><span class="sxs-lookup"><span data-stu-id="2ebca-126">If the watermark from a Subscribe request is not found, an error response will be returned to the client.</span></span> <span data-ttu-id="2ebca-127">如果水印已超过 30 天或水印从未邮箱中存在，则可能发生此错误。</span><span class="sxs-lookup"><span data-stu-id="2ebca-127">This error may occur if the watermark is older than 30 days or if the watermark was never present in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2ebca-128">Timeout</span><span class="sxs-lookup"><span data-stu-id="2ebca-128">Timeout</span></span>](timeout.md) <br/> |<span data-ttu-id="2ebca-129">表示的工期，以分钟为单位订阅可以持续为空闲状态 GetEvents 请求从客户端。</span><span class="sxs-lookup"><span data-stu-id="2ebca-129">Represents the duration, in minutes, that the subscription can remain idle without a GetEvents request from the client.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ebca-130">父元素</span><span class="sxs-lookup"><span data-stu-id="2ebca-130">Parent elements</span></span>

|<span data-ttu-id="2ebca-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ebca-131">**Element**</span></span>|<span data-ttu-id="2ebca-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ebca-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ebca-133">订阅</span><span class="sxs-lookup"><span data-stu-id="2ebca-133">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="2ebca-134">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="2ebca-134">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ebca-135">文本值</span><span class="sxs-lookup"><span data-stu-id="2ebca-135">Text value</span></span>

<span data-ttu-id="2ebca-136">无。</span><span class="sxs-lookup"><span data-stu-id="2ebca-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ebca-137">备注</span><span class="sxs-lookup"><span data-stu-id="2ebca-137">Remarks</span></span>

<span data-ttu-id="2ebca-138">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ebca-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ebca-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ebca-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ebca-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ebca-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2ebca-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ebca-141">Schema name</span></span>  <br/> |<span data-ttu-id="2ebca-142">消息架构</span><span class="sxs-lookup"><span data-stu-id="2ebca-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2ebca-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ebca-143">Validation file</span></span>  <br/> |<span data-ttu-id="2ebca-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2ebca-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2ebca-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ebca-145">Can be empty</span></span>  <br/> |<span data-ttu-id="2ebca-146">False</span><span class="sxs-lookup"><span data-stu-id="2ebca-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ebca-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ebca-147">See also</span></span>



[<span data-ttu-id="2ebca-148">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="2ebca-148">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
  
[<span data-ttu-id="2ebca-149">订阅操作</span><span class="sxs-lookup"><span data-stu-id="2ebca-149">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="2ebca-150">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="2ebca-150">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="2ebca-151">取消操作</span><span class="sxs-lookup"><span data-stu-id="2ebca-151">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="2ebca-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2ebca-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

