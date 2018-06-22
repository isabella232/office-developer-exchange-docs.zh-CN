---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: DaylightTime 元素表示从时间相对于协调世界时 (UTC) 表示的夏时制观察到的位置的区域中的斜线 (UTC) 元素的偏移量。 此元素还包含有关何时从标准时间转换到夏令时的信息。
ms.openlocfilehash: 07ec4b1a5f84669aca33d46cdf1fa2e578f3b43b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753760"
---
# <a name="daylighttime"></a><span data-ttu-id="bf5fb-104">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="bf5fb-104">DaylightTime</span></span>

<span data-ttu-id="bf5fb-105">**DaylightTime**元素表示从时间相对于协调世界时 (UTC) 表示的夏时制观察到的位置的区域中的[斜线 (UTC)](bias-utc.md)元素的偏移量。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-105">The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="bf5fb-106">此元素还包含有关何时从标准时间转换到夏令时的信息。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-106">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span> 
  
- [<span data-ttu-id="bf5fb-107">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="bf5fb-107">TimeZone (Availability)</span></span>](timezone-availability.md) 
- [<span data-ttu-id="bf5fb-108">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="bf5fb-108">DaylightTime</span></span>](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
```

<span data-ttu-id="bf5fb-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="bf5fb-109">**SerializableTimeZoneTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bf5fb-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bf5fb-110">Attributes and elements</span></span>

<span data-ttu-id="bf5fb-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf5fb-112">属性</span><span class="sxs-lookup"><span data-stu-id="bf5fb-112">Attributes</span></span>

<span data-ttu-id="bf5fb-113">无。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf5fb-114">子元素</span><span class="sxs-lookup"><span data-stu-id="bf5fb-114">Child elements</span></span>

|<span data-ttu-id="bf5fb-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf5fb-115">**Element**</span></span>|<span data-ttu-id="bf5fb-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf5fb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf5fb-117">Bias</span><span class="sxs-lookup"><span data-stu-id="bf5fb-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="bf5fb-118">表示从由标准时间和夏时制的[斜线 (UTC)](bias-utc.md)元素的 UTC 偏移的偏移量。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="bf5fb-119">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="bf5fb-120">Time</span><span class="sxs-lookup"><span data-stu-id="bf5fb-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="bf5fb-121">标准时间和夏时制表示转换时间。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="bf5fb-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="bf5fb-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="bf5fb-123">表示一天[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素，表示转换 from 和 to 标准时间和夏时制的日期中指定的 _n_th 匹配项。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="bf5fb-124">month</span><span class="sxs-lookup"><span data-stu-id="bf5fb-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="bf5fb-125">标准时间和夏时制表示转换月份。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="bf5fb-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="bf5fb-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="bf5fb-127">代表星期几切换到以及从标准时间和夏时制当发生。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="bf5fb-128">year()</span><span class="sxs-lookup"><span data-stu-id="bf5fb-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="bf5fb-129">用于定义更改这取决于一年的时区。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-129">Used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="bf5fb-130">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-130">This element is optional.</span></span> <span data-ttu-id="bf5fb-131">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bf5fb-132">父元素</span><span class="sxs-lookup"><span data-stu-id="bf5fb-132">Parent elements</span></span>

|<span data-ttu-id="bf5fb-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="bf5fb-133">**Element**</span></span>|<span data-ttu-id="bf5fb-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="bf5fb-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf5fb-135">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="bf5fb-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="bf5fb-136">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-136">Contains elements that identify time zone information.</span></span><br/><br/><span data-ttu-id="bf5fb-137">此元素还包含有关标准时间和夏时制之间的转换的信息。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-137">This element also contains information about the transition between standard time and daylight saving time.</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a><span data-ttu-id="bf5fb-138">示例</span><span class="sxs-lookup"><span data-stu-id="bf5fb-138">Example</span></span>

<span data-ttu-id="bf5fb-139">以下部分 GetUserAvailability 请求代表识别夏时制位置中的客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="bf5fb-139">The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="bf5fb-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="bf5fb-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf5fb-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="bf5fb-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bf5fb-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="bf5fb-142">Schema Name</span></span>  <br/> |<span data-ttu-id="bf5fb-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="bf5fb-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="bf5fb-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="bf5fb-144">Validation File</span></span>  <br/> |<span data-ttu-id="bf5fb-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bf5fb-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bf5fb-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="bf5fb-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="bf5fb-147">False</span><span class="sxs-lookup"><span data-stu-id="bf5fb-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bf5fb-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bf5fb-148">See also</span></span>

- [<span data-ttu-id="bf5fb-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="bf5fb-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="bf5fb-150">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="bf5fb-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

