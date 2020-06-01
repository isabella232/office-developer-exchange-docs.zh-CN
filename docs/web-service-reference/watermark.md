---
title: Watermark
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
description: 水印元素表示邮箱事件队列中的事件书签。
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459761"
---
# <a name="watermark"></a><span data-ttu-id="cde26-103">Watermark</span><span class="sxs-lookup"><span data-stu-id="cde26-103">Watermark</span></span>

<span data-ttu-id="cde26-104">**水印**元素表示邮箱事件队列中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="cde26-104">The **Watermark** element represents an event bookmark in the mailbox event queue.</span></span> 
  
```xml
<Watermark/>
```

 <span data-ttu-id="cde26-105">**WatermarkType**</span><span class="sxs-lookup"><span data-stu-id="cde26-105">**WatermarkType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cde26-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cde26-106">Attributes and elements</span></span>

<span data-ttu-id="cde26-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cde26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cde26-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cde26-108">Attributes</span></span>

<span data-ttu-id="cde26-109">无。</span><span class="sxs-lookup"><span data-stu-id="cde26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cde26-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cde26-110">Child elements</span></span>

<span data-ttu-id="cde26-111">无。</span><span class="sxs-lookup"><span data-stu-id="cde26-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cde26-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cde26-112">Parent elements</span></span>

|<span data-ttu-id="cde26-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cde26-113">**Element**</span></span>|<span data-ttu-id="cde26-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cde26-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cde26-115">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="cde26-115">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md) <br/> |<span data-ttu-id="cde26-116">表示对基于请求的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="cde26-116">Represents a subscription to a pull-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="cde26-117">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="cde26-117">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md) <br/> |<span data-ttu-id="cde26-118">表示对基于推送的事件通知订阅的订阅。</span><span class="sxs-lookup"><span data-stu-id="cde26-118">Represents a subscription to a push-based event notification subscription.</span></span>  <br/> |
|[<span data-ttu-id="cde26-119">GetEvents</span><span class="sxs-lookup"><span data-stu-id="cde26-119">GetEvents</span></span>](getevents.md) <br/> |<span data-ttu-id="cde26-120">表示由拉客户端用来从服务器请求通知的操作。</span><span class="sxs-lookup"><span data-stu-id="cde26-120">Represents the operation used by pull clients to request notifications from the server.</span></span>  <br/> |
|[<span data-ttu-id="cde26-121">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-121">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="cde26-122">代表复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="cde26-122">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="cde26-123">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-123">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="cde26-124">代表在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="cde26-124">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="cde26-125">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-125">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="cde26-126">表示一个事件，其中的项或文件夹被删除。</span><span class="sxs-lookup"><span data-stu-id="cde26-126">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="cde26-127">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-127">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="cde26-128">表示一个事件，其中的项或文件夹被修改。</span><span class="sxs-lookup"><span data-stu-id="cde26-128">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="cde26-129">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-129">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="cde26-130">表示将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="cde26-130">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="cde26-131">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-131">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="cde26-132">表示由邮箱中的新邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="cde26-132">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="cde26-133">StatusEvent</span><span class="sxs-lookup"><span data-stu-id="cde26-133">StatusEvent</span></span>](statusevent.md) <br/> |<span data-ttu-id="cde26-134">表示未在邮箱中发生任何新活动的通知。</span><span class="sxs-lookup"><span data-stu-id="cde26-134">Represents a notification that no new activity has occurred in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="cde26-135">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="cde26-135">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md) <br/> |<span data-ttu-id="cde26-136">包含订阅请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="cde26-136">Contains the status and result of a Subscribe request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cde26-137">文本值</span><span class="sxs-lookup"><span data-stu-id="cde26-137">Text value</span></span>

<span data-ttu-id="cde26-138">文本值可能是必需的，也可能是可选的，具体取决于此元素的使用方式。</span><span class="sxs-lookup"><span data-stu-id="cde26-138">A text value may be required or optional depending on how this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cde26-139">备注</span><span class="sxs-lookup"><span data-stu-id="cde26-139">Remarks</span></span>

<span data-ttu-id="cde26-140">如果订阅请求包含水印，将从水印向前创建订阅。</span><span class="sxs-lookup"><span data-stu-id="cde26-140">If a Subscribe request contains a watermark, the subscription is created from the watermark forward.</span></span> <span data-ttu-id="cde26-141">如果订阅请求包含在邮箱事件表中找不到的水印， `ErrorInvalidWatermark` 则会向客户端应用程序返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="cde26-141">If the Subscribe request contains a watermark that is not found in the mailbox events table, an  `ErrorInvalidWatermark` error is returned to the client application.</span></span> <span data-ttu-id="cde26-142">如果水印太旧，并且已从事件表的30天窗口中删除，或者在事件表中不存在该水印，则可能会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="cde26-142">This may occur if the watermark is too old and has been removed from the 30 day window of the events table or if the watermark was not ever present in the events table.</span></span> <span data-ttu-id="cde26-143">例如，如果水印是从其他数据库中的邮箱的不同订阅获取的，则可能会发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="cde26-143">This can happen, for example, if a watermark is obtained from a different subscription for a mailbox in a different database.</span></span> 
  
<span data-ttu-id="cde26-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cde26-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cde26-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="cde26-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cde26-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="cde26-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cde26-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="cde26-147">Schema name</span></span>  <br/> |<span data-ttu-id="cde26-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="cde26-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="cde26-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="cde26-149">Validation file</span></span>  <br/> |<span data-ttu-id="cde26-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cde26-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cde26-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="cde26-151">Can be empty</span></span>  <br/> |<span data-ttu-id="cde26-152">False</span><span class="sxs-lookup"><span data-stu-id="cde26-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cde26-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cde26-153">See also</span></span>



[<span data-ttu-id="cde26-154">订阅操作</span><span class="sxs-lookup"><span data-stu-id="cde26-154">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="cde26-155">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="cde26-155">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="cde26-156">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="cde26-156">Unsubscribe operation</span></span>](unsubscribe-operation.md)

