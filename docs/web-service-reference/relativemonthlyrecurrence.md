---
title: RelativeMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeMonthlyRecurrence
api_type:
- schema
ms.assetid: a76595db-7460-44ac-ac2a-53241caa33a7
description: RelativeMonthlyRecurrence 元素描述相对的每月定期模式。
ms.openlocfilehash: 9b695052c38e2693946837bf99f03baea093df08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827053"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="cd809-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cd809-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="cd809-104">**RelativeMonthlyRecurrence**元素描述相对的每月定期模式。</span><span class="sxs-lookup"><span data-stu-id="cd809-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="cd809-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="cd809-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd809-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd809-106">Attributes and elements</span></span>

<span data-ttu-id="cd809-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd809-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd809-108">属性</span><span class="sxs-lookup"><span data-stu-id="cd809-108">Attributes</span></span>

<span data-ttu-id="cd809-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd809-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd809-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd809-110">Child elements</span></span>

|<span data-ttu-id="cd809-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cd809-111">**Element**</span></span>|<span data-ttu-id="cd809-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cd809-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd809-113">Interval</span><span class="sxs-lookup"><span data-stu-id="cd809-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="cd809-114">定义两个连续每月定期模式项之间的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="cd809-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="cd809-115">此值的范围是 1 到 99。</span><span class="sxs-lookup"><span data-stu-id="cd809-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="cd809-116">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="cd809-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="cd809-117">介绍一周的哪几天所相对的每月定期模式中。</span><span class="sxs-lookup"><span data-stu-id="cd809-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="cd809-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="cd809-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="cd809-119">介绍在相对的每月定期模式中使用哪一周。</span><span class="sxs-lookup"><span data-stu-id="cd809-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd809-120">父元素</span><span class="sxs-lookup"><span data-stu-id="cd809-120">Parent elements</span></span>

|<span data-ttu-id="cd809-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="cd809-121">**Element**</span></span>|<span data-ttu-id="cd809-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="cd809-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd809-123">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="cd809-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="cd809-124">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="cd809-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="cd809-125">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="cd809-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="cd809-126">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="cd809-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd809-127">备注</span><span class="sxs-lookup"><span data-stu-id="cd809-127">Remarks</span></span>

<span data-ttu-id="cd809-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd809-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd809-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd809-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd809-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd809-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd809-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd809-131">Schema Name</span></span>  <br/> |<span data-ttu-id="cd809-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="cd809-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd809-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd809-133">Validation File</span></span>  <br/> |<span data-ttu-id="cd809-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd809-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd809-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd809-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd809-136">False</span><span class="sxs-lookup"><span data-stu-id="cd809-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd809-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd809-137">See also</span></span>



- [<span data-ttu-id="cd809-138">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cd809-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

