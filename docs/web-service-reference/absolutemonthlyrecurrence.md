---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: AbsoluteMonthlyRecurrence 元素表示的每月定期模式。
ms.openlocfilehash: f4613fa71a9164c45b60a82f675959817cd4bdd5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754241"
---
# <a name="absolutemonthlyrecurrence"></a><span data-ttu-id="b73fa-103">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="b73fa-103">AbsoluteMonthlyRecurrence</span></span>

<span data-ttu-id="b73fa-104">**AbsoluteMonthlyRecurrence**元素表示的每月定期模式。</span><span class="sxs-lookup"><span data-stu-id="b73fa-104">The **AbsoluteMonthlyRecurrence** element represents a monthly recurrence pattern.</span></span> 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 <span data-ttu-id="b73fa-105">**AbsoluteMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="b73fa-105">**AbsoluteMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b73fa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b73fa-106">Attributes and elements</span></span>

<span data-ttu-id="b73fa-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b73fa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b73fa-108">属性</span><span class="sxs-lookup"><span data-stu-id="b73fa-108">Attributes</span></span>

<span data-ttu-id="b73fa-109">无。</span><span class="sxs-lookup"><span data-stu-id="b73fa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b73fa-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b73fa-110">Child elements</span></span>

|<span data-ttu-id="b73fa-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b73fa-111">**Element**</span></span>|<span data-ttu-id="b73fa-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b73fa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b73fa-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="b73fa-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="b73fa-114">描述定期项目出现一个月中的一天。</span><span class="sxs-lookup"><span data-stu-id="b73fa-114">Describes the day in a month that a recurring item occurs.</span></span> <span data-ttu-id="b73fa-115">此属性的值范围为 1 到 31。</span><span class="sxs-lookup"><span data-stu-id="b73fa-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="b73fa-116">如果特定月此值大于当月的天数，相应月份的最后一天则假定此属性。</span><span class="sxs-lookup"><span data-stu-id="b73fa-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="b73fa-117">Interval</span><span class="sxs-lookup"><span data-stu-id="b73fa-117">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b73fa-118">定义两个连续的定期项目之间的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="b73fa-118">Defines the interval between two consecutive recurring items.</span></span> <span data-ttu-id="b73fa-119">例如，如果**间隔**元素具有值 5，定期项目发生每 5 个月。</span><span class="sxs-lookup"><span data-stu-id="b73fa-119">For example, if the **Interval** element has a value of 5, the recurring item occurs every 5 months.</span></span> <span data-ttu-id="b73fa-120">有效值范围是从 1 到 99。</span><span class="sxs-lookup"><span data-stu-id="b73fa-120">The range of valid values is from 1 to 99.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b73fa-121">父元素</span><span class="sxs-lookup"><span data-stu-id="b73fa-121">Parent elements</span></span>

|<span data-ttu-id="b73fa-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="b73fa-122">**Element**</span></span>|<span data-ttu-id="b73fa-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="b73fa-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b73fa-124">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b73fa-124">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b73fa-125">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="b73fa-125">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="b73fa-126">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b73fa-126">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b73fa-127">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="b73fa-127">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b73fa-128">备注</span><span class="sxs-lookup"><span data-stu-id="b73fa-128">Remarks</span></span>

<span data-ttu-id="b73fa-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b73fa-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b73fa-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="b73fa-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b73fa-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="b73fa-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b73fa-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="b73fa-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b73fa-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="b73fa-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="b73fa-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="b73fa-134">Validation File</span></span>  <br/> |<span data-ttu-id="b73fa-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b73fa-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b73fa-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="b73fa-136">Can Be Empty</span></span>  <br/> |<span data-ttu-id="b73fa-137">False</span><span class="sxs-lookup"><span data-stu-id="b73fa-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b73fa-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b73fa-138">See also</span></span>

- [<span data-ttu-id="b73fa-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b73fa-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

