---
title: Bias
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: ae10aa44-e6d3-483d-a3e6-bb9c45966810
description: Bias 元素表示由标准时间和夏令时的 偏置 (UTC) 元素标识的与协调世界时 (UTC) 时差的时差。此值以分钟为单位。
ms.openlocfilehash: 770bf97b030ac1293595560bc269f54896e35a15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753331"
---
# <a name="bias"></a><span data-ttu-id="8ff44-104">Bias</span><span class="sxs-lookup"><span data-stu-id="8ff44-104">Bias</span></span>

<span data-ttu-id="8ff44-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Bias** 元素表示由标准时间和夏令时的 [偏置 (UTC)](bias-utc.md) 元素标识的与协调世界时 (UTC) 时差的时差。此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="8ff44-p102">The **Bias** element represents the offset from the Coordinated Universal Time (UTC) offset identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time. This value is in minutes.</span></span> 
  
```xml
<Bias>...</Bias>
```

<span data-ttu-id="8ff44-107">**int**</span><span class="sxs-lookup"><span data-stu-id="8ff44-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8ff44-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8ff44-108">Attributes and elements</span></span>

<span data-ttu-id="8ff44-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8ff44-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ff44-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8ff44-110">Attributes</span></span>

<span data-ttu-id="8ff44-111">无。</span><span class="sxs-lookup"><span data-stu-id="8ff44-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ff44-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8ff44-112">Child elements</span></span>

<span data-ttu-id="8ff44-113">无。</span><span class="sxs-lookup"><span data-stu-id="8ff44-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ff44-114">父元素</span><span class="sxs-lookup"><span data-stu-id="8ff44-114">Parent elements</span></span>

|<span data-ttu-id="8ff44-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="8ff44-115">**Element**</span></span>|<span data-ttu-id="8ff44-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="8ff44-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8ff44-117">StandardTime</span><span class="sxs-lookup"><span data-stu-id="8ff44-117">StandardTime element</span></span>](standardtime.md) <br/> | <span data-ttu-id="8ff44-p103">表示与相对于 UTC（由 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。  </span><span class="sxs-lookup"><span data-stu-id="8ff44-p103">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="8ff44-120">下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8ff44-120">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="8ff44-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="8ff44-121">DaylightTime element</span></span>](daylighttime.md) <br/> | <span data-ttu-id="8ff44-p104">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="8ff44-p104">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/><br/><span data-ttu-id="8ff44-124">下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8ff44-124">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8ff44-125">文本值</span><span class="sxs-lookup"><span data-stu-id="8ff44-125">Text value</span></span>

<span data-ttu-id="8ff44-p105">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="8ff44-p105">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ff44-128">说明</span><span class="sxs-lookup"><span data-stu-id="8ff44-128">Remarks</span></span>

<span data-ttu-id="8ff44-p106">用于确定本地时间的时差只能由一个 **Bias** 元素提供。由 [DaylightTime](daylighttime.md) 元素或 [StandardTime](standardtime.md) 元素提供的 Bias 元素值的总和加上 [偏置 (UTC)](bias-utc.md) 元素来标识本地时间。</span><span class="sxs-lookup"><span data-stu-id="8ff44-p106">The offset used to determine the local time can only be provided by one of the **Bias** elements. The sum of the values of the Bias element provided by the [DaylightTime](daylighttime.md) element or the [StandardTime](standardtime.md) element plus the [Bias (UTC)](bias-utc.md) element identifies the local time.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8ff44-131">示例</span><span class="sxs-lookup"><span data-stu-id="8ff44-131">Example</span></span>

<span data-ttu-id="8ff44-p107">下面的示例显示 XML 请求的一部分，该请求标识通过从 UTC 时差调整 -60 分钟来观测夏令时的用户。这实际上造成与 UTC 偏差 420 分钟。</span><span class="sxs-lookup"><span data-stu-id="8ff44-p107">The following example shows part of an XML request that identifies a user who observes daylight saving time by adjusting the offset from UTC by -60 minutes. This effectively makes the bias 420 minutes from UTC.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="8ff44-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="8ff44-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ff44-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="8ff44-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ff44-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="8ff44-136">Schema Name</span></span>  <br/> |<span data-ttu-id="8ff44-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="8ff44-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ff44-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="8ff44-138">Validation File</span></span>  <br/> |<span data-ttu-id="8ff44-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8ff44-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ff44-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="8ff44-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ff44-141">False</span><span class="sxs-lookup"><span data-stu-id="8ff44-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ff44-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8ff44-142">See also</span></span>

- [<span data-ttu-id="8ff44-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="8ff44-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="8ff44-144">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="8ff44-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

