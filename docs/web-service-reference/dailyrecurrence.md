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
description: DailyRecurrence 元素描述日历项目或任务重复发生的频率（以天为单位）。
ms.openlocfilehash: d18a04ced19c87996c3a092f6668ab00c5a3f006
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462169"
---
# <a name="dailyrecurrence"></a><span data-ttu-id="fcaff-103">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="fcaff-103">DailyRecurrence</span></span>

<span data-ttu-id="fcaff-104">**DailyRecurrence**元素描述日历项目或任务重复发生的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="fcaff-104">The **DailyRecurrence** element describes the frequency, in days, in which a calendar item or a task recurs.</span></span> 
  
```xml
<DailyRecurrence>
   <Interval/>
</DailyRecurrence>
```

<span data-ttu-id="fcaff-105">**DailyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="fcaff-105">**DailyRecurrencePatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fcaff-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fcaff-106">Attributes and elements</span></span>

<span data-ttu-id="fcaff-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fcaff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcaff-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fcaff-108">Attributes</span></span>

<span data-ttu-id="fcaff-109">无。</span><span class="sxs-lookup"><span data-stu-id="fcaff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fcaff-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fcaff-110">Child elements</span></span>

|<span data-ttu-id="fcaff-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fcaff-111">**Element**</span></span>|<span data-ttu-id="fcaff-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fcaff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fcaff-113">Interval</span><span class="sxs-lookup"><span data-stu-id="fcaff-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="fcaff-114">定义两个连续定期项目之间的间隔（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="fcaff-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="fcaff-115">该值必须介于1到999之间。</span><span class="sxs-lookup"><span data-stu-id="fcaff-115">The value must be in the range from 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fcaff-116">父元素</span><span class="sxs-lookup"><span data-stu-id="fcaff-116">Parent elements</span></span>

|<span data-ttu-id="fcaff-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="fcaff-117">**Element**</span></span>|<span data-ttu-id="fcaff-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="fcaff-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fcaff-119">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="fcaff-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="fcaff-120">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="fcaff-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="fcaff-121">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="fcaff-121">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="fcaff-122">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="fcaff-122">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcaff-123">说明</span><span class="sxs-lookup"><span data-stu-id="fcaff-123">Remarks</span></span>

<span data-ttu-id="fcaff-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fcaff-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcaff-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="fcaff-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcaff-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="fcaff-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fcaff-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="fcaff-127">Schema name</span></span>  <br/> |<span data-ttu-id="fcaff-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="fcaff-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="fcaff-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="fcaff-129">Validation file</span></span>  <br/> |<span data-ttu-id="fcaff-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fcaff-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fcaff-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="fcaff-131">Can be empty</span></span>  <br/> |<span data-ttu-id="fcaff-132">False</span><span class="sxs-lookup"><span data-stu-id="fcaff-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcaff-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fcaff-133">See also</span></span>

- [<span data-ttu-id="fcaff-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fcaff-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

