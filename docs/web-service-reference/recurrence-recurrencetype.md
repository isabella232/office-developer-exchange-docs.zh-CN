---
title: 定期 (RecurrenceType)
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
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: Recurrence 元素包含日历项和会议请求的定期模式。
ms.openlocfilehash: f26ccf5912848a6d7fbbfa7d0a19d41635c896e0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827004"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="bcf04-103">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="bcf04-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="bcf04-104">**Recurrence**元素包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 <span data-ttu-id="bcf04-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="bcf04-105">**RecurrenceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bcf04-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bcf04-106">Attributes and elements</span></span>

<span data-ttu-id="bcf04-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bcf04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bcf04-108">属性</span><span class="sxs-lookup"><span data-stu-id="bcf04-108">Attributes</span></span>

<span data-ttu-id="bcf04-109">无。</span><span class="sxs-lookup"><span data-stu-id="bcf04-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bcf04-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bcf04-110">Child elements</span></span>

|<span data-ttu-id="bcf04-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bcf04-111">**Element**</span></span>|<span data-ttu-id="bcf04-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bcf04-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcf04-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="bcf04-114">介绍相对的每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="bcf04-116">代表每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="bcf04-118">介绍的相对每月定期模式的定期日历项目。</span><span class="sxs-lookup"><span data-stu-id="bcf04-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="bcf04-120">表示每月重复模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="bcf04-122">介绍周和几天所日历项目或任务重复频率。</span><span class="sxs-lookup"><span data-stu-id="bcf04-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="bcf04-124">介绍频率，以天为单位，在其日历项目或任务重复。</span><span class="sxs-lookup"><span data-stu-id="bcf04-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="bcf04-126">介绍没有定义的结束日期的定期模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="bcf04-127">使用此元素不包括[EndDateRecurrence](enddaterecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="bcf04-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="bcf04-129">介绍的开始日期和结束日期的项目定期模式。</span><span class="sxs-lookup"><span data-stu-id="bcf04-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="bcf04-130">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="bcf04-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="bcf04-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="bcf04-132">介绍的开始日期和定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="bcf04-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="bcf04-133">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[EndDateRecurrence](enddaterecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="bcf04-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bcf04-134">父元素</span><span class="sxs-lookup"><span data-stu-id="bcf04-134">Parent elements</span></span>

|<span data-ttu-id="bcf04-135">**元素**</span><span class="sxs-lookup"><span data-stu-id="bcf04-135">**Element**</span></span>|<span data-ttu-id="bcf04-136">**说明**</span><span class="sxs-lookup"><span data-stu-id="bcf04-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcf04-137">日历项目</span><span class="sxs-lookup"><span data-stu-id="bcf04-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="bcf04-138">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="bcf04-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="bcf04-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="bcf04-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="bcf04-140">表示 Exchange 存储中的会议请求</span><span class="sxs-lookup"><span data-stu-id="bcf04-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bcf04-141">注解</span><span class="sxs-lookup"><span data-stu-id="bcf04-141">Remarks</span></span>

<span data-ttu-id="bcf04-142">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="bcf04-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="bcf04-143">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bcf04-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcf04-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="bcf04-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcf04-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="bcf04-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bcf04-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="bcf04-146">Schema name</span></span>  <br/> |<span data-ttu-id="bcf04-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="bcf04-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="bcf04-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="bcf04-148">Validation file</span></span>  <br/> |<span data-ttu-id="bcf04-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bcf04-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bcf04-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="bcf04-150">Can be empty</span></span>  <br/> |<span data-ttu-id="bcf04-151">False</span><span class="sxs-lookup"><span data-stu-id="bcf04-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcf04-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bcf04-152">See also</span></span>



- [<span data-ttu-id="bcf04-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bcf04-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

