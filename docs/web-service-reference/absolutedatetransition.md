---
title: AbsoluteDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDateTransition
api_type:
- schema
ms.assetid: 8f5731eb-bed0-45bf-ba89-4aaf20c34a39
description: AbsoluteDateTransition 元素均表示在特定日期和在特定时间发生的时区转换。
ms.openlocfilehash: 1e9e5f3f2269814a82b827efe46c71a172e21348
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753092"
---
# <a name="absolutedatetransition"></a><span data-ttu-id="d6b50-103">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="d6b50-103">AbsoluteDateTransition</span></span>

<span data-ttu-id="d6b50-104">**AbsoluteDateTransition**元素均表示在特定日期和在特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="d6b50-104">The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time.</span></span> 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

<span data-ttu-id="d6b50-105">**AbsoluteDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="d6b50-105">**AbsoluteDateTransitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d6b50-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d6b50-106">Attributes and elements</span></span>

<span data-ttu-id="d6b50-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d6b50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6b50-108">属性</span><span class="sxs-lookup"><span data-stu-id="d6b50-108">Attributes</span></span>

<span data-ttu-id="d6b50-109">无。</span><span class="sxs-lookup"><span data-stu-id="d6b50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6b50-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d6b50-110">Child elements</span></span>

|<span data-ttu-id="d6b50-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d6b50-111">**Element**</span></span>|<span data-ttu-id="d6b50-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d6b50-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6b50-113">To</span><span class="sxs-lookup"><span data-stu-id="d6b50-113">To</span></span>](to.md) <br/> |<span data-ttu-id="d6b50-114">指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="d6b50-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="d6b50-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="d6b50-115">DateTime</span></span>](datetime.md) <br/> |<span data-ttu-id="d6b50-116">表示的日期和时间发生所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="d6b50-116">Represents the date and time at which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d6b50-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d6b50-117">Parent elements</span></span>

|<span data-ttu-id="d6b50-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d6b50-118">**Element**</span></span>|<span data-ttu-id="d6b50-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d6b50-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6b50-120">切换</span><span class="sxs-lookup"><span data-stu-id="d6b50-120">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="d6b50-121">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="d6b50-121">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="d6b50-122">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="d6b50-122">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="d6b50-123">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="d6b50-123">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6b50-124">备注</span><span class="sxs-lookup"><span data-stu-id="d6b50-124">Remarks</span></span>

<span data-ttu-id="d6b50-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d6b50-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6b50-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="d6b50-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6b50-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="d6b50-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6b50-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d6b50-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d6b50-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="d6b50-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6b50-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d6b50-130">Validation File</span></span>  <br/> |<span data-ttu-id="d6b50-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6b50-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6b50-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d6b50-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6b50-133">False</span><span class="sxs-lookup"><span data-stu-id="d6b50-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6b50-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d6b50-134">See also</span></span>

- [<span data-ttu-id="d6b50-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d6b50-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

