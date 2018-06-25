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
description: Contains 元素均表示一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。
ms.openlocfilehash: 083efdf32cd32bea6964361b5b558480aa937280
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753526"
---
# <a name="contains"></a><span data-ttu-id="f3713-103">Contains</span><span class="sxs-lookup"><span data-stu-id="f3713-103">Contains</span></span>

<span data-ttu-id="f3713-104">**Contains**元素均表示一个搜索表达式，确定给定的属性是否包含提供常量的字符串值。</span><span class="sxs-lookup"><span data-stu-id="f3713-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

 <span data-ttu-id="f3713-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="f3713-105">**ContainsExpressionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3713-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f3713-106">Attributes and elements</span></span>

<span data-ttu-id="f3713-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f3713-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3713-108">属性</span><span class="sxs-lookup"><span data-stu-id="f3713-108">Attributes</span></span>

|<span data-ttu-id="f3713-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f3713-109">**Attribute**</span></span>|<span data-ttu-id="f3713-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3713-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3713-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="f3713-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="f3713-112">标识搜索的边界。</span><span class="sxs-lookup"><span data-stu-id="f3713-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="f3713-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="f3713-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="f3713-114">确定搜索是否忽略大小写和空格。</span><span class="sxs-lookup"><span data-stu-id="f3713-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="f3713-115">ContainmentMode 属性值</span><span class="sxs-lookup"><span data-stu-id="f3713-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="f3713-116">**值**</span><span class="sxs-lookup"><span data-stu-id="f3713-116">**Value**</span></span>|<span data-ttu-id="f3713-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3713-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3713-118">FullString</span><span class="sxs-lookup"><span data-stu-id="f3713-118">FullString</span></span>  <br/> |<span data-ttu-id="f3713-119">比较不之间的完整字符串和常量。</span><span class="sxs-lookup"><span data-stu-id="f3713-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="f3713-120">该属性值和提供的常量保持完全相同。</span><span class="sxs-lookup"><span data-stu-id="f3713-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="f3713-121">作为前缀</span><span class="sxs-lookup"><span data-stu-id="f3713-121">Prefixed</span></span>  <br/> |<span data-ttu-id="f3713-122">比较结果为字符串前缀和常量之间。</span><span class="sxs-lookup"><span data-stu-id="f3713-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="f3713-123">子字符串</span><span class="sxs-lookup"><span data-stu-id="f3713-123">Substring</span></span>  <br/> |<span data-ttu-id="f3713-124">比较结果为字符串的子字符串和常量之间。</span><span class="sxs-lookup"><span data-stu-id="f3713-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="f3713-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="f3713-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="f3713-126">比较结果为字符串中的个别单词前缀和常量之间。</span><span class="sxs-lookup"><span data-stu-id="f3713-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="f3713-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="f3713-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="f3713-128">比较结果为字符串中的准确的短语和常量之间。</span><span class="sxs-lookup"><span data-stu-id="f3713-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="f3713-129">ContainmentComparison 属性值</span><span class="sxs-lookup"><span data-stu-id="f3713-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="f3713-130">**值**</span><span class="sxs-lookup"><span data-stu-id="f3713-130">**Value**</span></span>|<span data-ttu-id="f3713-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3713-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3713-132">Exact</span><span class="sxs-lookup"><span data-stu-id="f3713-132">Exact</span></span>  <br/> |<span data-ttu-id="f3713-133">比较结果必须完全正确。</span><span class="sxs-lookup"><span data-stu-id="f3713-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="f3713-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="f3713-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="f3713-135">比较忽略大小写。</span><span class="sxs-lookup"><span data-stu-id="f3713-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="f3713-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="f3713-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="f3713-137">比较忽略不占位字符。</span><span class="sxs-lookup"><span data-stu-id="f3713-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="f3713-138">稀疏</span><span class="sxs-lookup"><span data-stu-id="f3713-138">Loose</span></span>  <br/> |<span data-ttu-id="f3713-139">要删除。</span><span class="sxs-lookup"><span data-stu-id="f3713-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="f3713-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="f3713-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="f3713-141">比较结果将忽略大小写和无空格字符。</span><span class="sxs-lookup"><span data-stu-id="f3713-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="f3713-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="f3713-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="f3713-143">要删除。</span><span class="sxs-lookup"><span data-stu-id="f3713-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="f3713-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="f3713-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="f3713-145">要删除。</span><span class="sxs-lookup"><span data-stu-id="f3713-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="f3713-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="f3713-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="f3713-147">要删除。</span><span class="sxs-lookup"><span data-stu-id="f3713-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f3713-148">子元素</span><span class="sxs-lookup"><span data-stu-id="f3713-148">Child elements</span></span>

|<span data-ttu-id="f3713-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3713-149">**Element**</span></span>|<span data-ttu-id="f3713-150">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3713-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3713-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f3713-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f3713-152">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="f3713-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f3713-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f3713-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f3713-154">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="f3713-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="f3713-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f3713-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f3713-156">标识 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="f3713-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="f3713-157">常量</span><span class="sxs-lookup"><span data-stu-id="f3713-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="f3713-158">标识限制中的以常量值。</span><span class="sxs-lookup"><span data-stu-id="f3713-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f3713-159">父元素</span><span class="sxs-lookup"><span data-stu-id="f3713-159">Parent elements</span></span>

|<span data-ttu-id="f3713-160">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3713-160">**Element**</span></span>|<span data-ttu-id="f3713-161">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3713-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3713-162">限制</span><span class="sxs-lookup"><span data-stu-id="f3713-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="f3713-163">表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="f3713-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="f3713-164">not</span><span class="sxs-lookup"><span data-stu-id="f3713-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="f3713-165">代表一个搜索表达式，它包含的搜索表达式的布尔值求非。</span><span class="sxs-lookup"><span data-stu-id="f3713-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="f3713-166">And</span><span class="sxs-lookup"><span data-stu-id="f3713-166">And</span></span>](and.md) <br/> |<span data-ttu-id="f3713-167">代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间 Boolean 和操作。</span><span class="sxs-lookup"><span data-stu-id="f3713-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="f3713-168">如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。</span><span class="sxs-lookup"><span data-stu-id="f3713-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="f3713-169">或</span><span class="sxs-lookup"><span data-stu-id="f3713-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="f3713-170">表示对它所包含的搜索表达式执行逻辑或搜索表达式。</span><span class="sxs-lookup"><span data-stu-id="f3713-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="f3713-171">如果任何其子返回**true**，则将返回**true** [或](or.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f3713-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3713-172">注解</span><span class="sxs-lookup"><span data-stu-id="f3713-172">Remarks</span></span>

<span data-ttu-id="f3713-173">属性用于确定如何匹配元素。</span><span class="sxs-lookup"><span data-stu-id="f3713-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="f3713-174">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f3713-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3713-175">元素信息</span><span class="sxs-lookup"><span data-stu-id="f3713-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3713-176">命名空间</span><span class="sxs-lookup"><span data-stu-id="f3713-176">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3713-177">架构名称</span><span class="sxs-lookup"><span data-stu-id="f3713-177">Schema Name</span></span>  <br/> |<span data-ttu-id="f3713-178">类型架构</span><span class="sxs-lookup"><span data-stu-id="f3713-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3713-179">验证文件</span><span class="sxs-lookup"><span data-stu-id="f3713-179">Validation File</span></span>  <br/> |<span data-ttu-id="f3713-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3713-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3713-181">可以为空</span><span class="sxs-lookup"><span data-stu-id="f3713-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3713-182">False</span><span class="sxs-lookup"><span data-stu-id="f3713-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3713-183">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3713-183">See also</span></span>



- [<span data-ttu-id="f3713-184">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f3713-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

