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
description: AbsoluteDateTransition 元素表示在特定日期和特定时间发生的时区转换。
ms.openlocfilehash: 514464f69c3be5496aedbe184848ef9ed9f296b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461721"
---
# <a name="absolutedatetransition"></a><span data-ttu-id="bdd1e-103">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="bdd1e-103">AbsoluteDateTransition</span></span>

<span data-ttu-id="bdd1e-104">**AbsoluteDateTransition**元素表示在特定日期和特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-104">The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time.</span></span> 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

<span data-ttu-id="bdd1e-105">**AbsoluteDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="bdd1e-105">**AbsoluteDateTransitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bdd1e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bdd1e-106">Attributes and elements</span></span>

<span data-ttu-id="bdd1e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdd1e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bdd1e-108">Attributes</span></span>

<span data-ttu-id="bdd1e-109">无。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdd1e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bdd1e-110">Child elements</span></span>

|<span data-ttu-id="bdd1e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bdd1e-111">**Element**</span></span>|<span data-ttu-id="bdd1e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bdd1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdd1e-113">To</span><span class="sxs-lookup"><span data-stu-id="bdd1e-113">To</span></span>](to.md) <br/> |<span data-ttu-id="bdd1e-114">指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="bdd1e-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="bdd1e-115">DateTime</span></span>](datetime.md) <br/> |<span data-ttu-id="bdd1e-116">表示时区转换发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-116">Represents the date and time at which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdd1e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="bdd1e-117">Parent elements</span></span>

|<span data-ttu-id="bdd1e-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="bdd1e-118">**Element**</span></span>|<span data-ttu-id="bdd1e-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="bdd1e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdd1e-120">移交</span><span class="sxs-lookup"><span data-stu-id="bdd1e-120">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="bdd1e-121">表示时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-121">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="bdd1e-122">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="bdd1e-122">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="bdd1e-123">表示时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-123">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdd1e-124">说明</span><span class="sxs-lookup"><span data-stu-id="bdd1e-124">Remarks</span></span>

<span data-ttu-id="bdd1e-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bdd1e-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdd1e-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="bdd1e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdd1e-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="bdd1e-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bdd1e-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="bdd1e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="bdd1e-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="bdd1e-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="bdd1e-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="bdd1e-130">Validation File</span></span>  <br/> |<span data-ttu-id="bdd1e-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bdd1e-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bdd1e-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="bdd1e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="bdd1e-133">False</span><span class="sxs-lookup"><span data-stu-id="bdd1e-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdd1e-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdd1e-134">See also</span></span>

- [<span data-ttu-id="bdd1e-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bdd1e-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

