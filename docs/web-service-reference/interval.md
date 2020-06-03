---
title: Interval
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: Interval 元素定义两个连续周期性项目之间的间隔。
ms.openlocfilehash: 70a41cfc438f057cbe11d792f0004d46d0abcc85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526562"
---
# <a name="interval"></a><span data-ttu-id="ddc03-103">时间间隔</span><span class="sxs-lookup"><span data-stu-id="ddc03-103">Interval</span></span>

<span data-ttu-id="ddc03-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Interval** 元素定义两个连续周期性项目之间的间隔。</span><span class="sxs-lookup"><span data-stu-id="ddc03-104">The **Interval** element defines the interval between two consecutive recurring items.</span></span> 
  
```xml
<Interval/>
```

 <span data-ttu-id="ddc03-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ddc03-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ddc03-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ddc03-106">Attributes and elements</span></span>

<span data-ttu-id="ddc03-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ddc03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ddc03-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ddc03-108">Attributes</span></span>

<span data-ttu-id="ddc03-109">无。</span><span class="sxs-lookup"><span data-stu-id="ddc03-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ddc03-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ddc03-110">Child elements</span></span>

<span data-ttu-id="ddc03-111">无。</span><span class="sxs-lookup"><span data-stu-id="ddc03-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ddc03-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ddc03-112">Parent elements</span></span>

|<span data-ttu-id="ddc03-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ddc03-113">**Element**</span></span>|<span data-ttu-id="ddc03-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ddc03-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ddc03-115">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddc03-115">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="ddc03-116">表示每月重复模式。</span><span class="sxs-lookup"><span data-stu-id="ddc03-116">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-117">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="ddc03-117">DailyRegeneration</span></span>](dailyregeneration.md) <br/> |<span data-ttu-id="ddc03-118">描述任务重新生成的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-118">Describes the frequency, in days, in which a task is regenerated.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-119">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddc03-119">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="ddc03-120">描述任务重复出现的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-120">Describes the frequency, in days, in which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-121">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="ddc03-121">MonthlyRegeneration</span></span>](monthlyregeneration.md) <br/> |<span data-ttu-id="ddc03-122">描述任务重新生成的频率（以月为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-122">Describes the frequency, in months, in which a task is regenerated.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-123">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddc03-123">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="ddc03-124">描述周期性任务的每月相对模式。</span><span class="sxs-lookup"><span data-stu-id="ddc03-124">Describes a relative monthly pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-125">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ddc03-125">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="ddc03-126">描述任务重复出现的频率（以周或天为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-126">Describes the frequency, in weeks, in which and the days on which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-127">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="ddc03-127">WeeklyRegeneration</span></span>](weeklyregeneration.md) <br/> |<span data-ttu-id="ddc03-128">描述任务重新生成的频率（以周为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-128">Describes the frequency, in weeks, in which a task is regenerated.</span></span>  <br/> |
|[<span data-ttu-id="ddc03-129">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="ddc03-129">YearlyRegeneration</span></span>](yearlyregeneration.md) <br/> |<span data-ttu-id="ddc03-130">描述任务重新生成的频率（以年为单位）。</span><span class="sxs-lookup"><span data-stu-id="ddc03-130">Describes the frequency, in years, in which a task is regenerated.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ddc03-131">文本值</span><span class="sxs-lookup"><span data-stu-id="ddc03-131">Text value</span></span>

<span data-ttu-id="ddc03-132">需要表示整数的一个文本值。</span><span class="sxs-lookup"><span data-stu-id="ddc03-132">A text value that represents an integer is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddc03-133">说明</span><span class="sxs-lookup"><span data-stu-id="ddc03-133">Remarks</span></span>

<span data-ttu-id="ddc03-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ddc03-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ddc03-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="ddc03-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddc03-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="ddc03-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ddc03-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="ddc03-137">Schema name</span></span>  <br/> |<span data-ttu-id="ddc03-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="ddc03-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="ddc03-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="ddc03-139">Validation file</span></span>  <br/> |<span data-ttu-id="ddc03-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ddc03-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ddc03-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="ddc03-141">Can be empty</span></span>  <br/> |<span data-ttu-id="ddc03-142">False</span><span class="sxs-lookup"><span data-stu-id="ddc03-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ddc03-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ddc03-143">See also</span></span>



- [<span data-ttu-id="ddc03-144">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ddc03-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

