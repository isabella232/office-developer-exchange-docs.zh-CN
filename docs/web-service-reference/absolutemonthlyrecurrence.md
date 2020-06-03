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
description: AbsoluteMonthlyRecurrence 元素表示每月定期模式。
ms.openlocfilehash: 3176cd30a1cfe7b2310f960ce377ab7a277e795a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460433"
---
# <a name="absolutemonthlyrecurrence"></a><span data-ttu-id="b3dfc-103">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="b3dfc-103">AbsoluteMonthlyRecurrence</span></span>

<span data-ttu-id="b3dfc-104">**AbsoluteMonthlyRecurrence**元素表示每月定期模式。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-104">The **AbsoluteMonthlyRecurrence** element represents a monthly recurrence pattern.</span></span> 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 <span data-ttu-id="b3dfc-105">**AbsoluteMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="b3dfc-105">**AbsoluteMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3dfc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b3dfc-106">Attributes and elements</span></span>

<span data-ttu-id="b3dfc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3dfc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b3dfc-108">Attributes</span></span>

<span data-ttu-id="b3dfc-109">无。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3dfc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b3dfc-110">Child elements</span></span>

|<span data-ttu-id="b3dfc-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3dfc-111">**Element**</span></span>|<span data-ttu-id="b3dfc-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3dfc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3dfc-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="b3dfc-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="b3dfc-114">描述定期项目出现在一个月中的哪一天。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-114">Describes the day in a month that a recurring item occurs.</span></span> <span data-ttu-id="b3dfc-115">此属性的值的范围是1到31。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="b3dfc-116">如果特定月份的值大于该月的天数，则此属性假定为该月的最后一天。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="b3dfc-117">Interval</span><span class="sxs-lookup"><span data-stu-id="b3dfc-117">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b3dfc-118">定义两个连续定期项目之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-118">Defines the interval between two consecutive recurring items.</span></span> <span data-ttu-id="b3dfc-119">例如，如果**Interval**元素的值为5，则定期项目每5个月发生一次。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-119">For example, if the **Interval** element has a value of 5, the recurring item occurs every 5 months.</span></span> <span data-ttu-id="b3dfc-120">有效值的范围是从1到99。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-120">The range of valid values is from 1 to 99.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3dfc-121">父元素</span><span class="sxs-lookup"><span data-stu-id="b3dfc-121">Parent elements</span></span>

|<span data-ttu-id="b3dfc-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3dfc-122">**Element**</span></span>|<span data-ttu-id="b3dfc-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3dfc-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3dfc-124">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="b3dfc-124">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b3dfc-125">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-125">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="b3dfc-126">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="b3dfc-126">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b3dfc-127">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-127">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3dfc-128">说明</span><span class="sxs-lookup"><span data-stu-id="b3dfc-128">Remarks</span></span>

<span data-ttu-id="b3dfc-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b3dfc-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3dfc-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="b3dfc-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3dfc-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="b3dfc-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3dfc-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="b3dfc-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b3dfc-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="b3dfc-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3dfc-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="b3dfc-134">Validation File</span></span>  <br/> |<span data-ttu-id="b3dfc-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3dfc-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3dfc-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="b3dfc-136">Can Be Empty</span></span>  <br/> |<span data-ttu-id="b3dfc-137">False</span><span class="sxs-lookup"><span data-stu-id="b3dfc-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3dfc-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3dfc-138">See also</span></span>

- [<span data-ttu-id="b3dfc-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b3dfc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

