---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: StreamingSubscriptionRequest 元素表示对流式事件通知订阅的订阅。
ms.openlocfilehash: b469ba7598420189c1db0e2fe676a279390eb6bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468227"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="110f5-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="110f5-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="110f5-104">**StreamingSubscriptionRequest**元素表示对流式事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="110f5-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="110f5-105">订阅</span><span class="sxs-lookup"><span data-stu-id="110f5-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="110f5-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="110f5-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="110f5-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="110f5-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="110f5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="110f5-108">Attributes and elements</span></span>

<span data-ttu-id="110f5-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="110f5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="110f5-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="110f5-110">Attributes</span></span>

|<span data-ttu-id="110f5-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="110f5-111">**Attribute**</span></span>|<span data-ttu-id="110f5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="110f5-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="110f5-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="110f5-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="110f5-114">指示服务器是否将订阅用户邮箱中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="110f5-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="110f5-115">**如果值为 true** ，则表示服务器将订阅。</span><span class="sxs-lookup"><span data-stu-id="110f5-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="110f5-116">子元素</span><span class="sxs-lookup"><span data-stu-id="110f5-116">Child elements</span></span>

|<span data-ttu-id="110f5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="110f5-117">**Element**</span></span>|<span data-ttu-id="110f5-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="110f5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="110f5-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="110f5-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="110f5-120">包含用于标识要监视其事件通知的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="110f5-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="110f5-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="110f5-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="110f5-122">包含用于创建订阅的事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="110f5-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="110f5-123">父元素</span><span class="sxs-lookup"><span data-stu-id="110f5-123">Parent elements</span></span>

|<span data-ttu-id="110f5-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="110f5-124">**Element**</span></span>|<span data-ttu-id="110f5-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="110f5-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="110f5-126">订阅</span><span class="sxs-lookup"><span data-stu-id="110f5-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="110f5-127">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="110f5-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="110f5-128">文本值</span><span class="sxs-lookup"><span data-stu-id="110f5-128">Text value</span></span>

<span data-ttu-id="110f5-129">无。</span><span class="sxs-lookup"><span data-stu-id="110f5-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="110f5-130">说明</span><span class="sxs-lookup"><span data-stu-id="110f5-130">Remarks</span></span>

<span data-ttu-id="110f5-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="110f5-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="110f5-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="110f5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="110f5-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="110f5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="110f5-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="110f5-134">Schema name</span></span>  <br/> |<span data-ttu-id="110f5-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="110f5-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="110f5-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="110f5-136">Validation file</span></span>  <br/> |<span data-ttu-id="110f5-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="110f5-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="110f5-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="110f5-138">Can be empty</span></span>  <br/> |<span data-ttu-id="110f5-139">False</span><span class="sxs-lookup"><span data-stu-id="110f5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="110f5-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="110f5-140">See also</span></span>



[<span data-ttu-id="110f5-141">订阅操作</span><span class="sxs-lookup"><span data-stu-id="110f5-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="110f5-142">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="110f5-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="110f5-143">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="110f5-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="110f5-144">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="110f5-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

