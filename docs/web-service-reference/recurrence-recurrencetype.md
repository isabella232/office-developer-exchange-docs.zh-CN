---
title: 重复周期（RecurrenceType）
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
description: 定期元素包含日历项目和会议请求的定期模式。
ms.openlocfilehash: d00445c75fb35c3bb99eeed06e30cb1cf2883597
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529887"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="4d11d-103">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="4d11d-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="4d11d-104">**定期**元素包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

<span data-ttu-id="4d11d-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="4d11d-105">**RecurrenceType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4d11d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d11d-106">Attributes and elements</span></span>

<span data-ttu-id="4d11d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d11d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d11d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4d11d-108">Attributes</span></span>

<span data-ttu-id="4d11d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4d11d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d11d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4d11d-110">Child elements</span></span>

|<span data-ttu-id="4d11d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d11d-111">**Element**</span></span>|<span data-ttu-id="4d11d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d11d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d11d-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="4d11d-114">介绍相对年定期模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="4d11d-116">代表每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="4d11d-118">描述定期日历项的相对月定期模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="4d11d-120">表示每月重复模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="4d11d-122">描述频率（以周为单位）以及日历项目或任务的重复发生日期。</span><span class="sxs-lookup"><span data-stu-id="4d11d-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="4d11d-124">描述日历项目或任务重复发生的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="4d11d-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="4d11d-126">介绍没有定义的结束日期的定期模式。</span><span class="sxs-lookup"><span data-stu-id="4d11d-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="4d11d-127">使用此元素不包括[EndDateRecurrence](enddaterecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="4d11d-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="4d11d-129">描述项目定期模式的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="4d11d-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="4d11d-130">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="4d11d-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d11d-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="4d11d-132">描述定期项目的开始日期和发生次数。</span><span class="sxs-lookup"><span data-stu-id="4d11d-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="4d11d-133">使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[EndDateRecurrence](enddaterecurrence.md)元素的使用。</span><span class="sxs-lookup"><span data-stu-id="4d11d-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d11d-134">父元素</span><span class="sxs-lookup"><span data-stu-id="4d11d-134">Parent elements</span></span>

|<span data-ttu-id="4d11d-135">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d11d-135">**Element**</span></span>|<span data-ttu-id="4d11d-136">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d11d-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d11d-137">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4d11d-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4d11d-138">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="4d11d-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4d11d-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4d11d-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4d11d-140">表示 Exchange 存储中的会议请求</span><span class="sxs-lookup"><span data-stu-id="4d11d-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d11d-141">备注</span><span class="sxs-lookup"><span data-stu-id="4d11d-141">Remarks</span></span>

<span data-ttu-id="4d11d-142">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="4d11d-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="4d11d-143">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4d11d-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d11d-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d11d-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d11d-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d11d-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d11d-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d11d-146">Schema name</span></span>  <br/> |<span data-ttu-id="4d11d-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="4d11d-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d11d-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d11d-148">Validation file</span></span>  <br/> |<span data-ttu-id="4d11d-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4d11d-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d11d-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d11d-150">Can be empty</span></span>  <br/> |<span data-ttu-id="4d11d-151">False</span><span class="sxs-lookup"><span data-stu-id="4d11d-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d11d-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d11d-152">See also</span></span>

- [<span data-ttu-id="4d11d-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4d11d-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

