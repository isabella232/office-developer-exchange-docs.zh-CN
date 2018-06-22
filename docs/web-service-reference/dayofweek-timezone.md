---
title: DayOfWeek (TimeZone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: DayOfWeek 元素表示在所在的时区转换发生一周中的某一天。
ms.openlocfilehash: 7816b90000be36cf3a3354d26d978684bfdcfe40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753761"
---
# <a name="dayofweek-timezone"></a><span data-ttu-id="61bd4-103">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="61bd4-103">DayOfWeek (TimeZone)</span></span>

<span data-ttu-id="61bd4-104">**DayOfWeek**元素表示在所在的时区转换发生一周中的某一天。</span><span class="sxs-lookup"><span data-stu-id="61bd4-104">The **DayOfWeek** element represents the day of the week on which the time zone transition occurs.</span></span> 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

<span data-ttu-id="61bd4-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="61bd4-105">**DayOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="61bd4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="61bd4-106">Attributes and elements</span></span>

<span data-ttu-id="61bd4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="61bd4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61bd4-108">属性</span><span class="sxs-lookup"><span data-stu-id="61bd4-108">Attributes</span></span>

<span data-ttu-id="61bd4-109">无。</span><span class="sxs-lookup"><span data-stu-id="61bd4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61bd4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="61bd4-110">Child elements</span></span>

<span data-ttu-id="61bd4-111">无。</span><span class="sxs-lookup"><span data-stu-id="61bd4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61bd4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="61bd4-112">Parent elements</span></span>

|<span data-ttu-id="61bd4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="61bd4-113">**Element**</span></span>|<span data-ttu-id="61bd4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="61bd4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61bd4-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="61bd4-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="61bd4-116">表示从时间相对于协调世界时 (UTC)[斜线 (UTC)](bias-utc.md)元素所表示的偏移量。</span><span class="sxs-lookup"><span data-stu-id="61bd4-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="61bd4-117">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="61bd4-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="61bd4-118">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="61bd4-118">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="61bd4-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="61bd4-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="61bd4-120">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。</span><span class="sxs-lookup"><span data-stu-id="61bd4-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="61bd4-121">此元素还包含有关何时从标准时间转换到夏令时的信息。</span><span class="sxs-lookup"><span data-stu-id="61bd4-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="61bd4-122">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="61bd4-122">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[<span data-ttu-id="61bd4-123">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="61bd4-123">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="61bd4-124">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="61bd4-124">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61bd4-125">文本值</span><span class="sxs-lookup"><span data-stu-id="61bd4-125">Text value</span></span>

<span data-ttu-id="61bd4-126">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="61bd4-126">A text value is required.</span></span> <span data-ttu-id="61bd4-127">由一个枚举，具有以下可能的值表示的文本值：</span><span class="sxs-lookup"><span data-stu-id="61bd4-127">The text value is represented by an enumeration that has the following possible values:</span></span>
  
- <span data-ttu-id="61bd4-128">星期日</span><span class="sxs-lookup"><span data-stu-id="61bd4-128">Sunday</span></span>    
- <span data-ttu-id="61bd4-129">周一</span><span class="sxs-lookup"><span data-stu-id="61bd4-129">Monday</span></span>    
- <span data-ttu-id="61bd4-130">周二</span><span class="sxs-lookup"><span data-stu-id="61bd4-130">Tuesday</span></span>    
- <span data-ttu-id="61bd4-131">周三</span><span class="sxs-lookup"><span data-stu-id="61bd4-131">Wednesday</span></span>    
- <span data-ttu-id="61bd4-132">周四</span><span class="sxs-lookup"><span data-stu-id="61bd4-132">Thursday</span></span>    
- <span data-ttu-id="61bd4-133">周五</span><span class="sxs-lookup"><span data-stu-id="61bd4-133">Friday</span></span>    
- <span data-ttu-id="61bd4-134">周六</span><span class="sxs-lookup"><span data-stu-id="61bd4-134">Saturday</span></span>    
- <span data-ttu-id="61bd4-135">日</span><span class="sxs-lookup"><span data-stu-id="61bd4-135">Day</span></span>    
- <span data-ttu-id="61bd4-136">Weekday</span><span class="sxs-lookup"><span data-stu-id="61bd4-136">Weekday</span></span>   
- <span data-ttu-id="61bd4-137">WeekendDay</span><span class="sxs-lookup"><span data-stu-id="61bd4-137">WeekendDay</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61bd4-138">备注</span><span class="sxs-lookup"><span data-stu-id="61bd4-138">Remarks</span></span>

<span data-ttu-id="61bd4-139">[StandardTime](standardtime.md)元素，其中包含的值为 5 [DayOrder](dayorder.md)元素的值为 10， [Month](month.md)元素和的值为星期日**DayOfWeek**元素是指从标准时间转换为夏时制第十个月的第五个星期日节约时间发生。</span><span class="sxs-lookup"><span data-stu-id="61bd4-139">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a [Month](month.md) element that has a value of 10, and a **DayOfWeek** element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
<span data-ttu-id="61bd4-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="61bd4-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61bd4-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="61bd4-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61bd4-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="61bd4-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61bd4-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="61bd4-143">Schema Name</span></span>  <br/> |<span data-ttu-id="61bd4-144">类型架构</span><span class="sxs-lookup"><span data-stu-id="61bd4-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="61bd4-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="61bd4-145">Validation File</span></span>  <br/> |<span data-ttu-id="61bd4-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61bd4-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="61bd4-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="61bd4-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="61bd4-148">False</span><span class="sxs-lookup"><span data-stu-id="61bd4-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61bd4-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61bd4-149">See also</span></span>

- [<span data-ttu-id="61bd4-150">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="61bd4-150">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="61bd4-151">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="61bd4-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

