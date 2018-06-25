---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: WeeklyRecurrence 元素描述每周定期模式。
ms.openlocfilehash: 78bc76dd63c6737786df02f336217dc8de9a3a67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838553"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="2e316-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2e316-103">WeeklyRecurrence</span></span>

<span data-ttu-id="2e316-104">**WeeklyRecurrence**元素描述每周定期模式。</span><span class="sxs-lookup"><span data-stu-id="2e316-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="2e316-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="2e316-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e316-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e316-106">Attributes and elements</span></span>

<span data-ttu-id="2e316-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e316-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e316-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e316-108">Attributes</span></span>

<span data-ttu-id="2e316-109">无。</span><span class="sxs-lookup"><span data-stu-id="2e316-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e316-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2e316-110">Child elements</span></span>

|<span data-ttu-id="2e316-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e316-111">**Element**</span></span>|<span data-ttu-id="2e316-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e316-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e316-113">Interval</span><span class="sxs-lookup"><span data-stu-id="2e316-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="2e316-114">在两个连续每周定期模式项之间的周中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="2e316-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="2e316-115">值可以是介于 1 到 99。</span><span class="sxs-lookup"><span data-stu-id="2e316-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="2e316-116">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="2e316-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="2e316-117">介绍一周的哪几天所每周定期模式中。</span><span class="sxs-lookup"><span data-stu-id="2e316-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="2e316-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2e316-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="2e316-119">指定一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="2e316-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e316-120">父元素</span><span class="sxs-lookup"><span data-stu-id="2e316-120">Parent elements</span></span>

|<span data-ttu-id="2e316-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e316-121">**Element**</span></span>|<span data-ttu-id="2e316-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e316-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e316-123">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="2e316-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="2e316-124">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="2e316-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="2e316-125">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="2e316-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="2e316-126">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="2e316-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e316-127">文本值</span><span class="sxs-lookup"><span data-stu-id="2e316-127">Text value</span></span>

<span data-ttu-id="2e316-128">无。</span><span class="sxs-lookup"><span data-stu-id="2e316-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e316-129">注解</span><span class="sxs-lookup"><span data-stu-id="2e316-129">Remarks</span></span>

<span data-ttu-id="2e316-130">如果没有等于每周定期模式的第一个匹配项的日期的定期主项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)日期，所在的时区偏移的信息将丢失。</span><span class="sxs-lookup"><span data-stu-id="2e316-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="2e316-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2e316-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e316-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e316-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e316-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e316-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e316-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e316-134">Schema Name</span></span>  <br/> |<span data-ttu-id="2e316-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="2e316-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e316-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e316-136">Validation File</span></span>  <br/> |<span data-ttu-id="2e316-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e316-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e316-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e316-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e316-139">False</span><span class="sxs-lookup"><span data-stu-id="2e316-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e316-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e316-140">See also</span></span>



- [<span data-ttu-id="2e316-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2e316-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

