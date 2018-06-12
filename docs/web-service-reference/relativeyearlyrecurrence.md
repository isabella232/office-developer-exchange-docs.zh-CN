---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: RelativeYearlyRecurrence 元素描述相对的每年定期模式。
ms.openlocfilehash: ce8d2b134ce1fa34cbce8bd2fa921cab18d908a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827057"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="83262-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="83262-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="83262-104">**RelativeYearlyRecurrence**元素描述相对的每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="83262-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="83262-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="83262-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83262-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="83262-106">Attributes and elements</span></span>

<span data-ttu-id="83262-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="83262-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83262-108">属性</span><span class="sxs-lookup"><span data-stu-id="83262-108">Attributes</span></span>

<span data-ttu-id="83262-109">无。</span><span class="sxs-lookup"><span data-stu-id="83262-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83262-110">子元素</span><span class="sxs-lookup"><span data-stu-id="83262-110">Child elements</span></span>

|<span data-ttu-id="83262-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="83262-111">**Element**</span></span>|<span data-ttu-id="83262-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="83262-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83262-113">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="83262-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="83262-114">描述项定期模式中使用内容的星期数。</span><span class="sxs-lookup"><span data-stu-id="83262-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="83262-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="83262-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="83262-116">介绍在相对的每年定期模式中使用一个月中的周。</span><span class="sxs-lookup"><span data-stu-id="83262-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="83262-117">每月 （项重复）</span><span class="sxs-lookup"><span data-stu-id="83262-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="83262-118">介绍当每年定期项目发生的月份。</span><span class="sxs-lookup"><span data-stu-id="83262-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83262-119">父元素</span><span class="sxs-lookup"><span data-stu-id="83262-119">Parent elements</span></span>

|<span data-ttu-id="83262-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="83262-120">**Element**</span></span>|<span data-ttu-id="83262-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="83262-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83262-122">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="83262-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="83262-123">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="83262-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="83262-124">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="83262-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="83262-125">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="83262-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="83262-126">标准</span><span class="sxs-lookup"><span data-stu-id="83262-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="83262-127">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="83262-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="83262-128">夏时制</span><span class="sxs-lookup"><span data-stu-id="83262-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="83262-129">表示的日期和时间更改时从标准时间到夏时制的时间。</span><span class="sxs-lookup"><span data-stu-id="83262-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83262-130">备注</span><span class="sxs-lookup"><span data-stu-id="83262-130">Remarks</span></span>

<span data-ttu-id="83262-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="83262-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83262-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="83262-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83262-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="83262-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83262-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="83262-134">Schema Name</span></span>  <br/> |<span data-ttu-id="83262-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="83262-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="83262-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="83262-136">Validation File</span></span>  <br/> |<span data-ttu-id="83262-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83262-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83262-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="83262-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="83262-139">False</span><span class="sxs-lookup"><span data-stu-id="83262-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83262-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83262-140">See also</span></span>



- [<span data-ttu-id="83262-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="83262-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
