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
description: Notification 元素包含有关订阅的信息以及自上次通知之后发生的事件。
ms.openlocfilehash: c4a5206c14985ec46cf40162a9ce4eaec68242ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530385"
---
# <a name="notification"></a><span data-ttu-id="7313f-103">通知</span><span class="sxs-lookup"><span data-stu-id="7313f-103">Notification</span></span>

<span data-ttu-id="7313f-104">**Notification**元素包含有关订阅的信息以及自上次通知之后发生的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-104">The **Notification** element contains information about the subscription and the events that have occurred since the last notification.</span></span> 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

<span data-ttu-id="7313f-105">**NotificationType**</span><span class="sxs-lookup"><span data-stu-id="7313f-105">**NotificationType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7313f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7313f-106">Attributes and elements</span></span>

<span data-ttu-id="7313f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7313f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7313f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7313f-108">Attributes</span></span>

<span data-ttu-id="7313f-109">无。</span><span class="sxs-lookup"><span data-stu-id="7313f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7313f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7313f-110">Child elements</span></span>

|<span data-ttu-id="7313f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7313f-111">**Element**</span></span>|<span data-ttu-id="7313f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7313f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7313f-113">SubscriptionId （GetEvents）</span><span class="sxs-lookup"><span data-stu-id="7313f-113">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md) <br/> |<span data-ttu-id="7313f-114">表示订阅的标识符。</span><span class="sxs-lookup"><span data-stu-id="7313f-114">Represents the identifier for a subscription.</span></span>  <br/> |
|[<span data-ttu-id="7313f-115">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="7313f-115">PreviousWatermark</span></span>](previouswatermark.md) <br/> |<span data-ttu-id="7313f-116">表示成功传递给订阅客户端的最新事件的水印。</span><span class="sxs-lookup"><span data-stu-id="7313f-116">Represents the watermark of the latest event that was successfully communicated to the client for the subscription.</span></span>  <br/> |
|[<span data-ttu-id="7313f-117">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="7313f-117">MoreEvents</span></span>](moreevents.md) <br/> |<span data-ttu-id="7313f-118">指示队列中是否存在要传递到客户端的更多事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-118">Indicates whether there are more events in the queue to be delivered to the client.</span></span>  <br/> |
|[<span data-ttu-id="7313f-119">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-119">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="7313f-120">表示在其中复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-120">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="7313f-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-121">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="7313f-122">代表在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-122">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="7313f-123">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-123">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="7313f-124">代表在其中删除项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-124">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="7313f-125">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-125">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="7313f-126">表示在其中修改项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-126">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="7313f-127">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-127">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="7313f-128">代表将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-128">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="7313f-129">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-129">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="7313f-130">代表由邮箱中的新邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-130">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7313f-131">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-131">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="7313f-132">表示未在邮箱中发生任何新活动的通知。</span><span class="sxs-lookup"><span data-stu-id="7313f-132">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7313f-133">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="7313f-133">FreeBusyChangedEvent</span></span>](freebusychangedevent.md) <br/> |<span data-ttu-id="7313f-134">表示项目的忙/闲时间已更改的事件。</span><span class="sxs-lookup"><span data-stu-id="7313f-134">Represents an event in which an item's free/busy time has changed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7313f-135">父元素</span><span class="sxs-lookup"><span data-stu-id="7313f-135">Parent elements</span></span>

|<span data-ttu-id="7313f-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="7313f-136">**Element**</span></span>|<span data-ttu-id="7313f-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="7313f-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7313f-138">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7313f-138">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md) <br/> |<span data-ttu-id="7313f-139">包含单个 GetEvents 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="7313f-139">Contains the status and result of a single GetEvents request.</span></span>  <br/> |
|[<span data-ttu-id="7313f-140">SendNotificationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7313f-140">SendNotificationResponseMessage</span></span>](sendnotificationresponsemessage.md) <br/> |<span data-ttu-id="7313f-141">包含单个 SendNotification 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="7313f-141">Contains the status and result of a single SendNotification request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7313f-142">文本值</span><span class="sxs-lookup"><span data-stu-id="7313f-142">Text value</span></span>

<span data-ttu-id="7313f-143">无。</span><span class="sxs-lookup"><span data-stu-id="7313f-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7313f-144">说明</span><span class="sxs-lookup"><span data-stu-id="7313f-144">Remarks</span></span>

<span data-ttu-id="7313f-145">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7313f-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7313f-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="7313f-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7313f-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="7313f-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7313f-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="7313f-148">Schema Name</span></span>  <br/> |<span data-ttu-id="7313f-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="7313f-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="7313f-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="7313f-150">Validation File</span></span>  <br/> |<span data-ttu-id="7313f-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7313f-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7313f-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="7313f-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="7313f-153">False</span><span class="sxs-lookup"><span data-stu-id="7313f-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7313f-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7313f-154">See also</span></span>

- [<span data-ttu-id="7313f-155">订阅操作</span><span class="sxs-lookup"><span data-stu-id="7313f-155">Subscribe operation</span></span>](subscribe-operation.md) 
- [<span data-ttu-id="7313f-156">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="7313f-156">GetEvents operation</span></span>](getevents-operation.md) 
- [<span data-ttu-id="7313f-157">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="7313f-157">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) 
- [<span data-ttu-id="7313f-158">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="7313f-158">Unsubscribe operation</span></span>](unsubscribe-operation.md)

