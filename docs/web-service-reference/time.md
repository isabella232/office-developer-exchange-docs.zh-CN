---
title: 时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: Time 元素表示从标准时间和夏时制的一天的转换时间。
ms.openlocfilehash: 97c89fbcbdb85fcdd4d32a1d44075ac42adef053
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460293"
---
# <a name="time"></a><span data-ttu-id="ddefc-103">Time</span><span class="sxs-lookup"><span data-stu-id="ddefc-103">Time</span></span>

<span data-ttu-id="ddefc-104">**Time**元素表示从标准时间和夏时制的一天的转换时间。</span><span class="sxs-lookup"><span data-stu-id="ddefc-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="ddefc-105">**string**</span><span class="sxs-lookup"><span data-stu-id="ddefc-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ddefc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ddefc-106">Attributes and elements</span></span>

<span data-ttu-id="ddefc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ddefc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddefc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ddefc-108">Attributes</span></span>

<span data-ttu-id="ddefc-109">无。</span><span class="sxs-lookup"><span data-stu-id="ddefc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ddefc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ddefc-110">Child elements</span></span>

<span data-ttu-id="ddefc-111">无。</span><span class="sxs-lookup"><span data-stu-id="ddefc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ddefc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ddefc-112">Parent elements</span></span>

|<span data-ttu-id="ddefc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ddefc-113">**Element**</span></span>|<span data-ttu-id="ddefc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ddefc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddefc-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="ddefc-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="ddefc-116">表示相对于[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。</span><span class="sxs-lookup"><span data-stu-id="ddefc-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="ddefc-117">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="ddefc-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="ddefc-118">下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ddefc-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="ddefc-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="ddefc-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="ddefc-p102">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="ddefc-p102">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/><br/>  <span data-ttu-id="ddefc-122">下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ddefc-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ddefc-123">文本值</span><span class="sxs-lookup"><span data-stu-id="ddefc-123">Text value</span></span>

<span data-ttu-id="ddefc-124">该文本值表示以以下格式表示的小时、分钟和秒数： hh： mm： ss。</span><span class="sxs-lookup"><span data-stu-id="ddefc-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddefc-125">备注</span><span class="sxs-lookup"><span data-stu-id="ddefc-125">Remarks</span></span>

<span data-ttu-id="ddefc-126">当**time**元素出现在[DaylightTime](daylighttime.md)元素中时，它表示一天中从夏时制转换为标准时间的时间。</span><span class="sxs-lookup"><span data-stu-id="ddefc-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="ddefc-127">当[time](time.md)元素出现在[StandardTime](standardtime.md)元素中时，它表示一天中从标准时间到夏令时的转换发生的时间。</span><span class="sxs-lookup"><span data-stu-id="ddefc-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="ddefc-128">此元素的最小匹配项为零，最大值为1。</span><span class="sxs-lookup"><span data-stu-id="ddefc-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="ddefc-129">示例</span><span class="sxs-lookup"><span data-stu-id="ddefc-129">Example</span></span>

<span data-ttu-id="ddefc-130">请求的以下部分表示转换时间为凌晨2点。</span><span class="sxs-lookup"><span data-stu-id="ddefc-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="ddefc-131">从标准时间到夏时制。</span><span class="sxs-lookup"><span data-stu-id="ddefc-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="ddefc-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="ddefc-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddefc-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="ddefc-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddefc-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="ddefc-134">Schema Name</span></span>  <br/> |<span data-ttu-id="ddefc-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="ddefc-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddefc-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="ddefc-136">Validation File</span></span>  <br/> |<span data-ttu-id="ddefc-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ddefc-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddefc-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="ddefc-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="ddefc-139">False</span><span class="sxs-lookup"><span data-stu-id="ddefc-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddefc-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ddefc-140">See also</span></span>

- [<span data-ttu-id="ddefc-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ddefc-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="ddefc-142">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="ddefc-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

