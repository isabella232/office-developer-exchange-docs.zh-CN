---
title: 定期 (TaskRecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: Recurrence 元素包含定期周期性任务信息。
ms.openlocfilehash: ae2bb35e89a0a50c7ca67cb0e580427150afb99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827006"
---
# <a name="recurrence-taskrecurrencetype"></a><span data-ttu-id="2981c-103">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="2981c-103">Recurrence (TaskRecurrenceType)</span></span>

<span data-ttu-id="2981c-104">**Recurrence**元素包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="2981c-104">The **Recurrence** element contains recurrence information for recurring tasks.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 <span data-ttu-id="2981c-105">**TaskRecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="2981c-105">**TaskRecurrenceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2981c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2981c-106">Attributes and elements</span></span>

<span data-ttu-id="2981c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2981c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2981c-108">属性</span><span class="sxs-lookup"><span data-stu-id="2981c-108">Attributes</span></span>

<span data-ttu-id="2981c-109">无。</span><span class="sxs-lookup"><span data-stu-id="2981c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2981c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2981c-110">Child elements</span></span>

|<span data-ttu-id="2981c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2981c-111">**Element**</span></span>|<span data-ttu-id="2981c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2981c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2981c-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="2981c-114">描述定期任务的相对于每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="2981c-114">Describes a relative yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="2981c-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="2981c-116">代表每年定期模式的定期任务。</span><span class="sxs-lookup"><span data-stu-id="2981c-116">Represents a yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="2981c-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="2981c-118">介绍的相对每月定期模式的定期任务。</span><span class="sxs-lookup"><span data-stu-id="2981c-118">Describes a relative monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="2981c-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="2981c-120">代表每月定期模式的定期任务。</span><span class="sxs-lookup"><span data-stu-id="2981c-120">Represents a monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="2981c-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="2981c-122">介绍频率，周和任务重复的天数。</span><span class="sxs-lookup"><span data-stu-id="2981c-122">Describes the frequency, in weeks, and the days on which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="2981c-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="2981c-124">描述任务重复出现的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="2981c-124">Describes the frequency, in days, in which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="2981c-125">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="2981c-125">DailyRegeneration</span></span>](dailyregeneration.md) <br/> |<span data-ttu-id="2981c-126">介绍多少天后完成当前任务的下一个匹配项将到期。</span><span class="sxs-lookup"><span data-stu-id="2981c-126">Describes how many days after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="2981c-127">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="2981c-127">WeeklyRegeneration</span></span>](weeklyregeneration.md) <br/> |<span data-ttu-id="2981c-128">介绍多少周后完成当前任务的下一个匹配项将到期。</span><span class="sxs-lookup"><span data-stu-id="2981c-128">Describes how many weeks after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="2981c-129">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="2981c-129">MonthlyRegeneration</span></span>](monthlyregeneration.md) <br/> |<span data-ttu-id="2981c-130">介绍多少个月后完成当前任务的下一个匹配项将到期。</span><span class="sxs-lookup"><span data-stu-id="2981c-130">Describes how many months after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="2981c-131">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="2981c-131">YearlyRegeneration</span></span>](yearlyregeneration.md) <br/> |<span data-ttu-id="2981c-132">介绍如何许多年后完成当前任务的下一个匹配项将到期。</span><span class="sxs-lookup"><span data-stu-id="2981c-132">Describes how many years after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="2981c-133">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-133">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="2981c-134">介绍没有定义的结束日期的定期模式。</span><span class="sxs-lookup"><span data-stu-id="2981c-134">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="2981c-135">使用此元素不包括[EndDateRecurrence](enddaterecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="2981c-135">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="2981c-136">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-136">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="2981c-137">介绍的开始日期和结束日期的项目定期模式。</span><span class="sxs-lookup"><span data-stu-id="2981c-137">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="2981c-138">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="2981c-138">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> <span data-ttu-id="2981c-139">[EndDateRecurrence](enddaterecurrence.md)无法一起再生模式。</span><span class="sxs-lookup"><span data-stu-id="2981c-139">[EndDateRecurrence](enddaterecurrence.md) cannot be used together with a regeneration pattern.</span></span>  <br/> |
|[<span data-ttu-id="2981c-140">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="2981c-140">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="2981c-141">介绍的开始日期和定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="2981c-141">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="2981c-142">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[EndDateRecurrence](enddaterecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="2981c-142">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2981c-143">父元素</span><span class="sxs-lookup"><span data-stu-id="2981c-143">Parent elements</span></span>

|<span data-ttu-id="2981c-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="2981c-144">**Element**</span></span>|<span data-ttu-id="2981c-145">**说明**</span><span class="sxs-lookup"><span data-stu-id="2981c-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2981c-146">任务</span><span class="sxs-lookup"><span data-stu-id="2981c-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="2981c-147">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="2981c-147">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2981c-148">备注</span><span class="sxs-lookup"><span data-stu-id="2981c-148">Remarks</span></span>

<span data-ttu-id="2981c-149">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2981c-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2981c-150">元素信息</span><span class="sxs-lookup"><span data-stu-id="2981c-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2981c-151">命名空间</span><span class="sxs-lookup"><span data-stu-id="2981c-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2981c-152">架构名称</span><span class="sxs-lookup"><span data-stu-id="2981c-152">Schema name</span></span>  <br/> |<span data-ttu-id="2981c-153">类型架构</span><span class="sxs-lookup"><span data-stu-id="2981c-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="2981c-154">验证文件</span><span class="sxs-lookup"><span data-stu-id="2981c-154">Validation file</span></span>  <br/> |<span data-ttu-id="2981c-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2981c-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2981c-156">可以为空</span><span class="sxs-lookup"><span data-stu-id="2981c-156">Can be empty</span></span>  <br/> |<span data-ttu-id="2981c-157">False</span><span class="sxs-lookup"><span data-stu-id="2981c-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2981c-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2981c-158">See also</span></span>



- [<span data-ttu-id="2981c-159">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2981c-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

