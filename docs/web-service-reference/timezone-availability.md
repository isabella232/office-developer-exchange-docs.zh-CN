---
title: TimeZone （可用性）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: TimeZone 元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间的转换的信息。
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838253"
---
# <a name="timezone-availability"></a><span data-ttu-id="809fd-104">TimeZone （可用性）</span><span class="sxs-lookup"><span data-stu-id="809fd-104">TimeZone (Availability)</span></span>

<span data-ttu-id="809fd-105">**TimeZone**元素包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="809fd-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="809fd-106">此元素还包含有关标准时间和夏时制之间的转换的信息。</span><span class="sxs-lookup"><span data-stu-id="809fd-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="809fd-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="809fd-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="809fd-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="809fd-108">Attributes and elements</span></span>

<span data-ttu-id="809fd-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="809fd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="809fd-110">属性</span><span class="sxs-lookup"><span data-stu-id="809fd-110">Attributes</span></span>

<span data-ttu-id="809fd-111">无。</span><span class="sxs-lookup"><span data-stu-id="809fd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="809fd-112">子元素</span><span class="sxs-lookup"><span data-stu-id="809fd-112">Child elements</span></span>

|<span data-ttu-id="809fd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="809fd-113">**Element**</span></span>|<span data-ttu-id="809fd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="809fd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="809fd-115">斜线 (UTC)</span><span class="sxs-lookup"><span data-stu-id="809fd-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="809fd-116">从协调世界时 (UTC) 表示的常规的偏移量。</span><span class="sxs-lookup"><span data-stu-id="809fd-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="809fd-117">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="809fd-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="809fd-118">StandardTime</span><span class="sxs-lookup"><span data-stu-id="809fd-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="809fd-p104">表示与相对于 UTC（由 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。  </span><span class="sxs-lookup"><span data-stu-id="809fd-p104">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.  </span></span><br/> |
|[<span data-ttu-id="809fd-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="809fd-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="809fd-p105">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="809fd-p105">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="809fd-124">父元素</span><span class="sxs-lookup"><span data-stu-id="809fd-124">Parent elements</span></span>

|<span data-ttu-id="809fd-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="809fd-125">**Element**</span></span>|<span data-ttu-id="809fd-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="809fd-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="809fd-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="809fd-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="809fd-128">包含用于获取用户的可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="809fd-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="809fd-129">这是根元素。</span><span class="sxs-lookup"><span data-stu-id="809fd-129">This is a root element.</span></span>  <br/> <span data-ttu-id="809fd-130">GetUserAvailabilityRequest 消息中的**TimeZone**元素表示请求中的日期时间值指定的时区。</span><span class="sxs-lookup"><span data-stu-id="809fd-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="809fd-131">可用性服务返回的 DateTime 值也是在此所在的时区。</span><span class="sxs-lookup"><span data-stu-id="809fd-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="809fd-132">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="809fd-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="809fd-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="809fd-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="809fd-134">表示所在的时区设置和请求的邮箱用户的工作时间。</span><span class="sxs-lookup"><span data-stu-id="809fd-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="809fd-135">GetUserAvailabilityResponse 消息中的**TimeZone**元素表示请求的邮箱用户所在的时区设置。</span><span class="sxs-lookup"><span data-stu-id="809fd-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="809fd-136">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="809fd-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="809fd-137">备注</span><span class="sxs-lookup"><span data-stu-id="809fd-137">Remarks</span></span>

<span data-ttu-id="809fd-138">此元素是[GetUserAvailabilityRequest](getuseravailabilityrequest.md)元素中必需的。</span><span class="sxs-lookup"><span data-stu-id="809fd-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="809fd-139">此元素发生最一次或至少零次时的父元素是[WorkingHours](workinghours-ex15websvcsotherref.md)元素。</span><span class="sxs-lookup"><span data-stu-id="809fd-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="809fd-140">示例</span><span class="sxs-lookup"><span data-stu-id="809fd-140">Example</span></span>

<span data-ttu-id="809fd-141">下面的示例演示标识与客户端应用程序中的 8 小时的 UTC 偏移量 XML 请求的一部分。</span><span class="sxs-lookup"><span data-stu-id="809fd-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="809fd-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="809fd-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="809fd-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="809fd-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="809fd-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="809fd-144">Schema Name</span></span>  <br/> |<span data-ttu-id="809fd-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="809fd-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="809fd-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="809fd-146">Validation File</span></span>  <br/> |<span data-ttu-id="809fd-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="809fd-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="809fd-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="809fd-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="809fd-149">False</span><span class="sxs-lookup"><span data-stu-id="809fd-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="809fd-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="809fd-150">See also</span></span>



[<span data-ttu-id="809fd-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="809fd-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="809fd-152">Bias</span><span class="sxs-lookup"><span data-stu-id="809fd-152">Bias</span></span>](bias.md)


[<span data-ttu-id="809fd-153">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="809fd-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

