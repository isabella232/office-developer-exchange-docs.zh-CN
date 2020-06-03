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
description: NumberedRecurrence 元素描述开始日期和定期项目的发生次数。
ms.openlocfilehash: 000674e5b0bad9deea5aa4ac78d41135a922c755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465938"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="d473f-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="d473f-103">NumberedRecurrence</span></span>

<span data-ttu-id="d473f-104">**NumberedRecurrence**元素描述开始日期和定期项目的发生次数。</span><span class="sxs-lookup"><span data-stu-id="d473f-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="d473f-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="d473f-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d473f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d473f-106">Attributes and elements</span></span>

<span data-ttu-id="d473f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d473f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d473f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d473f-108">Attributes</span></span>

<span data-ttu-id="d473f-109">无。</span><span class="sxs-lookup"><span data-stu-id="d473f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d473f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d473f-110">Child elements</span></span>

|<span data-ttu-id="d473f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d473f-111">**Element**</span></span>|<span data-ttu-id="d473f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d473f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d473f-113">起始日期（定期）</span><span class="sxs-lookup"><span data-stu-id="d473f-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="d473f-114">表示定期任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="d473f-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d473f-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="d473f-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="d473f-116">包含定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="d473f-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d473f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d473f-117">Parent elements</span></span>

|<span data-ttu-id="d473f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d473f-118">**Element**</span></span>|<span data-ttu-id="d473f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d473f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d473f-120">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="d473f-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="d473f-121">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="d473f-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="d473f-122">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="d473f-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="d473f-123">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="d473f-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d473f-124">说明</span><span class="sxs-lookup"><span data-stu-id="d473f-124">Remarks</span></span>

<span data-ttu-id="d473f-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d473f-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d473f-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="d473f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d473f-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="d473f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d473f-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d473f-128">Schema name</span></span>  <br/> |<span data-ttu-id="d473f-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="d473f-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d473f-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d473f-130">Validation file</span></span>  <br/> |<span data-ttu-id="d473f-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d473f-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d473f-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d473f-132">Can be empty</span></span>  <br/> |<span data-ttu-id="d473f-133">False</span><span class="sxs-lookup"><span data-stu-id="d473f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d473f-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d473f-134">See also</span></span>



- [<span data-ttu-id="d473f-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d473f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

