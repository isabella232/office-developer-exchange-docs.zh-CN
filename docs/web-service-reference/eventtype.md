---
title: EventType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventType
api_type:
- schema
ms.assetid: 04b70f9e-c226-4130-958e-0db0275cf58b
description: EventType 元素用于创建订阅并标识在通知中报告的事件类型。
ms.openlocfilehash: fb54c9e042f105d10e68cb0e9b48feae7ed8bf7b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754162"
---
# <a name="eventtype"></a><span data-ttu-id="e075c-103">EventType</span><span class="sxs-lookup"><span data-stu-id="e075c-103">EventType</span></span>

<span data-ttu-id="e075c-104">**EventType**元素用于创建订阅并标识在通知中报告的事件类型。</span><span class="sxs-lookup"><span data-stu-id="e075c-104">The **EventType** element is used to create a subscription and identifies an event type to be reported in a notification.</span></span> 
  
```xml
<EventType/>
```

 <span data-ttu-id="e075c-105">**NotificationEventTypeType**</span><span class="sxs-lookup"><span data-stu-id="e075c-105">**NotificationEventTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e075c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e075c-106">Attributes and elements</span></span>

<span data-ttu-id="e075c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e075c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e075c-108">属性</span><span class="sxs-lookup"><span data-stu-id="e075c-108">Attributes</span></span>

<span data-ttu-id="e075c-109">无。</span><span class="sxs-lookup"><span data-stu-id="e075c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e075c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e075c-110">Child elements</span></span>

<span data-ttu-id="e075c-111">无。</span><span class="sxs-lookup"><span data-stu-id="e075c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e075c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e075c-112">Parent elements</span></span>

|<span data-ttu-id="e075c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e075c-113">**Element**</span></span>|<span data-ttu-id="e075c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e075c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e075c-115">EventTypes</span><span class="sxs-lookup"><span data-stu-id="e075c-115">EventTypes</span></span>](eventtypes.md) <br/> |<span data-ttu-id="e075c-116">包含用于创建订阅事件通知事件类型的集合。</span><span class="sxs-lookup"><span data-stu-id="e075c-116">Contains a collection of event notification event types that are used to create a subscription.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e075c-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e075c-117">Text value</span></span>

<span data-ttu-id="e075c-118">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="e075c-118">A text value is required.</span></span> <span data-ttu-id="e075c-119">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="e075c-119">The following are the possible values:</span></span>
  
- <span data-ttu-id="e075c-120">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-120">CopiedEvent</span></span>
    
- <span data-ttu-id="e075c-121">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-121">CreatedEvent</span></span>
    
- <span data-ttu-id="e075c-122">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-122">DeletedEvent</span></span>
    
- <span data-ttu-id="e075c-123">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-123">ModifiedEvent</span></span>
    
- <span data-ttu-id="e075c-124">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-124">MovedEvent</span></span>
    
- <span data-ttu-id="e075c-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-125">NewMailEvent</span></span>
    
- <span data-ttu-id="e075c-126">FreeBusyChangedEvent</span><span class="sxs-lookup"><span data-stu-id="e075c-126">FreeBusyChangedEvent</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e075c-127">备注</span><span class="sxs-lookup"><span data-stu-id="e075c-127">Remarks</span></span>

<span data-ttu-id="e075c-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e075c-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e075c-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="e075c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e075c-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="e075c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e075c-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="e075c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e075c-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="e075c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e075c-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="e075c-133">Validation File</span></span>  <br/> |<span data-ttu-id="e075c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e075c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e075c-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="e075c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e075c-136">False</span><span class="sxs-lookup"><span data-stu-id="e075c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e075c-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e075c-137">See also</span></span>



[<span data-ttu-id="e075c-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="e075c-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="e075c-139">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="e075c-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="e075c-140">取消操作</span><span class="sxs-lookup"><span data-stu-id="e075c-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)
