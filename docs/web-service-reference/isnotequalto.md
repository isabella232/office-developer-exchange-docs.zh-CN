---
title: IsNotEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotEqualTo
api_type:
- schema
ms.assetid: e2eff26c-3403-45cd-bb74-1eb98c7dbfcd
description: IsNotEqualTo 元素均表示一个搜索表达式的比较一个常数值的属性或另一个属性，并返回 true 如果值不相同。
ms.openlocfilehash: 75b580d97fbadbf3aa28c29159973f53768df624
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353250"
---
# <a name="isnotequalto"></a><span data-ttu-id="e62e8-103">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="e62e8-103">IsNotEqualTo</span></span>

<span data-ttu-id="e62e8-104">**IsNotEqualTo**元素均表示一个搜索表达式，如果值不相同比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="e62e8-104">The **IsNotEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span> 
  
```xml
<IsNotEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

<span data-ttu-id="e62e8-105">**IsNotEqualToType**</span><span class="sxs-lookup"><span data-stu-id="e62e8-105">**IsNotEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e62e8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e62e8-106">Attributes and elements</span></span>

<span data-ttu-id="e62e8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e62e8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e62e8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e62e8-108">Attributes</span></span>

<span data-ttu-id="e62e8-109">无。</span><span class="sxs-lookup"><span data-stu-id="e62e8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e62e8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e62e8-110">Child elements</span></span>

|<span data-ttu-id="e62e8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e62e8-111">**Element**</span></span>|<span data-ttu-id="e62e8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e62e8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e62e8-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e62e8-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e62e8-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="e62e8-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e62e8-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e62e8-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="e62e8-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e62e8-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e62e8-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="e62e8-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="e62e8-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="e62e8-120">代表属性或以常量值，用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="e62e8-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e62e8-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e62e8-121">Parent elements</span></span>

|<span data-ttu-id="e62e8-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="e62e8-122">**Element**</span></span>|<span data-ttu-id="e62e8-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="e62e8-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e62e8-124">限制</span><span class="sxs-lookup"><span data-stu-id="e62e8-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="e62e8-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="e62e8-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-126">not</span><span class="sxs-lookup"><span data-stu-id="e62e8-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="e62e8-127">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="e62e8-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-128">And</span><span class="sxs-lookup"><span data-stu-id="e62e8-128">And</span></span>](and.md) <br/> |<span data-ttu-id="e62e8-129">代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间 Boolean 和操作。</span><span class="sxs-lookup"><span data-stu-id="e62e8-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="e62e8-130">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="e62e8-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="e62e8-131">或</span><span class="sxs-lookup"><span data-stu-id="e62e8-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="e62e8-132">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="e62e8-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="e62e8-133">如果其任何子级返回 [true](or.md)，则 **或** 将返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="e62e8-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="e62e8-134">**Or** 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="e62e8-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e62e8-135">备注</span><span class="sxs-lookup"><span data-stu-id="e62e8-135">Remarks</span></span>

<span data-ttu-id="e62e8-136">若要执行字符串比较，应考虑使用[Contains](contains.md)元素，它提供用于匹配参数，如案例和空白选项。</span><span class="sxs-lookup"><span data-stu-id="e62e8-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters such as case and white space.</span></span> <span data-ttu-id="e62e8-137">将[不](not.md)元素中[包含](contains.md)元素结合使用，以否定结果。</span><span class="sxs-lookup"><span data-stu-id="e62e8-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="e62e8-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e62e8-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e62e8-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="e62e8-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e62e8-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="e62e8-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e62e8-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="e62e8-141">Schema Name</span></span>  <br/> |<span data-ttu-id="e62e8-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="e62e8-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="e62e8-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="e62e8-143">Validation File</span></span>  <br/> |<span data-ttu-id="e62e8-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e62e8-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e62e8-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="e62e8-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="e62e8-146">False</span><span class="sxs-lookup"><span data-stu-id="e62e8-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e62e8-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e62e8-147">See also</span></span>

- [<span data-ttu-id="e62e8-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e62e8-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

