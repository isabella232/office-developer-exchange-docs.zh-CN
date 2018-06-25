---
title: 日
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Day
api_type:
- schema
ms.assetid: d3b2dc66-486a-41d1-bff3-606f0bf92715
description: Day 元素表示在所在的时区转换发生相应月份的某一天。
ms.openlocfilehash: 01d1bf7833a89c0bb9a2b1af95ec8dfc627336d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753756"
---
# <a name="day"></a><span data-ttu-id="64933-103">日</span><span class="sxs-lookup"><span data-stu-id="64933-103">Day</span></span>

<span data-ttu-id="64933-104">**Day**元素表示在所在的时区转换发生相应月份的某一天。</span><span class="sxs-lookup"><span data-stu-id="64933-104">The **Day** element represents the day of the month on which the time zone transition occurs.</span></span> 
  
```xml
<Day/>
```

<span data-ttu-id="64933-105">**int**</span><span class="sxs-lookup"><span data-stu-id="64933-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="64933-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64933-106">Attributes and elements</span></span>

<span data-ttu-id="64933-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64933-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64933-108">属性</span><span class="sxs-lookup"><span data-stu-id="64933-108">Attributes</span></span>

<span data-ttu-id="64933-109">无。</span><span class="sxs-lookup"><span data-stu-id="64933-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64933-110">子元素</span><span class="sxs-lookup"><span data-stu-id="64933-110">Child elements</span></span>

<span data-ttu-id="64933-111">无。</span><span class="sxs-lookup"><span data-stu-id="64933-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="64933-112">父元素</span><span class="sxs-lookup"><span data-stu-id="64933-112">Parent elements</span></span>

|<span data-ttu-id="64933-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="64933-113">**Element**</span></span>|<span data-ttu-id="64933-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="64933-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64933-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="64933-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="64933-116">表示每年的特定日期发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="64933-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="64933-117">文本值</span><span class="sxs-lookup"><span data-stu-id="64933-117">Text value</span></span>

<span data-ttu-id="64933-118">**Day**元素的文本值是一个整数，表示在所在的时区转换发生相应月份的某一天。</span><span class="sxs-lookup"><span data-stu-id="64933-118">The text value of the **Day** element is an integer that represents the day of the month on which the time zone transition occurs.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="64933-119">备注</span><span class="sxs-lookup"><span data-stu-id="64933-119">Remarks</span></span>

<span data-ttu-id="64933-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="64933-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64933-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="64933-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64933-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="64933-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64933-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="64933-123">Schema Name</span></span>  <br/> |<span data-ttu-id="64933-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="64933-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="64933-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="64933-125">Validation File</span></span>  <br/> |<span data-ttu-id="64933-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="64933-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64933-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="64933-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="64933-128">False</span><span class="sxs-lookup"><span data-stu-id="64933-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64933-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64933-129">See also</span></span>

- [<span data-ttu-id="64933-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="64933-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

