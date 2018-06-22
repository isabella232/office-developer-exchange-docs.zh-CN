---
title: 斜线 (UTC)
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
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: Bias 元素表示的常规的偏移量与协调世界时 (UTC)。 此值以分钟为单位。
ms.openlocfilehash: 43613593565ca15be97bd2a98dbe5c512dbe5fc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753327"
---
# <a name="bias-utc"></a><span data-ttu-id="67683-104">斜线 (UTC)</span><span class="sxs-lookup"><span data-stu-id="67683-104">Bias (UTC)</span></span>

<span data-ttu-id="67683-105">**Bias**元素表示的常规的偏移量与协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="67683-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="67683-106">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="67683-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="67683-107">**int**</span><span class="sxs-lookup"><span data-stu-id="67683-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="67683-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67683-108">Attributes and elements</span></span>

<span data-ttu-id="67683-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67683-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67683-110">属性</span><span class="sxs-lookup"><span data-stu-id="67683-110">Attributes</span></span>

<span data-ttu-id="67683-111">无。</span><span class="sxs-lookup"><span data-stu-id="67683-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67683-112">子元素</span><span class="sxs-lookup"><span data-stu-id="67683-112">Child elements</span></span>

<span data-ttu-id="67683-113">无。</span><span class="sxs-lookup"><span data-stu-id="67683-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="67683-114">父元素</span><span class="sxs-lookup"><span data-stu-id="67683-114">Parent elements</span></span>

|<span data-ttu-id="67683-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="67683-115">**Element**</span></span>|<span data-ttu-id="67683-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="67683-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67683-117">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="67683-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="67683-118">标识的请求的日期时间信息的容器。</span><span class="sxs-lookup"><span data-stu-id="67683-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="67683-119">此元素包含有关标准时间和夏时制之间的转换的信息。</span><span class="sxs-lookup"><span data-stu-id="67683-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="67683-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="67683-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="67683-121">文本值</span><span class="sxs-lookup"><span data-stu-id="67683-121">Text value</span></span>

<span data-ttu-id="67683-p104">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="67683-p104">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67683-124">备注</span><span class="sxs-lookup"><span data-stu-id="67683-124">Remarks</span></span>

<span data-ttu-id="67683-125">架构中的第二个[Bias](bias.md)元素表示从协调世界时 (UTC) 偏移的偏移量。</span><span class="sxs-lookup"><span data-stu-id="67683-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="67683-126">示例</span><span class="sxs-lookup"><span data-stu-id="67683-126">Example</span></span>

<span data-ttu-id="67683-127">下面的示例演示标识偏移量 8 小时从 UTC 的客户端应用程序 XML 请求的一部分。</span><span class="sxs-lookup"><span data-stu-id="67683-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="67683-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="67683-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67683-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="67683-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67683-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="67683-130">Schema Name</span></span>  <br/> |<span data-ttu-id="67683-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="67683-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="67683-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="67683-132">Validation File</span></span>  <br/> |<span data-ttu-id="67683-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67683-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67683-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="67683-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="67683-135">False</span><span class="sxs-lookup"><span data-stu-id="67683-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67683-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67683-136">See also</span></span>

- [<span data-ttu-id="67683-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="67683-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="67683-138">Bias</span><span class="sxs-lookup"><span data-stu-id="67683-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="67683-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="67683-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

