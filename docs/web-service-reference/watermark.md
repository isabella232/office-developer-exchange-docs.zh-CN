---
title: 水印
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: 水印元素均表示邮箱事件队列中的事件书签。
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838535"
---
# <a name="watermark"></a><span data-ttu-id="0a3f6-103">水印</span><span class="sxs-lookup"><span data-stu-id="0a3f6-103">Watermark</span></span>

<span data-ttu-id="0a3f6-104">**水印**元素均表示邮箱事件队列中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="0a3f6-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="0a3f6-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a3f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a3f6-106">Attributes and elements</span></span>

<span data-ttu-id="0a3f6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a3f6-108">属性</span><span class="sxs-lookup"><span data-stu-id="0a3f6-108">Attributes</span></span>

<span data-ttu-id="0a3f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a3f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0a3f6-110">Child elements</span></span>

<span data-ttu-id="0a3f6-111">无。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a3f6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0a3f6-112">Parent elements</span></span>

|<span data-ttu-id="0a3f6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a3f6-113">**Element**</span></span>|<span data-ttu-id="0a3f6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a3f6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a3f6-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0a3f6-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="0a3f6-116">代表对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="0a3f6-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="0a3f6-118">代表对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="0a3f6-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="0a3f6-120">表示从服务器请求通知使用拉客户端的操作。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="0a3f6-122">表示复制的项或文件夹位置的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="0a3f6-124">表示在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="0a3f6-126">表示删除项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="0a3f6-128">表示修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="0a3f6-130">表示其中的项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="0a3f6-132">表示由邮箱中的一个新的邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-133">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="0a3f6-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="0a3f6-134">表示没有新的活动发生的邮箱中的通知。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0a3f6-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0a3f6-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="0a3f6-136">包含状态和 Subscribe 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a3f6-137">文本值</span><span class="sxs-lookup"><span data-stu-id="0a3f6-137">Text value</span></span>

<span data-ttu-id="0a3f6-138">必需或可选根据如何使用此元素是可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a3f6-139">注解</span><span class="sxs-lookup"><span data-stu-id="0a3f6-139">Remarks</span></span>

<span data-ttu-id="0a3f6-140">如果的 Subscribe 请求包含水印，从水印转接创建订阅。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="0a3f6-141">如果订阅请求包含邮箱事件表格中找不到水印`ErrorInvalidWatermark`错误返回给客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="0a3f6-142">这可能会发生如果水印太旧，已从事件表的 30 天窗口或如果水印未以往演示事件表格中。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="0a3f6-143">可以这样做，例如，如果从其他数据库中邮箱的不同订阅获得水印。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="0a3f6-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a3f6-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a3f6-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a3f6-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a3f6-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a3f6-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a3f6-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a3f6-147">Schema name</span></span>  <br/> |<span data-ttu-id="0a3f6-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="0a3f6-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a3f6-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a3f6-149">Validation file</span></span>  <br/> |<span data-ttu-id="0a3f6-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a3f6-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a3f6-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a3f6-151">Can be empty</span></span>  <br/> |<span data-ttu-id="0a3f6-152">False</span><span class="sxs-lookup"><span data-stu-id="0a3f6-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a3f6-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a3f6-153">See also</span></span>



[<span data-ttu-id="0a3f6-154">订阅操作</span><span class="sxs-lookup"><span data-stu-id="0a3f6-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="0a3f6-155">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="0a3f6-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="0a3f6-156">取消操作</span><span class="sxs-lookup"><span data-stu-id="0a3f6-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

