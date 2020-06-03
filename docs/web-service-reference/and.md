---
title: And
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: And 元素表示允许您在两个或多个搜索表达式之间执行布尔 AND 操作的搜索表达式。如果 And 元素中包含的所有搜索表达式为 true，则 AND 操作的结果为 true。
ms.openlocfilehash: f5239f19c2b5a931eefa9ff4a9dd8ed9d775bae2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464719"
---
# <a name="and"></a><span data-ttu-id="c6225-104">和</span><span class="sxs-lookup"><span data-stu-id="c6225-104">And</span></span>

<span data-ttu-id="c6225-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **And** 元素表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。如果 **And** 元素中包含的所有搜索表达式为 **true**，则 **AND** 操作的结果为 **true**。</span><span class="sxs-lookup"><span data-stu-id="c6225-p102">The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions. The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 <span data-ttu-id="c6225-107">**AndType**</span><span class="sxs-lookup"><span data-stu-id="c6225-107">**AndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6225-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6225-108">Attributes and elements</span></span>

<span data-ttu-id="c6225-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6225-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6225-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6225-110">Attributes</span></span>

<span data-ttu-id="c6225-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6225-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6225-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c6225-112">Child elements</span></span>

|<span data-ttu-id="c6225-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6225-113">**Element**</span></span>|<span data-ttu-id="c6225-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6225-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6225-115">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="c6225-115">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="c6225-p103">表示某个限制范围内表达式的基类。And 操作中必须有两个或多个搜索表达式。  </span><span class="sxs-lookup"><span data-stu-id="c6225-p103">Represents the base class for expressions within a restriction. There must be two or more search expressions in an And operation.</span></span><br/><br/>  <span data-ttu-id="c6225-118">必须将以下元素之一替换为 **SearchExpression** 元素：</span><span class="sxs-lookup"><span data-stu-id="c6225-118">One of the following elements must be substituted for the **SearchExpression** element:</span></span><ul><li> [<span data-ttu-id="c6225-119">Exists</span><span class="sxs-lookup"><span data-stu-id="c6225-119">Exists</span></span>](exists.md)</li><li>[<span data-ttu-id="c6225-120">不包括</span><span class="sxs-lookup"><span data-stu-id="c6225-120">Excludes</span></span>](excludes.md)</li><li>[<span data-ttu-id="c6225-121">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="c6225-121">IsEqualTo</span></span>](isequalto.md)</li><li>[<span data-ttu-id="c6225-122">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="c6225-122">IsNotEqualTo</span></span>](isnotequalto.md)</li><li>[<span data-ttu-id="c6225-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="c6225-123">IsGreaterThan</span></span>](isgreaterthan.md)</li><li>[<span data-ttu-id="c6225-124">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="c6225-124">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)</li><li>[<span data-ttu-id="c6225-125">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="c6225-125">IsLessThan</span></span>](islessthan.md)</li><li>[<span data-ttu-id="c6225-126">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="c6225-126">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)</li><li>[<span data-ttu-id="c6225-127">Contains</span><span class="sxs-lookup"><span data-stu-id="c6225-127">Contains</span></span>](contains.md)</li><li>[<span data-ttu-id="c6225-128">Not</span><span class="sxs-lookup"><span data-stu-id="c6225-128">Not</span></span>](not.md)</li><li><span data-ttu-id="c6225-129">**And**</span><span class="sxs-lookup"><span data-stu-id="c6225-129">**And**</span></span></li><li>[<span data-ttu-id="c6225-130">或</span><span class="sxs-lookup"><span data-stu-id="c6225-130">Or</span></span>](or.md) </li></ul> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6225-131">父元素</span><span class="sxs-lookup"><span data-stu-id="c6225-131">Parent elements</span></span>

|<span data-ttu-id="c6225-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6225-132">**Element**</span></span>|<span data-ttu-id="c6225-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6225-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6225-134">限制</span><span class="sxs-lookup"><span data-stu-id="c6225-134">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="c6225-135">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="c6225-135">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="c6225-136">not</span><span class="sxs-lookup"><span data-stu-id="c6225-136">Not</span></span>](not.md) <br/> |<span data-ttu-id="c6225-137">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="c6225-137">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|<span data-ttu-id="c6225-138">**And**</span><span class="sxs-lookup"><span data-stu-id="c6225-138">**And**</span></span> <br/> |<span data-ttu-id="c6225-p104">表示允许您在两个或多个搜索表达式之间执行布尔 **AND** 操作的搜索表达式。如果 **And** 元素中包含的所有搜索表达式为 **true**，则 **AND** 操作的结果为 **true**。  </span><span class="sxs-lookup"><span data-stu-id="c6225-p104">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions. The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.  </span></span><br/> |
|[<span data-ttu-id="c6225-141">或</span><span class="sxs-lookup"><span data-stu-id="c6225-141">Or</span></span>](or.md) <br/> |<span data-ttu-id="c6225-p105">表示在其包含的搜索表达式上执行逻辑 **OR** 操作的搜索表达式。如果其任何子级返回 **true**，则 **Or** 将返回 **true**。 **Or** 必须有两个或多个子级。  </span><span class="sxs-lookup"><span data-stu-id="c6225-p105">Represents a search expression that performs a logical **OR** operation on the search expression that it contains. **Or** will return **true** if any of its children return **true**. **Or** must have two or more children.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6225-145">说明</span><span class="sxs-lookup"><span data-stu-id="c6225-145">Remarks</span></span>

<span data-ttu-id="c6225-146">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6225-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6225-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6225-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6225-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6225-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6225-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6225-149">Schema Name</span></span>  <br/> |<span data-ttu-id="c6225-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="c6225-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6225-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6225-151">Validation File</span></span>  <br/> |<span data-ttu-id="c6225-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c6225-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6225-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6225-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6225-154">False</span><span class="sxs-lookup"><span data-stu-id="c6225-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6225-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6225-155">See also</span></span>

- [<span data-ttu-id="c6225-156">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6225-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

