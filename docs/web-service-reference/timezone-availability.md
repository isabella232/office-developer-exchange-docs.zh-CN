---
title: 时区（可用性）
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
description: 时区元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间转换的信息。
ms.openlocfilehash: ba4b0a4805dba54450e01e89c5e9ef746404b716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460272"
---
# <a name="timezone-availability"></a><span data-ttu-id="4b565-104">时区（可用性）</span><span class="sxs-lookup"><span data-stu-id="4b565-104">TimeZone (Availability)</span></span>

<span data-ttu-id="4b565-105">**时区**元素包含标识时区信息的元素。</span><span class="sxs-lookup"><span data-stu-id="4b565-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="4b565-106">此元素还包含有关标准时间和夏时制之间转换的信息。</span><span class="sxs-lookup"><span data-stu-id="4b565-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="4b565-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="4b565-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b565-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b565-108">Attributes and elements</span></span>

<span data-ttu-id="4b565-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b565-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b565-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="4b565-110">Attributes</span></span>

<span data-ttu-id="4b565-111">无。</span><span class="sxs-lookup"><span data-stu-id="4b565-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b565-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4b565-112">Child elements</span></span>

|<span data-ttu-id="4b565-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b565-113">**Element**</span></span>|<span data-ttu-id="4b565-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b565-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b565-115">偏差（UTC）</span><span class="sxs-lookup"><span data-stu-id="4b565-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="4b565-116">表示与协调世界时（UTC）的常规偏移量。</span><span class="sxs-lookup"><span data-stu-id="4b565-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="4b565-117">此值以分钟为单位。</span><span class="sxs-lookup"><span data-stu-id="4b565-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="4b565-118">StandardTime</span><span class="sxs-lookup"><span data-stu-id="4b565-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="4b565-p104">表示与相对于 UTC（由 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。  </span><span class="sxs-lookup"><span data-stu-id="4b565-p104">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element. This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.  </span></span><br/> |
|[<span data-ttu-id="4b565-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="4b565-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="4b565-p105">表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  </span><span class="sxs-lookup"><span data-stu-id="4b565-p105">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed. This element also contains information about when the transition to daylight saving time from standard time occurs.  </span></span><br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b565-124">父元素</span><span class="sxs-lookup"><span data-stu-id="4b565-124">Parent elements</span></span>

|<span data-ttu-id="4b565-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b565-125">**Element**</span></span>|<span data-ttu-id="4b565-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b565-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b565-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="4b565-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="4b565-128">包含用于获取用户可用性信息的参数。</span><span class="sxs-lookup"><span data-stu-id="4b565-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="4b565-129">这是一个根元素。</span><span class="sxs-lookup"><span data-stu-id="4b565-129">This is a root element.</span></span>  <br/> <span data-ttu-id="4b565-130">GetUserAvailabilityRequest 消息中的**时区**元素表示在其中指定请求中的 DateTime 值的时区。</span><span class="sxs-lookup"><span data-stu-id="4b565-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="4b565-131">可用性服务返回的日期/时间值也在此时区中。</span><span class="sxs-lookup"><span data-stu-id="4b565-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="4b565-132">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="4b565-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="4b565-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="4b565-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4b565-134">表示所请求的邮箱用户的时区设置和工作时间。</span><span class="sxs-lookup"><span data-stu-id="4b565-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="4b565-135">GetUserAvailabilityResponse 消息中的**时区**元素表示请求的邮箱用户的时区设置。</span><span class="sxs-lookup"><span data-stu-id="4b565-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="4b565-136">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="4b565-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b565-137">备注</span><span class="sxs-lookup"><span data-stu-id="4b565-137">Remarks</span></span>

<span data-ttu-id="4b565-138">在[GetUserAvailabilityRequest](getuseravailabilityrequest.md)元素中，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="4b565-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="4b565-139">当 parent 元素是[WorkingHours](workinghours-ex15websvcsotherref.md)元素时，此元素最多执行一次或至少出现零次。</span><span class="sxs-lookup"><span data-stu-id="4b565-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4b565-140">示例</span><span class="sxs-lookup"><span data-stu-id="4b565-140">Example</span></span>

<span data-ttu-id="4b565-141">下面的示例显示了 XML 请求的一部分，它标识客户端应用程序中的 UTC 时间为8小时的偏移量。</span><span class="sxs-lookup"><span data-stu-id="4b565-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="4b565-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="4b565-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b565-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="4b565-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4b565-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="4b565-144">Schema Name</span></span>  <br/> |<span data-ttu-id="4b565-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="4b565-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="4b565-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="4b565-146">Validation File</span></span>  <br/> |<span data-ttu-id="4b565-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4b565-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4b565-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="4b565-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b565-149">False</span><span class="sxs-lookup"><span data-stu-id="4b565-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b565-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b565-150">See also</span></span>



[<span data-ttu-id="4b565-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="4b565-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="4b565-152">偏置</span><span class="sxs-lookup"><span data-stu-id="4b565-152">Bias</span></span>](bias.md)


[<span data-ttu-id="4b565-153">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="4b565-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

