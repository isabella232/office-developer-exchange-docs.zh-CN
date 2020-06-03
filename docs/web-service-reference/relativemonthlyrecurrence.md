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
description: RelativeMonthlyRecurrence 元素描述相对月定期模式。
ms.openlocfilehash: 90aa0e43684bfb09a3e13cf86ec96f680e80a714
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457506"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="77989-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="77989-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="77989-104">**RelativeMonthlyRecurrence**元素描述相对月定期模式。</span><span class="sxs-lookup"><span data-stu-id="77989-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="77989-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="77989-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77989-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77989-106">Attributes and elements</span></span>

<span data-ttu-id="77989-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77989-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77989-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="77989-108">Attributes</span></span>

<span data-ttu-id="77989-109">无。</span><span class="sxs-lookup"><span data-stu-id="77989-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77989-110">子元素</span><span class="sxs-lookup"><span data-stu-id="77989-110">Child elements</span></span>

|<span data-ttu-id="77989-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="77989-111">**Element**</span></span>|<span data-ttu-id="77989-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="77989-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77989-113">Interval</span><span class="sxs-lookup"><span data-stu-id="77989-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="77989-114">定义两个连续的每月定期模式项目之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="77989-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="77989-115">此值的范围是1到99。</span><span class="sxs-lookup"><span data-stu-id="77989-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="77989-116">DaysOfWeek （DayOfWeekType）</span><span class="sxs-lookup"><span data-stu-id="77989-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="77989-117">描述星期几的相对于每月定期模式。</span><span class="sxs-lookup"><span data-stu-id="77989-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="77989-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="77989-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="77989-119">描述在相对月定期模式中使用哪一周。</span><span class="sxs-lookup"><span data-stu-id="77989-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77989-120">父元素</span><span class="sxs-lookup"><span data-stu-id="77989-120">Parent elements</span></span>

|<span data-ttu-id="77989-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="77989-121">**Element**</span></span>|<span data-ttu-id="77989-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="77989-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77989-123">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="77989-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="77989-124">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="77989-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="77989-125">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="77989-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="77989-126">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="77989-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77989-127">说明</span><span class="sxs-lookup"><span data-stu-id="77989-127">Remarks</span></span>

<span data-ttu-id="77989-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="77989-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77989-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="77989-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77989-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="77989-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77989-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="77989-131">Schema Name</span></span>  <br/> |<span data-ttu-id="77989-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="77989-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="77989-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="77989-133">Validation File</span></span>  <br/> |<span data-ttu-id="77989-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77989-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77989-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="77989-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="77989-136">False</span><span class="sxs-lookup"><span data-stu-id="77989-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77989-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77989-137">See also</span></span>



- [<span data-ttu-id="77989-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="77989-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

