---
title: EndDateRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: EndDateRecurrence 元素描述项目定期模式的开始日期和结束日期。
ms.openlocfilehash: e8ae72012e5bcac8d8b2a06b6d3a9b3a7caf30d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460146"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="12d5a-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="12d5a-103">EndDateRecurrence</span></span>

<span data-ttu-id="12d5a-104">**EndDateRecurrence**元素描述项目定期模式的开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="12d5a-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="12d5a-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="12d5a-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12d5a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="12d5a-106">Attributes and elements</span></span>

<span data-ttu-id="12d5a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="12d5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12d5a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="12d5a-108">Attributes</span></span>

<span data-ttu-id="12d5a-109">无。</span><span class="sxs-lookup"><span data-stu-id="12d5a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12d5a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="12d5a-110">Child elements</span></span>

|<span data-ttu-id="12d5a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="12d5a-111">**Element**</span></span>|<span data-ttu-id="12d5a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="12d5a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12d5a-113">起始日期（定期）</span><span class="sxs-lookup"><span data-stu-id="12d5a-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="12d5a-114">表示定期任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="12d5a-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="12d5a-115">结束日期（定期）</span><span class="sxs-lookup"><span data-stu-id="12d5a-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="12d5a-116">表示定期任务或日历项的结束日期。</span><span class="sxs-lookup"><span data-stu-id="12d5a-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12d5a-117">父元素</span><span class="sxs-lookup"><span data-stu-id="12d5a-117">Parent elements</span></span>

|<span data-ttu-id="12d5a-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="12d5a-118">**Element**</span></span>|<span data-ttu-id="12d5a-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="12d5a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12d5a-120">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="12d5a-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="12d5a-121">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="12d5a-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="12d5a-122">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="12d5a-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="12d5a-123">包含定期任务的定期模式。</span><span class="sxs-lookup"><span data-stu-id="12d5a-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12d5a-124">说明</span><span class="sxs-lookup"><span data-stu-id="12d5a-124">Remarks</span></span>

<span data-ttu-id="12d5a-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="12d5a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12d5a-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="12d5a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12d5a-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="12d5a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12d5a-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="12d5a-128">Schema name</span></span>  <br/> |<span data-ttu-id="12d5a-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="12d5a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="12d5a-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="12d5a-130">Validation file</span></span>  <br/> |<span data-ttu-id="12d5a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="12d5a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="12d5a-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="12d5a-132">Can be empty</span></span>  <br/> |<span data-ttu-id="12d5a-133">False</span><span class="sxs-lookup"><span data-stu-id="12d5a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12d5a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12d5a-134">See also</span></span>



- [<span data-ttu-id="12d5a-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="12d5a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

