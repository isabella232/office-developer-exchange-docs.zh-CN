---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: StandardTime 元素表示的时间相对于协调世界时 (UTC) 表示斜线 (UTC) 元素的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827546"
---
# <a name="standardtime"></a><span data-ttu-id="cde5d-104">StandardTime</span><span class="sxs-lookup"><span data-stu-id="cde5d-104">StandardTime</span></span>

<span data-ttu-id="cde5d-105">**StandardTime**元素表示的时间相对于协调世界时 (UTC) 表示[斜线 (UTC)](bias-utc.md)元素的偏移量。</span><span class="sxs-lookup"><span data-stu-id="cde5d-105">The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="cde5d-106">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="cde5d-106">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> 
  
- [<span data-ttu-id="cde5d-107">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="cde5d-107">TimeZone (Availability)</span></span>](timezone-availability.md)
- [<span data-ttu-id="cde5d-108">StandardTime</span><span class="sxs-lookup"><span data-stu-id="cde5d-108">StandardTime</span></span>](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 <span data-ttu-id="cde5d-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="cde5d-109">**SerializableTimeZoneTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cde5d-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cde5d-110">Attributes and elements</span></span>

<span data-ttu-id="cde5d-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cde5d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cde5d-112">属性</span><span class="sxs-lookup"><span data-stu-id="cde5d-112">Attributes</span></span>

<span data-ttu-id="cde5d-113">无。</span><span class="sxs-lookup"><span data-stu-id="cde5d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cde5d-114">子元素</span><span class="sxs-lookup"><span data-stu-id="cde5d-114">Child elements</span></span>

|<span data-ttu-id="cde5d-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="cde5d-115">**Element**</span></span>|<span data-ttu-id="cde5d-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="cde5d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cde5d-117">Bias</span><span class="sxs-lookup"><span data-stu-id="cde5d-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="cde5d-118">表示从由标准时间和夏时制的[斜线 (UTC)](bias-utc.md)元素的 UTC 偏移的偏移量。</span><span class="sxs-lookup"><span data-stu-id="cde5d-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="cde5d-119">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="cde5d-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="cde5d-120">Time</span><span class="sxs-lookup"><span data-stu-id="cde5d-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="cde5d-121">标准时间和夏时制表示转换时间。</span><span class="sxs-lookup"><span data-stu-id="cde5d-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cde5d-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="cde5d-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="cde5d-123">表示一天[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素，表示转换 from 和 to 标准时间和夏时制的日期中指定的 _n_th 匹配项。</span><span class="sxs-lookup"><span data-stu-id="cde5d-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cde5d-124">month</span><span class="sxs-lookup"><span data-stu-id="cde5d-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="cde5d-125">标准时间和夏时制表示转换月份。</span><span class="sxs-lookup"><span data-stu-id="cde5d-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="cde5d-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="cde5d-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="cde5d-127">代表星期几切换到以及从标准时间和夏时制当发生。</span><span class="sxs-lookup"><span data-stu-id="cde5d-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="cde5d-128">year()</span><span class="sxs-lookup"><span data-stu-id="cde5d-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="cde5d-129">定义更改这取决于一年的时区。</span><span class="sxs-lookup"><span data-stu-id="cde5d-129">Defines a time zone that changes depending on the year.</span></span> <span data-ttu-id="cde5d-130">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="cde5d-130">This element is optional.</span></span> <span data-ttu-id="cde5d-131">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cde5d-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cde5d-132">父元素</span><span class="sxs-lookup"><span data-stu-id="cde5d-132">Parent elements</span></span>

|<span data-ttu-id="cde5d-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="cde5d-133">**Element**</span></span>|<span data-ttu-id="cde5d-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="cde5d-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cde5d-135">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="cde5d-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="cde5d-136">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="cde5d-136">Contains elements that identify time zone information.</span></span> <span data-ttu-id="cde5d-137">此元素还包含有关标准时间和夏时制之间的转换的信息。</span><span class="sxs-lookup"><span data-stu-id="cde5d-137">This element also contains information about the transition between standard time and daylight saving time.</span></span> <br/><br/><span data-ttu-id="cde5d-138">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="cde5d-138">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cde5d-139">注解</span><span class="sxs-lookup"><span data-stu-id="cde5d-139">Remarks</span></span>

<span data-ttu-id="cde5d-140">**StandardTime**元素表示一个偏移的时间表示的[斜线 (UTC)](bias-utc.md)元素。</span><span class="sxs-lookup"><span data-stu-id="cde5d-140">The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="cde5d-141">子[Bias](bias.md)元素等于 0，标准时间时等于从由[斜线 (UTC)](bias-utc.md)元素的 UTC 的偏向偏移量。</span><span class="sxs-lookup"><span data-stu-id="cde5d-141">When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cde5d-142">示例</span><span class="sxs-lookup"><span data-stu-id="cde5d-142">Example</span></span>

<span data-ttu-id="cde5d-143">下面的示例演示一个区域夏时制观察到的位置。</span><span class="sxs-lookup"><span data-stu-id="cde5d-143">The following example shows a region where daylight saving time is observed.</span></span> <span data-ttu-id="cde5d-144">从夏时制转换为标准时间观察到凌晨 2</span><span class="sxs-lookup"><span data-stu-id="cde5d-144">The transition from daylight saving time to standard time is observed at 2 A.M.</span></span> <span data-ttu-id="cde5d-145">在第十个月的第五个星期日。</span><span class="sxs-lookup"><span data-stu-id="cde5d-145">on the fifth Sunday of the tenth month.</span></span>
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="cde5d-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="cde5d-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cde5d-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="cde5d-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cde5d-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="cde5d-148">Schema Name</span></span>  <br/> |<span data-ttu-id="cde5d-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="cde5d-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="cde5d-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="cde5d-150">Validation File</span></span>  <br/> |<span data-ttu-id="cde5d-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cde5d-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cde5d-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="cde5d-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="cde5d-153">False</span><span class="sxs-lookup"><span data-stu-id="cde5d-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cde5d-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cde5d-154">See also</span></span>

- [<span data-ttu-id="cde5d-155">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="cde5d-155">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="cde5d-156">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="cde5d-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

