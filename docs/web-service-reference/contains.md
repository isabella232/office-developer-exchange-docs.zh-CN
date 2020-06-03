---
title: Contains
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: Contains 元素表示一个搜索表达式，用于确定给定属性是否包含提供的常量字符串值。
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527115"
---
# <a name="contains"></a><span data-ttu-id="0ec71-103">Contains</span><span class="sxs-lookup"><span data-stu-id="0ec71-103">Contains</span></span>

<span data-ttu-id="0ec71-104">**Contains**元素表示一个搜索表达式，用于确定给定属性是否包含提供的常量字符串值。</span><span class="sxs-lookup"><span data-stu-id="0ec71-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


<span data-ttu-id="0ec71-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="0ec71-105">**ContainsExpressionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0ec71-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0ec71-106">Attributes and elements</span></span>

<span data-ttu-id="0ec71-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ec71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ec71-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0ec71-108">Attributes</span></span>

|<span data-ttu-id="0ec71-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0ec71-109">**Attribute**</span></span>|<span data-ttu-id="0ec71-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ec71-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ec71-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="0ec71-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="0ec71-112">标识搜索的边界。</span><span class="sxs-lookup"><span data-stu-id="0ec71-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="0ec71-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="0ec71-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="0ec71-114">确定搜索是否忽略大小写和空格。</span><span class="sxs-lookup"><span data-stu-id="0ec71-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="0ec71-115">ContainmentMode 属性值</span><span class="sxs-lookup"><span data-stu-id="0ec71-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="0ec71-116">**值**</span><span class="sxs-lookup"><span data-stu-id="0ec71-116">**Value**</span></span>|<span data-ttu-id="0ec71-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ec71-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ec71-118">FullString</span><span class="sxs-lookup"><span data-stu-id="0ec71-118">FullString</span></span>  <br/> |<span data-ttu-id="0ec71-119">在完整字符串和常量之间进行比较。</span><span class="sxs-lookup"><span data-stu-id="0ec71-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="0ec71-120">属性值和提供的常量完全相同。</span><span class="sxs-lookup"><span data-stu-id="0ec71-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="0ec71-121">作</span><span class="sxs-lookup"><span data-stu-id="0ec71-121">Prefixed</span></span>  <br/> |<span data-ttu-id="0ec71-122">在字符串前缀和常量之间进行比较。</span><span class="sxs-lookup"><span data-stu-id="0ec71-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="0ec71-123">取</span><span class="sxs-lookup"><span data-stu-id="0ec71-123">Substring</span></span>  <br/> |<span data-ttu-id="0ec71-124">在字符串的子字符串和常量之间进行比较。</span><span class="sxs-lookup"><span data-stu-id="0ec71-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="0ec71-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="0ec71-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="0ec71-126">在字符串中单个词的前缀和常量之间进行比较。</span><span class="sxs-lookup"><span data-stu-id="0ec71-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="0ec71-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="0ec71-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="0ec71-128">在字符串中的精确短语和常量之间进行比较。</span><span class="sxs-lookup"><span data-stu-id="0ec71-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="0ec71-129">ContainmentComparison 属性值</span><span class="sxs-lookup"><span data-stu-id="0ec71-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="0ec71-130">**值**</span><span class="sxs-lookup"><span data-stu-id="0ec71-130">**Value**</span></span>|<span data-ttu-id="0ec71-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="0ec71-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0ec71-132">混杂</span><span class="sxs-lookup"><span data-stu-id="0ec71-132">Exact</span></span>  <br/> |<span data-ttu-id="0ec71-133">比较必须准确。</span><span class="sxs-lookup"><span data-stu-id="0ec71-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="0ec71-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="0ec71-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="0ec71-135">比较将忽略大小写。</span><span class="sxs-lookup"><span data-stu-id="0ec71-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="0ec71-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="0ec71-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="0ec71-137">比较将忽略非空格字符。</span><span class="sxs-lookup"><span data-stu-id="0ec71-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="0ec71-138">稀疏</span><span class="sxs-lookup"><span data-stu-id="0ec71-138">Loose</span></span>  <br/> |<span data-ttu-id="0ec71-139">要删除的。</span><span class="sxs-lookup"><span data-stu-id="0ec71-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="0ec71-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="0ec71-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="0ec71-141">比较将忽略大小写和非空格字符。</span><span class="sxs-lookup"><span data-stu-id="0ec71-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="0ec71-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="0ec71-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="0ec71-143">要删除的。</span><span class="sxs-lookup"><span data-stu-id="0ec71-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="0ec71-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="0ec71-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="0ec71-145">要删除的。</span><span class="sxs-lookup"><span data-stu-id="0ec71-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="0ec71-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="0ec71-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="0ec71-147">要删除的。</span><span class="sxs-lookup"><span data-stu-id="0ec71-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0ec71-148">子元素</span><span class="sxs-lookup"><span data-stu-id="0ec71-148">Child elements</span></span>

|<span data-ttu-id="0ec71-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ec71-149">**Element**</span></span>|<span data-ttu-id="0ec71-150">**描述**</span><span class="sxs-lookup"><span data-stu-id="0ec71-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ec71-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="0ec71-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="0ec71-152">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="0ec71-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="0ec71-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="0ec71-154">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="0ec71-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="0ec71-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="0ec71-156">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="0ec71-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-157">常量</span><span class="sxs-lookup"><span data-stu-id="0ec71-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="0ec71-158">标识限制中的常量值。</span><span class="sxs-lookup"><span data-stu-id="0ec71-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ec71-159">父元素</span><span class="sxs-lookup"><span data-stu-id="0ec71-159">Parent elements</span></span>

|<span data-ttu-id="0ec71-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="0ec71-160">**Element**</span></span>|<span data-ttu-id="0ec71-161">**描述**</span><span class="sxs-lookup"><span data-stu-id="0ec71-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ec71-162">限制</span><span class="sxs-lookup"><span data-stu-id="0ec71-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="0ec71-163">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="0ec71-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-164">not</span><span class="sxs-lookup"><span data-stu-id="0ec71-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="0ec71-165">表示对其包含的搜索表达式的布尔值求反的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="0ec71-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-166">And</span><span class="sxs-lookup"><span data-stu-id="0ec71-166">And</span></span>](and.md) <br/> |<span data-ttu-id="0ec71-167">表示允许您在两个或多个搜索表达式之间执行布尔 And 运算的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="0ec71-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="0ec71-168">如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="0ec71-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="0ec71-169">或</span><span class="sxs-lookup"><span data-stu-id="0ec71-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="0ec71-170">表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="0ec71-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="0ec71-171">如果其任何子级返回**true**，则[或](or.md)元素将返回**true** 。</span><span class="sxs-lookup"><span data-stu-id="0ec71-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ec71-172">备注</span><span class="sxs-lookup"><span data-stu-id="0ec71-172">Remarks</span></span>

<span data-ttu-id="0ec71-173">属性用于确定元素的匹配方式。</span><span class="sxs-lookup"><span data-stu-id="0ec71-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="0ec71-174">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0ec71-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ec71-175">元素信息</span><span class="sxs-lookup"><span data-stu-id="0ec71-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ec71-176">命名空间</span><span class="sxs-lookup"><span data-stu-id="0ec71-176">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0ec71-177">架构名称</span><span class="sxs-lookup"><span data-stu-id="0ec71-177">Schema Name</span></span>  <br/> |<span data-ttu-id="0ec71-178">类型架构</span><span class="sxs-lookup"><span data-stu-id="0ec71-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="0ec71-179">验证文件</span><span class="sxs-lookup"><span data-stu-id="0ec71-179">Validation File</span></span>  <br/> |<span data-ttu-id="0ec71-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0ec71-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0ec71-181">可以为空</span><span class="sxs-lookup"><span data-stu-id="0ec71-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ec71-182">False</span><span class="sxs-lookup"><span data-stu-id="0ec71-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ec71-183">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0ec71-183">See also</span></span>

- [<span data-ttu-id="0ec71-184">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0ec71-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

