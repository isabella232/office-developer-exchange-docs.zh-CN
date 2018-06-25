---
title: 标准
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Standard
api_type:
- schema
ms.assetid: d598f0a6-e296-423f-8ce5-3da57cfd8189
description: 标准元素均表示的日期和时间更改时夏时制为标准时间的时间。
ms.openlocfilehash: 1c9be4cf35773583078bc8e16ddf44433d3ad98c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827536"
---
# <a name="standard"></a><span data-ttu-id="27e9b-103">标准</span><span class="sxs-lookup"><span data-stu-id="27e9b-103">Standard</span></span>

<span data-ttu-id="27e9b-104">**标准**元素均表示的日期和时间更改时夏时制为标准时间的时间。</span><span class="sxs-lookup"><span data-stu-id="27e9b-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

 <span data-ttu-id="27e9b-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="27e9b-105">**TimeChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27e9b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27e9b-106">Attributes and elements</span></span>

<span data-ttu-id="27e9b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27e9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27e9b-108">属性</span><span class="sxs-lookup"><span data-stu-id="27e9b-108">Attributes</span></span>

|<span data-ttu-id="27e9b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="27e9b-109">**Attribute**</span></span>|<span data-ttu-id="27e9b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="27e9b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27e9b-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="27e9b-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="27e9b-112">介绍时区的名称。</span><span class="sxs-lookup"><span data-stu-id="27e9b-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="27e9b-113">子元素</span><span class="sxs-lookup"><span data-stu-id="27e9b-113">Child elements</span></span>

|<span data-ttu-id="27e9b-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="27e9b-114">**Element**</span></span>|<span data-ttu-id="27e9b-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="27e9b-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27e9b-116">Offset</span><span class="sxs-lookup"><span data-stu-id="27e9b-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="27e9b-117">介绍从[BaseOffset](baseoffset.md)的偏移量。</span><span class="sxs-lookup"><span data-stu-id="27e9b-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="27e9b-118">**BaseOffset**元素中，以及**偏移**元素标识时间是否标准时间或夏令时。</span><span class="sxs-lookup"><span data-stu-id="27e9b-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="27e9b-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="27e9b-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="27e9b-120">介绍所在的时区转换日期相对的每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="27e9b-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="27e9b-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="27e9b-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="27e9b-122">表示当时间从标准时间或夏令时更改时的日期。</span><span class="sxs-lookup"><span data-stu-id="27e9b-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="27e9b-123">时间 (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="27e9b-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="27e9b-124">介绍当时间更改标准时间和夏时制之间的时间。</span><span class="sxs-lookup"><span data-stu-id="27e9b-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27e9b-125">父元素</span><span class="sxs-lookup"><span data-stu-id="27e9b-125">Parent elements</span></span>

|<span data-ttu-id="27e9b-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="27e9b-126">**Element**</span></span>|<span data-ttu-id="27e9b-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="27e9b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27e9b-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="27e9b-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="27e9b-129">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="27e9b-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27e9b-130">备注</span><span class="sxs-lookup"><span data-stu-id="27e9b-130">Remarks</span></span>

<span data-ttu-id="27e9b-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27e9b-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27e9b-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="27e9b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27e9b-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="27e9b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27e9b-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="27e9b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="27e9b-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="27e9b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="27e9b-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="27e9b-136">Validation File</span></span>  <br/> |<span data-ttu-id="27e9b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27e9b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27e9b-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="27e9b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="27e9b-139">False</span><span class="sxs-lookup"><span data-stu-id="27e9b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27e9b-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27e9b-140">See also</span></span>



- [<span data-ttu-id="27e9b-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27e9b-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

