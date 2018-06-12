---
title: 月
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: Month 元素表示转换月份的标准时间和夏时制。
ms.openlocfilehash: 73d052ef16bc51cd574eb8b04e21546f97347258
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826476"
---
# <a name="month"></a><span data-ttu-id="65900-103">月</span><span class="sxs-lookup"><span data-stu-id="65900-103">Month</span></span>

<span data-ttu-id="65900-104">**Month**元素表示转换月份的标准时间和夏时制。</span><span class="sxs-lookup"><span data-stu-id="65900-104">The **Month** element represents the transition month of the year to and from standard time and daylight saving time.</span></span> 
  
```xml
<Month>...</Month>
```

 <span data-ttu-id="65900-105">**短**</span><span class="sxs-lookup"><span data-stu-id="65900-105">**Short**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65900-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="65900-106">Attributes and elements</span></span>

<span data-ttu-id="65900-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="65900-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65900-108">属性</span><span class="sxs-lookup"><span data-stu-id="65900-108">Attributes</span></span>

<span data-ttu-id="65900-109">无。</span><span class="sxs-lookup"><span data-stu-id="65900-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65900-110">子元素</span><span class="sxs-lookup"><span data-stu-id="65900-110">Child elements</span></span>

<span data-ttu-id="65900-111">无。</span><span class="sxs-lookup"><span data-stu-id="65900-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65900-112">父元素</span><span class="sxs-lookup"><span data-stu-id="65900-112">Parent elements</span></span>

|<span data-ttu-id="65900-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="65900-113">**Element**</span></span>|<span data-ttu-id="65900-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="65900-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65900-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="65900-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="65900-116">表示从时间相对于协调世界时 (UTC)[斜线 (UTC)](bias-utc.md)元素所表示的偏移量。</span><span class="sxs-lookup"><span data-stu-id="65900-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="65900-117">此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。</span><span class="sxs-lookup"><span data-stu-id="65900-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> <br/> <br/>  <span data-ttu-id="65900-118">下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="65900-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="65900-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="65900-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="65900-p102">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="65900-p102">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/><br/>  <span data-ttu-id="65900-122">下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="65900-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65900-123">文本值</span><span class="sxs-lookup"><span data-stu-id="65900-123">Text value</span></span>

<span data-ttu-id="65900-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="65900-124">A text value is required.</span></span> <span data-ttu-id="65900-125">此值表示相应月份的序号排名的匹配项，并且必须是介于 1 和 12。</span><span class="sxs-lookup"><span data-stu-id="65900-125">The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12.</span></span> <span data-ttu-id="65900-126">这是短整数数据类型。</span><span class="sxs-lookup"><span data-stu-id="65900-126">This is a short integer data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65900-127">备注</span><span class="sxs-lookup"><span data-stu-id="65900-127">Remarks</span></span>

<span data-ttu-id="65900-128">[StandardTime](standardtime.md)元素，其中包含的值为 5 [DayOrder](dayorder.md)元素的值为 10， **Month**元素和的值为星期日[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素是指从标准时间的转换第十个月的第五个星期日发生夏时制。</span><span class="sxs-lookup"><span data-stu-id="65900-128">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="65900-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="65900-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65900-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="65900-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65900-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="65900-131">Schema Name</span></span>  <br/> |<span data-ttu-id="65900-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="65900-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="65900-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="65900-133">Validation File</span></span>  <br/> |<span data-ttu-id="65900-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="65900-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65900-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="65900-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="65900-136">False</span><span class="sxs-lookup"><span data-stu-id="65900-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65900-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65900-137">See also</span></span>

- [<span data-ttu-id="65900-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="65900-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="65900-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="65900-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

