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
description: FieldURIOrConstant 元素表示与其他属性进行比较时要使用的属性或常数值。
ms.openlocfilehash: 8b5cb888a3bd2026b15e38fc8c005ab5ef5a2b11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461224"
---
# <a name="fielduriorconstant"></a><span data-ttu-id="58c28-103">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="58c28-103">FieldURIOrConstant</span></span>

<span data-ttu-id="58c28-104">**FieldURIOrConstant**元素表示与其他属性进行比较时要使用的属性或常数值。</span><span class="sxs-lookup"><span data-stu-id="58c28-104">The **FieldURIOrConstant** element represents either a property or a constant value to be used when comparing with another property.</span></span> 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
    <IndexedFieldURI/> 
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <FieldURI/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <ExtendedFieldURI/> 
</FieldURIOrConstant>
```

<span data-ttu-id="58c28-105">**FieldURIOrConstantType**</span><span class="sxs-lookup"><span data-stu-id="58c28-105">**FieldURIOrConstantType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="58c28-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58c28-106">Attributes and elements</span></span>

<span data-ttu-id="58c28-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58c28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58c28-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="58c28-108">Attributes</span></span>

<span data-ttu-id="58c28-109">无。</span><span class="sxs-lookup"><span data-stu-id="58c28-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58c28-110">子元素</span><span class="sxs-lookup"><span data-stu-id="58c28-110">Child elements</span></span>

|<span data-ttu-id="58c28-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="58c28-111">**Element**</span></span>|<span data-ttu-id="58c28-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="58c28-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58c28-113">常量</span><span class="sxs-lookup"><span data-stu-id="58c28-113">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="58c28-114">标识限制中的常量值。</span><span class="sxs-lookup"><span data-stu-id="58c28-114">Identifies a constant value in a restriction.</span></span>  <br/> |
|[<span data-ttu-id="58c28-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="58c28-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="58c28-116">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="58c28-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="58c28-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="58c28-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="58c28-118">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="58c28-118">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="58c28-119">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="58c28-119">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="58c28-120">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="58c28-120">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58c28-121">父元素</span><span class="sxs-lookup"><span data-stu-id="58c28-121">Parent elements</span></span>

|<span data-ttu-id="58c28-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="58c28-122">**Element**</span></span>|<span data-ttu-id="58c28-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="58c28-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58c28-124">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="58c28-124">IsEqualTo</span></span>](isequalto.md) <br/> |<span data-ttu-id="58c28-125">表示搜索表达式，该表达式将属性与常数值或其他属性进行比较，如果它们相等，则计算结果为 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-125">Represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span>  <br/> |
|[<span data-ttu-id="58c28-126">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="58c28-126">IsGreaterThan</span></span>](isgreaterthan.md) <br/> |<span data-ttu-id="58c28-127">表示用于将属性与常数值或其他属性进行比较的搜索表达式，如果第一个属性较大，则返回 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-127">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater.</span></span>  <br/> |
|[<span data-ttu-id="58c28-128">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="58c28-128">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md) <br/> |<span data-ttu-id="58c28-129">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性大于或等于第二个值或属性，则返回 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-129">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is greater than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="58c28-130">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="58c28-130">IsLessThan</span></span>](islessthan.md) <br/> |<span data-ttu-id="58c28-131">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于第二个值或属性，则返回 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-131">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="58c28-132">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="58c28-132">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md) <br/> |<span data-ttu-id="58c28-133">表示一个搜索表达式，该表达式将属性与一个常数值或另一个属性进行比较，如果第一个属性小于或等于第二个值或属性，则返回 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-133">Represents a search expression that compares a property with either a constant value or another property and returns true if the first property is less than or equal to the second value or property.</span></span>  <br/> |
|[<span data-ttu-id="58c28-134">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="58c28-134">IsNotEqualTo</span></span>](isnotequalto.md) <br/> |<span data-ttu-id="58c28-135">表示用于将属性与常量值或其他属性进行比较的搜索表达式，如果值不相同，则返回 true。</span><span class="sxs-lookup"><span data-stu-id="58c28-135">Represents a search expression that compares a property with either a constant value or another property and returns true if the values are not the same.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58c28-136">说明</span><span class="sxs-lookup"><span data-stu-id="58c28-136">Remarks</span></span>

<span data-ttu-id="58c28-137">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58c28-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="58c28-138">示例</span><span class="sxs-lookup"><span data-stu-id="58c28-138">Example</span></span>

<span data-ttu-id="58c28-139">以下 XML 示例显示了与常量和字段 URI 一起使用的 FieldURIOrConstant 元素。</span><span class="sxs-lookup"><span data-stu-id="58c28-139">The following XML example shows the FieldURIOrConstant element used with both a constant and field URI.</span></span>
  
```xml
<Restriction>
  <Or xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="58c28-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="58c28-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58c28-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="58c28-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58c28-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="58c28-142">Schema Name</span></span>  <br/> |<span data-ttu-id="58c28-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="58c28-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="58c28-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="58c28-144">Validation File</span></span>  <br/> |<span data-ttu-id="58c28-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58c28-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58c28-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="58c28-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="58c28-147">False</span><span class="sxs-lookup"><span data-stu-id="58c28-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58c28-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58c28-148">See also</span></span>

- [<span data-ttu-id="58c28-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58c28-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

