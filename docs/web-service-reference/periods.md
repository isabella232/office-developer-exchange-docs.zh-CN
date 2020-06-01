---
title: 课时
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: 时段元素表示定义时区的不同阶段的时间偏移量的一组句点。
ms.openlocfilehash: 773457a6e4c0237eaeaf23109a7022427cc7dd0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467772"
---
# <a name="periods"></a><span data-ttu-id="9ab52-103">课时</span><span class="sxs-lookup"><span data-stu-id="9ab52-103">Periods</span></span>

<span data-ttu-id="9ab52-104">**时段**元素表示定义时区的不同阶段的时间偏移量的一组句点。</span><span class="sxs-lookup"><span data-stu-id="9ab52-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="9ab52-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="9ab52-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ab52-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ab52-106">Attributes and elements</span></span>

<span data-ttu-id="9ab52-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ab52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ab52-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9ab52-108">Attributes</span></span>

<span data-ttu-id="9ab52-109">无。</span><span class="sxs-lookup"><span data-stu-id="9ab52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ab52-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9ab52-110">Child elements</span></span>

|<span data-ttu-id="9ab52-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ab52-111">**Element**</span></span>|<span data-ttu-id="9ab52-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ab52-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ab52-113">Period</span><span class="sxs-lookup"><span data-stu-id="9ab52-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="9ab52-114">定义时区的特定阶段的名称、时间偏移和唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="9ab52-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ab52-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9ab52-115">Parent elements</span></span>

|<span data-ttu-id="9ab52-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ab52-116">**Element**</span></span>|<span data-ttu-id="9ab52-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ab52-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ab52-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="9ab52-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="9ab52-119">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的开始时间的时区。</span><span class="sxs-lookup"><span data-stu-id="9ab52-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="9ab52-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="9ab52-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="9ab52-121">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的结束时间的时区。</span><span class="sxs-lookup"><span data-stu-id="9ab52-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="9ab52-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="9ab52-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="9ab52-123">定义时区。</span><span class="sxs-lookup"><span data-stu-id="9ab52-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ab52-124">备注</span><span class="sxs-lookup"><span data-stu-id="9ab52-124">Remarks</span></span>

<span data-ttu-id="9ab52-125">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9ab52-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ab52-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ab52-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ab52-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ab52-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ab52-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ab52-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9ab52-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="9ab52-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ab52-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ab52-130">Validation File</span></span>  <br/> |<span data-ttu-id="9ab52-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ab52-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ab52-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ab52-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ab52-133">False</span><span class="sxs-lookup"><span data-stu-id="9ab52-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ab52-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ab52-134">See also</span></span>



- [<span data-ttu-id="9ab52-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9ab52-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

