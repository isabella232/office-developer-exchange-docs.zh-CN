---
title: 排除
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
description: 排除元素执行指定的属性和提供的值的按位掩码。
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754191"
---
# <a name="excludes"></a><span data-ttu-id="84859-103">排除</span><span class="sxs-lookup"><span data-stu-id="84859-103">Excludes</span></span>

<span data-ttu-id="84859-104">**排除**元素执行指定的属性和提供的值的按位掩码。</span><span class="sxs-lookup"><span data-stu-id="84859-104">The **Excludes** element performs a bitwise mask of the specified property and a supplied value.</span></span> 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 <span data-ttu-id="84859-105">**ExcludesType**</span><span class="sxs-lookup"><span data-stu-id="84859-105">**ExcludesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84859-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84859-106">Attributes and elements</span></span>

<span data-ttu-id="84859-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84859-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84859-108">属性</span><span class="sxs-lookup"><span data-stu-id="84859-108">Attributes</span></span>

<span data-ttu-id="84859-109">无。</span><span class="sxs-lookup"><span data-stu-id="84859-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84859-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84859-110">Child elements</span></span>

|<span data-ttu-id="84859-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="84859-111">**Element**</span></span>|<span data-ttu-id="84859-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="84859-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84859-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="84859-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="84859-114">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="84859-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="84859-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="84859-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="84859-116">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="84859-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="84859-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="84859-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="84859-118">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="84859-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="84859-119">位掩码</span><span class="sxs-lookup"><span data-stu-id="84859-119">Bitmask</span></span>](bitmask.md) <br/> |<span data-ttu-id="84859-120">代表用于[排除](excludes.md)限制操作过程中使用十六进制或小数的掩码。</span><span class="sxs-lookup"><span data-stu-id="84859-120">Represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> <span data-ttu-id="84859-121">如果位掩码表示的十六进制数，它必须由 0 x 或 0x 作为前缀。</span><span class="sxs-lookup"><span data-stu-id="84859-121">If the bitmask represents a hexadecimal number, it must be prefixed by 0x or 0X.</span></span> <span data-ttu-id="84859-122">否则，它将被视为十进制数。</span><span class="sxs-lookup"><span data-stu-id="84859-122">Otherwise, it will be considered a decimal number.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84859-123">父元素</span><span class="sxs-lookup"><span data-stu-id="84859-123">Parent elements</span></span>

|<span data-ttu-id="84859-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="84859-124">**Element**</span></span>|<span data-ttu-id="84859-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="84859-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84859-126">限制</span><span class="sxs-lookup"><span data-stu-id="84859-126">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="84859-127">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="84859-127">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="84859-128">not</span><span class="sxs-lookup"><span data-stu-id="84859-128">Not</span></span>](not.md) <br/> |<span data-ttu-id="84859-129">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="84859-129">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="84859-130">And</span><span class="sxs-lookup"><span data-stu-id="84859-130">And</span></span>](and.md) <br/> |<span data-ttu-id="84859-131">代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间 Boolean 和操作。</span><span class="sxs-lookup"><span data-stu-id="84859-131">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="84859-132">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="84859-132">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="84859-133">或</span><span class="sxs-lookup"><span data-stu-id="84859-133">Or</span></span>](or.md) <br/> |<span data-ttu-id="84859-134">表示对它所包含的搜索表达式执行逻辑或搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="84859-134">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="84859-135">如果任何其子返回**true**，则将返回**true** [或](or.md)元素。</span><span class="sxs-lookup"><span data-stu-id="84859-135">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84859-136">备注</span><span class="sxs-lookup"><span data-stu-id="84859-136">Remarks</span></span>

 <span data-ttu-id="84859-137">如果执行下面的 AND 操作将解析为 0，**排除**将解析为**true** :</span><span class="sxs-lookup"><span data-stu-id="84859-137">**Excludes** will resolve to **true** if an AND operation performed on the following resolves to 0:</span></span> 
  
1. <span data-ttu-id="84859-138">属性的按位值</span><span class="sxs-lookup"><span data-stu-id="84859-138">The bitwise value for the property</span></span>
    
2. <span data-ttu-id="84859-139">属性的位掩码值</span><span class="sxs-lookup"><span data-stu-id="84859-139">The bitmask value for the property</span></span>
    
 <span data-ttu-id="84859-140">**排除**可只能应用于该属性的整数值。</span><span class="sxs-lookup"><span data-stu-id="84859-140">**Excludes** can only be applied to a property that has an integer value.</span></span> <span data-ttu-id="84859-141">属性类型是一个整数之外的任何内容，如果是响应中返回的错误代码为**ErrorUnsupportedPathForQuery** 。</span><span class="sxs-lookup"><span data-stu-id="84859-141">If the property type is anything other than an integer, an error code of **ErrorUnsupportedPathForQuery** is returned in the response.</span></span> 
  
<span data-ttu-id="84859-142">您可以通过调用 Not(Excludes) 执行还原操作。</span><span class="sxs-lookup"><span data-stu-id="84859-142">You can perform the reverse operation by calling Not(Excludes).</span></span>
  
<span data-ttu-id="84859-143">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84859-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84859-144">元素信息</span><span class="sxs-lookup"><span data-stu-id="84859-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84859-145">命名空间</span><span class="sxs-lookup"><span data-stu-id="84859-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84859-146">架构名称</span><span class="sxs-lookup"><span data-stu-id="84859-146">Schema Name</span></span>  <br/> |<span data-ttu-id="84859-147">类型架构</span><span class="sxs-lookup"><span data-stu-id="84859-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="84859-148">验证文件</span><span class="sxs-lookup"><span data-stu-id="84859-148">Validation File</span></span>  <br/> |<span data-ttu-id="84859-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84859-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84859-150">可以为空</span><span class="sxs-lookup"><span data-stu-id="84859-150">Can be Empty</span></span>  <br/> |<span data-ttu-id="84859-151">False</span><span class="sxs-lookup"><span data-stu-id="84859-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84859-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84859-152">See also</span></span>



- [<span data-ttu-id="84859-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84859-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

