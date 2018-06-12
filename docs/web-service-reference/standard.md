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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827536"
---
# <a name="standard"></a><span data-ttu-id="fbd5a-103">标准</span><span class="sxs-lookup"><span data-stu-id="fbd5a-103">Standard</span></span>

<span data-ttu-id="fbd5a-104">**标准**元素均表示的日期和时间更改时夏时制为标准时间的时间。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

 <span data-ttu-id="fbd5a-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-105">**TimeChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbd5a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fbd5a-106">Attributes and elements</span></span>

<span data-ttu-id="fbd5a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbd5a-108">属性</span><span class="sxs-lookup"><span data-stu-id="fbd5a-108">Attributes</span></span>

|<span data-ttu-id="fbd5a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-109">**Attribute**</span></span>|<span data-ttu-id="fbd5a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fbd5a-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="fbd5a-112">介绍时区的名称。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbd5a-113">子元素</span><span class="sxs-lookup"><span data-stu-id="fbd5a-113">Child elements</span></span>

|<span data-ttu-id="fbd5a-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-114">**Element**</span></span>|<span data-ttu-id="fbd5a-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd5a-116">Offset</span><span class="sxs-lookup"><span data-stu-id="fbd5a-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="fbd5a-117">介绍从[BaseOffset](baseoffset.md)的偏移量。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="fbd5a-118">**BaseOffset**元素中，以及**偏移**元素标识时间是否标准时间或夏令时。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="fbd5a-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="fbd5a-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="fbd5a-120">介绍所在的时区转换日期相对的每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="fbd5a-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="fbd5a-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="fbd5a-122">表示当时间从标准时间或夏令时更改时的日期。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="fbd5a-123">时间 (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="fbd5a-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="fbd5a-124">介绍当时间更改标准时间和夏时制之间的时间。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbd5a-125">父元素</span><span class="sxs-lookup"><span data-stu-id="fbd5a-125">Parent elements</span></span>

|<span data-ttu-id="fbd5a-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-126">**Element**</span></span>|<span data-ttu-id="fbd5a-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="fbd5a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbd5a-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="fbd5a-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="fbd5a-129">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbd5a-130">备注</span><span class="sxs-lookup"><span data-stu-id="fbd5a-130">Remarks</span></span>

<span data-ttu-id="fbd5a-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fbd5a-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbd5a-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="fbd5a-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbd5a-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="fbd5a-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbd5a-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="fbd5a-134">Schema Name</span></span>  <br/> |<span data-ttu-id="fbd5a-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="fbd5a-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbd5a-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="fbd5a-136">Validation File</span></span>  <br/> |<span data-ttu-id="fbd5a-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbd5a-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbd5a-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="fbd5a-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbd5a-139">False</span><span class="sxs-lookup"><span data-stu-id="fbd5a-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbd5a-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fbd5a-140">See also</span></span>



- [<span data-ttu-id="fbd5a-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fbd5a-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

