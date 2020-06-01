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
description: Standard 元素表示时间从夏时制更改为标准时间的日期和时间。
ms.openlocfilehash: 1214a1debb53c9a31ca7c92a0c9e5c0722960d75
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467562"
---
# <a name="standard"></a><span data-ttu-id="2c2a7-103">标准</span><span class="sxs-lookup"><span data-stu-id="2c2a7-103">Standard</span></span>

<span data-ttu-id="2c2a7-104">**Standard**元素表示时间从夏时制更改为标准时间的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-104">The **Standard** element represents the date and time when the time changes from daylight saving time to standard time.</span></span> 
  
```xml
<Standard TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Standard>
```

```xml
<Standard TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Standard>
```

<span data-ttu-id="2c2a7-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2c2a7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2c2a7-106">Attributes and elements</span></span>

<span data-ttu-id="2c2a7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c2a7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2c2a7-108">Attributes</span></span>

|<span data-ttu-id="2c2a7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-109">**Attribute**</span></span>|<span data-ttu-id="2c2a7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c2a7-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="2c2a7-112">描述时区的名称。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2c2a7-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2c2a7-113">Child elements</span></span>

|<span data-ttu-id="2c2a7-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-114">**Element**</span></span>|<span data-ttu-id="2c2a7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c2a7-116">Offset</span><span class="sxs-lookup"><span data-stu-id="2c2a7-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="2c2a7-117">描述[BaseOffset](baseoffset.md)中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="2c2a7-118">**Offset**元素与**BaseOffset**元素一起标识时间是标准时间还是夏时制。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-118">Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2c2a7-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2c2a7-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="2c2a7-120">描述时区转换日期的相对年定期模式。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-120">Describes a relative yearly recurrence pattern for a time zone transition date.</span></span>  <br/> |
|[<span data-ttu-id="2c2a7-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="2c2a7-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="2c2a7-122">表示从标准时间或夏时制的时间更改的日期。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-122">Represents the date when the time changes from standard time or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2c2a7-123">Time （TimeChangeType）</span><span class="sxs-lookup"><span data-stu-id="2c2a7-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="2c2a7-124">描述在标准时间和夏时制时间之间的时间更改时间。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2c2a7-125">父元素</span><span class="sxs-lookup"><span data-stu-id="2c2a7-125">Parent elements</span></span>

|<span data-ttu-id="2c2a7-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-126">**Element**</span></span>|<span data-ttu-id="2c2a7-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c2a7-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c2a7-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="2c2a7-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="2c2a7-129">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c2a7-130">说明</span><span class="sxs-lookup"><span data-stu-id="2c2a7-130">Remarks</span></span>

<span data-ttu-id="2c2a7-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2c2a7-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c2a7-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="2c2a7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c2a7-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="2c2a7-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c2a7-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="2c2a7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="2c2a7-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="2c2a7-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c2a7-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="2c2a7-136">Validation File</span></span>  <br/> |<span data-ttu-id="2c2a7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c2a7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c2a7-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="2c2a7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c2a7-139">False</span><span class="sxs-lookup"><span data-stu-id="2c2a7-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c2a7-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c2a7-140">See also</span></span>

- [<span data-ttu-id="2c2a7-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2c2a7-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

