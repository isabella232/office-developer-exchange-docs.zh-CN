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
description: RelativeYearlyRecurrence 元素描述相对年定期模式。
ms.openlocfilehash: 2abe09ddfe52c24211ef5d0a392ddecaf15bf7bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456724"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="78e5d-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="78e5d-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="78e5d-104">**RelativeYearlyRecurrence**元素描述相对年定期模式。</span><span class="sxs-lookup"><span data-stu-id="78e5d-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="78e5d-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="78e5d-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78e5d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="78e5d-106">Attributes and elements</span></span>

<span data-ttu-id="78e5d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="78e5d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78e5d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="78e5d-108">Attributes</span></span>

<span data-ttu-id="78e5d-109">无。</span><span class="sxs-lookup"><span data-stu-id="78e5d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78e5d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="78e5d-110">Child elements</span></span>

|<span data-ttu-id="78e5d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="78e5d-111">**Element**</span></span>|<span data-ttu-id="78e5d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="78e5d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78e5d-113">DaysOfWeek （DayOfWeekType）</span><span class="sxs-lookup"><span data-stu-id="78e5d-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="78e5d-114">介绍在项目定期模式中使用的一周中的各天。</span><span class="sxs-lookup"><span data-stu-id="78e5d-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="78e5d-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="78e5d-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="78e5d-116">介绍在相对年定期模式中使用某个月中的哪一周。</span><span class="sxs-lookup"><span data-stu-id="78e5d-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="78e5d-117">月（项目定期）</span><span class="sxs-lookup"><span data-stu-id="78e5d-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="78e5d-118">描述每年定期项目发生的月份。</span><span class="sxs-lookup"><span data-stu-id="78e5d-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78e5d-119">父元素</span><span class="sxs-lookup"><span data-stu-id="78e5d-119">Parent elements</span></span>

|<span data-ttu-id="78e5d-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="78e5d-120">**Element**</span></span>|<span data-ttu-id="78e5d-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="78e5d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78e5d-122">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="78e5d-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="78e5d-123">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="78e5d-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="78e5d-124">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="78e5d-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="78e5d-125">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="78e5d-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="78e5d-126">标准</span><span class="sxs-lookup"><span data-stu-id="78e5d-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="78e5d-127">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="78e5d-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="78e5d-128">夏时制</span><span class="sxs-lookup"><span data-stu-id="78e5d-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="78e5d-129">表示时间从标准时间更改为夏时制的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="78e5d-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78e5d-130">说明</span><span class="sxs-lookup"><span data-stu-id="78e5d-130">Remarks</span></span>

<span data-ttu-id="78e5d-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="78e5d-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78e5d-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="78e5d-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78e5d-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="78e5d-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78e5d-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="78e5d-134">Schema Name</span></span>  <br/> |<span data-ttu-id="78e5d-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="78e5d-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="78e5d-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="78e5d-136">Validation File</span></span>  <br/> |<span data-ttu-id="78e5d-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78e5d-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78e5d-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="78e5d-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="78e5d-139">False</span><span class="sxs-lookup"><span data-stu-id="78e5d-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78e5d-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="78e5d-140">See also</span></span>



- [<span data-ttu-id="78e5d-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="78e5d-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

