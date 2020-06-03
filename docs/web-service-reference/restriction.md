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
description: 限制元素表示用于筛选 FindItem/FindFolder 中的项或文件夹以及搜索文件夹操作的限制或查询。
ms.openlocfilehash: 6037ba15417d67d393ca70f3edf2248749c396e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465287"
---
# <a name="restriction"></a><span data-ttu-id="f80da-103">限制</span><span class="sxs-lookup"><span data-stu-id="f80da-103">Restriction</span></span>

<span data-ttu-id="f80da-104">**限制**元素表示用于筛选 FindItem/FindFolder 中的项或文件夹以及搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="f80da-104">The **Restriction** element represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span> 
  
```xml
<Restriction>
   <SearchExpression/>
</Restriction>
```

 <span data-ttu-id="f80da-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="f80da-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f80da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f80da-106">Attributes and elements</span></span>

<span data-ttu-id="f80da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f80da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f80da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f80da-108">Attributes</span></span>

<span data-ttu-id="f80da-109">无。</span><span class="sxs-lookup"><span data-stu-id="f80da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f80da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f80da-110">Child elements</span></span>

|<span data-ttu-id="f80da-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f80da-111">**Element**</span></span>|<span data-ttu-id="f80da-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f80da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f80da-113">And</span><span class="sxs-lookup"><span data-stu-id="f80da-113">And</span></span>](and.md) <br/> |<span data-ttu-id="f80da-114">表示允许您在两个或多个搜索表达式之间执行布尔**AND**运算的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f80da-114">Represents a search expression that enables you to perform a Boolean **AND** operation between two or more search expressions.</span></span>  <br/> |
|[<span data-ttu-id="f80da-115">Contains</span><span class="sxs-lookup"><span data-stu-id="f80da-115">Contains</span></span>](contains.md) <br/> |<span data-ttu-id="f80da-116">表示一个搜索表达式，该表达式确定给定属性是否包含提供的常量字符串值。</span><span class="sxs-lookup"><span data-stu-id="f80da-116">Represents a search expression that determines whether a given property contains the supplied constant string value.</span></span>  <br/> |
|[<span data-ttu-id="f80da-117">不包括</span><span class="sxs-lookup"><span data-stu-id="f80da-117">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="f80da-118">执行这些属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="f80da-118">Performs a bitwise mask of the properties.</span></span>  <br/> |
|[<span data-ttu-id="f80da-119">Exists</span><span class="sxs-lookup"><span data-stu-id="f80da-119">Exists</span></span>](exists.md) <br/> |<span data-ttu-id="f80da-120">表示在项上存在提供的属性时返回**true**的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f80da-120">Represents a search expression that returns **true** if the supplied property exists on an item.</span></span>  <br/> |
|[<span data-ttu-id="f80da-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="f80da-121">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="f80da-122">表示搜索表达式，该表达式将属性与常数值或其他属性进行比较，如果它们相等，则计算结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-122">Represents a search expression that compares a property with either a constant value or another property and evaluates to **true** if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="f80da-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="f80da-123">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="f80da-124">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于值或属性，**则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-124">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="f80da-125">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="f80da-125">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="f80da-126">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于或等于 value 或属性，**则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-126">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="f80da-127">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="f80da-127">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="f80da-128">表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果第一个属性小于值或属性，**则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-128">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the value or property.</span></span>  <br/> |
|[<span data-ttu-id="f80da-129">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="f80da-129">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="f80da-130">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于或等于 value 或属性，**则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-130">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the value or property.</span></span>  <br/> |
|[<span data-ttu-id="f80da-131">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="f80da-131">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="f80da-132">表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果值不相同，**则返回 true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-132">Represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span>  <br/> |
|[<span data-ttu-id="f80da-133">Not</span><span class="sxs-lookup"><span data-stu-id="f80da-133">Not</span></span>](not.md) <br/> |<span data-ttu-id="f80da-134">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f80da-134">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="f80da-135">或</span><span class="sxs-lookup"><span data-stu-id="f80da-135">Or</span></span>](or.md) <br/> |<span data-ttu-id="f80da-136">表示在其包含的搜索表达式上执行逻辑**OR**运算的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f80da-136">Represents a search expression that performs a logical **OR** operation on the search expression it contains.</span></span> <span data-ttu-id="f80da-137">如果其任何子级返回**true**，则**或**元素将返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="f80da-137">The **Or** element will return **true** if any of its children return **true**.</span></span>  <br/> |
|[<span data-ttu-id="f80da-138">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="f80da-138">SearchExpression</span></span>](searchexpression.md) <br/> |<span data-ttu-id="f80da-139">表示限制中的替代元素。</span><span class="sxs-lookup"><span data-stu-id="f80da-139">Represents the substituted element within a restriction.</span></span> <span data-ttu-id="f80da-140">XML 实例文档中不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="f80da-140">This element is not used in an XML instance document.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f80da-141">父元素</span><span class="sxs-lookup"><span data-stu-id="f80da-141">Parent elements</span></span>

|<span data-ttu-id="f80da-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="f80da-142">**Element**</span></span>|<span data-ttu-id="f80da-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="f80da-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f80da-144">FindFolder</span><span class="sxs-lookup"><span data-stu-id="f80da-144">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="f80da-145">定义用于标识邮箱中的文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="f80da-145">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f80da-146">FindItem</span><span class="sxs-lookup"><span data-stu-id="f80da-146">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f80da-147">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f80da-147">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f80da-148">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="f80da-148">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="f80da-149">表示用于定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="f80da-149">Represents the parameters that define a search folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f80da-150">说明</span><span class="sxs-lookup"><span data-stu-id="f80da-150">Remarks</span></span>

<span data-ttu-id="f80da-151">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f80da-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f80da-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="f80da-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f80da-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="f80da-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f80da-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="f80da-154">Schema Name</span></span>  <br/> |<span data-ttu-id="f80da-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="f80da-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="f80da-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="f80da-156">Validation File</span></span>  <br/> |<span data-ttu-id="f80da-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f80da-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f80da-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="f80da-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="f80da-159">False</span><span class="sxs-lookup"><span data-stu-id="f80da-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f80da-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f80da-160">See also</span></span>



- [<span data-ttu-id="f80da-161">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f80da-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

