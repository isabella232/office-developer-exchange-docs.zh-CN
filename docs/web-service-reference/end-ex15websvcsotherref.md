---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: End 元素表示持续时间的结束。
ms.openlocfilehash: d36f555d2ac9c0c1d82053029720ec17a53f2d92
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456141"
---
# <a name="end"></a><span data-ttu-id="51a62-103">End</span><span class="sxs-lookup"><span data-stu-id="51a62-103">End</span></span>

<span data-ttu-id="51a62-104">**End**元素表示持续时间的结束。</span><span class="sxs-lookup"><span data-stu-id="51a62-104">The **End** element represents the end of a duration.</span></span> 
  
```xml
<End/>
```

 <span data-ttu-id="51a62-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="51a62-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51a62-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="51a62-106">Attributes and elements</span></span>

<span data-ttu-id="51a62-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="51a62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51a62-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="51a62-108">Attributes</span></span>

<span data-ttu-id="51a62-109">无。</span><span class="sxs-lookup"><span data-stu-id="51a62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51a62-110">子元素</span><span class="sxs-lookup"><span data-stu-id="51a62-110">Child elements</span></span>

<span data-ttu-id="51a62-111">无。</span><span class="sxs-lookup"><span data-stu-id="51a62-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="51a62-112">父元素</span><span class="sxs-lookup"><span data-stu-id="51a62-112">Parent elements</span></span>

|<span data-ttu-id="51a62-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="51a62-113">**Element**</span></span>|<span data-ttu-id="51a62-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="51a62-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51a62-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="51a62-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="51a62-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="51a62-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="51a62-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="51a62-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="51a62-118">表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="51a62-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="51a62-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="51a62-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="51a62-120">表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="51a62-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="51a62-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="51a62-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="51a62-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="51a62-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="51a62-123">重复</span><span class="sxs-lookup"><span data-stu-id="51a62-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="51a62-124">代表定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="51a62-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="51a62-125">文本值</span><span class="sxs-lookup"><span data-stu-id="51a62-125">Text value</span></span>

<span data-ttu-id="51a62-126">该文本值表示工期的结束。</span><span class="sxs-lookup"><span data-stu-id="51a62-126">The text value represents the end of a duration.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51a62-127">备注</span><span class="sxs-lookup"><span data-stu-id="51a62-127">Remarks</span></span>

<span data-ttu-id="51a62-128">UpdateItem 操作可以设置 Exchange 存储项的[开始](start.md)和**结束**时间。</span><span class="sxs-lookup"><span data-stu-id="51a62-128">The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item.</span></span> <span data-ttu-id="51a62-129">在 UpdateItem 请求中，可以设置[开始](start.md)时间，而无需同时设置**结束**时间。</span><span class="sxs-lookup"><span data-stu-id="51a62-129">In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time.</span></span> <span data-ttu-id="51a62-130">如果[开始](start.md)时间晚于**结束**时间，这可能会导致错误。</span><span class="sxs-lookup"><span data-stu-id="51a62-130">This can cause an error if the [Start](start.md) time is later than the **End** time.</span></span> <span data-ttu-id="51a62-131">请注意，客户端应用程序必须在[开始](start.md)时间更改时对**结束**时间进行调整，以便保留持续时间。</span><span class="sxs-lookup"><span data-stu-id="51a62-131">Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
 <span data-ttu-id="51a62-132">**注释**如果定期主项目的[开始](start.md)和**结束**日期不具有与每周定期模式的第一个匹配项相等的日期，则将丢失时区偏移信息。</span><span class="sxs-lookup"><span data-stu-id="51a62-132">**Note** The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="51a62-133">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="51a62-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51a62-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="51a62-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51a62-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="51a62-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="51a62-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="51a62-136">Schema Name</span></span>  <br/> |<span data-ttu-id="51a62-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="51a62-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="51a62-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="51a62-138">Validation File</span></span>  <br/> |<span data-ttu-id="51a62-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="51a62-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="51a62-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="51a62-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="51a62-141">False</span><span class="sxs-lookup"><span data-stu-id="51a62-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51a62-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="51a62-142">See also</span></span>



[<span data-ttu-id="51a62-143">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="51a62-143">WeeklyRecurrence</span></span>](weeklyrecurrence.md)
  
 <span data-ttu-id="51a62-144">**End**</span><span class="sxs-lookup"><span data-stu-id="51a62-144">**End**</span></span>


- [<span data-ttu-id="51a62-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="51a62-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

