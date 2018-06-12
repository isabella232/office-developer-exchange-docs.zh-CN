---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: NoEndRecurrence 元素描述没有定义的结束日期项目定期模式的开始日期。
ms.openlocfilehash: fc3eae170f5c07e31d7a80b45836efd07d74e543
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826537"
---
# <a name="noendrecurrence"></a><span data-ttu-id="7b8e9-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="7b8e9-103">NoEndRecurrence</span></span>

<span data-ttu-id="7b8e9-104">**NoEndRecurrence**元素描述没有定义的结束日期项目定期模式的开始日期。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="7b8e9-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="7b8e9-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b8e9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b8e9-106">Attributes and elements</span></span>

<span data-ttu-id="7b8e9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b8e9-108">属性</span><span class="sxs-lookup"><span data-stu-id="7b8e9-108">Attributes</span></span>

<span data-ttu-id="7b8e9-109">无。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b8e9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7b8e9-110">Child elements</span></span>

|<span data-ttu-id="7b8e9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b8e9-111">**Element**</span></span>|<span data-ttu-id="7b8e9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b8e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b8e9-113">StartDate （重复）</span><span class="sxs-lookup"><span data-stu-id="7b8e9-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="7b8e9-114">代表一个周期性任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b8e9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7b8e9-115">Parent elements</span></span>

|<span data-ttu-id="7b8e9-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b8e9-116">**Element**</span></span>|<span data-ttu-id="7b8e9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b8e9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b8e9-118">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="7b8e9-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="7b8e9-119">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="7b8e9-120">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="7b8e9-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="7b8e9-121">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b8e9-122">备注</span><span class="sxs-lookup"><span data-stu-id="7b8e9-122">Remarks</span></span>

<span data-ttu-id="7b8e9-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b8e9-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b8e9-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b8e9-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b8e9-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b8e9-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b8e9-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b8e9-126">Schema name</span></span>  <br/> |<span data-ttu-id="7b8e9-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="7b8e9-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b8e9-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b8e9-128">Validation file</span></span>  <br/> |<span data-ttu-id="7b8e9-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b8e9-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b8e9-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b8e9-130">Can be empty</span></span>  <br/> |<span data-ttu-id="7b8e9-131">False</span><span class="sxs-lookup"><span data-stu-id="7b8e9-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b8e9-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b8e9-132">See also</span></span>



- [<span data-ttu-id="7b8e9-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7b8e9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

