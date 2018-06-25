---
title: FieldURIOrConstant
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: FieldURIOrConstant 元素表示的属性或常量值用于比较与另一个属性。
ms.openlocfilehash: 5195feec2a314d9ec15dc4a25a7a014aded1696a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754303"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="e9041-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="e9041-103">FieldURIOrConstant</span></span>

<span data-ttu-id="e9041-104">**FieldURIOrConstant**元素表示的属性或常量值用于比较与另一个属性。</span><span class="sxs-lookup"><span data-stu-id="e9041-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

 <span data-ttu-id="e9041-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="e9041-105">**FieldURIOrConstantType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9041-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e9041-106">Attributes and elements</span></span>

<span data-ttu-id="e9041-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9041-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9041-108">属性</span><span class="sxs-lookup"><span data-stu-id="e9041-108">Attributes</span></span>

<span data-ttu-id="e9041-109">无。</span><span class="sxs-lookup"><span data-stu-id="e9041-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9041-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e9041-110">Child elements</span></span>

|<span data-ttu-id="e9041-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9041-111">**Element**</span></span>|<span data-ttu-id="e9041-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9041-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9041-113">常量</span><span class="sxs-lookup"><span data-stu-id="e9041-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="e9041-114">标识限制中的以常量值。</span><span class="sxs-lookup"><span data-stu-id="e9041-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="e9041-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="e9041-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="e9041-116">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="e9041-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="e9041-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e9041-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="e9041-118">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="e9041-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="e9041-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="e9041-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="e9041-120">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="e9041-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9041-121">父元素</span><span class="sxs-lookup"><span data-stu-id="e9041-121">Parent elements</span></span>

|<span data-ttu-id="e9041-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9041-122">**Element**</span></span>|<span data-ttu-id="e9041-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9041-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9041-124">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="e9041-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="e9041-125">代表一个搜索表达式的比较一个常数值的属性或另一个属性，并计算结果为 true，如果二者相等。</span><span class="sxs-lookup"><span data-stu-id="e9041-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="e9041-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="e9041-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="e9041-127">代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为更高版本时为 true。</span><span class="sxs-lookup"><span data-stu-id="e9041-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="e9041-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e9041-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="e9041-129">代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为大于或等于第二个值或属性时为 true。</span><span class="sxs-lookup"><span data-stu-id="e9041-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e9041-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="e9041-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="e9041-131">代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为小于第二个值或属性时为 true。</span><span class="sxs-lookup"><span data-stu-id="e9041-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e9041-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="e9041-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="e9041-133">代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为小于或等于第二个值或属性时为 true。</span><span class="sxs-lookup"><span data-stu-id="e9041-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="e9041-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="e9041-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="e9041-135">代表一个搜索表达式的比较一个常数值的属性或另一个属性，并返回 true 如果值不相同。</span><span class="sxs-lookup"><span data-stu-id="e9041-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9041-136">备注</span><span class="sxs-lookup"><span data-stu-id="e9041-136">Remarks</span></span>

<span data-ttu-id="e9041-137">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e9041-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="e9041-138">示例</span><span class="sxs-lookup"><span data-stu-id="e9041-138">Example</span></span>

<span data-ttu-id="e9041-139">下面的 XML 示例演示用于常量和字段 URI FieldURIOrConstant 元素。</span><span class="sxs-lookup"><span data-stu-id="e9041-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```
[xml]
<Restriction>
  <Or xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## <a name="element-information"></a><span data-ttu-id="e9041-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="e9041-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9041-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="e9041-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9041-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="e9041-142">Schema Name</span></span>  <br/> |<span data-ttu-id="e9041-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="e9041-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9041-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="e9041-144">Validation File</span></span>  <br/> |<span data-ttu-id="e9041-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9041-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9041-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="e9041-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9041-147">False</span><span class="sxs-lookup"><span data-stu-id="e9041-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9041-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9041-148">See also</span></span>



- [<span data-ttu-id="e9041-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e9041-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

