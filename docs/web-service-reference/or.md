---
title: 或
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Or
api_type:
- schema
ms.assetid: 4876d83a-73a3-4953-9d95-3048e6b76ccb
description: Or 元素均表示一个搜索表达式，对它所包含的搜索表达式执行逻辑或。 或者，将返回 true 如果任何其子返回 true。 或必须有两个或多个子。
ms.openlocfilehash: 46cf031047aeb09e05a385150ab7587968aef345
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826661"
---
# <a name="or"></a><span data-ttu-id="9c660-105">或</span><span class="sxs-lookup"><span data-stu-id="9c660-105">Or</span></span>

<span data-ttu-id="9c660-106">**或**元素表示对它所包含的搜索表达式执行逻辑**或**搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9c660-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="9c660-107">如果其任何子级返回 **true**，则 **Or** 将返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="9c660-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="9c660-108">**Or** 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="9c660-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="9c660-109">**OrType**</span><span class="sxs-lookup"><span data-stu-id="9c660-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c660-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c660-110">Attributes and elements</span></span>

<span data-ttu-id="9c660-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c660-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c660-112">属性</span><span class="sxs-lookup"><span data-stu-id="9c660-112">Attributes</span></span>

<span data-ttu-id="9c660-113">无。</span><span class="sxs-lookup"><span data-stu-id="9c660-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c660-114">子元素</span><span class="sxs-lookup"><span data-stu-id="9c660-114">Child elements</span></span>

|<span data-ttu-id="9c660-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c660-115">**Element**</span></span>|<span data-ttu-id="9c660-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c660-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c660-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="9c660-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="9c660-118">表示某个限制范围内表达式的基类。</span><span class="sxs-lookup"><span data-stu-id="9c660-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="9c660-119">必须将以下元素之一替换为 **SearchExpression** 元素：</span><span class="sxs-lookup"><span data-stu-id="9c660-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="9c660-120">- [存在](exists.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="9c660-121">- [排除](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="9c660-122">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="9c660-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="9c660-124">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="9c660-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="9c660-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="9c660-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="9c660-128">- [包含](contains.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="9c660-129">- [不](not.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="9c660-130">- [和](and.md)</span><span class="sxs-lookup"><span data-stu-id="9c660-130">- [And](and.md)</span></span> <br/><span data-ttu-id="9c660-131">- **或**</span><span class="sxs-lookup"><span data-stu-id="9c660-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c660-132">父元素</span><span class="sxs-lookup"><span data-stu-id="9c660-132">Parent elements</span></span>

|<span data-ttu-id="9c660-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c660-133">**Element**</span></span>|<span data-ttu-id="9c660-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c660-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c660-135">限制</span><span class="sxs-lookup"><span data-stu-id="9c660-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9c660-136">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="9c660-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9c660-137">not</span><span class="sxs-lookup"><span data-stu-id="9c660-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="9c660-138">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9c660-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="9c660-139">And</span><span class="sxs-lookup"><span data-stu-id="9c660-139">And</span></span>](and.md) <br/> |<span data-ttu-id="9c660-140">表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="9c660-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="9c660-141">如果**和**元素中包含的所有搜索表达式都都为**true**，则**和**操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="9c660-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="9c660-142">**或**</span><span class="sxs-lookup"><span data-stu-id="9c660-142">**Or**</span></span> <br/> |<span data-ttu-id="9c660-p104">表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  </span><span class="sxs-lookup"><span data-stu-id="9c660-p104">Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c660-146">备注</span><span class="sxs-lookup"><span data-stu-id="9c660-146">Remarks</span></span>

<span data-ttu-id="9c660-147">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c660-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c660-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c660-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c660-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c660-149">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c660-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c660-150">Schema Name</span></span>  <br/> |<span data-ttu-id="9c660-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="9c660-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c660-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c660-152">Validation File</span></span>  <br/> |<span data-ttu-id="9c660-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c660-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c660-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c660-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c660-155">False</span><span class="sxs-lookup"><span data-stu-id="9c660-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c660-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c660-156">See also</span></span>

- [<span data-ttu-id="9c660-157">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9c660-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

