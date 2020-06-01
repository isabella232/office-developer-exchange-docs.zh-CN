---
title: 偏差（UTC）
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
description: 偏置元素表示与协调世界时（UTC）的常规偏移量。 此值以分钟为单位。
ms.openlocfilehash: d95284aa28e59542d1a1ee40686163138b015702
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460244"
---
# <a name="bias-utc"></a><span data-ttu-id="8a356-104">偏差（UTC）</span><span class="sxs-lookup"><span data-stu-id="8a356-104">Bias (UTC)</span></span>

<span data-ttu-id="8a356-105">**偏置**元素表示与协调世界时（UTC）的常规偏移量。</span><span class="sxs-lookup"><span data-stu-id="8a356-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8a356-106">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="8a356-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="8a356-107">**int**</span><span class="sxs-lookup"><span data-stu-id="8a356-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8a356-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a356-108">Attributes and elements</span></span>

<span data-ttu-id="8a356-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a356-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a356-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8a356-110">Attributes</span></span>

<span data-ttu-id="8a356-111">无。</span><span class="sxs-lookup"><span data-stu-id="8a356-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a356-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8a356-112">Child elements</span></span>

<span data-ttu-id="8a356-113">无。</span><span class="sxs-lookup"><span data-stu-id="8a356-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a356-114">父元素</span><span class="sxs-lookup"><span data-stu-id="8a356-114">Parent elements</span></span>

|<span data-ttu-id="8a356-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a356-115">**Element**</span></span>|<span data-ttu-id="8a356-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a356-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a356-117">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="8a356-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="8a356-118">标识请求的日期时间信息的容器。</span><span class="sxs-lookup"><span data-stu-id="8a356-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="8a356-119">此元素包含有关标准时间和夏时制之间的过渡的信息。</span><span class="sxs-lookup"><span data-stu-id="8a356-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="8a356-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8a356-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a356-121">文本值</span><span class="sxs-lookup"><span data-stu-id="8a356-121">Text value</span></span>

<span data-ttu-id="8a356-p104">文本值是必需的。文本值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="8a356-p104">A text value is required. The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a356-124">说明</span><span class="sxs-lookup"><span data-stu-id="8a356-124">Remarks</span></span>

<span data-ttu-id="8a356-125">架构中的第二个[偏向](bias.md)元素表示与协调世界时（UTC）偏移量的偏移量。</span><span class="sxs-lookup"><span data-stu-id="8a356-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8a356-126">示例</span><span class="sxs-lookup"><span data-stu-id="8a356-126">Example</span></span>

<span data-ttu-id="8a356-127">下面的示例显示了 XML 请求的一部分，它在客户端应用程序上标识从 UTC 到 UTC 的偏移量为8小时。</span><span class="sxs-lookup"><span data-stu-id="8a356-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="8a356-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a356-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a356-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a356-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a356-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a356-130">Schema Name</span></span>  <br/> |<span data-ttu-id="8a356-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="8a356-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="8a356-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a356-132">Validation File</span></span>  <br/> |<span data-ttu-id="8a356-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8a356-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a356-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a356-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a356-135">False</span><span class="sxs-lookup"><span data-stu-id="8a356-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a356-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a356-136">See also</span></span>

- [<span data-ttu-id="8a356-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="8a356-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="8a356-138">偏置</span><span class="sxs-lookup"><span data-stu-id="8a356-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="8a356-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="8a356-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

