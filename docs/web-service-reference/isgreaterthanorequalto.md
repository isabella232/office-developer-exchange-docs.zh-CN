---
title: IsGreaterThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThanOrEqualTo
api_type:
- schema
ms.assetid: 373cc954-314d-40e2-be03-cc08aefc0d5b
description: IsGreaterThanOrEqualTo 元素均表示一个搜索表达式，比较并以常量值或另一个属性，并返回 true，如果第一个属性大于或等于第二个属性。
ms.openlocfilehash: c469f2535ab717e7bc09b6317e01f0f8b3be8170
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354370"
---
# <a name="isgreaterthanorequalto"></a><span data-ttu-id="f4cc5-103">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="f4cc5-103">IsGreaterThanOrEqualTo</span></span>

<span data-ttu-id="f4cc5-104">**IsGreaterThanOrEqualTo**元素均表示一个搜索表达式，如果第一个属性是大于或等于第二个比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-104">The **IsGreaterThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the second.</span></span> 
  
```xml
<IsGreaterThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

```xml
<IsGreaterThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

<span data-ttu-id="f4cc5-105">**IsGreaterThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="f4cc5-105">**IsGreaterThanOrEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f4cc5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f4cc5-106">Attributes and elements</span></span>

<span data-ttu-id="f4cc5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4cc5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f4cc5-108">Attributes</span></span>

<span data-ttu-id="f4cc5-109">无。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4cc5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f4cc5-110">Child elements</span></span>

|<span data-ttu-id="f4cc5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4cc5-111">**Element**</span></span>|<span data-ttu-id="f4cc5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4cc5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4cc5-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f4cc5-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f4cc5-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f4cc5-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f4cc5-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f4cc5-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f4cc5-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="f4cc5-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="f4cc5-120">代表属性或以常量值，用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4cc5-121">父元素</span><span class="sxs-lookup"><span data-stu-id="f4cc5-121">Parent elements</span></span>

|<span data-ttu-id="f4cc5-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4cc5-122">**Element**</span></span>|<span data-ttu-id="f4cc5-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4cc5-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4cc5-124">限制</span><span class="sxs-lookup"><span data-stu-id="f4cc5-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="f4cc5-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-126">not</span><span class="sxs-lookup"><span data-stu-id="f4cc5-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="f4cc5-127">代表一个搜索表达式，它包含的搜索表达式的布尔值求非。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-128">And</span><span class="sxs-lookup"><span data-stu-id="f4cc5-128">And</span></span>](and.md) <br/> |<span data-ttu-id="f4cc5-129">表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="f4cc5-130">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="f4cc5-131">或</span><span class="sxs-lookup"><span data-stu-id="f4cc5-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="f4cc5-132">表示对它所包含的搜索表达式执行逻辑或搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="f4cc5-133">[或](or.md)将返回 true 如果任何其子返回 true。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="f4cc5-134">[Or](or.md) 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4cc5-135">备注</span><span class="sxs-lookup"><span data-stu-id="f4cc5-135">Remarks</span></span>

<span data-ttu-id="f4cc5-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f4cc5-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4cc5-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="f4cc5-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4cc5-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="f4cc5-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4cc5-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="f4cc5-139">Schema Name</span></span>  <br/> |<span data-ttu-id="f4cc5-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="f4cc5-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4cc5-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="f4cc5-141">Validation File</span></span>  <br/> |<span data-ttu-id="f4cc5-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4cc5-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4cc5-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="f4cc5-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4cc5-144">False</span><span class="sxs-lookup"><span data-stu-id="f4cc5-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4cc5-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4cc5-145">See also</span></span>

- [<span data-ttu-id="f4cc5-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f4cc5-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

