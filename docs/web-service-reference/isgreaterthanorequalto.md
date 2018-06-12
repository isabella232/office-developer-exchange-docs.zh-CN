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
ms.openlocfilehash: 81df79d15e6c5c8d301e69a822d038588ce42325
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826030"
---
# <a name="isgreaterthanorequalto"></a><span data-ttu-id="9e863-103">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="9e863-103">IsGreaterThanOrEqualTo</span></span>

<span data-ttu-id="9e863-104">**IsGreaterThanOrEqualTo**元素均表示一个搜索表达式，如果第一个属性是大于或等于第二个比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="9e863-104">The **IsGreaterThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the second.</span></span> 
  
```xml
<IsGreaterThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThanOrEqualTo>
```

 <span data-ttu-id="9e863-105">**IsGreaterThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="9e863-105">**IsGreaterThanOrEqualToType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e863-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9e863-106">Attributes and elements</span></span>

<span data-ttu-id="9e863-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9e863-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e863-108">属性</span><span class="sxs-lookup"><span data-stu-id="9e863-108">Attributes</span></span>

<span data-ttu-id="9e863-109">无。</span><span class="sxs-lookup"><span data-stu-id="9e863-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e863-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9e863-110">Child elements</span></span>

|<span data-ttu-id="9e863-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9e863-111">**Element**</span></span>|<span data-ttu-id="9e863-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e863-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e863-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="9e863-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="9e863-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="9e863-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="9e863-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9e863-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="9e863-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="9e863-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="9e863-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9e863-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="9e863-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="9e863-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="9e863-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="9e863-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="9e863-120">代表属性或以常量值，用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="9e863-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9e863-121">父元素</span><span class="sxs-lookup"><span data-stu-id="9e863-121">Parent elements</span></span>

|<span data-ttu-id="9e863-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="9e863-122">**Element**</span></span>|<span data-ttu-id="9e863-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e863-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e863-124">限制</span><span class="sxs-lookup"><span data-stu-id="9e863-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9e863-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="9e863-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9e863-126">not</span><span class="sxs-lookup"><span data-stu-id="9e863-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="9e863-127">代表一个搜索表达式，它包含的搜索表达式的布尔值求非。</span><span class="sxs-lookup"><span data-stu-id="9e863-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="9e863-128">And</span><span class="sxs-lookup"><span data-stu-id="9e863-128">And</span></span>](and.md) <br/> |<span data-ttu-id="9e863-129">表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9e863-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="9e863-130">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="9e863-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="9e863-131">或</span><span class="sxs-lookup"><span data-stu-id="9e863-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="9e863-132">表示对它所包含的搜索表达式执行逻辑或搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9e863-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="9e863-133">[或](or.md)将返回 true 如果任何其子返回 true。</span><span class="sxs-lookup"><span data-stu-id="9e863-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="9e863-134">[Or](or.md) 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="9e863-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e863-135">备注</span><span class="sxs-lookup"><span data-stu-id="9e863-135">Remarks</span></span>

<span data-ttu-id="9e863-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9e863-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e863-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="9e863-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e863-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="9e863-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e863-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="9e863-139">Schema Name</span></span>  <br/> |<span data-ttu-id="9e863-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="9e863-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e863-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="9e863-141">Validation File</span></span>  <br/> |<span data-ttu-id="9e863-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e863-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e863-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="9e863-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e863-144">False</span><span class="sxs-lookup"><span data-stu-id="9e863-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e863-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e863-145">See also</span></span>



- [<span data-ttu-id="9e863-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9e863-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
