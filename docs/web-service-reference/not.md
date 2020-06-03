---
title: 不
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Not
api_type:
- schema
ms.assetid: 1aa16318-7e90-4b19-bce8-dd1a20a66223
description: Not 元素表示对其包含的搜索表达式的布尔值求反的搜索表达式。
ms.openlocfilehash: 84c64a6d9d39f260d416fc32e4e5f5fcdef027e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466715"
---
# <a name="not"></a><span data-ttu-id="cb9ae-103">不</span><span class="sxs-lookup"><span data-stu-id="cb9ae-103">Not</span></span>

<span data-ttu-id="cb9ae-104">**Not**元素表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-104">The **Not** element represents a search expression that negates the Boolean value of the search expression that it contains.</span></span> 
  
```xml
<Not>
   <SearchExpression/>
</Not>
```

 <span data-ttu-id="cb9ae-105">**NotType**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-105">**NotType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb9ae-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb9ae-106">Attributes and elements</span></span>

<span data-ttu-id="cb9ae-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb9ae-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cb9ae-108">Attributes</span></span>

<span data-ttu-id="cb9ae-109">无。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb9ae-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cb9ae-110">Child elements</span></span>

|<span data-ttu-id="cb9ae-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-111">**Element**</span></span>|<span data-ttu-id="cb9ae-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb9ae-113">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="cb9ae-113">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="cb9ae-114">表示某个限制范围内表达式的基类。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-114">Represents the base class for expressions within a restriction.</span></span> <br/><br/><span data-ttu-id="cb9ae-115">必须将以下元素之一替换为 **SearchExpression** 元素：</span><span class="sxs-lookup"><span data-stu-id="cb9ae-115">One of the following elements must be substituted for the **SearchExpression** element:</span></span> <br/> <br/><span data-ttu-id="cb9ae-116">- [存在](exists.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-116">- [Exists](exists.md)</span></span> <br/><span data-ttu-id="cb9ae-117">- [除外](excludes.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-117">- [Excludes](excludes.md)</span></span> <br/><span data-ttu-id="cb9ae-118">- [IsEqualTo](isequalto.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-118">- [IsEqualTo](isequalto.md)</span></span> <br/><span data-ttu-id="cb9ae-119">- [IsNotEqualTo](isnotequalto.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-119">- [IsNotEqualTo](isnotequalto.md)</span></span> <br/><span data-ttu-id="cb9ae-120">- [IsGreaterThan](isgreaterthan.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-120">- [IsGreaterThan](isgreaterthan.md)</span></span> <br/><span data-ttu-id="cb9ae-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-121">- [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)</span></span> <br/><span data-ttu-id="cb9ae-122">- [IsLessThan](islessthan.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-122">- [IsLessThan](islessthan.md)</span></span> <br/><span data-ttu-id="cb9ae-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-123">- [IsLessThanOrEqualTo](islessthanorequalto.md)</span></span> <br/><span data-ttu-id="cb9ae-124">- [包含](contains.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-124">- [Contains](contains.md)</span></span> <br/><span data-ttu-id="cb9ae-125">- **不要**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-125">- **Not**</span></span> <br/><span data-ttu-id="cb9ae-126">- [并](and.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-126">- [And](and.md)</span></span> <br/><span data-ttu-id="cb9ae-127">- [和](or.md)</span><span class="sxs-lookup"><span data-stu-id="cb9ae-127">- [Or](or.md)</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb9ae-128">父元素</span><span class="sxs-lookup"><span data-stu-id="cb9ae-128">Parent elements</span></span>

|<span data-ttu-id="cb9ae-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-129">**Element**</span></span>|<span data-ttu-id="cb9ae-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb9ae-131">限制</span><span class="sxs-lookup"><span data-stu-id="cb9ae-131">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="cb9ae-132">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-132">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|<span data-ttu-id="cb9ae-133">**not**</span><span class="sxs-lookup"><span data-stu-id="cb9ae-133">**Not**</span></span> <br/> |<span data-ttu-id="cb9ae-134">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-134">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="cb9ae-135">And</span><span class="sxs-lookup"><span data-stu-id="cb9ae-135">And</span></span>](and.md) <br/> |<span data-ttu-id="cb9ae-136">表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-136">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="cb9ae-137">如果**and**元素中包含的所有搜索表达式为**True**，则**and**操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-137">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="cb9ae-138">或</span><span class="sxs-lookup"><span data-stu-id="cb9ae-138">Or</span></span>](or.md) <br/> |<span data-ttu-id="cb9ae-p102">表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  </span><span class="sxs-lookup"><span data-stu-id="cb9ae-p102">Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb9ae-142">说明</span><span class="sxs-lookup"><span data-stu-id="cb9ae-142">Remarks</span></span>

<span data-ttu-id="cb9ae-143">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cb9ae-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb9ae-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb9ae-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb9ae-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb9ae-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb9ae-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb9ae-146">Schema Name</span></span>  <br/> |<span data-ttu-id="cb9ae-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="cb9ae-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb9ae-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb9ae-148">Validation File</span></span>  <br/> |<span data-ttu-id="cb9ae-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb9ae-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb9ae-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb9ae-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb9ae-151">False</span><span class="sxs-lookup"><span data-stu-id="cb9ae-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb9ae-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb9ae-152">See also</span></span>

- [<span data-ttu-id="cb9ae-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb9ae-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

