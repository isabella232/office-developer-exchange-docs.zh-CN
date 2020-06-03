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
description: Or 元素表示一个搜索表达式，该表达式对它包含的搜索表达式执行逻辑 OR。 如果其任何子级返回 true，则 Or 将返回 true。 Or 必须有两个或多个子级。
ms.openlocfilehash: 9bc676da5bbaad64f11f6717fb487c2e9bcf2d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462477"
---
# <a name="or"></a><span data-ttu-id="5f0bf-105">或</span><span class="sxs-lookup"><span data-stu-id="5f0bf-105">Or</span></span>

<span data-ttu-id="5f0bf-106">**Or**元素表示一个搜索表达式，该表达式对它包含的搜索表达式执行逻辑**Or** 。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-106">The **Or** element represents a search expression that performs a logical **OR** on the search expression that it contains.</span></span> <span data-ttu-id="5f0bf-107">如果其任何子级返回 **true**，则 **Or** 将返回 **true**。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-107">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="5f0bf-108">**Or** 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-108">**Or** must have two or more children.</span></span> 
  
```xml
<Or>
   <SearchExpression/>
   <SearchExpression/>
</Or>
```

 <span data-ttu-id="5f0bf-109">**或类型**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-109">**OrType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f0bf-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5f0bf-110">Attributes and elements</span></span>

<span data-ttu-id="5f0bf-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f0bf-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="5f0bf-112">Attributes</span></span>

<span data-ttu-id="5f0bf-113">无。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f0bf-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5f0bf-114">Child elements</span></span>

|<span data-ttu-id="5f0bf-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-115">**Element**</span></span>|<span data-ttu-id="5f0bf-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f0bf-117">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="5f0bf-117">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="5f0bf-118">表示某个限制范围内表达式的基类。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-118">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="5f0bf-119">必须将以下元素之一替换为 **SearchExpression** 元素：</span><span class="sxs-lookup"><span data-stu-id="5f0bf-119">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="5f0bf-120">- [存在](exists.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-120">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="5f0bf-121">- [除外](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-121">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="5f0bf-122">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-122">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="5f0bf-123">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-123">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="5f0bf-124">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-124">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="5f0bf-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-125">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="5f0bf-126">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-126">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="5f0bf-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-127">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="5f0bf-128">- [包含](contains.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-128">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="5f0bf-129">- [不要](not.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-129">- [Not](not.md)</span></span> <br/><span data-ttu-id="5f0bf-130">- [并](and.md)</span><span class="sxs-lookup"><span data-stu-id="5f0bf-130">- [And](and.md)</span></span> <br/><span data-ttu-id="5f0bf-131">- **和**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-131">- **Or**</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f0bf-132">父元素</span><span class="sxs-lookup"><span data-stu-id="5f0bf-132">Parent elements</span></span>

|<span data-ttu-id="5f0bf-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-133">**Element**</span></span>|<span data-ttu-id="5f0bf-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f0bf-135">限制</span><span class="sxs-lookup"><span data-stu-id="5f0bf-135">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="5f0bf-136">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-136">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="5f0bf-137">not</span><span class="sxs-lookup"><span data-stu-id="5f0bf-137">Not</span></span>](not.md) <br/> |<span data-ttu-id="5f0bf-138">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-138">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="5f0bf-139">And</span><span class="sxs-lookup"><span data-stu-id="5f0bf-139">And</span></span>](and.md) <br/> |<span data-ttu-id="5f0bf-140">表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-140">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="5f0bf-141">如果**and**元素中包含的所有搜索表达式为**True**，则**and**操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-141">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|<span data-ttu-id="5f0bf-142">**或**</span><span class="sxs-lookup"><span data-stu-id="5f0bf-142">**Or**</span></span> <br/> |<span data-ttu-id="5f0bf-p104">表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  </span><span class="sxs-lookup"><span data-stu-id="5f0bf-p104">Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f0bf-146">说明</span><span class="sxs-lookup"><span data-stu-id="5f0bf-146">Remarks</span></span>

<span data-ttu-id="5f0bf-147">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5f0bf-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f0bf-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="5f0bf-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f0bf-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="5f0bf-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f0bf-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="5f0bf-150">Schema Name</span></span>  <br/> |<span data-ttu-id="5f0bf-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="5f0bf-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f0bf-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="5f0bf-152">Validation File</span></span>  <br/> |<span data-ttu-id="5f0bf-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f0bf-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f0bf-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="5f0bf-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f0bf-155">False</span><span class="sxs-lookup"><span data-stu-id="5f0bf-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f0bf-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f0bf-156">See also</span></span>

- [<span data-ttu-id="5f0bf-157">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f0bf-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

