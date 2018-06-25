---
title: 切换
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: 切换元素均表示一个数组所在的时区转换。
ms.openlocfilehash: df7cacdef71c3fdfaa3ecadb486843ea30e6109d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838283"
---
# <a name="transitions"></a><span data-ttu-id="21853-103">切换</span><span class="sxs-lookup"><span data-stu-id="21853-103">Transitions</span></span>

<span data-ttu-id="21853-104">**切换**元素均表示一个数组所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="21853-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="21853-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="21853-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21853-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21853-106">Attributes and elements</span></span>

<span data-ttu-id="21853-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21853-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21853-108">属性</span><span class="sxs-lookup"><span data-stu-id="21853-108">Attributes</span></span>

|<span data-ttu-id="21853-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="21853-109">**Attribute**</span></span>|<span data-ttu-id="21853-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="21853-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21853-111">Id</span><span class="sxs-lookup"><span data-stu-id="21853-111">Id</span></span>  <br/> |<span data-ttu-id="21853-112">代表所在的时区定义的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="21853-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21853-113">子元素</span><span class="sxs-lookup"><span data-stu-id="21853-113">Child elements</span></span>

|<span data-ttu-id="21853-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="21853-114">**Element**</span></span>|<span data-ttu-id="21853-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="21853-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21853-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="21853-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="21853-117">代表在特定日期和在特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="21853-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="21853-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="21853-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="21853-119">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="21853-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="21853-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="21853-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="21853-121">表示在一年中的指定日期发生所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="21853-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="21853-122">转换</span><span class="sxs-lookup"><span data-stu-id="21853-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="21853-123">代表所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="21853-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21853-124">父元素</span><span class="sxs-lookup"><span data-stu-id="21853-124">Parent elements</span></span>

|<span data-ttu-id="21853-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="21853-125">**Element**</span></span>|<span data-ttu-id="21853-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="21853-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21853-127">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="21853-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="21853-128">定义开始时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="21853-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="21853-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="21853-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="21853-130">定义的结束时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="21853-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="21853-131">时区定义</span><span class="sxs-lookup"><span data-stu-id="21853-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="21853-132">定义时区。</span><span class="sxs-lookup"><span data-stu-id="21853-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21853-133">文本值</span><span class="sxs-lookup"><span data-stu-id="21853-133">Text value</span></span>

<span data-ttu-id="21853-134">无。</span><span class="sxs-lookup"><span data-stu-id="21853-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21853-135">备注</span><span class="sxs-lookup"><span data-stu-id="21853-135">Remarks</span></span>

<span data-ttu-id="21853-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21853-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21853-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="21853-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21853-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="21853-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21853-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="21853-139">Schema Name</span></span>  <br/> |<span data-ttu-id="21853-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="21853-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="21853-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="21853-141">Validation File</span></span>  <br/> |<span data-ttu-id="21853-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21853-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21853-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="21853-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="21853-144">False</span><span class="sxs-lookup"><span data-stu-id="21853-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21853-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21853-145">See also</span></span>



- [<span data-ttu-id="21853-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21853-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

