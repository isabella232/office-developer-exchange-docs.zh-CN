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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468794"
---
# <a name="to"></a><span data-ttu-id="7e51e-104">To</span><span class="sxs-lookup"><span data-stu-id="7e51e-104">To</span></span>

<span data-ttu-id="7e51e-105">**To**元素指定时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="7e51e-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="7e51e-106">目标为时区时间段或时区转换组。</span><span class="sxs-lookup"><span data-stu-id="7e51e-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="7e51e-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="7e51e-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e51e-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e51e-108">Attributes and elements</span></span>

<span data-ttu-id="7e51e-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e51e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e51e-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="7e51e-110">Attributes</span></span>

|<span data-ttu-id="7e51e-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="7e51e-111">**Attribute**</span></span>|<span data-ttu-id="7e51e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e51e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e51e-113">Kind</span><span class="sxs-lookup"><span data-stu-id="7e51e-113">Kind</span></span>  <br/> |<span data-ttu-id="7e51e-114">指示时区转换目标是时区转换的时间段还是一组时区转换。</span><span class="sxs-lookup"><span data-stu-id="7e51e-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="7e51e-115">Kind 属性值</span><span class="sxs-lookup"><span data-stu-id="7e51e-115">Kind attribute values</span></span>

|<span data-ttu-id="7e51e-116">**值**</span><span class="sxs-lookup"><span data-stu-id="7e51e-116">**Value**</span></span>|<span data-ttu-id="7e51e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7e51e-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e51e-118">句点</span><span class="sxs-lookup"><span data-stu-id="7e51e-118">Period</span></span>  <br/> |<span data-ttu-id="7e51e-119">指定时区转换目标为时区时间段。</span><span class="sxs-lookup"><span data-stu-id="7e51e-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="7e51e-120">Group</span><span class="sxs-lookup"><span data-stu-id="7e51e-120">Group</span></span>  <br/> |<span data-ttu-id="7e51e-121">指定时区转换目标是一组时区转换。</span><span class="sxs-lookup"><span data-stu-id="7e51e-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e51e-122">子元素</span><span class="sxs-lookup"><span data-stu-id="7e51e-122">Child elements</span></span>

<span data-ttu-id="7e51e-123">无。</span><span class="sxs-lookup"><span data-stu-id="7e51e-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7e51e-124">父元素</span><span class="sxs-lookup"><span data-stu-id="7e51e-124">Parent elements</span></span>

|<span data-ttu-id="7e51e-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="7e51e-125">**Element**</span></span>|<span data-ttu-id="7e51e-126">**描述**</span><span class="sxs-lookup"><span data-stu-id="7e51e-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7e51e-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="7e51e-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="7e51e-128">表示在特定日期和特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="7e51e-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="7e51e-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="7e51e-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="7e51e-130">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="7e51e-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="7e51e-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="7e51e-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="7e51e-132">表示在指定的一年中的某一天发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="7e51e-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="7e51e-133">移交</span><span class="sxs-lookup"><span data-stu-id="7e51e-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="7e51e-134">表示时区转换。</span><span class="sxs-lookup"><span data-stu-id="7e51e-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7e51e-135">文本值</span><span class="sxs-lookup"><span data-stu-id="7e51e-135">Text value</span></span>

<span data-ttu-id="7e51e-136">Text 值是一个字符串，它指定作为时区转换目标的[句点](period.md)或[TransitionsGroup](transitionsgroup.md)的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7e51e-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7e51e-137">备注</span><span class="sxs-lookup"><span data-stu-id="7e51e-137">Remarks</span></span>

<span data-ttu-id="7e51e-138">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e51e-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e51e-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e51e-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e51e-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e51e-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7e51e-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e51e-141">Schema Name</span></span>  <br/> |<span data-ttu-id="7e51e-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="7e51e-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="7e51e-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e51e-143">Validation File</span></span>  <br/> |<span data-ttu-id="7e51e-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7e51e-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7e51e-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e51e-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="7e51e-146">False</span><span class="sxs-lookup"><span data-stu-id="7e51e-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7e51e-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7e51e-147">See also</span></span>



- [<span data-ttu-id="7e51e-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7e51e-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

