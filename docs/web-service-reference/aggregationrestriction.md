---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: AggregationRestriction 元素指定应用于由 FindPeople 请求生成的一组角色属性的值，并根据指定的限制筛选结果。
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463522"
---
# <a name="aggregationrestriction"></a><span data-ttu-id="34d7e-103">AggregationRestriction</span><span class="sxs-lookup"><span data-stu-id="34d7e-103">AggregationRestriction</span></span>

<span data-ttu-id="34d7e-104">**AggregationRestriction**元素指定应用于由 FindPeople 请求生成的一组角色属性的值，并根据指定的限制筛选结果。</span><span class="sxs-lookup"><span data-stu-id="34d7e-104">The **AggregationRestriction** element specifies a value that is applied to a set of Persona properties resulting from a FindPeople request and filters the result according to the specified restriction.</span></span> 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 <span data-ttu-id="34d7e-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="34d7e-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34d7e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34d7e-106">Attributes and elements</span></span>

<span data-ttu-id="34d7e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34d7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34d7e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="34d7e-108">Attributes</span></span>

<span data-ttu-id="34d7e-109">无。</span><span class="sxs-lookup"><span data-stu-id="34d7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34d7e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="34d7e-110">Child elements</span></span>

[<span data-ttu-id="34d7e-111">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="34d7e-111">SearchExpression</span></span>](searchexpression.md)
  
### <a name="parent-elements"></a><span data-ttu-id="34d7e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="34d7e-112">Parent elements</span></span>

[<span data-ttu-id="34d7e-113">FindPeople</span><span class="sxs-lookup"><span data-stu-id="34d7e-113">FindPeople</span></span>](findpeople.md)
  
## <a name="remarks"></a><span data-ttu-id="34d7e-114">备注</span><span class="sxs-lookup"><span data-stu-id="34d7e-114">Remarks</span></span>

<span data-ttu-id="34d7e-115">**AggregationRestriction**元素可以包含使用**SearchExpression**替换组的任何子元素。</span><span class="sxs-lookup"><span data-stu-id="34d7e-115">The **AggregationRestriction** element can contain any child element that uses the **SearchExpression** substitution group.</span></span> <span data-ttu-id="34d7e-116">作为**SearchExpression**替换组的一部分的元素为： [Contains](contains.md)、不[包括](excludes.md)、 [Exists](exists.md)、 [Not](not.md)、 [Or](or.md)、 [And](and.md)、 [IsEqualTo](isequalto.md)、 [IsNotEqualTo](isnotequalto.md)、 [IsGreaterThan](isgreaterthan.md)、 [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)、 [IsLessThan](islessthan.md)和[IsLessThanOrEqualTo](islessthanorequalto.md)。</span><span class="sxs-lookup"><span data-stu-id="34d7e-116">The elements that are a part of the **SearchExpression** substitution group are: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md), and [IsLessThanOrEqualTo](islessthanorequalto.md).</span></span>
  
<span data-ttu-id="34d7e-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="34d7e-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="34d7e-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="34d7e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34d7e-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="34d7e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34d7e-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="34d7e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="34d7e-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="34d7e-121">Schema name</span></span>  <br/> |<span data-ttu-id="34d7e-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="34d7e-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="34d7e-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="34d7e-123">Validation file</span></span>  <br/> |<span data-ttu-id="34d7e-124">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="34d7e-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="34d7e-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="34d7e-125">Can be empty</span></span>  <br/> |<span data-ttu-id="34d7e-126">false</span><span class="sxs-lookup"><span data-stu-id="34d7e-126">false</span></span>  <br/> |
   

