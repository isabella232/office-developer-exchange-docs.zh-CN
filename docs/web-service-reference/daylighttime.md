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
description: DaylightTime 元素表示相对于协调世界时（UTC）的时间的偏移量，该时间由观察到夏时制的区域中的偏置（UTC）元素表示。 此元素还包含有关何时从标准时间转换到夏令时的信息。
ms.openlocfilehash: 350fcb4ce278f423c62fcc5ecaa160eda71e4a2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455651"
---
# <a name="daylighttime"></a><span data-ttu-id="634ff-104">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="634ff-104">DaylightTime</span></span>

<span data-ttu-id="634ff-105">**DaylightTime**元素表示相对于协调世界时（utc）的时间的偏移量，该时间由观察到夏时制的区域中的[偏置（utc）](bias-utc.md)元素表示。</span><span class="sxs-lookup"><span data-stu-id="634ff-105">The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="634ff-106">此元素还包含有关何时从标准时间转换到夏令时的信息。</span><span class="sxs-lookup"><span data-stu-id="634ff-106">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span> 
  
- [<span data-ttu-id="634ff-107">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="634ff-107">TimeZone (Availability)</span></span>](timezone-availability.md) 
- [<span data-ttu-id="634ff-108">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="634ff-108">DaylightTime</span></span>](daylighttime.md)
  
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

<span data-ttu-id="634ff-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="634ff-109">**SerializableTimeZoneTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="634ff-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="634ff-110">Attributes and elements</span></span>

<span data-ttu-id="634ff-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="634ff-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="634ff-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="634ff-112">Attributes</span></span>

<span data-ttu-id="634ff-113">无。</span><span class="sxs-lookup"><span data-stu-id="634ff-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="634ff-114">子元素</span><span class="sxs-lookup"><span data-stu-id="634ff-114">Child elements</span></span>

|<span data-ttu-id="634ff-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="634ff-115">**Element**</span></span>|<span data-ttu-id="634ff-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="634ff-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="634ff-117">偏置</span><span class="sxs-lookup"><span data-stu-id="634ff-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="634ff-118">表示从 UTC 偏移量（由标准时间和夏令时的[偏置（UTC）](bias-utc.md)元素标识）的偏移量。</span><span class="sxs-lookup"><span data-stu-id="634ff-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="634ff-119">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="634ff-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="634ff-120">Time</span><span class="sxs-lookup"><span data-stu-id="634ff-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="634ff-121">表示从标准时间到夏令时和夏时制的过渡时间。</span><span class="sxs-lookup"><span data-stu-id="634ff-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="634ff-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="634ff-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="634ff-123">表示在 DayOfWeek （时区）元素中指定的、表示从到标准时间和夏时制转换的日期的[（时区）](dayofweek-timezone.md)元素中指定的日期的 _n_th 事件。</span><span class="sxs-lookup"><span data-stu-id="634ff-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="634ff-124">Month</span><span class="sxs-lookup"><span data-stu-id="634ff-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="634ff-125">表示一年的转换月份和标准时间以及夏时制。</span><span class="sxs-lookup"><span data-stu-id="634ff-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="634ff-126">DayOfWeek （时区）</span><span class="sxs-lookup"><span data-stu-id="634ff-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="634ff-127">表示从标准时间和夏时制转换到的一周中的某一天。</span><span class="sxs-lookup"><span data-stu-id="634ff-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="634ff-128">Year</span><span class="sxs-lookup"><span data-stu-id="634ff-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="634ff-129">用于定义根据年份变化的时区。</span><span class="sxs-lookup"><span data-stu-id="634ff-129">Used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="634ff-130">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="634ff-130">This element is optional.</span></span> <span data-ttu-id="634ff-131">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="634ff-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="634ff-132">父元素</span><span class="sxs-lookup"><span data-stu-id="634ff-132">Parent elements</span></span>

|<span data-ttu-id="634ff-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="634ff-133">**Element**</span></span>|<span data-ttu-id="634ff-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="634ff-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="634ff-135">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="634ff-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="634ff-136">包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="634ff-136">Contains elements that identify time zone information.</span></span><br/><br/><span data-ttu-id="634ff-137">此元素还包含有关标准时间和夏时制之间转换的信息。</span><span class="sxs-lookup"><span data-stu-id="634ff-137">This element also contains information about the transition between standard time and daylight saving time.</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a><span data-ttu-id="634ff-138">示例</span><span class="sxs-lookup"><span data-stu-id="634ff-138">Example</span></span>

<span data-ttu-id="634ff-139">下面的部分 GetUserAvailability 请求代表一个可识别夏时制的位置的客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="634ff-139">The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="634ff-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="634ff-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="634ff-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="634ff-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="634ff-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="634ff-142">Schema Name</span></span>  <br/> |<span data-ttu-id="634ff-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="634ff-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="634ff-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="634ff-144">Validation File</span></span>  <br/> |<span data-ttu-id="634ff-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="634ff-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="634ff-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="634ff-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="634ff-147">False</span><span class="sxs-lookup"><span data-stu-id="634ff-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="634ff-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="634ff-148">See also</span></span>

- [<span data-ttu-id="634ff-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="634ff-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="634ff-150">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="634ff-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

