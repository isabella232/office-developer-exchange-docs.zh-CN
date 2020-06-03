---
title: SearchExpression
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchExpression
api_type:
- schema
ms.assetid: daa179b6-8c7f-4268-a312-c2acc67fa7c3
description: SearchExpression 元素是一个抽象元素，表示限制中的替换元素。 所有搜索表达式均派生自此基类型。 XML 实例文档中不使用此元素。
ms.openlocfilehash: db06ce8e2faa0f2589963d58aab55073c618c171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530350"
---
# <a name="searchexpression"></a><span data-ttu-id="e62e9-105">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="e62e9-105">SearchExpression</span></span>

<span data-ttu-id="e62e9-106">**SearchExpression**元素是一个抽象元素，表示限制中的替换元素。</span><span class="sxs-lookup"><span data-stu-id="e62e9-106">The **SearchExpression** element is an abstract element that represents the substituted element within a restriction.</span></span> <span data-ttu-id="e62e9-107">所有搜索表达式均派生自此基类型。</span><span class="sxs-lookup"><span data-stu-id="e62e9-107">All search expressions derive from this base type.</span></span> <span data-ttu-id="e62e9-108">XML 实例文档中不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="e62e9-108">This element is not used in an XML instance document.</span></span> 
  
```xml
<SearchExpression/>
```

 <span data-ttu-id="e62e9-109">**SearchExpressionType**</span><span class="sxs-lookup"><span data-stu-id="e62e9-109">**SearchExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e62e9-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e62e9-110">Attributes and elements</span></span>

<span data-ttu-id="e62e9-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e62e9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e62e9-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="e62e9-112">Attributes</span></span>

<span data-ttu-id="e62e9-113">无。</span><span class="sxs-lookup"><span data-stu-id="e62e9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e62e9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e62e9-114">Child elements</span></span>

<span data-ttu-id="e62e9-115">无。</span><span class="sxs-lookup"><span data-stu-id="e62e9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e62e9-116">父元素</span><span class="sxs-lookup"><span data-stu-id="e62e9-116">Parent elements</span></span>

|<span data-ttu-id="e62e9-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="e62e9-117">**Element**</span></span>|<span data-ttu-id="e62e9-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="e62e9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e62e9-119">限制</span><span class="sxs-lookup"><span data-stu-id="e62e9-119">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="e62e9-120">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="e62e9-120">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="e62e9-121">not</span><span class="sxs-lookup"><span data-stu-id="e62e9-121">Not</span></span>](not.md) <br/> |<span data-ttu-id="e62e9-122">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="e62e9-122">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="e62e9-123">And</span><span class="sxs-lookup"><span data-stu-id="e62e9-123">And</span></span>](and.md) <br/> |<span data-ttu-id="e62e9-124">表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="e62e9-124">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="e62e9-125">如果**and**元素中包含的所有搜索表达式为**True**，则**and**操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="e62e9-125">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="e62e9-126">或</span><span class="sxs-lookup"><span data-stu-id="e62e9-126">Or</span></span>](or.md) <br/> |<span data-ttu-id="e62e9-p104">表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  </span><span class="sxs-lookup"><span data-stu-id="e62e9-p104">Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="e62e9-130">说明</span><span class="sxs-lookup"><span data-stu-id="e62e9-130">Remarks</span></span>

<span data-ttu-id="e62e9-131">作为 SearchExpression 替换组的一部分的任何 filter 元素都可以出现在 SearchExpression 元素的位置。</span><span class="sxs-lookup"><span data-stu-id="e62e9-131">Any filter element that is part of the SearchExpression substitution group can appear in place of the SearchExpression element.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e62e9-132">此元素永远不会直接出现在实例文档中。</span><span class="sxs-lookup"><span data-stu-id="e62e9-132">This element will never occur directly within an instance document.</span></span> 
  
<span data-ttu-id="e62e9-133">以下元素是 SearchExpression 替换组的成员：</span><span class="sxs-lookup"><span data-stu-id="e62e9-133">The following elements are members of the SearchExpression substitution group:</span></span>
  
- [<span data-ttu-id="e62e9-134">Exists</span><span class="sxs-lookup"><span data-stu-id="e62e9-134">Exists</span></span>](exists.md)
    
- [<span data-ttu-id="e62e9-135">不包括</span><span class="sxs-lookup"><span data-stu-id="e62e9-135">Excludes</span></span>](excludes.md)
    
- [<span data-ttu-id="e62e9-136">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="e62e9-136">IsEqualTo</span></span>](isequalto.md)
    
- [<span data-ttu-id="e62e9-137">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="e62e9-137">IsNotEqualTo</span></span>](isnotequalto.md)
    
- [<span data-ttu-id="e62e9-138">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="e62e9-138">IsGreaterThan</span></span>](isgreaterthan.md)
    
- [<span data-ttu-id="e62e9-139">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e62e9-139">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)
    
- [<span data-ttu-id="e62e9-140">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="e62e9-140">IsLessThan</span></span>](islessthan.md)
    
- [<span data-ttu-id="e62e9-141">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e62e9-141">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)
    
- [<span data-ttu-id="e62e9-142">Contains</span><span class="sxs-lookup"><span data-stu-id="e62e9-142">Contains</span></span>](contains.md)
    
- [<span data-ttu-id="e62e9-143">Not</span><span class="sxs-lookup"><span data-stu-id="e62e9-143">Not</span></span>](not.md)
    
- [<span data-ttu-id="e62e9-144">And</span><span class="sxs-lookup"><span data-stu-id="e62e9-144">And</span></span>](and.md)
    
- [<span data-ttu-id="e62e9-145">或</span><span class="sxs-lookup"><span data-stu-id="e62e9-145">Or</span></span>](or.md)
    
<span data-ttu-id="e62e9-146">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e62e9-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e62e9-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="e62e9-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e62e9-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="e62e9-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e62e9-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="e62e9-149">Schema Name</span></span>  <br/> |<span data-ttu-id="e62e9-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="e62e9-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="e62e9-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="e62e9-151">Validation File</span></span>  <br/> |<span data-ttu-id="e62e9-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e62e9-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e62e9-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="e62e9-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="e62e9-154">False</span><span class="sxs-lookup"><span data-stu-id="e62e9-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e62e9-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e62e9-155">See also</span></span>



- [<span data-ttu-id="e62e9-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e62e9-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

