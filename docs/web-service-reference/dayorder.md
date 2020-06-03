---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: DayOrder 元素表示在 DayOfWeek （时区）元素中指定的日期的第 n 个事件，该事件代表从到标准时间和夏令时的转换日期和时间。
ms.openlocfilehash: 53a8cb979bdb7aefead5623b4680f4c1a4ef5509
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526961"
---
# <a name="dayorder"></a><span data-ttu-id="aa548-103">DayOrder</span><span class="sxs-lookup"><span data-stu-id="aa548-103">DayOrder</span></span>

<span data-ttu-id="aa548-104">**DayOrder**元素表示在[DayOfWeek （时区）](dayofweek-timezone.md)元素中指定的日期的 _n_th 匹配项，该事件表示从到标准时间和夏时制的转换日期。</span><span class="sxs-lookup"><span data-stu-id="aa548-104">The **DayOrder** element represents the  _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span> 
  
```xml
<DayOrder>...</DayOrder>
```

<span data-ttu-id="aa548-105">**简洁**</span><span class="sxs-lookup"><span data-stu-id="aa548-105">**short**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="aa548-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa548-106">Attributes and elements</span></span>

<span data-ttu-id="aa548-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa548-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa548-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="aa548-108">Attributes</span></span>

<span data-ttu-id="aa548-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa548-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa548-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa548-110">Child elements</span></span>

<span data-ttu-id="aa548-111">无。</span><span class="sxs-lookup"><span data-stu-id="aa548-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa548-112">父元素</span><span class="sxs-lookup"><span data-stu-id="aa548-112">Parent elements</span></span>

|<span data-ttu-id="aa548-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa548-113">**Element**</span></span>|<span data-ttu-id="aa548-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa548-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa548-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="aa548-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="aa548-116">表示相对于[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。</span><span class="sxs-lookup"><span data-stu-id="aa548-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="aa548-117">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="aa548-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="aa548-118">下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="aa548-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="aa548-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="aa548-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="aa548-120">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。</span><span class="sxs-lookup"><span data-stu-id="aa548-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="aa548-121">此元素还包含有关何时从标准时间转换到夏令时的信息。</span><span class="sxs-lookup"><span data-stu-id="aa548-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="aa548-122">下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="aa548-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa548-123">文本值</span><span class="sxs-lookup"><span data-stu-id="aa548-123">Text value</span></span>

<span data-ttu-id="aa548-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="aa548-124">A text value is required.</span></span> <span data-ttu-id="aa548-125">**DayOrder**元素的值可以是1到5。</span><span class="sxs-lookup"><span data-stu-id="aa548-125">The value for the **DayOrder** element can be 1 through 5.</span></span> <span data-ttu-id="aa548-126">此元素的最大值可以是4或5，具体取决于月和年。</span><span class="sxs-lookup"><span data-stu-id="aa548-126">The maximum value for this element can be either 4 or 5, depending on the month and year.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aa548-127">备注</span><span class="sxs-lookup"><span data-stu-id="aa548-127">Remarks</span></span>

<span data-ttu-id="aa548-128">一个[StandardTime](standardtime.md)元素，其中包含值为5的**DayOrder**元素、值为10的[月份](month.md)元素以及值为周日的[DayOfWeek （时区）](dayofweek-timezone.md)元素。第十个月的第五个星期日发生从标准时间转换为夏时制。</span><span class="sxs-lookup"><span data-stu-id="aa548-128">A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="aa548-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa548-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa548-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa548-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa548-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa548-131">Schema Name</span></span>  <br/> |<span data-ttu-id="aa548-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="aa548-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa548-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa548-133">Validation File</span></span>  <br/> |<span data-ttu-id="aa548-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa548-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa548-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa548-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa548-136">False</span><span class="sxs-lookup"><span data-stu-id="aa548-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa548-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa548-137">See also</span></span>

- [<span data-ttu-id="aa548-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="aa548-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="aa548-139">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="aa548-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

