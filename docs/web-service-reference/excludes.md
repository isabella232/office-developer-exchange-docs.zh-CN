---
title: 不包括
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: 排除元素执行指定属性的按位掩码和提供的值。
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530612"
---
# <a name="excludes"></a><span data-ttu-id="14c92-103">不包括</span><span class="sxs-lookup"><span data-stu-id="14c92-103">Excludes</span></span>

<span data-ttu-id="14c92-104">**排除**元素执行指定属性的按位掩码和提供的值。</span><span class="sxs-lookup"><span data-stu-id="14c92-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

<span data-ttu-id="14c92-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="14c92-105">**ExcludesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="14c92-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14c92-106">Attributes and elements</span></span>

<span data-ttu-id="14c92-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14c92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14c92-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="14c92-108">Attributes</span></span>

<span data-ttu-id="14c92-109">无。</span><span class="sxs-lookup"><span data-stu-id="14c92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14c92-110">子元素</span><span class="sxs-lookup"><span data-stu-id="14c92-110">Child elements</span></span>

|<span data-ttu-id="14c92-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="14c92-111">**Element**</span></span>|<span data-ttu-id="14c92-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="14c92-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14c92-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="14c92-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="14c92-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="14c92-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="14c92-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="14c92-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="14c92-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="14c92-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="14c92-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="14c92-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="14c92-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="14c92-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="14c92-119">位掩码</span><span class="sxs-lookup"><span data-stu-id="14c92-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="14c92-120">表示在不[包括](excludes.md)的限制操作期间要使用的十六进制或小数掩码。</span><span class="sxs-lookup"><span data-stu-id="14c92-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="14c92-121">如果位掩码代表十六进制数，则它的前缀必须为0x 或0X。</span><span class="sxs-lookup"><span data-stu-id="14c92-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="14c92-122">否则，它将被视为十进制数。</span><span class="sxs-lookup"><span data-stu-id="14c92-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="14c92-123">父元素</span><span class="sxs-lookup"><span data-stu-id="14c92-123">Parent elements</span></span>

|<span data-ttu-id="14c92-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="14c92-124">**Element**</span></span>|<span data-ttu-id="14c92-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="14c92-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14c92-126">限制</span><span class="sxs-lookup"><span data-stu-id="14c92-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="14c92-127">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="14c92-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="14c92-128">not</span><span class="sxs-lookup"><span data-stu-id="14c92-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="14c92-129">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="14c92-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="14c92-130">And</span><span class="sxs-lookup"><span data-stu-id="14c92-130">And</span></span>](and.md) <br/> |<span data-ttu-id="14c92-131">表示允许您在两个或多个搜索表达式之间执行布尔 And 运算的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="14c92-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="14c92-132">如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="14c92-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="14c92-133">或</span><span class="sxs-lookup"><span data-stu-id="14c92-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="14c92-134">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="14c92-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="14c92-135">如果其任何子级返回**true**，则[或](or.md)元素将返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="14c92-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14c92-136">备注</span><span class="sxs-lookup"><span data-stu-id="14c92-136">Remarks</span></span>

<span data-ttu-id="14c92-137">如果对以下项执行的 AND 操作解析为0，则**排除**将解析为**true** ：</span><span class="sxs-lookup"><span data-stu-id="14c92-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="14c92-138">属性的按位值</span><span class="sxs-lookup"><span data-stu-id="14c92-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="14c92-139">属性的位掩码值</span><span class="sxs-lookup"><span data-stu-id="14c92-139">The bitmask value for the property</span></span>
    
<span data-ttu-id="14c92-140">"**排除**" 仅可应用于具有整数值的属性。</span><span class="sxs-lookup"><span data-stu-id="14c92-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="14c92-141">如果属性类型不是整数，则会在响应中返回**ErrorUnsupportedPathForQuery**的错误代码。</span><span class="sxs-lookup"><span data-stu-id="14c92-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="14c92-142">您可以通过不调用（不包括）执行反向操作。</span><span class="sxs-lookup"><span data-stu-id="14c92-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="14c92-143">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="14c92-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14c92-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="14c92-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14c92-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="14c92-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="14c92-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="14c92-146">Schema Name</span></span>  <br/> |<span data-ttu-id="14c92-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="14c92-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="14c92-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="14c92-148">Validation File</span></span>  <br/> |<span data-ttu-id="14c92-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="14c92-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="14c92-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="14c92-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="14c92-151">False</span><span class="sxs-lookup"><span data-stu-id="14c92-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14c92-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14c92-152">See also</span></span>

- [<span data-ttu-id="14c92-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="14c92-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

