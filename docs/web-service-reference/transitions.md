---
title: 移交
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
description: 转换元素表示时区转换的数组。
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467436"
---
# <a name="transitions"></a><span data-ttu-id="2ecfc-103">移交</span><span class="sxs-lookup"><span data-stu-id="2ecfc-103">Transitions</span></span>

<span data-ttu-id="2ecfc-104">**转换**元素表示时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="2ecfc-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ecfc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ecfc-106">Attributes and elements</span></span>

<span data-ttu-id="2ecfc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ecfc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2ecfc-108">Attributes</span></span>

|<span data-ttu-id="2ecfc-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-109">**Attribute**</span></span>|<span data-ttu-id="2ecfc-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ecfc-111">Id</span><span class="sxs-lookup"><span data-stu-id="2ecfc-111">Id</span></span>  <br/> |<span data-ttu-id="2ecfc-112">表示时区定义的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2ecfc-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2ecfc-113">Child elements</span></span>

|<span data-ttu-id="2ecfc-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-114">**Element**</span></span>|<span data-ttu-id="2ecfc-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ecfc-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="2ecfc-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="2ecfc-117">表示在特定日期和特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="2ecfc-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="2ecfc-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="2ecfc-119">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="2ecfc-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="2ecfc-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="2ecfc-121">表示在指定的一年中的某一天发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="2ecfc-122">移交</span><span class="sxs-lookup"><span data-stu-id="2ecfc-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="2ecfc-123">表示时区转换。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ecfc-124">父元素</span><span class="sxs-lookup"><span data-stu-id="2ecfc-124">Parent elements</span></span>

|<span data-ttu-id="2ecfc-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-125">**Element**</span></span>|<span data-ttu-id="2ecfc-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ecfc-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ecfc-127">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="2ecfc-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="2ecfc-128">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的开始时间的时区。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="2ecfc-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="2ecfc-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="2ecfc-130">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的结束时间的时区。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="2ecfc-131">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="2ecfc-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="2ecfc-132">定义时区。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ecfc-133">文本值</span><span class="sxs-lookup"><span data-stu-id="2ecfc-133">Text value</span></span>

<span data-ttu-id="2ecfc-134">无。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ecfc-135">说明</span><span class="sxs-lookup"><span data-stu-id="2ecfc-135">Remarks</span></span>

<span data-ttu-id="2ecfc-136">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ecfc-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ecfc-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ecfc-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ecfc-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ecfc-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ecfc-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ecfc-139">Schema Name</span></span>  <br/> |<span data-ttu-id="2ecfc-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="2ecfc-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="2ecfc-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ecfc-141">Validation File</span></span>  <br/> |<span data-ttu-id="2ecfc-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ecfc-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ecfc-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ecfc-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="2ecfc-144">False</span><span class="sxs-lookup"><span data-stu-id="2ecfc-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ecfc-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ecfc-145">See also</span></span>



- [<span data-ttu-id="2ecfc-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2ecfc-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

