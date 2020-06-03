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
ms.openlocfilehash: 19b617dfd5c0a3d206d62439c880da084fd5f5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460412"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="60f40-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="60f40-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="60f40-104">**AbsoluteYearlyRecurrence**元素表示每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="60f40-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="60f40-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="60f40-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60f40-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="60f40-106">Attributes and elements</span></span>

<span data-ttu-id="60f40-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="60f40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60f40-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="60f40-108">Attributes</span></span>

<span data-ttu-id="60f40-109">无。</span><span class="sxs-lookup"><span data-stu-id="60f40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60f40-110">子元素</span><span class="sxs-lookup"><span data-stu-id="60f40-110">Child elements</span></span>

|<span data-ttu-id="60f40-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="60f40-111">**Element**</span></span>|<span data-ttu-id="60f40-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="60f40-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60f40-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="60f40-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="60f40-114">描述定期项目发生在一个月中的哪一天。</span><span class="sxs-lookup"><span data-stu-id="60f40-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="60f40-115">此属性的值的范围是1到31。</span><span class="sxs-lookup"><span data-stu-id="60f40-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="60f40-116">如果特定月份的值大于该月的天数，则此属性假定为该月的最后一天。</span><span class="sxs-lookup"><span data-stu-id="60f40-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="60f40-117">月（项目定期）</span><span class="sxs-lookup"><span data-stu-id="60f40-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="60f40-118">描述每年定期项目发生的月份。</span><span class="sxs-lookup"><span data-stu-id="60f40-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60f40-119">父元素</span><span class="sxs-lookup"><span data-stu-id="60f40-119">Parent elements</span></span>

|<span data-ttu-id="60f40-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="60f40-120">**Element**</span></span>|<span data-ttu-id="60f40-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="60f40-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60f40-122">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="60f40-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="60f40-123">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="60f40-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="60f40-124">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="60f40-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="60f40-125">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="60f40-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60f40-126">说明</span><span class="sxs-lookup"><span data-stu-id="60f40-126">Remarks</span></span>

<span data-ttu-id="60f40-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="60f40-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60f40-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="60f40-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60f40-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="60f40-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60f40-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="60f40-130">Schema Name</span></span>  <br/> |<span data-ttu-id="60f40-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="60f40-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="60f40-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="60f40-132">Validation File</span></span>  <br/> |<span data-ttu-id="60f40-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60f40-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60f40-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="60f40-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="60f40-135">False</span><span class="sxs-lookup"><span data-stu-id="60f40-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60f40-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="60f40-136">See also</span></span>

- [<span data-ttu-id="60f40-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="60f40-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

