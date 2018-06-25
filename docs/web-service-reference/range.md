---
title: Range
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: 范围元素指定各种重复的日历项目的日历项目发生次数。
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826946"
---
# <a name="range"></a><span data-ttu-id="13189-103">Range</span><span class="sxs-lookup"><span data-stu-id="13189-103">Range</span></span>

<span data-ttu-id="13189-104">**范围**元素指定各种重复的日历项目的日历项目发生次数。</span><span class="sxs-lookup"><span data-stu-id="13189-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="13189-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="13189-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13189-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="13189-106">Attributes and elements</span></span>

<span data-ttu-id="13189-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="13189-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13189-108">属性</span><span class="sxs-lookup"><span data-stu-id="13189-108">Attributes</span></span>

|<span data-ttu-id="13189-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="13189-109">**Attribute**</span></span>|<span data-ttu-id="13189-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="13189-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13189-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="13189-111">**Start**</span></span> <br/> |<span data-ttu-id="13189-112">**启动**属性的文本值是定期项目范围的开始日期。</span><span class="sxs-lookup"><span data-stu-id="13189-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="13189-113">这是**dateTime**值。</span><span class="sxs-lookup"><span data-stu-id="13189-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="13189-114">**End**</span><span class="sxs-lookup"><span data-stu-id="13189-114">**End**</span></span> <br/> |<span data-ttu-id="13189-115">**End**属性的文本值是定期项目范围的结束日期。</span><span class="sxs-lookup"><span data-stu-id="13189-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="13189-116">这是**dateTime**值。</span><span class="sxs-lookup"><span data-stu-id="13189-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="13189-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="13189-117">**Count**</span></span> <br/> |<span data-ttu-id="13189-118">**计数**属性的文本值是定期项目的次数。</span><span class="sxs-lookup"><span data-stu-id="13189-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="13189-119">这是一个**整数**值。</span><span class="sxs-lookup"><span data-stu-id="13189-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="13189-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="13189-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="13189-121">文本值为**true**的**CompareOriginalStartTime**属性指示客户端应比较使用新的开始时间的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="13189-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="13189-122">如果值为**false**指示客户端不需要比较使用新的开始时间的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="13189-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13189-123">子元素</span><span class="sxs-lookup"><span data-stu-id="13189-123">Child elements</span></span>

<span data-ttu-id="13189-124">无。</span><span class="sxs-lookup"><span data-stu-id="13189-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="13189-125">父元素</span><span class="sxs-lookup"><span data-stu-id="13189-125">Parent elements</span></span>

[<span data-ttu-id="13189-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="13189-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="13189-127">备注</span><span class="sxs-lookup"><span data-stu-id="13189-127">Remarks</span></span>

<span data-ttu-id="13189-128">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="13189-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="13189-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="13189-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13189-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="13189-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13189-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="13189-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13189-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="13189-132">Schema name</span></span>  <br/> |<span data-ttu-id="13189-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="13189-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="13189-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="13189-134">Validation file</span></span>  <br/> |<span data-ttu-id="13189-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13189-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13189-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="13189-136">Can be empty</span></span>  <br/> ||
   

