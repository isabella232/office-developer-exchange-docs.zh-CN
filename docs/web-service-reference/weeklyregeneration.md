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
description: WeeklyRegeneration 元素介绍任务会重新生成的几周内的频率。
ms.openlocfilehash: 36cd3cc5c180f2b2cf53708e7787d0595f518def
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838559"
---
# <a name="weeklyregeneration"></a><span data-ttu-id="aa522-103">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="aa522-103">WeeklyRegeneration</span></span>

<span data-ttu-id="aa522-104">**WeeklyRegeneration**元素介绍任务会重新生成的几周内的频率。</span><span class="sxs-lookup"><span data-stu-id="aa522-104">The **WeeklyRegeneration** element describes the frequency, in weeks, in which a task is regenerated.</span></span> 
  
```xml
<WeeklyRegeneration>
   <Interval/>
</WeeklyRegeneration>
```

 <span data-ttu-id="aa522-105">**WeeklyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="aa522-105">**WeeklyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa522-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa522-106">Attributes and elements</span></span>

<span data-ttu-id="aa522-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa522-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa522-108">属性</span><span class="sxs-lookup"><span data-stu-id="aa522-108">Attributes</span></span>

<span data-ttu-id="aa522-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa522-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa522-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa522-110">Child elements</span></span>

|<span data-ttu-id="aa522-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa522-111">**Element**</span></span>|<span data-ttu-id="aa522-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa522-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa522-113">Interval</span><span class="sxs-lookup"><span data-stu-id="aa522-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="aa522-114">由于任务已完成之后重新生成新任务，请在周中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="aa522-114">Defines the interval, in weeks, since the task was completed, after which a new task is regenerated.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa522-115">父元素</span><span class="sxs-lookup"><span data-stu-id="aa522-115">Parent elements</span></span>

|<span data-ttu-id="aa522-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa522-116">**Element**</span></span>|<span data-ttu-id="aa522-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa522-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa522-118">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="aa522-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="aa522-119">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="aa522-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa522-120">备注</span><span class="sxs-lookup"><span data-stu-id="aa522-120">Remarks</span></span>

<span data-ttu-id="aa522-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aa522-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa522-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa522-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa522-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa522-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa522-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa522-124">Schema Name</span></span>  <br/> |<span data-ttu-id="aa522-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="aa522-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa522-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa522-126">Validation File</span></span>  <br/> |<span data-ttu-id="aa522-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa522-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa522-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa522-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa522-129">False</span><span class="sxs-lookup"><span data-stu-id="aa522-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa522-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa522-130">See also</span></span>



- [<span data-ttu-id="aa522-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aa522-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

