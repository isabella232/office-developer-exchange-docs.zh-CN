---
title: TimeZoneDefinition
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
description: TimeZoneDefinition 元素指定用于定义时区的周期和转换。
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466064"
---
# <a name="timezonedefinition"></a><span data-ttu-id="5c675-103">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="5c675-103">TimeZoneDefinition</span></span>

<span data-ttu-id="5c675-104">**TimeZoneDefinition**元素指定用于定义时区的周期和转换。</span><span class="sxs-lookup"><span data-stu-id="5c675-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="5c675-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="5c675-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c675-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c675-106">Attributes and elements</span></span>

<span data-ttu-id="5c675-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c675-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c675-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5c675-108">Attributes</span></span>

|<span data-ttu-id="5c675-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5c675-109">**Attribute**</span></span>|<span data-ttu-id="5c675-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c675-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c675-111">Id</span><span class="sxs-lookup"><span data-stu-id="5c675-111">Id</span></span>  <br/> |<span data-ttu-id="5c675-112">表示时区的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="5c675-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="5c675-113">名称</span><span class="sxs-lookup"><span data-stu-id="5c675-113">Name</span></span>  <br/> |<span data-ttu-id="5c675-114">表示时区的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="5c675-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5c675-115">子元素</span><span class="sxs-lookup"><span data-stu-id="5c675-115">Child elements</span></span>

|<span data-ttu-id="5c675-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c675-116">**Element**</span></span>|<span data-ttu-id="5c675-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c675-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c675-118">课时</span><span class="sxs-lookup"><span data-stu-id="5c675-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="5c675-119">表示用于定义时区的不同阶段的时间偏移量的[Period](period.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="5c675-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="5c675-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="5c675-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="5c675-121">表示[TransitionsGroup](transitionsgroup.md)元素的数组，这些元素指定时区转换。</span><span class="sxs-lookup"><span data-stu-id="5c675-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="5c675-122">移交</span><span class="sxs-lookup"><span data-stu-id="5c675-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="5c675-123">表示时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="5c675-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5c675-124">父元素</span><span class="sxs-lookup"><span data-stu-id="5c675-124">Parent elements</span></span>

|<span data-ttu-id="5c675-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c675-125">**Element**</span></span>|<span data-ttu-id="5c675-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c675-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c675-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="5c675-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="5c675-128">表示时区定义的数组。</span><span class="sxs-lookup"><span data-stu-id="5c675-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="5c675-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="5c675-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="5c675-130">表示用于限定使用 Exchange Web 服务（EWS）创建、更新和检索的对象的日期/时间属性的默认时区定义。</span><span class="sxs-lookup"><span data-stu-id="5c675-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c675-131">说明</span><span class="sxs-lookup"><span data-stu-id="5c675-131">Remarks</span></span>

<span data-ttu-id="5c675-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5c675-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c675-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c675-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c675-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c675-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c675-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c675-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5c675-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="5c675-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c675-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c675-137">Validation File</span></span>  <br/> |<span data-ttu-id="5c675-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c675-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c675-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c675-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c675-140">False</span><span class="sxs-lookup"><span data-stu-id="5c675-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c675-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c675-141">See also</span></span>



- [<span data-ttu-id="5c675-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5c675-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

