---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: AggregationRestriction 元素指定的一组由 FindPeople 请求产生的个人属性应用于和筛选结果，根据指定限制的值。
ms.openlocfilehash: 8b4d5952dedb4de0201d2ecf2219c69f65f7dc09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753135"
---
# <a name="aggregationrestriction"></a><span data-ttu-id="1e6dc-103">AggregationRestriction</span><span class="sxs-lookup"><span data-stu-id="1e6dc-103">AggregationRestriction</span></span>

<span data-ttu-id="1e6dc-104">**AggregationRestriction**元素指定的一组由 FindPeople 请求产生的个人属性应用于和筛选结果，根据指定限制的值。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-104">The **AggregationRestriction** element specifies a value that is applied to a set of Persona properties resulting from a FindPeople request and filters the result according to the specified restriction.</span></span> 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 <span data-ttu-id="1e6dc-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="1e6dc-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e6dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e6dc-106">Attributes and elements</span></span>

<span data-ttu-id="1e6dc-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e6dc-108">属性</span><span class="sxs-lookup"><span data-stu-id="1e6dc-108">Attributes</span></span>

<span data-ttu-id="1e6dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e6dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e6dc-110">Child elements</span></span>

[<span data-ttu-id="1e6dc-111">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="1e6dc-111">SearchExpression</span></span>](searchexpression.md)
  
### <a name="parent-elements"></a><span data-ttu-id="1e6dc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1e6dc-112">Parent elements</span></span>

[<span data-ttu-id="1e6dc-113">FindPeople</span><span class="sxs-lookup"><span data-stu-id="1e6dc-113">FindPeople</span></span>](findpeople.md)
  
## <a name="remarks"></a><span data-ttu-id="1e6dc-114">注解</span><span class="sxs-lookup"><span data-stu-id="1e6dc-114">Remarks</span></span>

<span data-ttu-id="1e6dc-115">**AggregationRestriction**元素可以包含使用**SearchExpression**替换组任何子元素。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-115">The **AggregationRestriction** element can contain any child element that uses the **SearchExpression** substitution group.</span></span> <span data-ttu-id="1e6dc-116">属于**SearchExpression**替换组元素：[包含](contains.md)[排除](excludes.md)、 [Exists](exists.md)、[不](not.md)、[或](or.md)、[和](and.md)、 [IsEqualTo](isequalto.md)、 [IsNotEqualTo](isnotequalto.md)， [IsGreaterThan](isgreaterthan.md)， [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)、 [IsLessThan](islessthan.md)和[IsLessThanOrEqualTo](islessthanorequalto.md)。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-116">The elements that are a part of the **SearchExpression** substitution group are: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md), and [IsLessThanOrEqualTo](islessthanorequalto.md).</span></span>
  
<span data-ttu-id="1e6dc-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1e6dc-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e6dc-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e6dc-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e6dc-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e6dc-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e6dc-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1e6dc-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e6dc-121">Schema name</span></span>  <br/> |<span data-ttu-id="1e6dc-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="1e6dc-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1e6dc-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e6dc-123">Validation file</span></span>  <br/> |<span data-ttu-id="1e6dc-124">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1e6dc-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1e6dc-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e6dc-125">Can be empty</span></span>  <br/> |<span data-ttu-id="1e6dc-126">false</span><span class="sxs-lookup"><span data-stu-id="1e6dc-126">false</span></span>  <br/> |
   

