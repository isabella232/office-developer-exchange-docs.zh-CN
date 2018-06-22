---
title: DailyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRecurrence
api_type:
- schema
ms.assetid: 0aaf265d-b723-49c6-8e9c-9ba60141e9ab
description: DailyRecurrence 元素介绍以天为单位，重复日历项目或任务的频率。
ms.openlocfilehash: d02c1f7425372d60c10b40527dc5f0d65f923b45
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753726"
---
# <a name="dailyrecurrence"></a><span data-ttu-id="daa45-103">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="daa45-103">DailyRecurrence</span></span>

<span data-ttu-id="daa45-104">**DailyRecurrence**元素介绍以天为单位，重复日历项目或任务的频率。</span><span class="sxs-lookup"><span data-stu-id="daa45-104">The **DailyRecurrence** element describes the frequency, in days, in which a calendar item or a task recurs.</span></span> 
  
```xml
<DailyRecurrence>
   <Interval/>
</DailyRecurrence>
```

<span data-ttu-id="daa45-105">**DailyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="daa45-105">**DailyRecurrencePatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="daa45-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="daa45-106">Attributes and elements</span></span>

<span data-ttu-id="daa45-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="daa45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="daa45-108">属性</span><span class="sxs-lookup"><span data-stu-id="daa45-108">Attributes</span></span>

<span data-ttu-id="daa45-109">无。</span><span class="sxs-lookup"><span data-stu-id="daa45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="daa45-110">子元素</span><span class="sxs-lookup"><span data-stu-id="daa45-110">Child elements</span></span>

|<span data-ttu-id="daa45-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="daa45-111">**Element**</span></span>|<span data-ttu-id="daa45-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="daa45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="daa45-113">Interval</span><span class="sxs-lookup"><span data-stu-id="daa45-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="daa45-114">以天为单位，两个连续的定期项目间中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="daa45-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="daa45-115">值必须是介于 1 到 999 之间。</span><span class="sxs-lookup"><span data-stu-id="daa45-115">The value must be in the range from 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="daa45-116">父元素</span><span class="sxs-lookup"><span data-stu-id="daa45-116">Parent elements</span></span>

|<span data-ttu-id="daa45-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="daa45-117">**Element**</span></span>|<span data-ttu-id="daa45-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="daa45-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="daa45-119">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="daa45-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="daa45-120">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="daa45-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="daa45-121">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="daa45-121">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="daa45-122">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="daa45-122">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="daa45-123">备注</span><span class="sxs-lookup"><span data-stu-id="daa45-123">Remarks</span></span>

<span data-ttu-id="daa45-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="daa45-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="daa45-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="daa45-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="daa45-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="daa45-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="daa45-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="daa45-127">Schema name</span></span>  <br/> |<span data-ttu-id="daa45-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="daa45-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="daa45-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="daa45-129">Validation file</span></span>  <br/> |<span data-ttu-id="daa45-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="daa45-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="daa45-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="daa45-131">Can be empty</span></span>  <br/> |<span data-ttu-id="daa45-132">False</span><span class="sxs-lookup"><span data-stu-id="daa45-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="daa45-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="daa45-133">See also</span></span>

- [<span data-ttu-id="daa45-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="daa45-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

