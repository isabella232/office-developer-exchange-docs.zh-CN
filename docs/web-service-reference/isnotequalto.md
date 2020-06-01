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
description: IsNotEqualTo 元素表示一个搜索表达式，该表达式将属性与一个常量值或另一个属性进行比较，如果值不相同，则返回 true。
ms.openlocfilehash: 8c40fd1ce8c7c1f14b70f4fccfd3a24e4c99f1b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464187"
---
# <a name="isnotequalto"></a><span data-ttu-id="d7342-103">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="d7342-103">IsNotEqualTo</span></span>

<span data-ttu-id="d7342-104">**IsNotEqualTo**元素表示一个搜索表达式，该表达式将属性与一个常量值或另一个属性进行比较，如果值不相同，则返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="d7342-104">The **IsNotEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span> 
  
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

<span data-ttu-id="d7342-105">**IsNotEqualToType**</span><span class="sxs-lookup"><span data-stu-id="d7342-105">**IsNotEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d7342-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d7342-106">Attributes and elements</span></span>

<span data-ttu-id="d7342-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d7342-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7342-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d7342-108">Attributes</span></span>

<span data-ttu-id="d7342-109">无。</span><span class="sxs-lookup"><span data-stu-id="d7342-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7342-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d7342-110">Child elements</span></span>

|<span data-ttu-id="d7342-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7342-111">**Element**</span></span>|<span data-ttu-id="d7342-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7342-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7342-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d7342-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="d7342-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="d7342-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="d7342-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d7342-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="d7342-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="d7342-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="d7342-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d7342-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="d7342-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="d7342-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="d7342-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="d7342-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="d7342-120">表示与其他属性进行比较时要使用的属性或常数值。</span><span class="sxs-lookup"><span data-stu-id="d7342-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7342-121">父元素</span><span class="sxs-lookup"><span data-stu-id="d7342-121">Parent elements</span></span>

|<span data-ttu-id="d7342-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7342-122">**Element**</span></span>|<span data-ttu-id="d7342-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7342-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7342-124">限制</span><span class="sxs-lookup"><span data-stu-id="d7342-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="d7342-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="d7342-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="d7342-126">not</span><span class="sxs-lookup"><span data-stu-id="d7342-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="d7342-127">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="d7342-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="d7342-128">And</span><span class="sxs-lookup"><span data-stu-id="d7342-128">And</span></span>](and.md) <br/> |<span data-ttu-id="d7342-129">表示允许您在两个或多个搜索表达式之间执行布尔 And 运算的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="d7342-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="d7342-130">如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="d7342-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="d7342-131">或</span><span class="sxs-lookup"><span data-stu-id="d7342-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="d7342-132">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="d7342-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="d7342-133">如果其任何子级返回 [true](or.md)，则 **或** 将返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="d7342-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="d7342-134">**Or** 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="d7342-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7342-135">说明</span><span class="sxs-lookup"><span data-stu-id="d7342-135">Remarks</span></span>

<span data-ttu-id="d7342-136">若要执行字符串比较，请考虑使用[Contains](contains.md)元素，因为它提供了匹配参数（如大小写和空格）的选项。</span><span class="sxs-lookup"><span data-stu-id="d7342-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters such as case and white space.</span></span> <span data-ttu-id="d7342-137">将[Not](not.md)元素与[Contains](contains.md)元素一起使用可对结果取负。</span><span class="sxs-lookup"><span data-stu-id="d7342-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="d7342-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d7342-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7342-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="d7342-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7342-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="d7342-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7342-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="d7342-141">Schema Name</span></span>  <br/> |<span data-ttu-id="d7342-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="d7342-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="d7342-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="d7342-143">Validation File</span></span>  <br/> |<span data-ttu-id="d7342-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7342-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7342-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="d7342-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7342-146">False</span><span class="sxs-lookup"><span data-stu-id="d7342-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7342-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7342-147">See also</span></span>

- [<span data-ttu-id="d7342-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d7342-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

