---
title: IsLessThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsLessThanOrEqualTo
api_type:
- schema
ms.assetid: b5d85eb2-5e15-4d01-ad49-6289e735ad8a
description: IsLessThanOrEqualTo 元素表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于或等于第二个属性，则返回 true。
ms.openlocfilehash: 7b153803b1c895c86e74428468c8e592c02a0acc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530027"
---
# <a name="islessthanorequalto"></a><span data-ttu-id="03b34-103">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="03b34-103">IsLessThanOrEqualTo</span></span>

<span data-ttu-id="03b34-104">**IsLessThanOrEqualTo**元素表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于或等于第二个属性，则返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="03b34-104">The **IsLessThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the second.</span></span> 
  
```xml
<IsLessThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

```xml
<IsLessThanOrEqualTo>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

```xml
<IsLessThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

<span data-ttu-id="03b34-105">**IsLessThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="03b34-105">**IsLessThanOrEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="03b34-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="03b34-106">Attributes and elements</span></span>

<span data-ttu-id="03b34-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="03b34-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03b34-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="03b34-108">Attributes</span></span>

<span data-ttu-id="03b34-109">无。</span><span class="sxs-lookup"><span data-stu-id="03b34-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="03b34-110">子元素</span><span class="sxs-lookup"><span data-stu-id="03b34-110">Child elements</span></span>

|<span data-ttu-id="03b34-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="03b34-111">**Element**</span></span>|<span data-ttu-id="03b34-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="03b34-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03b34-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="03b34-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="03b34-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="03b34-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="03b34-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="03b34-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="03b34-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="03b34-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="03b34-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="03b34-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="03b34-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="03b34-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="03b34-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="03b34-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="03b34-120">表示与其他属性进行比较时要使用的属性或常数值。</span><span class="sxs-lookup"><span data-stu-id="03b34-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="03b34-121">父元素</span><span class="sxs-lookup"><span data-stu-id="03b34-121">Parent elements</span></span>

|<span data-ttu-id="03b34-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="03b34-122">**Element**</span></span>|<span data-ttu-id="03b34-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="03b34-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="03b34-124">限制</span><span class="sxs-lookup"><span data-stu-id="03b34-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="03b34-125">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="03b34-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="03b34-126">not</span><span class="sxs-lookup"><span data-stu-id="03b34-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="03b34-127">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="03b34-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="03b34-128">And</span><span class="sxs-lookup"><span data-stu-id="03b34-128">And</span></span>](and.md) <br/> |<span data-ttu-id="03b34-129">表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="03b34-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="03b34-130">如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="03b34-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="03b34-131">或</span><span class="sxs-lookup"><span data-stu-id="03b34-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="03b34-132">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="03b34-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="03b34-133">[或者](or.md)，如果其任何子级返回 true，则返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="03b34-133">[Or](or.md) will return **true** if any of its children return true.</span></span> <span data-ttu-id="03b34-134">[Or](or.md) 必须有两个或多个子级。</span><span class="sxs-lookup"><span data-stu-id="03b34-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03b34-135">说明</span><span class="sxs-lookup"><span data-stu-id="03b34-135">Remarks</span></span>

<span data-ttu-id="03b34-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="03b34-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03b34-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="03b34-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03b34-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="03b34-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="03b34-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="03b34-139">Schema Name</span></span>  <br/> |<span data-ttu-id="03b34-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="03b34-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="03b34-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="03b34-141">Validation File</span></span>  <br/> |<span data-ttu-id="03b34-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="03b34-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="03b34-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="03b34-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="03b34-144">False</span><span class="sxs-lookup"><span data-stu-id="03b34-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="03b34-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="03b34-145">See also</span></span>

- [<span data-ttu-id="03b34-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="03b34-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

