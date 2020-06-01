---
title: 范围
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Range 元素指定重复日历项目的日历项目发生的范围。
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465308"
---
# <a name="range"></a><span data-ttu-id="c1a7e-103">范围</span><span class="sxs-lookup"><span data-stu-id="c1a7e-103">Range</span></span>

<span data-ttu-id="c1a7e-104">**Range**元素指定重复日历项目的日历项目发生的范围。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="c1a7e-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1a7e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1a7e-106">Attributes and elements</span></span>

<span data-ttu-id="c1a7e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1a7e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c1a7e-108">Attributes</span></span>

|<span data-ttu-id="c1a7e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-109">**Attribute**</span></span>|<span data-ttu-id="c1a7e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1a7e-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-111">**Start**</span></span> <br/> |<span data-ttu-id="c1a7e-112">**Start**属性的文本值是定期项目范围的开始日期。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="c1a7e-113">这是一个**日期/时间**值。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="c1a7e-114">**End**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-114">**End**</span></span> <br/> |<span data-ttu-id="c1a7e-115">**End**属性的文本值是定期项目范围的结束日期。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="c1a7e-116">这是一个**日期/时间**值。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="c1a7e-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-117">**Count**</span></span> <br/> |<span data-ttu-id="c1a7e-118">**Count**属性的文本值是定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="c1a7e-119">这是**整数**值。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="c1a7e-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="c1a7e-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="c1a7e-121">如果**CompareOriginalStartTime**属性的文本值为**true，则**表示客户端应将原始开始时间与新的开始时间进行比较。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="c1a7e-122">**如果值为 false** ，则表示客户端无需将原始开始时间与新开始时间进行比较。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1a7e-123">子元素</span><span class="sxs-lookup"><span data-stu-id="c1a7e-123">Child elements</span></span>

<span data-ttu-id="c1a7e-124">无。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1a7e-125">父元素</span><span class="sxs-lookup"><span data-stu-id="c1a7e-125">Parent elements</span></span>

[<span data-ttu-id="c1a7e-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="c1a7e-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="c1a7e-127">备注</span><span class="sxs-lookup"><span data-stu-id="c1a7e-127">Remarks</span></span>

<span data-ttu-id="c1a7e-128">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1a7e-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c1a7e-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1a7e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1a7e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1a7e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1a7e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1a7e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1a7e-132">Schema name</span></span>  <br/> |<span data-ttu-id="c1a7e-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="c1a7e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1a7e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1a7e-134">Validation file</span></span>  <br/> |<span data-ttu-id="c1a7e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1a7e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1a7e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1a7e-136">Can be empty</span></span>  <br/> ||
   

