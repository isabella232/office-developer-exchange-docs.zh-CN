---
title: 句点
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: Period 元素定义时区的特定阶段的名称、时间偏移和唯一标识符。
ms.openlocfilehash: a7c36a9de01fd0484a7df75de3b5525992ef7ee7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459719"
---
# <a name="period"></a><span data-ttu-id="2d786-103">句点</span><span class="sxs-lookup"><span data-stu-id="2d786-103">Period</span></span>

<span data-ttu-id="2d786-104">**Period**元素定义时区的特定阶段的名称、时间偏移和唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="2d786-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="2d786-105">**PeriodType**</span><span class="sxs-lookup"><span data-stu-id="2d786-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d786-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d786-106">Attributes and elements</span></span>

<span data-ttu-id="2d786-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d786-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d786-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2d786-108">Attributes</span></span>

|<span data-ttu-id="2d786-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2d786-109">**Attribute**</span></span>|<span data-ttu-id="2d786-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d786-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d786-111">Bias</span><span class="sxs-lookup"><span data-stu-id="2d786-111">Bias</span></span>  <br/> |<span data-ttu-id="2d786-112">一个 xs： duration 值，表示与时间段协调世界时（UTC）的时间偏移量。</span><span class="sxs-lookup"><span data-stu-id="2d786-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="2d786-113">名称</span><span class="sxs-lookup"><span data-stu-id="2d786-113">Name</span></span>  <br/> |<span data-ttu-id="2d786-114">一个 string 值，它代表句点的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="2d786-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="2d786-115">Id</span><span class="sxs-lookup"><span data-stu-id="2d786-115">Id</span></span>  <br/> |<span data-ttu-id="2d786-116">一个 string 值，它代表句点的标识符。</span><span class="sxs-lookup"><span data-stu-id="2d786-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2d786-117">子元素</span><span class="sxs-lookup"><span data-stu-id="2d786-117">Child elements</span></span>

<span data-ttu-id="2d786-118">无。</span><span class="sxs-lookup"><span data-stu-id="2d786-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d786-119">父元素</span><span class="sxs-lookup"><span data-stu-id="2d786-119">Parent elements</span></span>

|<span data-ttu-id="2d786-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d786-120">**Element**</span></span>|<span data-ttu-id="2d786-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d786-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d786-122">课时</span><span class="sxs-lookup"><span data-stu-id="2d786-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="2d786-123">表示定义时区的不同阶段的时间偏移量的一组句点。</span><span class="sxs-lookup"><span data-stu-id="2d786-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d786-124">文本值</span><span class="sxs-lookup"><span data-stu-id="2d786-124">Text value</span></span>

<span data-ttu-id="2d786-125">无。</span><span class="sxs-lookup"><span data-stu-id="2d786-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d786-126">说明</span><span class="sxs-lookup"><span data-stu-id="2d786-126">Remarks</span></span>

<span data-ttu-id="2d786-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d786-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d786-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d786-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d786-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d786-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d786-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d786-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2d786-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="2d786-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2d786-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d786-132">Validation File</span></span>  <br/> |<span data-ttu-id="2d786-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2d786-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d786-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d786-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d786-135">False</span><span class="sxs-lookup"><span data-stu-id="2d786-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d786-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d786-136">See also</span></span>



- [<span data-ttu-id="2d786-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d786-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

