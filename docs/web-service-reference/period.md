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
description: 期间元素定义的一个特定的时区的阶段名称、 时间偏移和唯一标识符。
ms.openlocfilehash: 3b5d5877e6d9baffdfe536a0feec3b25b6d2883f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826726"
---
# <a name="period"></a><span data-ttu-id="98e19-103">句点</span><span class="sxs-lookup"><span data-stu-id="98e19-103">Period</span></span>

<span data-ttu-id="98e19-104">**段**元素定义的一个特定的时区的阶段名称、 时间偏移和唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="98e19-104">The **Period** element defines the name, time offset, and unique identifier for a specific stage of the time zone.</span></span> 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 <span data-ttu-id="98e19-105">**PeriodType**</span><span class="sxs-lookup"><span data-stu-id="98e19-105">**PeriodType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98e19-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="98e19-106">Attributes and elements</span></span>

<span data-ttu-id="98e19-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="98e19-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98e19-108">属性</span><span class="sxs-lookup"><span data-stu-id="98e19-108">Attributes</span></span>

|<span data-ttu-id="98e19-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="98e19-109">**Attribute**</span></span>|<span data-ttu-id="98e19-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="98e19-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98e19-111">Bias</span><span class="sxs-lookup"><span data-stu-id="98e19-111">Bias</span></span>  <br/> |<span data-ttu-id="98e19-112">Xs:duration 值，该值代表时段的时间偏移从协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="98e19-112">An xs:duration value that represents the time offset from Coordinated Universal Time (UTC) for the period.</span></span>  <br/> |
|<span data-ttu-id="98e19-113">名称</span><span class="sxs-lookup"><span data-stu-id="98e19-113">Name</span></span>  <br/> |<span data-ttu-id="98e19-114">一个字符串值，该值代表时段的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="98e19-114">A string value that represents the descriptive name of the period.</span></span>  <br/> |
|<span data-ttu-id="98e19-115">Id</span><span class="sxs-lookup"><span data-stu-id="98e19-115">Id</span></span>  <br/> |<span data-ttu-id="98e19-116">一个字符串值，表示为期间的标识符。</span><span class="sxs-lookup"><span data-stu-id="98e19-116">A string value that represents the identifier for the period.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98e19-117">子元素</span><span class="sxs-lookup"><span data-stu-id="98e19-117">Child elements</span></span>

<span data-ttu-id="98e19-118">无。</span><span class="sxs-lookup"><span data-stu-id="98e19-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="98e19-119">父元素</span><span class="sxs-lookup"><span data-stu-id="98e19-119">Parent elements</span></span>

|<span data-ttu-id="98e19-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="98e19-120">**Element**</span></span>|<span data-ttu-id="98e19-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="98e19-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98e19-122">时间段</span><span class="sxs-lookup"><span data-stu-id="98e19-122">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="98e19-123">代表一个数组定义的时间偏移量的时区的不同阶段的时间段。</span><span class="sxs-lookup"><span data-stu-id="98e19-123">Represents an array of periods that define the time offset at different stages of the time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98e19-124">文本值</span><span class="sxs-lookup"><span data-stu-id="98e19-124">Text value</span></span>

<span data-ttu-id="98e19-125">无。</span><span class="sxs-lookup"><span data-stu-id="98e19-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98e19-126">备注</span><span class="sxs-lookup"><span data-stu-id="98e19-126">Remarks</span></span>

<span data-ttu-id="98e19-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="98e19-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98e19-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="98e19-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98e19-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="98e19-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98e19-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="98e19-130">Schema Name</span></span>  <br/> |<span data-ttu-id="98e19-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="98e19-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="98e19-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="98e19-132">Validation File</span></span>  <br/> |<span data-ttu-id="98e19-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="98e19-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="98e19-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="98e19-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="98e19-135">False</span><span class="sxs-lookup"><span data-stu-id="98e19-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98e19-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98e19-136">See also</span></span>



- [<span data-ttu-id="98e19-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="98e19-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

