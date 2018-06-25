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
description: To 元素指定的时区转换的目标。 目标是所在的时区句点或一组所在的时区转换。
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838242"
---
# <a name="to"></a><span data-ttu-id="ba63d-104">To</span><span class="sxs-lookup"><span data-stu-id="ba63d-104">To</span></span>

<span data-ttu-id="ba63d-105">**To**元素指定的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="ba63d-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="ba63d-106">目标是所在的时区句点或一组所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="ba63d-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="ba63d-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba63d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba63d-108">Attributes and elements</span></span>

<span data-ttu-id="ba63d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba63d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba63d-110">属性</span><span class="sxs-lookup"><span data-stu-id="ba63d-110">Attributes</span></span>

|<span data-ttu-id="ba63d-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="ba63d-111">**Attribute**</span></span>|<span data-ttu-id="ba63d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba63d-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba63d-113">类型</span><span class="sxs-lookup"><span data-stu-id="ba63d-113">Kind</span></span>  <br/> |<span data-ttu-id="ba63d-114">指示所在的时区转换目标是否所在的时区期间或一组所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="ba63d-115">Kind 属性值</span><span class="sxs-lookup"><span data-stu-id="ba63d-115">Kind attribute values</span></span>

|<span data-ttu-id="ba63d-116">**值**</span><span class="sxs-lookup"><span data-stu-id="ba63d-116">**Value**</span></span>|<span data-ttu-id="ba63d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba63d-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba63d-118">句点</span><span class="sxs-lookup"><span data-stu-id="ba63d-118">Period</span></span>  <br/> |<span data-ttu-id="ba63d-119">指定时区转换目标时区句号。</span><span class="sxs-lookup"><span data-stu-id="ba63d-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="ba63d-120">组</span><span class="sxs-lookup"><span data-stu-id="ba63d-120">Group</span></span>  <br/> |<span data-ttu-id="ba63d-121">指定时区转换目标是一组所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ba63d-122">子元素</span><span class="sxs-lookup"><span data-stu-id="ba63d-122">Child elements</span></span>

<span data-ttu-id="ba63d-123">无。</span><span class="sxs-lookup"><span data-stu-id="ba63d-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba63d-124">父元素</span><span class="sxs-lookup"><span data-stu-id="ba63d-124">Parent elements</span></span>

|<span data-ttu-id="ba63d-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba63d-125">**Element**</span></span>|<span data-ttu-id="ba63d-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba63d-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba63d-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="ba63d-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="ba63d-128">代表在特定日期和在特定时间发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="ba63d-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="ba63d-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="ba63d-130">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="ba63d-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="ba63d-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="ba63d-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="ba63d-132">表示在一年中的指定日期发生所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="ba63d-133">转换</span><span class="sxs-lookup"><span data-stu-id="ba63d-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="ba63d-134">代表所在的时区转换。</span><span class="sxs-lookup"><span data-stu-id="ba63d-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba63d-135">文本值</span><span class="sxs-lookup"><span data-stu-id="ba63d-135">Text value</span></span>

<span data-ttu-id="ba63d-136">文本值是一个字符串，指定的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ba63d-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba63d-137">注解</span><span class="sxs-lookup"><span data-stu-id="ba63d-137">Remarks</span></span>

<span data-ttu-id="ba63d-138">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ba63d-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba63d-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba63d-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba63d-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba63d-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba63d-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba63d-141">Schema Name</span></span>  <br/> |<span data-ttu-id="ba63d-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="ba63d-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba63d-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba63d-143">Validation File</span></span>  <br/> |<span data-ttu-id="ba63d-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba63d-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba63d-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba63d-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba63d-146">False</span><span class="sxs-lookup"><span data-stu-id="ba63d-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba63d-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba63d-147">See also</span></span>



- [<span data-ttu-id="ba63d-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ba63d-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

