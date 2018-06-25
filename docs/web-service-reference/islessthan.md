---
title: IsLessThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsLessThan
api_type:
- schema
ms.assetid: 2550469b-6e5d-45a5-9ecc-090d1b409296
description: IsLessThan 元素均表示一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为小于时为 true 的第二个。
ms.openlocfilehash: 374bfc20b86f99923034f126c3fd1fe9480fdf67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826040"
---
# <a name="islessthan"></a><span data-ttu-id="fad02-103">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="fad02-103">IsLessThan</span></span>

<span data-ttu-id="fad02-104">**IsLessThan**元素均表示一个搜索表达式的比较一个常数值的属性或另一个属性，并返回**true** ，如果第一个属性小于第二个。</span><span class="sxs-lookup"><span data-stu-id="fad02-104">The **IsLessThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than the second.</span></span> 
  
```xml
<IsLessThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsLessThan>
```

 <span data-ttu-id="fad02-105">**IsLessThanType**</span><span class="sxs-lookup"><span data-stu-id="fad02-105">**IsLessThanType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fad02-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fad02-106">Attributes and elements</span></span>

<span data-ttu-id="fad02-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fad02-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fad02-108">属性</span><span class="sxs-lookup"><span data-stu-id="fad02-108">Attributes</span></span>

<span data-ttu-id="fad02-109">无。</span><span class="sxs-lookup"><span data-stu-id="fad02-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fad02-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fad02-110">Child elements</span></span>

|<span data-ttu-id="fad02-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fad02-111">**Element**</span></span>|<span data-ttu-id="fad02-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fad02-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fad02-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="fad02-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="fad02-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="fad02-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="fad02-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="fad02-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="fad02-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="fad02-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="fad02-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="fad02-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="fad02-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="fad02-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="fad02-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="fad02-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="fad02-120">代表属性或以常量值，用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="fad02-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fad02-121">父元素</span><span class="sxs-lookup"><span data-stu-id="fad02-121">Parent elements</span></span>

|<span data-ttu-id="fad02-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="fad02-122">**Element**</span></span>|<span data-ttu-id="fad02-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="fad02-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fad02-124">限制</span><span class="sxs-lookup"><span data-stu-id="fad02-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="fad02-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="fad02-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="fad02-126">not</span><span class="sxs-lookup"><span data-stu-id="fad02-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="fad02-127">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="fad02-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="fad02-128">And</span><span class="sxs-lookup"><span data-stu-id="fad02-128">And</span></span>](and.md) <br/> |<span data-ttu-id="fad02-129">表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="fad02-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="fad02-130">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="fad02-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="fad02-131">或</span><span class="sxs-lookup"><span data-stu-id="fad02-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="fad02-132">表示对它所包含的搜索表达式执行逻辑或搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="fad02-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="fad02-133">[或](or.md)将返回 true 如果任何其子返回 true。</span><span class="sxs-lookup"><span data-stu-id="fad02-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="fad02-134">[Or](or.md) 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="fad02-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fad02-135">备注</span><span class="sxs-lookup"><span data-stu-id="fad02-135">Remarks</span></span>

<span data-ttu-id="fad02-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fad02-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fad02-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="fad02-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fad02-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="fad02-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fad02-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="fad02-139">Schema Name</span></span>  <br/> |<span data-ttu-id="fad02-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="fad02-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="fad02-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="fad02-141">Validation File</span></span>  <br/> |<span data-ttu-id="fad02-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fad02-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fad02-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="fad02-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="fad02-144">False</span><span class="sxs-lookup"><span data-stu-id="fad02-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fad02-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fad02-145">See also</span></span>



- [<span data-ttu-id="fad02-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fad02-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

