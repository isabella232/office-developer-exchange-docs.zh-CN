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
description: EndDateRecurrence 元素描述的开始日期和结束日期的项目定期模式。
ms.openlocfilehash: 73450bf69c6b122e806d85011975159e348ad740
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754118"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="bd822-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="bd822-103">EndDateRecurrence</span></span>

<span data-ttu-id="bd822-104">**EndDateRecurrence**元素描述的开始日期和结束日期的项目定期模式。</span><span class="sxs-lookup"><span data-stu-id="bd822-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="bd822-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="bd822-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd822-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd822-106">Attributes and elements</span></span>

<span data-ttu-id="bd822-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd822-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd822-108">属性</span><span class="sxs-lookup"><span data-stu-id="bd822-108">Attributes</span></span>

<span data-ttu-id="bd822-109">无。</span><span class="sxs-lookup"><span data-stu-id="bd822-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd822-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bd822-110">Child elements</span></span>

|<span data-ttu-id="bd822-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd822-111">**Element**</span></span>|<span data-ttu-id="bd822-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd822-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd822-113">StartDate （重复）</span><span class="sxs-lookup"><span data-stu-id="bd822-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="bd822-114">代表一个周期性任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="bd822-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="bd822-115">EndDate （重复）</span><span class="sxs-lookup"><span data-stu-id="bd822-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="bd822-116">代表一个周期性任务或日历项的结束日期。</span><span class="sxs-lookup"><span data-stu-id="bd822-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd822-117">父元素</span><span class="sxs-lookup"><span data-stu-id="bd822-117">Parent elements</span></span>

|<span data-ttu-id="bd822-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd822-118">**Element**</span></span>|<span data-ttu-id="bd822-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd822-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd822-120">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="bd822-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="bd822-121">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="bd822-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="bd822-122">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="bd822-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="bd822-123">包含定期任务的定期模式。</span><span class="sxs-lookup"><span data-stu-id="bd822-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd822-124">备注</span><span class="sxs-lookup"><span data-stu-id="bd822-124">Remarks</span></span>

<span data-ttu-id="bd822-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bd822-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd822-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="bd822-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd822-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="bd822-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd822-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="bd822-128">Schema name</span></span>  <br/> |<span data-ttu-id="bd822-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="bd822-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd822-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="bd822-130">Validation file</span></span>  <br/> |<span data-ttu-id="bd822-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd822-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd822-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="bd822-132">Can be empty</span></span>  <br/> |<span data-ttu-id="bd822-133">False</span><span class="sxs-lookup"><span data-stu-id="bd822-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd822-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd822-134">See also</span></span>



- [<span data-ttu-id="bd822-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bd822-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

