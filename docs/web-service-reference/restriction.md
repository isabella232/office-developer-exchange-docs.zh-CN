---
title: 限制
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Restriction
api_type:
- schema
ms.assetid: 77f19014-d112-4999-8e83-ecc32a117a73
description: 限制元素均表示的限制或用于筛选项目或 FindItem/FindFolder 和搜索文件夹操作中的文件夹的查询。
ms.openlocfilehash: 6b5702696db29910ae476a370bf362fe6a036ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827213"
---
# <a name="restriction"></a><span data-ttu-id="9239c-103">限制</span><span class="sxs-lookup"><span data-stu-id="9239c-103">Restriction</span></span>

<span data-ttu-id="9239c-104">**限制**元素均表示的限制或用于筛选项目或 FindItem/FindFolder 和搜索文件夹操作中的文件夹的查询。</span><span class="sxs-lookup"><span data-stu-id="9239c-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="9239c-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="9239c-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9239c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9239c-106">Attributes and elements</span></span>

<span data-ttu-id="9239c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9239c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9239c-108">属性</span><span class="sxs-lookup"><span data-stu-id="9239c-108">Attributes</span></span>

<span data-ttu-id="9239c-109">无。</span><span class="sxs-lookup"><span data-stu-id="9239c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9239c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9239c-110">Child elements</span></span>

|<span data-ttu-id="9239c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9239c-111">**Element**</span></span>|<span data-ttu-id="9239c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9239c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9239c-113">And</span><span class="sxs-lookup"><span data-stu-id="9239c-113">And</span></span>](and.md) <br/> |<span data-ttu-id="9239c-114">代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间的布尔**和**操作。</span><span class="sxs-lookup"><span data-stu-id="9239c-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="9239c-115">Contains</span><span class="sxs-lookup"><span data-stu-id="9239c-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="9239c-116">代表一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。</span><span class="sxs-lookup"><span data-stu-id="9239c-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="9239c-117">不包括</span><span class="sxs-lookup"><span data-stu-id="9239c-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="9239c-118">执行这些属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="9239c-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="9239c-119">Exists</span><span class="sxs-lookup"><span data-stu-id="9239c-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="9239c-120">代表返回**true**如果所提供的属性存在项目的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9239c-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="9239c-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="9239c-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="9239c-122">代表一个搜索表达式的比较一个常数值的属性或另一个属性，并计算结果为**true** ，如果二者相等。</span><span class="sxs-lookup"><span data-stu-id="9239c-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="9239c-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="9239c-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="9239c-124">代表一个搜索表达式，如果第一个属性大于属性的值比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="9239c-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="9239c-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="9239c-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="9239c-126">代表一个搜索表达式，如果第一个属性是大于或等于或属性的值比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="9239c-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="9239c-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="9239c-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="9239c-128">代表一个搜索表达式，如果第一个属性或属性的值小于比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="9239c-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="9239c-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="9239c-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="9239c-130">代表一个搜索表达式，如果第一个属性小于或等于或属性的值比较常量值或另一个属性，返回**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="9239c-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="9239c-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="9239c-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="9239c-132">表示搜索表达式的比较常量值或另一个属性，返回**true**的属性，如果值不相同。</span><span class="sxs-lookup"><span data-stu-id="9239c-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="9239c-133">not</span><span class="sxs-lookup"><span data-stu-id="9239c-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="9239c-134">代表一个搜索表达式，它包含的搜索表达式的布尔值求非。</span><span class="sxs-lookup"><span data-stu-id="9239c-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="9239c-135">或</span><span class="sxs-lookup"><span data-stu-id="9239c-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="9239c-136">代表搜索表达式执行逻辑**OR**运算上包含的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9239c-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="9239c-137">如果任何其子返回**true**，则将返回**true** **或**元素。</span><span class="sxs-lookup"><span data-stu-id="9239c-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="9239c-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="9239c-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="9239c-139">代表限制中的替代的元素。</span><span class="sxs-lookup"><span data-stu-id="9239c-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="9239c-140">XML 实例文档中不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="9239c-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9239c-141">父元素</span><span class="sxs-lookup"><span data-stu-id="9239c-141">Parent elements</span></span>

|<span data-ttu-id="9239c-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="9239c-142">**Element**</span></span>|<span data-ttu-id="9239c-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="9239c-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9239c-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="9239c-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="9239c-145">定义一个请求，以确定邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="9239c-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="9239c-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="9239c-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="9239c-147">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="9239c-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="9239c-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="9239c-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="9239c-149">表示定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="9239c-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9239c-150">备注</span><span class="sxs-lookup"><span data-stu-id="9239c-150">Remarks</span></span>

<span data-ttu-id="9239c-151">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9239c-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9239c-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="9239c-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9239c-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="9239c-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9239c-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="9239c-154">Schema Name</span></span>  <br/> |<span data-ttu-id="9239c-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="9239c-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="9239c-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="9239c-156">Validation File</span></span>  <br/> |<span data-ttu-id="9239c-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9239c-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9239c-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="9239c-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="9239c-159">False</span><span class="sxs-lookup"><span data-stu-id="9239c-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9239c-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9239c-160">See also</span></span>



- [<span data-ttu-id="9239c-161">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9239c-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

