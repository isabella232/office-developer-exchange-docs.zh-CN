---
title: WeeklyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRegeneration
api_type:
- schema
ms.assetid: f128fdaa-ca3d-4614-8e55-f25e76a67b6c
description: WeeklyRegeneration 元素描述任务重新生成的频率（以周为单位）。
ms.openlocfilehash: dc333e051fd2213942e629a3f2764c72abfaeba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459747"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="d7895-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="d7895-103">WeeklyRegeneration</span></span>

<span data-ttu-id="d7895-104">**WeeklyRegeneration**元素描述任务重新生成的频率（以周为单位）。</span><span class="sxs-lookup"><span data-stu-id="d7895-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="d7895-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="d7895-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7895-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d7895-106">Attributes and elements</span></span>

<span data-ttu-id="d7895-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d7895-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7895-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d7895-108">Attributes</span></span>

<span data-ttu-id="d7895-109">无。</span><span class="sxs-lookup"><span data-stu-id="d7895-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7895-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d7895-110">Child elements</span></span>

|<span data-ttu-id="d7895-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7895-111">**Element**</span></span>|<span data-ttu-id="d7895-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7895-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7895-113">Interval</span><span class="sxs-lookup"><span data-stu-id="d7895-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="d7895-114">定义自任务完成后重新生成新任务之后的间隔（以周为单位）。</span><span class="sxs-lookup"><span data-stu-id="d7895-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7895-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d7895-115">Parent elements</span></span>

|<span data-ttu-id="d7895-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7895-116">**Element**</span></span>|<span data-ttu-id="d7895-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7895-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7895-118">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="d7895-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="d7895-119">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="d7895-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7895-120">说明</span><span class="sxs-lookup"><span data-stu-id="d7895-120">Remarks</span></span>

<span data-ttu-id="d7895-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d7895-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7895-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="d7895-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7895-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="d7895-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7895-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="d7895-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d7895-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="d7895-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7895-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="d7895-126">Validation File</span></span>  <br/> |<span data-ttu-id="d7895-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7895-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7895-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="d7895-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7895-129">False</span><span class="sxs-lookup"><span data-stu-id="d7895-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7895-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7895-130">See also</span></span>



- [<span data-ttu-id="d7895-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d7895-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

