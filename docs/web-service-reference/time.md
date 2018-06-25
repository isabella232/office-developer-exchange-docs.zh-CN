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
description: 时间元素表示转换时间与标准时间和夏时制。
ms.openlocfilehash: 716487fb7ed64dbaa6fa97caf1ea608e4673d2ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838212"
---
# <a name="time"></a><span data-ttu-id="0d7b7-103">时间</span><span class="sxs-lookup"><span data-stu-id="0d7b7-103">Time</span></span>

<span data-ttu-id="0d7b7-104">**时间**元素表示转换时间与标准时间和夏时制。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="0d7b7-105">**string**</span><span class="sxs-lookup"><span data-stu-id="0d7b7-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d7b7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d7b7-106">Attributes and elements</span></span>

<span data-ttu-id="0d7b7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d7b7-108">属性</span><span class="sxs-lookup"><span data-stu-id="0d7b7-108">Attributes</span></span>

<span data-ttu-id="0d7b7-109">无。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d7b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0d7b7-110">Child elements</span></span>

<span data-ttu-id="0d7b7-111">无。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d7b7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0d7b7-112">Parent elements</span></span>

|<span data-ttu-id="0d7b7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d7b7-113">**Element**</span></span>|<span data-ttu-id="0d7b7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d7b7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d7b7-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="0d7b7-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="0d7b7-116">表示从时间相对于协调世界时 (UTC)[斜线 (UTC)](bias-utc.md)元素所表示的偏移量。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="0d7b7-117">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="0d7b7-118">下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="0d7b7-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="0d7b7-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="0d7b7-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="0d7b7-p102">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="0d7b7-p102">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/><br/>  <span data-ttu-id="0d7b7-122">下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="0d7b7-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d7b7-123">文本值</span><span class="sxs-lookup"><span data-stu-id="0d7b7-123">Text value</span></span>

<span data-ttu-id="0d7b7-124">文本值代表小时、 分钟和秒采用以下格式： mm: ss。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d7b7-125">注解</span><span class="sxs-lookup"><span data-stu-id="0d7b7-125">Remarks</span></span>

<span data-ttu-id="0d7b7-126">[DaylightTime](daylighttime.md)元素**时间**元素时，它代表从夏时制转换为标准时间发生的一天的时间。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="0d7b7-127">[StandardTime](standardtime.md)元素中的[时间](time.md)元素时，它代表从标准时间转换为夏时，发生此事件的一天的时间。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="0d7b7-128">此元素具有零最小匹配项，并且之一的最大匹配项。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="0d7b7-129">示例</span><span class="sxs-lookup"><span data-stu-id="0d7b7-129">Example</span></span>

<span data-ttu-id="0d7b7-130">请求的以下部分表示上午 2 点转换时间</span><span class="sxs-lookup"><span data-stu-id="0d7b7-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="0d7b7-131">从夏时制标准时间。</span><span class="sxs-lookup"><span data-stu-id="0d7b7-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="0d7b7-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="0d7b7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d7b7-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="0d7b7-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d7b7-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="0d7b7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="0d7b7-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="0d7b7-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d7b7-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="0d7b7-136">Validation File</span></span>  <br/> |<span data-ttu-id="0d7b7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d7b7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d7b7-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="0d7b7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d7b7-139">False</span><span class="sxs-lookup"><span data-stu-id="0d7b7-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d7b7-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d7b7-140">See also</span></span>

- [<span data-ttu-id="0d7b7-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="0d7b7-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="0d7b7-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="0d7b7-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

