---
title: 时区定义
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: 时区定义元素指定时间段和定义时区的切换。
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838248"
---
# <a name="timezonedefinition"></a><span data-ttu-id="1ebdf-103">时区定义</span><span class="sxs-lookup"><span data-stu-id="1ebdf-103">TimeZoneDefinition</span></span>

<span data-ttu-id="1ebdf-104">**时区定义**元素指定时间段和定义时区的切换。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="1ebdf-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ebdf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1ebdf-106">Attributes and elements</span></span>

<span data-ttu-id="1ebdf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ebdf-108">属性</span><span class="sxs-lookup"><span data-stu-id="1ebdf-108">Attributes</span></span>

|<span data-ttu-id="1ebdf-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-109">**Attribute**</span></span>|<span data-ttu-id="1ebdf-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ebdf-111">Id</span><span class="sxs-lookup"><span data-stu-id="1ebdf-111">Id</span></span>  <br/> |<span data-ttu-id="1ebdf-112">代表时区的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="1ebdf-113">名称</span><span class="sxs-lookup"><span data-stu-id="1ebdf-113">Name</span></span>  <br/> |<span data-ttu-id="1ebdf-114">代表时区的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1ebdf-115">子元素</span><span class="sxs-lookup"><span data-stu-id="1ebdf-115">Child elements</span></span>

|<span data-ttu-id="1ebdf-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-116">**Element**</span></span>|<span data-ttu-id="1ebdf-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ebdf-118">时间段</span><span class="sxs-lookup"><span data-stu-id="1ebdf-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="1ebdf-119">表示定义的时间偏移量的时区的不同阶段的[时间段](period.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="1ebdf-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="1ebdf-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="1ebdf-121">代表指定时区转换的[TransitionsGroup](transitionsgroup.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="1ebdf-122">切换</span><span class="sxs-lookup"><span data-stu-id="1ebdf-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="1ebdf-123">代表所在的时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ebdf-124">父元素</span><span class="sxs-lookup"><span data-stu-id="1ebdf-124">Parent elements</span></span>

|<span data-ttu-id="1ebdf-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-125">**Element**</span></span>|<span data-ttu-id="1ebdf-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ebdf-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ebdf-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="1ebdf-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="1ebdf-128">代表所在的时区定义的数组。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="1ebdf-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="1ebdf-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="1ebdf-130">表示用于范围对象的创建、 更新和使用 Exchange Web Services (EWS) 检索 DateTime 属性的默认时区定义。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ebdf-131">备注</span><span class="sxs-lookup"><span data-stu-id="1ebdf-131">Remarks</span></span>

<span data-ttu-id="1ebdf-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1ebdf-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ebdf-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="1ebdf-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ebdf-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="1ebdf-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ebdf-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="1ebdf-135">Schema Name</span></span>  <br/> |<span data-ttu-id="1ebdf-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="1ebdf-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ebdf-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="1ebdf-137">Validation File</span></span>  <br/> |<span data-ttu-id="1ebdf-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ebdf-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ebdf-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="1ebdf-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ebdf-140">False</span><span class="sxs-lookup"><span data-stu-id="1ebdf-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ebdf-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1ebdf-141">See also</span></span>



- [<span data-ttu-id="1ebdf-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1ebdf-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

