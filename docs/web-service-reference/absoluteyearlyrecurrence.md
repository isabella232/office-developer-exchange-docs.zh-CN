---
title: AbsoluteYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteYearlyRecurrence
api_type:
- schema
ms.assetid: 96f53e2c-3893-4f6e-a78a-ac179f45c5db
description: AbsoluteYearlyRecurrence 元素表示每年定期模式。
ms.openlocfilehash: 205da336a6a6ca4fd39120e83ab264e1543354e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754236"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="d914a-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d914a-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="d914a-104">**AbsoluteYearlyRecurrence**元素表示每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="d914a-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="d914a-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="d914a-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d914a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d914a-106">Attributes and elements</span></span>

<span data-ttu-id="d914a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d914a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d914a-108">属性</span><span class="sxs-lookup"><span data-stu-id="d914a-108">Attributes</span></span>

<span data-ttu-id="d914a-109">无。</span><span class="sxs-lookup"><span data-stu-id="d914a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d914a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d914a-110">Child elements</span></span>

|<span data-ttu-id="d914a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d914a-111">**Element**</span></span>|<span data-ttu-id="d914a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d914a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d914a-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="d914a-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="d914a-114">描述定期项目出现在其一个月中的一天。</span><span class="sxs-lookup"><span data-stu-id="d914a-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="d914a-115">此属性的值范围为 1 到 31。</span><span class="sxs-lookup"><span data-stu-id="d914a-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="d914a-116">如果特定月此值大于当月的天数，相应月份的最后一天则假定此属性。</span><span class="sxs-lookup"><span data-stu-id="d914a-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="d914a-117">每月 （项重复）</span><span class="sxs-lookup"><span data-stu-id="d914a-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="d914a-118">介绍每年定期项目发生的月份。</span><span class="sxs-lookup"><span data-stu-id="d914a-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d914a-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d914a-119">Parent elements</span></span>

|<span data-ttu-id="d914a-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="d914a-120">**Element**</span></span>|<span data-ttu-id="d914a-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="d914a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d914a-122">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="d914a-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="d914a-123">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="d914a-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="d914a-124">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="d914a-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="d914a-125">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="d914a-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d914a-126">备注</span><span class="sxs-lookup"><span data-stu-id="d914a-126">Remarks</span></span>

<span data-ttu-id="d914a-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d914a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d914a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="d914a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d914a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="d914a-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d914a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="d914a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="d914a-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="d914a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="d914a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="d914a-132">Validation File</span></span>  <br/> |<span data-ttu-id="d914a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d914a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d914a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="d914a-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="d914a-135">False</span><span class="sxs-lookup"><span data-stu-id="d914a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d914a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d914a-136">See also</span></span>

- [<span data-ttu-id="d914a-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d914a-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

