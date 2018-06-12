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
description: StreamingSubscriptionRequest 元素均表示对流式处理的事件通知订阅的订阅。
ms.openlocfilehash: 088ec3b8048d70803b4837548ca918c0005d91bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827601"
---
# <a name="streamingsubscriptionrequest"></a><span data-ttu-id="89cff-103">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="89cff-103">StreamingSubscriptionRequest</span></span>

<span data-ttu-id="89cff-104">**StreamingSubscriptionRequest**元素均表示对流式处理的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="89cff-104">The **StreamingSubscriptionRequest** element represents a subscription to a streaming event notification subscription.</span></span> 
  
[<span data-ttu-id="89cff-105">订阅</span><span class="sxs-lookup"><span data-stu-id="89cff-105">Subscribe</span></span>](subscribe.md)
  
[<span data-ttu-id="89cff-106">StreamingSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="89cff-106">StreamingSubscriptionRequest</span></span>](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 <span data-ttu-id="89cff-107">**StreamingSubscriptionRequest**</span><span class="sxs-lookup"><span data-stu-id="89cff-107">**StreamingSubscriptionRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89cff-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89cff-108">Attributes and elements</span></span>

<span data-ttu-id="89cff-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89cff-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89cff-110">属性</span><span class="sxs-lookup"><span data-stu-id="89cff-110">Attributes</span></span>

|<span data-ttu-id="89cff-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="89cff-111">**Attribute**</span></span>|<span data-ttu-id="89cff-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="89cff-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89cff-113">**SubscribeToAllFolders**</span><span class="sxs-lookup"><span data-stu-id="89cff-113">**SubscribeToAllFolders**</span></span> <br/> |<span data-ttu-id="89cff-114">指示是否服务器将订阅用户的邮箱中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="89cff-114">Indicates whether the server will subscribe to all folders in the user's mailbox.</span></span> <span data-ttu-id="89cff-115">值为**true**指示服务器将订阅。</span><span class="sxs-lookup"><span data-stu-id="89cff-115">A value of **true** indicates that the server will subscribe.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="89cff-116">子元素</span><span class="sxs-lookup"><span data-stu-id="89cff-116">Child elements</span></span>

|<span data-ttu-id="89cff-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="89cff-117">**Element**</span></span>|<span data-ttu-id="89cff-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="89cff-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89cff-119">FolderIds</span><span class="sxs-lookup"><span data-stu-id="89cff-119">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="89cff-120">包含用于标识要监视的事件通知文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="89cff-120">Contains an array of folder identifiers that are used to identify folders to monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="89cff-121">EventTypes</span><span class="sxs-lookup"><span data-stu-id="89cff-121">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="89cff-122">包含用于创建订阅事件通知的集合。</span><span class="sxs-lookup"><span data-stu-id="89cff-122">Contains a collection of event notifications that are used to create a subscription.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89cff-123">父元素</span><span class="sxs-lookup"><span data-stu-id="89cff-123">Parent elements</span></span>

|<span data-ttu-id="89cff-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="89cff-124">**Element**</span></span>|<span data-ttu-id="89cff-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="89cff-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89cff-126">订阅</span><span class="sxs-lookup"><span data-stu-id="89cff-126">Subscribe</span></span>](subscribe.md) <br/> |<span data-ttu-id="89cff-127">包含用于创建订阅的属性。</span><span class="sxs-lookup"><span data-stu-id="89cff-127">Contains the properties that are used to create subscriptions.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89cff-128">文本值</span><span class="sxs-lookup"><span data-stu-id="89cff-128">Text value</span></span>

<span data-ttu-id="89cff-129">无。</span><span class="sxs-lookup"><span data-stu-id="89cff-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89cff-130">备注</span><span class="sxs-lookup"><span data-stu-id="89cff-130">Remarks</span></span>

<span data-ttu-id="89cff-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="89cff-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89cff-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="89cff-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89cff-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="89cff-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89cff-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="89cff-134">Schema name</span></span>  <br/> |<span data-ttu-id="89cff-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="89cff-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89cff-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="89cff-136">Validation file</span></span>  <br/> |<span data-ttu-id="89cff-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="89cff-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89cff-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="89cff-138">Can be empty</span></span>  <br/> |<span data-ttu-id="89cff-139">False</span><span class="sxs-lookup"><span data-stu-id="89cff-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89cff-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89cff-140">See also</span></span>



[<span data-ttu-id="89cff-141">订阅操作</span><span class="sxs-lookup"><span data-stu-id="89cff-141">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="89cff-142">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="89cff-142">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="89cff-143">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="89cff-143">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="89cff-144">取消操作</span><span class="sxs-lookup"><span data-stu-id="89cff-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

