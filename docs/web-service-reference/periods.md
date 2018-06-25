---
title: 时间段
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
description: 阶段元素均表示一个数组定义的时间偏移量的时区的不同阶段的时间段。
ms.openlocfilehash: f2f9cf7c724b453d2b1975fcf72c55bc02caa54b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826729"
---
# <a name="periods"></a><span data-ttu-id="cbdde-103">时间段</span><span class="sxs-lookup"><span data-stu-id="cbdde-103">Periods</span></span>

<span data-ttu-id="cbdde-104">**阶段**元素均表示一个数组定义的时间偏移量的时区的不同阶段的时间段。</span><span class="sxs-lookup"><span data-stu-id="cbdde-104">The **Periods** element represents an array of periods that define the time offset at different stages of the time zone.</span></span> 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 <span data-ttu-id="cbdde-105">**NonEmptyArrayOfPeriodsType**</span><span class="sxs-lookup"><span data-stu-id="cbdde-105">**NonEmptyArrayOfPeriodsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbdde-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbdde-106">Attributes and elements</span></span>

<span data-ttu-id="cbdde-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbdde-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbdde-108">属性</span><span class="sxs-lookup"><span data-stu-id="cbdde-108">Attributes</span></span>

<span data-ttu-id="cbdde-109">无。</span><span class="sxs-lookup"><span data-stu-id="cbdde-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbdde-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cbdde-110">Child elements</span></span>

|<span data-ttu-id="cbdde-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbdde-111">**Element**</span></span>|<span data-ttu-id="cbdde-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbdde-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbdde-113">Period</span><span class="sxs-lookup"><span data-stu-id="cbdde-113">Period</span></span>](period.md) <br/> |<span data-ttu-id="cbdde-114">为特定的时区的阶段定义名称、 时间偏移和唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="cbdde-114">Defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbdde-115">父元素</span><span class="sxs-lookup"><span data-stu-id="cbdde-115">Parent elements</span></span>

|<span data-ttu-id="cbdde-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbdde-116">**Element**</span></span>|<span data-ttu-id="cbdde-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbdde-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbdde-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="cbdde-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="cbdde-119">定义开始时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="cbdde-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="cbdde-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="cbdde-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="cbdde-121">定义的结束时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="cbdde-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="cbdde-122">时区定义</span><span class="sxs-lookup"><span data-stu-id="cbdde-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="cbdde-123">定义时区。</span><span class="sxs-lookup"><span data-stu-id="cbdde-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbdde-124">注解</span><span class="sxs-lookup"><span data-stu-id="cbdde-124">Remarks</span></span>

<span data-ttu-id="cbdde-125">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cbdde-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbdde-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbdde-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbdde-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbdde-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cbdde-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbdde-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cbdde-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="cbdde-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="cbdde-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbdde-130">Validation File</span></span>  <br/> |<span data-ttu-id="cbdde-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cbdde-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cbdde-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbdde-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbdde-133">False</span><span class="sxs-lookup"><span data-stu-id="cbdde-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbdde-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbdde-134">See also</span></span>



- [<span data-ttu-id="cbdde-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cbdde-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

