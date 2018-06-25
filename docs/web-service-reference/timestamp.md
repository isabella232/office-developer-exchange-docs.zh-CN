---
title: 时间戳
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: 时间戳元素均表示邮箱事件的时间戳。
ms.openlocfilehash: d020d9a4cf3a128d26e0ff2b83be9f3deb024339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838279"
---
# <a name="timestamp"></a><span data-ttu-id="93c56-103">时间戳</span><span class="sxs-lookup"><span data-stu-id="93c56-103">TimeStamp</span></span>

<span data-ttu-id="93c56-104">**时间戳**元素均表示邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="93c56-104">The **Timestamp** element represents the timestamp of a mailbox event.</span></span> 
  
```xml
<TimeStamp/>
```

 <span data-ttu-id="93c56-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="93c56-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93c56-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="93c56-106">Attributes and elements</span></span>

<span data-ttu-id="93c56-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="93c56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93c56-108">属性</span><span class="sxs-lookup"><span data-stu-id="93c56-108">Attributes</span></span>

<span data-ttu-id="93c56-109">无。</span><span class="sxs-lookup"><span data-stu-id="93c56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93c56-110">子元素</span><span class="sxs-lookup"><span data-stu-id="93c56-110">Child elements</span></span>

<span data-ttu-id="93c56-111">无。</span><span class="sxs-lookup"><span data-stu-id="93c56-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="93c56-112">父元素</span><span class="sxs-lookup"><span data-stu-id="93c56-112">Parent elements</span></span>

|<span data-ttu-id="93c56-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="93c56-113">**Element**</span></span>|<span data-ttu-id="93c56-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="93c56-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93c56-115">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-115">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="93c56-116">表示复制的项或文件夹位置的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-116">Represents an event where an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="93c56-117">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-117">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="93c56-118">表示在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-118">Represents an event where an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="93c56-119">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-119">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="93c56-120">表示删除项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-120">Represents an event where an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="93c56-121">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-121">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="93c56-122">表示修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-122">Represents an event where an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="93c56-123">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-123">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="93c56-124">表示其中的项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-124">Represents an event where an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="93c56-125">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="93c56-125">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="93c56-126">表示由邮箱中的一个新的邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="93c56-126">Represents an event triggered by a new mail item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="93c56-127">文本值</span><span class="sxs-lookup"><span data-stu-id="93c56-127">Text value</span></span>

<span data-ttu-id="93c56-128">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="93c56-128">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93c56-129">注解</span><span class="sxs-lookup"><span data-stu-id="93c56-129">Remarks</span></span>

<span data-ttu-id="93c56-130">此元素是主要可供使用的事件频率的客户端确定中。</span><span class="sxs-lookup"><span data-stu-id="93c56-130">This element is primarily available for use in client determination of event frequency.</span></span> <span data-ttu-id="93c56-131">这是不存在于[StatusEvent](statusevent.md)中。</span><span class="sxs-lookup"><span data-stu-id="93c56-131">This is not present in [StatusEvent](statusevent.md).</span></span>
  
<span data-ttu-id="93c56-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="93c56-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93c56-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="93c56-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93c56-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="93c56-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="93c56-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="93c56-135">Schema name</span></span>  <br/> |<span data-ttu-id="93c56-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="93c56-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="93c56-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="93c56-137">Validation file</span></span>  <br/> |<span data-ttu-id="93c56-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="93c56-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="93c56-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="93c56-139">Can be empty</span></span>  <br/> |<span data-ttu-id="93c56-140">False</span><span class="sxs-lookup"><span data-stu-id="93c56-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93c56-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="93c56-141">See also</span></span>



[<span data-ttu-id="93c56-142">订阅操作</span><span class="sxs-lookup"><span data-stu-id="93c56-142">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="93c56-143">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="93c56-143">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="93c56-144">取消操作</span><span class="sxs-lookup"><span data-stu-id="93c56-144">Unsubscribe operation</span></span>](unsubscribe-operation.md)

