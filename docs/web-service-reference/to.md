---
title: To
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: To 元素指定时区转换的目标。 目标为时区时间段或时区转换组。
ms.openlocfilehash: 8cce700eedd64035f2e21be4db6b517f3f85d98d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2020
ms.locfileid: "44468794"
---
# <a name="to"></a><span data-ttu-id="228f2-104">To</span><span class="sxs-lookup"><span data-stu-id="228f2-104">To</span></span>

<span data-ttu-id="228f2-105">**To**元素指定时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="228f2-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="228f2-106">目标为时区时间段或时区转换组。</span><span class="sxs-lookup"><span data-stu-id="228f2-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="228f2-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="228f2-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="228f2-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="228f2-108">Attributes and elements</span></span>

<span data-ttu-id="228f2-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="228f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="228f2-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="228f2-110">Attributes</span></span>

|<span data-ttu-id="228f2-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="228f2-111">**Attribute**</span></span>|<span data-ttu-id="228f2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="228f2-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="228f2-113">Kind</span><span class="sxs-lookup"><span data-stu-id="228f2-113">Kind</span></span>  <br/> |<span data-ttu-id="228f2-114">指示时区转换目标是时区转换的时间段还是一组时区转换。</span><span class="sxs-lookup"><span data-stu-id="228f2-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="228f2-115">Kind 属性值</span><span class="sxs-lookup"><span data-stu-id="228f2-115">Kind attribute values</span></span>

|<span data-ttu-id="228f2-116">**值**</span><span class="sxs-lookup"><span data-stu-id="228f2-116">**Value**</span></span>|<span data-ttu-id="228f2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="228f2-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="228f2-118">句点</span><span class="sxs-lookup"><span data-stu-id="228f2-118">Period</span></span>  <br/> |<span data-ttu-id="228f2-119">指定时区转换目标为时区时间段。</span><span class="sxs-lookup"><span data-stu-id="228f2-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="228f2-120">Group</span><span class="sxs-lookup"><span data-stu-id="228f2-120">Group</span></span>  <br/> |<span data-ttu-id="228f2-121">指定时区转换目标是一组时区转换。</span><span class="sxs-lookup"><span data-stu-id="228f2-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="228f2-122">子元素</span><span class="sxs-lookup"><span data-stu-id="228f2-122">Child elements</span></span>

<span data-ttu-id="228f2-123">无。</span><span class="sxs-lookup"><span data-stu-id="228f2-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="228f2-124">父元素</span><span class="sxs-lookup"><span data-stu-id="228f2-124">Parent elements</span></span>

|<span data-ttu-id="228f2-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="228f2-125">**Element**</span></span>|<span data-ttu-id="228f2-126">**描述**</span><span class="sxs-lookup"><span data-stu-id="228f2-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="228f2-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="228f2-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="228f2-128">表示在特定日期和特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="228f2-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="228f2-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="228f2-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="228f2-130">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="228f2-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="228f2-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="228f2-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="228f2-132">表示在指定的一年中的某一天发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="228f2-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="228f2-133">移交</span><span class="sxs-lookup"><span data-stu-id="228f2-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="228f2-134">表示时区转换。</span><span class="sxs-lookup"><span data-stu-id="228f2-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="228f2-135">文本值</span><span class="sxs-lookup"><span data-stu-id="228f2-135">Text value</span></span>

<span data-ttu-id="228f2-136">Text 值是一个字符串，它指定作为时区转换目标的[句点](period.md)或[TransitionsGroup](transitionsgroup.md)的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="228f2-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="228f2-137">备注</span><span class="sxs-lookup"><span data-stu-id="228f2-137">Remarks</span></span>

<span data-ttu-id="228f2-138">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="228f2-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="228f2-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="228f2-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="228f2-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="228f2-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="228f2-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="228f2-141">Schema Name</span></span>  <br/> |<span data-ttu-id="228f2-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="228f2-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="228f2-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="228f2-143">Validation File</span></span>  <br/> |<span data-ttu-id="228f2-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="228f2-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="228f2-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="228f2-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="228f2-146">False</span><span class="sxs-lookup"><span data-stu-id="228f2-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="228f2-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="228f2-147">See also</span></span>



- [<span data-ttu-id="228f2-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="228f2-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

