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
description: StandardTime 元素表示相对于由偏差（UTC）元素表示的协调世界时（UTC）的时间的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。
ms.openlocfilehash: 793f058840d4fd9216f03e660f5be0f7564906cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456400"
---
# <a name="standardtime"></a><span data-ttu-id="137fa-104">StandardTime</span><span class="sxs-lookup"><span data-stu-id="137fa-104">StandardTime</span></span>

<span data-ttu-id="137fa-105">**StandardTime**元素表示相对于由[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。</span><span class="sxs-lookup"><span data-stu-id="137fa-105">The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="137fa-106">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="137fa-106">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> 
  
- [<span data-ttu-id="137fa-107">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="137fa-107">TimeZone (Availability)</span></span>](timezone-availability.md)
- [<span data-ttu-id="137fa-108">StandardTime</span><span class="sxs-lookup"><span data-stu-id="137fa-108">StandardTime</span></span>](standardtime.md)
  
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

 <span data-ttu-id="137fa-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="137fa-109">**SerializableTimeZoneTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="137fa-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="137fa-110">Attributes and elements</span></span>

<span data-ttu-id="137fa-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="137fa-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="137fa-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="137fa-112">Attributes</span></span>

<span data-ttu-id="137fa-113">无。</span><span class="sxs-lookup"><span data-stu-id="137fa-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="137fa-114">子元素</span><span class="sxs-lookup"><span data-stu-id="137fa-114">Child elements</span></span>

|<span data-ttu-id="137fa-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="137fa-115">**Element**</span></span>|<span data-ttu-id="137fa-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="137fa-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="137fa-117">偏置</span><span class="sxs-lookup"><span data-stu-id="137fa-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="137fa-118">表示从 UTC 偏移量（由标准时间和夏令时的[偏置（UTC）](bias-utc.md)元素标识）的偏移量。</span><span class="sxs-lookup"><span data-stu-id="137fa-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="137fa-119">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="137fa-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="137fa-120">Time</span><span class="sxs-lookup"><span data-stu-id="137fa-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="137fa-121">表示从标准时间到夏令时和夏时制的过渡时间。</span><span class="sxs-lookup"><span data-stu-id="137fa-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="137fa-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="137fa-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="137fa-123">表示在 DayOfWeek （时区）元素中指定的、表示从到标准时间和夏时制转换的日期的[（时区）](dayofweek-timezone.md)元素中指定的日期的 _n_th 事件。</span><span class="sxs-lookup"><span data-stu-id="137fa-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="137fa-124">Month</span><span class="sxs-lookup"><span data-stu-id="137fa-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="137fa-125">表示一年的转换月份和标准时间以及夏时制。</span><span class="sxs-lookup"><span data-stu-id="137fa-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="137fa-126">DayOfWeek （时区）</span><span class="sxs-lookup"><span data-stu-id="137fa-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="137fa-127">表示从标准时间和夏时制转换到的一周中的某一天。</span><span class="sxs-lookup"><span data-stu-id="137fa-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="137fa-128">Year</span><span class="sxs-lookup"><span data-stu-id="137fa-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="137fa-129">定义根据年份变化的时区。</span><span class="sxs-lookup"><span data-stu-id="137fa-129">Defines a time zone that changes depending on the year.</span></span> <span data-ttu-id="137fa-130">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="137fa-130">This element is optional.</span></span> <span data-ttu-id="137fa-131">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="137fa-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="137fa-132">父元素</span><span class="sxs-lookup"><span data-stu-id="137fa-132">Parent elements</span></span>

|<span data-ttu-id="137fa-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="137fa-133">**Element**</span></span>|<span data-ttu-id="137fa-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="137fa-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="137fa-135">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="137fa-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="137fa-136">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="137fa-136">Contains elements that identify time zone information.</span></span> <span data-ttu-id="137fa-137">此元素还包含有关标准时间和夏时制之间转换的信息。</span><span class="sxs-lookup"><span data-stu-id="137fa-137">This element also contains information about the transition between standard time and daylight saving time.</span></span> <br/><br/><span data-ttu-id="137fa-138">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="137fa-138">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="137fa-139">备注</span><span class="sxs-lookup"><span data-stu-id="137fa-139">Remarks</span></span>

<span data-ttu-id="137fa-140">**StandardTime**元素表示由[偏置（UTC）](bias-utc.md)元素表示的偏移时间。</span><span class="sxs-lookup"><span data-stu-id="137fa-140">The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="137fa-141">当子[偏移](bias.md)元素等于0时，标准时间等于由[偏置（UTC）](bias-utc.md)元素表示的 UTC 偏差偏移量。</span><span class="sxs-lookup"><span data-stu-id="137fa-141">When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="137fa-142">示例</span><span class="sxs-lookup"><span data-stu-id="137fa-142">Example</span></span>

<span data-ttu-id="137fa-143">下面的示例展示了夏时制时间遵循的区域。</span><span class="sxs-lookup"><span data-stu-id="137fa-143">The following example shows a region where daylight saving time is observed.</span></span> <span data-ttu-id="137fa-144">从夏时制转换到标准时间的时间为凌晨2点。</span><span class="sxs-lookup"><span data-stu-id="137fa-144">The transition from daylight saving time to standard time is observed at 2 A.M.</span></span> <span data-ttu-id="137fa-145">第十个月的第五个星期日。</span><span class="sxs-lookup"><span data-stu-id="137fa-145">on the fifth Sunday of the tenth month.</span></span>
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="137fa-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="137fa-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="137fa-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="137fa-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="137fa-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="137fa-148">Schema Name</span></span>  <br/> |<span data-ttu-id="137fa-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="137fa-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="137fa-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="137fa-150">Validation File</span></span>  <br/> |<span data-ttu-id="137fa-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="137fa-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="137fa-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="137fa-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="137fa-153">False</span><span class="sxs-lookup"><span data-stu-id="137fa-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="137fa-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="137fa-154">See also</span></span>

- [<span data-ttu-id="137fa-155">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="137fa-155">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="137fa-156">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="137fa-156">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

