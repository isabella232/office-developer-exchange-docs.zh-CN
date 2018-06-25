---
title: NumberedRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberedRecurrence
api_type:
- schema
ms.assetid: 53746909-ef21-4764-8715-a7769b943cca
description: NumberedRecurrence 元素描述的开始日期和定期项目的次数。
ms.openlocfilehash: 01fbf831fa7ff378221d4db3d873af730ac564d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826628"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="abe7d-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="abe7d-103">NumberedRecurrence</span></span>

<span data-ttu-id="abe7d-104">**NumberedRecurrence**元素描述的开始日期和定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="abe7d-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="abe7d-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="abe7d-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abe7d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="abe7d-106">Attributes and elements</span></span>

<span data-ttu-id="abe7d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="abe7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abe7d-108">属性</span><span class="sxs-lookup"><span data-stu-id="abe7d-108">Attributes</span></span>

<span data-ttu-id="abe7d-109">无。</span><span class="sxs-lookup"><span data-stu-id="abe7d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abe7d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="abe7d-110">Child elements</span></span>

|<span data-ttu-id="abe7d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="abe7d-111">**Element**</span></span>|<span data-ttu-id="abe7d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="abe7d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abe7d-113">StartDate （重复）</span><span class="sxs-lookup"><span data-stu-id="abe7d-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="abe7d-114">代表一个周期性任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="abe7d-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="abe7d-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="abe7d-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="abe7d-116">包含定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="abe7d-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abe7d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="abe7d-117">Parent elements</span></span>

|<span data-ttu-id="abe7d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="abe7d-118">**Element**</span></span>|<span data-ttu-id="abe7d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="abe7d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abe7d-120">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="abe7d-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="abe7d-121">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="abe7d-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="abe7d-122">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="abe7d-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="abe7d-123">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="abe7d-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abe7d-124">备注</span><span class="sxs-lookup"><span data-stu-id="abe7d-124">Remarks</span></span>

<span data-ttu-id="abe7d-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="abe7d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abe7d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="abe7d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abe7d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="abe7d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abe7d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="abe7d-128">Schema name</span></span>  <br/> |<span data-ttu-id="abe7d-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="abe7d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="abe7d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="abe7d-130">Validation file</span></span>  <br/> |<span data-ttu-id="abe7d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abe7d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abe7d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="abe7d-132">Can be empty</span></span>  <br/> |<span data-ttu-id="abe7d-133">False</span><span class="sxs-lookup"><span data-stu-id="abe7d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abe7d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="abe7d-134">See also</span></span>



- [<span data-ttu-id="abe7d-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="abe7d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

