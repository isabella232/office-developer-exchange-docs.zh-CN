---
title: 夏时制
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: 夏时制元素均表示的日期和时间更改时从标准时间到夏时制的时间。
ms.openlocfilehash: cdb6ed305f1d77a73b952f8c659991f3b2a8df7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753757"
---
# <a name="daylight"></a><span data-ttu-id="a85f4-103">夏时制</span><span class="sxs-lookup"><span data-stu-id="a85f4-103">Daylight</span></span>

<span data-ttu-id="a85f4-104">**夏时制**元素均表示的日期和时间更改时从标准时间到夏时制的时间。</span><span class="sxs-lookup"><span data-stu-id="a85f4-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

<span data-ttu-id="a85f4-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="a85f4-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a85f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a85f4-106">Attributes and elements</span></span>

<span data-ttu-id="a85f4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a85f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a85f4-108">属性</span><span class="sxs-lookup"><span data-stu-id="a85f4-108">Attributes</span></span>

|<span data-ttu-id="a85f4-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="a85f4-109">**Attribute**</span></span>|<span data-ttu-id="a85f4-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a85f4-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="a85f4-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="a85f4-112">介绍时区的名称。</span><span class="sxs-lookup"><span data-stu-id="a85f4-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a85f4-113">子元素</span><span class="sxs-lookup"><span data-stu-id="a85f4-113">Child elements</span></span>

|<span data-ttu-id="a85f4-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="a85f4-114">**Element**</span></span>|<span data-ttu-id="a85f4-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f4-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a85f4-116">Offset</span><span class="sxs-lookup"><span data-stu-id="a85f4-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="a85f4-117">介绍从[BaseOffset](baseoffset.md)的偏移量。</span><span class="sxs-lookup"><span data-stu-id="a85f4-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="a85f4-118">基线偏移除了此偏移量标识根据是否是标准或夏时制的时间。</span><span class="sxs-lookup"><span data-stu-id="a85f4-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="a85f4-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="a85f4-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="a85f4-120">介绍所在的时区转换日期模式相对每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="a85f4-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="a85f4-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="a85f4-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="a85f4-122">表示从标准版或夏时制时间的更改时的日期。</span><span class="sxs-lookup"><span data-stu-id="a85f4-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="a85f4-123">时间 (TimeChangeType)</span><span class="sxs-lookup"><span data-stu-id="a85f4-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="a85f4-124">介绍当时间更改标准时间和夏时制之间的时间。</span><span class="sxs-lookup"><span data-stu-id="a85f4-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a85f4-125">父元素</span><span class="sxs-lookup"><span data-stu-id="a85f4-125">Parent elements</span></span>

|<span data-ttu-id="a85f4-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="a85f4-126">**Element**</span></span>|<span data-ttu-id="a85f4-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="a85f4-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a85f4-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="a85f4-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="a85f4-129">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="a85f4-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a85f4-130">备注</span><span class="sxs-lookup"><span data-stu-id="a85f4-130">Remarks</span></span>

<span data-ttu-id="a85f4-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a85f4-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a85f4-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="a85f4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a85f4-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="a85f4-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a85f4-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="a85f4-134">Schema Name</span></span>  <br/> |<span data-ttu-id="a85f4-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="a85f4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="a85f4-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="a85f4-136">Validation File</span></span>  <br/> |<span data-ttu-id="a85f4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a85f4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a85f4-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="a85f4-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="a85f4-139">False</span><span class="sxs-lookup"><span data-stu-id="a85f4-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a85f4-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a85f4-140">See also</span></span>

- [<span data-ttu-id="a85f4-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a85f4-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

