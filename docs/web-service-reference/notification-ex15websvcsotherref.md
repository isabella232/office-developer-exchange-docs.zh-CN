---
title: 通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: 通知元素包含有关订阅和自上次通知以来发生的事件的信息。
ms.openlocfilehash: a769d8988eb68d0fa0b02f3838cd891e714571b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826547"
---
# <a name="notification"></a><span data-ttu-id="ffce4-103">通知</span><span class="sxs-lookup"><span data-stu-id="ffce4-103">Notification</span></span>

<span data-ttu-id="ffce4-104">**通知**元素包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="ffce4-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

 <span data-ttu-id="ffce4-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="ffce4-105">**NotificationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffce4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ffce4-106">Attributes and elements</span></span>

<span data-ttu-id="ffce4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ffce4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffce4-108">属性</span><span class="sxs-lookup"><span data-stu-id="ffce4-108">Attributes</span></span>

<span data-ttu-id="ffce4-109">无。</span><span class="sxs-lookup"><span data-stu-id="ffce4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffce4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ffce4-110">Child elements</span></span>

|<span data-ttu-id="ffce4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ffce4-111">**Element**</span></span>|<span data-ttu-id="ffce4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ffce4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffce4-113">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="ffce4-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="ffce4-114">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="ffce4-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="ffce4-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="ffce4-116">表示对订阅的客户端的最新事件的成功传水印。</span><span class="sxs-lookup"><span data-stu-id="ffce4-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="ffce4-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="ffce4-118">指示队列传送到客户端中是否有多个事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="ffce4-120">表示复制的项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="ffce4-122">表示在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="ffce4-124">表示删除项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="ffce4-126">表示在其中修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="ffce4-128">表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="ffce4-130">表示由邮箱中的一个新的邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="ffce4-132">表示没有新的活动发生的邮箱中的通知。</span><span class="sxs-lookup"><span data-stu-id="ffce4-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="ffce4-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="ffce4-134">表示项目的忙/闲时间已发生更改的事件。</span><span class="sxs-lookup"><span data-stu-id="ffce4-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffce4-135">父元素</span><span class="sxs-lookup"><span data-stu-id="ffce4-135">Parent elements</span></span>

|<span data-ttu-id="ffce4-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="ffce4-136">**Element**</span></span>|<span data-ttu-id="ffce4-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="ffce4-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffce4-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ffce4-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="ffce4-139">包含状态和单个 GetEvents 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="ffce4-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="ffce4-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ffce4-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="ffce4-141">包含状态和单个 SendNotification 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="ffce4-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ffce4-142">文本值</span><span class="sxs-lookup"><span data-stu-id="ffce4-142">Text value</span></span>

<span data-ttu-id="ffce4-143">无。</span><span class="sxs-lookup"><span data-stu-id="ffce4-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffce4-144">备注</span><span class="sxs-lookup"><span data-stu-id="ffce4-144">Remarks</span></span>

<span data-ttu-id="ffce4-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ffce4-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffce4-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="ffce4-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffce4-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="ffce4-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ffce4-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="ffce4-148">Schema Name</span></span>  <br/> |<span data-ttu-id="ffce4-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="ffce4-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="ffce4-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="ffce4-150">Validation File</span></span>  <br/> |<span data-ttu-id="ffce4-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ffce4-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ffce4-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="ffce4-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffce4-153">False</span><span class="sxs-lookup"><span data-stu-id="ffce4-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffce4-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ffce4-154">See also</span></span>



[<span data-ttu-id="ffce4-155">订阅操作</span><span class="sxs-lookup"><span data-stu-id="ffce4-155">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="ffce4-156">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="ffce4-156">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="ffce4-157">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="ffce4-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md)
  
[<span data-ttu-id="ffce4-158">取消操作</span><span class="sxs-lookup"><span data-stu-id="ffce4-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

