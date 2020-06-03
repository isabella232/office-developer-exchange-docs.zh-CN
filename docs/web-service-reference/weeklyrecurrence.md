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
ms.openlocfilehash: 5006238590c4cd7556a92fb1fbe13292383412b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530364"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="b886e-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="b886e-103">WeeklyRecurrence</span></span>

<span data-ttu-id="b886e-104">**WeeklyRecurrence**元素描述每周定期模式。</span><span class="sxs-lookup"><span data-stu-id="b886e-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="b886e-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="b886e-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b886e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b886e-106">Attributes and elements</span></span>

<span data-ttu-id="b886e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b886e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b886e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b886e-108">Attributes</span></span>

<span data-ttu-id="b886e-109">无。</span><span class="sxs-lookup"><span data-stu-id="b886e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b886e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b886e-110">Child elements</span></span>

|<span data-ttu-id="b886e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b886e-111">**Element**</span></span>|<span data-ttu-id="b886e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b886e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b886e-113">Interval</span><span class="sxs-lookup"><span data-stu-id="b886e-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b886e-114">定义两个连续的每周定期模式项目之间的时间间隔（以周为单位）。</span><span class="sxs-lookup"><span data-stu-id="b886e-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="b886e-115">该值可以介于1到99之间。</span><span class="sxs-lookup"><span data-stu-id="b886e-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="b886e-116">DaysOfWeek （DaysOfWeekType）</span><span class="sxs-lookup"><span data-stu-id="b886e-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="b886e-117">介绍周中的哪几天在每周定期模式中。</span><span class="sxs-lookup"><span data-stu-id="b886e-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="b886e-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b886e-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="b886e-119">指定一周的第一天。</span><span class="sxs-lookup"><span data-stu-id="b886e-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b886e-120">父元素</span><span class="sxs-lookup"><span data-stu-id="b886e-120">Parent elements</span></span>

|<span data-ttu-id="b886e-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="b886e-121">**Element**</span></span>|<span data-ttu-id="b886e-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="b886e-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b886e-123">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="b886e-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b886e-124">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="b886e-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="b886e-125">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="b886e-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b886e-126">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="b886e-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b886e-127">文本值</span><span class="sxs-lookup"><span data-stu-id="b886e-127">Text value</span></span>

<span data-ttu-id="b886e-128">无。</span><span class="sxs-lookup"><span data-stu-id="b886e-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b886e-129">说明</span><span class="sxs-lookup"><span data-stu-id="b886e-129">Remarks</span></span>

<span data-ttu-id="b886e-130">如果定期主项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)日期不具有与每周定期模式的第一个匹配项相等的日期，则将丢失时区偏移信息。</span><span class="sxs-lookup"><span data-stu-id="b886e-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="b886e-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b886e-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b886e-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="b886e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b886e-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="b886e-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b886e-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="b886e-134">Schema Name</span></span>  <br/> |<span data-ttu-id="b886e-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="b886e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="b886e-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="b886e-136">Validation File</span></span>  <br/> |<span data-ttu-id="b886e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b886e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b886e-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="b886e-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="b886e-139">False</span><span class="sxs-lookup"><span data-stu-id="b886e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b886e-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b886e-140">See also</span></span>



- [<span data-ttu-id="b886e-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b886e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

