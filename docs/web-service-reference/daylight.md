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
description: 夏令元素表示时间从标准时间更改为夏时制的日期和时间。
ms.openlocfilehash: bf2041cb4677f837ddb5b399041f1c19a7b5f577
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457457"
---
# <a name="daylight"></a><span data-ttu-id="f8af7-103">夏时制</span><span class="sxs-lookup"><span data-stu-id="f8af7-103">Daylight</span></span>

<span data-ttu-id="f8af7-104">**夏令**元素表示时间从标准时间更改为夏时制的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="f8af7-104">The **Daylight** element represents the date and time when the time changes from standard time to daylight saving time.</span></span> 
  
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

<span data-ttu-id="f8af7-105">**TimeChangeType**</span><span class="sxs-lookup"><span data-stu-id="f8af7-105">**TimeChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f8af7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f8af7-106">Attributes and elements</span></span>

<span data-ttu-id="f8af7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8af7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8af7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f8af7-108">Attributes</span></span>

|<span data-ttu-id="f8af7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f8af7-109">**Attribute**</span></span>|<span data-ttu-id="f8af7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8af7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8af7-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="f8af7-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="f8af7-112">描述时区的名称。</span><span class="sxs-lookup"><span data-stu-id="f8af7-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8af7-113">子元素</span><span class="sxs-lookup"><span data-stu-id="f8af7-113">Child elements</span></span>

|<span data-ttu-id="f8af7-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="f8af7-114">**Element**</span></span>|<span data-ttu-id="f8af7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8af7-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8af7-116">Offset</span><span class="sxs-lookup"><span data-stu-id="f8af7-116">Offset</span></span>](offset.md) <br/> |<span data-ttu-id="f8af7-117">描述[BaseOffset](baseoffset.md)中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="f8af7-117">Describes the offset from the [BaseOffset](baseoffset.md).</span></span> <span data-ttu-id="f8af7-118">除此偏移量之外的基础偏移根据其是标准还是夏时制来标识时间。</span><span class="sxs-lookup"><span data-stu-id="f8af7-118">The base offset in addition to this offset identifies the time according to whether it is standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="f8af7-119">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="f8af7-119">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="f8af7-120">描述时区转换日期模式的相对年定期模式。</span><span class="sxs-lookup"><span data-stu-id="f8af7-120">Describes a relative yearly recurrence pattern for a time zone transition date pattern.</span></span>  <br/> |
|[<span data-ttu-id="f8af7-121">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="f8af7-121">AbsoluteDate</span></span>](absolutedate.md) <br/> |<span data-ttu-id="f8af7-122">表示从标准或夏时制的时间更改的日期。</span><span class="sxs-lookup"><span data-stu-id="f8af7-122">Represents the date when the time changes from standard or daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="f8af7-123">Time （TimeChangeType）</span><span class="sxs-lookup"><span data-stu-id="f8af7-123">Time (TimeChangeType)</span></span>](time-timechangetype.md) <br/> |<span data-ttu-id="f8af7-124">描述在标准时间和夏时制时间之间的时间更改时间。</span><span class="sxs-lookup"><span data-stu-id="f8af7-124">Describes the time when the time changes between standard time and daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8af7-125">父元素</span><span class="sxs-lookup"><span data-stu-id="f8af7-125">Parent elements</span></span>

|<span data-ttu-id="f8af7-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="f8af7-126">**Element**</span></span>|<span data-ttu-id="f8af7-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8af7-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8af7-128">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="f8af7-128">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="f8af7-129">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="f8af7-129">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8af7-130">说明</span><span class="sxs-lookup"><span data-stu-id="f8af7-130">Remarks</span></span>

<span data-ttu-id="f8af7-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f8af7-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8af7-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="f8af7-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8af7-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="f8af7-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8af7-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="f8af7-134">Schema Name</span></span>  <br/> |<span data-ttu-id="f8af7-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="f8af7-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8af7-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="f8af7-136">Validation File</span></span>  <br/> |<span data-ttu-id="f8af7-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8af7-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8af7-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="f8af7-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8af7-139">False</span><span class="sxs-lookup"><span data-stu-id="f8af7-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8af7-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8af7-140">See also</span></span>

- [<span data-ttu-id="f8af7-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f8af7-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

