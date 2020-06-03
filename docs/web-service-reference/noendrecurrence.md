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
description: NoEndRecurrence 元素描述不具有定义的结束日期的项目定期模式的开始日期。
ms.openlocfilehash: 31a3bd6ae2d7ce94debbeebc4fd4f536447433a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466792"
---
# <a name="noendrecurrence"></a><span data-ttu-id="83d5e-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="83d5e-103">NoEndRecurrence</span></span>

<span data-ttu-id="83d5e-104">**NoEndRecurrence**元素描述不具有定义的结束日期的项目定期模式的开始日期。</span><span class="sxs-lookup"><span data-stu-id="83d5e-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="83d5e-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="83d5e-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83d5e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="83d5e-106">Attributes and elements</span></span>

<span data-ttu-id="83d5e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="83d5e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83d5e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="83d5e-108">Attributes</span></span>

<span data-ttu-id="83d5e-109">无。</span><span class="sxs-lookup"><span data-stu-id="83d5e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83d5e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="83d5e-110">Child elements</span></span>

|<span data-ttu-id="83d5e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="83d5e-111">**Element**</span></span>|<span data-ttu-id="83d5e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="83d5e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83d5e-113">起始日期（定期）</span><span class="sxs-lookup"><span data-stu-id="83d5e-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="83d5e-114">表示定期任务或日历项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="83d5e-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83d5e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="83d5e-115">Parent elements</span></span>

|<span data-ttu-id="83d5e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="83d5e-116">**Element**</span></span>|<span data-ttu-id="83d5e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="83d5e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83d5e-118">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="83d5e-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="83d5e-119">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="83d5e-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="83d5e-120">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="83d5e-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="83d5e-121">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="83d5e-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83d5e-122">说明</span><span class="sxs-lookup"><span data-stu-id="83d5e-122">Remarks</span></span>

<span data-ttu-id="83d5e-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="83d5e-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83d5e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="83d5e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83d5e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="83d5e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83d5e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="83d5e-126">Schema name</span></span>  <br/> |<span data-ttu-id="83d5e-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="83d5e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="83d5e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="83d5e-128">Validation file</span></span>  <br/> |<span data-ttu-id="83d5e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83d5e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83d5e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="83d5e-130">Can be empty</span></span>  <br/> |<span data-ttu-id="83d5e-131">False</span><span class="sxs-lookup"><span data-stu-id="83d5e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83d5e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83d5e-132">See also</span></span>



- [<span data-ttu-id="83d5e-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="83d5e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

