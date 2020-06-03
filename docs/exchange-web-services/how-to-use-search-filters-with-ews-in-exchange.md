---
title: 在 Exchange 中将搜索筛选器与 EWS 结合使用
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: 了解如何将搜索筛选器与 Exchange 中的 EWS 托管 API 或 EWS 结合使用。
localization_priority: Priority
ms.openlocfilehash: 04a74ec92d4bced8abd58d164a1c186d6405e679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455833"
---
# <a name="use-search-filters-with-ews-in-exchange"></a><span data-ttu-id="abbe9-103">在 Exchange 中将搜索筛选器与 EWS 结合使用</span><span class="sxs-lookup"><span data-stu-id="abbe9-103">Use search filters with EWS in Exchange</span></span>

<span data-ttu-id="abbe9-104">了解如何将搜索筛选器与 Exchange 中的 EWS 托管 API 或 EWS 结合使用。</span><span class="sxs-lookup"><span data-stu-id="abbe9-104">Find out how to use search filters with the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="abbe9-105">搜索筛选器是在 EWS 托管 API 或 EWS 应用程序中表示搜索条件的主要工具。</span><span class="sxs-lookup"><span data-stu-id="abbe9-105">Search filters are the primary tool for expressing search criteria in your EWS Managed API or EWS application.</span></span> <span data-ttu-id="abbe9-106">建议使用搜索筛选器（而不是[查询字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)）执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="abbe9-106">We recommend that you use search filters, as opposed to [query strings](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), to do the following:</span></span>
  
- <span data-ttu-id="abbe9-107">搜索特定属性或一组属性。</span><span class="sxs-lookup"><span data-stu-id="abbe9-107">Search on a specific property or set of properties.</span></span>  
- <span data-ttu-id="abbe9-108">使用多个搜索条件的搜索。</span><span class="sxs-lookup"><span data-stu-id="abbe9-108">Search using multiple search criteria.</span></span>
    
<span data-ttu-id="abbe9-109">仅当您执行以下任一操作时，才可以选择搜索筛选器：</span><span class="sxs-lookup"><span data-stu-id="abbe9-109">Search filters are your only option if you are doing any of the following:</span></span>
  
- <span data-ttu-id="abbe9-110">搜索自定义属性。</span><span class="sxs-lookup"><span data-stu-id="abbe9-110">Searching custom properties.</span></span>  
- <span data-ttu-id="abbe9-111">执行区分大小写的字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="abbe9-111">Performing case-sensitive string searches.</span></span>  
- <span data-ttu-id="abbe9-112">执行前缀或完全匹配的字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="abbe9-112">Performing prefix or exact match string searches.</span></span> 
- <span data-ttu-id="abbe9-113">执行位掩码搜索。</span><span class="sxs-lookup"><span data-stu-id="abbe9-113">Performing bitmask searches.</span></span>
- <span data-ttu-id="abbe9-114">搜索具有特定属性集的项目，而不考虑值。</span><span class="sxs-lookup"><span data-stu-id="abbe9-114">Searching for items that have a specific property set, regardless of value.</span></span>
- <span data-ttu-id="abbe9-115">搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="abbe9-115">Searching for folders.</span></span>
- <span data-ttu-id="abbe9-116">创建搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="abbe9-116">Creating search folders.</span></span>
    
## <a name="determine-what-type-of-search-filter-you-need"></a><span data-ttu-id="abbe9-117">确定所需的搜索筛选器的类型</span><span class="sxs-lookup"><span data-stu-id="abbe9-117">Determine what type of search filter you need</span></span>
<span data-ttu-id="abbe9-118"><a name="bk_SelectFilter"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-118"><a name="bk_SelectFilter"> </a></span></span>

<span data-ttu-id="abbe9-119">在创建搜索筛选器之前，请先确定所需的筛选器类型。</span><span class="sxs-lookup"><span data-stu-id="abbe9-119">Before you create a search filter, first determine which type of filter you need.</span></span> <span data-ttu-id="abbe9-120">筛选器类型在 EWS 托管 API 中作为[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)类的子类实现，并作为 ews 中的[限制](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)元素的子元素实现。</span><span class="sxs-lookup"><span data-stu-id="abbe9-120">The filter types are implemented as descendant classes of the [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) class in the EWS Managed API, and as child elements of the [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="abbe9-121">**表1。搜索筛选器的类型**</span><span class="sxs-lookup"><span data-stu-id="abbe9-121">**Table 1. Types of search filters**</span></span>

|<span data-ttu-id="abbe9-122">**筛选器类型**</span><span class="sxs-lookup"><span data-stu-id="abbe9-122">**Filter type**</span></span>|<span data-ttu-id="abbe9-123">**EWS 托管 API 类**</span><span class="sxs-lookup"><span data-stu-id="abbe9-123">**EWS Managed API class**</span></span>|<span data-ttu-id="abbe9-124">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="abbe9-124">**EWS element**</span></span>|<span data-ttu-id="abbe9-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="abbe9-125">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="abbe9-126">包含筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-126">Contains filter</span></span>  <br/> |[<span data-ttu-id="abbe9-127">ContainsSubstring</span><span class="sxs-lookup"><span data-stu-id="abbe9-127">ContainsSubstring</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-128">Contains</span><span class="sxs-lookup"><span data-stu-id="abbe9-128">Contains</span></span>](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-129">用于字符串比较的最佳筛选器类型。</span><span class="sxs-lookup"><span data-stu-id="abbe9-129">The best filter type to use for string comparisons.</span></span> <span data-ttu-id="abbe9-130">它允许您控制区分大小写，是否忽略空白，并设置包含模式。</span><span class="sxs-lookup"><span data-stu-id="abbe9-130">It allows you to control case sensitivity, whether to ignore whitespace, and set the containment mode.</span></span>  <br/> |
|<span data-ttu-id="abbe9-131">位掩码筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-131">Bitmask filter</span></span>  <br/> |[<span data-ttu-id="abbe9-132">ExcludesBitmask</span><span class="sxs-lookup"><span data-stu-id="abbe9-132">ExcludesBitmask</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-133">不包括</span><span class="sxs-lookup"><span data-stu-id="abbe9-133">Excludes</span></span>](https://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-134">允许您将整数属性作为位掩码进行搜索，并且仅返回其位与指定的位掩码设置相对应的结果。</span><span class="sxs-lookup"><span data-stu-id="abbe9-134">Allows you to search integer properties as bitmasks and only return results that have bits corresponding to the specified bitmask unset.</span></span>  <br/> |
|<span data-ttu-id="abbe9-135">存在筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-135">Exists filter</span></span>  <br/> |[<span data-ttu-id="abbe9-136">Exists</span><span class="sxs-lookup"><span data-stu-id="abbe9-136">Exists</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-137">Exists</span><span class="sxs-lookup"><span data-stu-id="abbe9-137">Exists</span></span>](https://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-138">返回具有指定属性的所有项，而不考虑值。</span><span class="sxs-lookup"><span data-stu-id="abbe9-138">Returns all items that have the specified property present, regardless of value.</span></span>  <br/> |
|<span data-ttu-id="abbe9-139">等式筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-139">Equality filter</span></span>  <br/> |[<span data-ttu-id="abbe9-140">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-140">IsEqualTo</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="abbe9-141">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-141">IsNotEqualTo</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-142">IsEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-142">IsEqualTo</span></span>](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [<span data-ttu-id="abbe9-143">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-143">IsNotEqualTo</span></span>](https://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-144">将指定的属性的值与指定的常数值或另一个属性的值进行比较，并返回具有相等值（在**IsEqualTo**筛选器中）或非相等值（如果为**IsNotEqualTo**筛选器）的所有项。</span><span class="sxs-lookup"><span data-stu-id="abbe9-144">Compares the value of the specified property with either a specified constant value or the value of another property and return all items that have an equal value (in the case of an **IsEqualTo** filter) or a non-equal value (in the case of an **IsNotEqualTo** filter).</span></span>  <br/> |
|<span data-ttu-id="abbe9-145">关系测试筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-145">Relational testing filter</span></span>  <br/> |[<span data-ttu-id="abbe9-146">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="abbe9-146">IsGreaterThan</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="abbe9-147">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-147">IsGreaterThanOrEqualTo</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="abbe9-148">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="abbe9-148">IsLessThan</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="abbe9-149">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-149">IsLessThanOrEqualTo</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-150">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="abbe9-150">IsGreaterThan</span></span>](https://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [<span data-ttu-id="abbe9-151">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-151">IsGreaterThanOrEqualTo</span></span>](https://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [<span data-ttu-id="abbe9-152">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="abbe9-152">IsLessThan</span></span>](https://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [<span data-ttu-id="abbe9-153">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="abbe9-153">IsLessThanOrEqualTo</span></span>](https://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-154">返回具有与指定的常量值或其他属性的相应关系的指定属性的值的所有项。</span><span class="sxs-lookup"><span data-stu-id="abbe9-154">Returns all items that have a value for the specified property in the appropriate relation to either a specified constant value or another property.</span></span> <span data-ttu-id="abbe9-155">例如， **IsGreaterThan**筛选器将返回一个值大于指定属性中指定值的所有项。</span><span class="sxs-lookup"><span data-stu-id="abbe9-155">For example, an **IsGreaterThan** filter returns all items that have a value that is greater than the specified value in the specified property.</span></span>  <br/> |
|<span data-ttu-id="abbe9-156">Negating 筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-156">Negating filter</span></span>  <br/> |[<span data-ttu-id="abbe9-157">Not</span><span class="sxs-lookup"><span data-stu-id="abbe9-157">Not</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-158">Not</span><span class="sxs-lookup"><span data-stu-id="abbe9-158">Not</span></span>](https://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-159">对其他筛选器的结果求反。</span><span class="sxs-lookup"><span data-stu-id="abbe9-159">Negates the result of the other filters.</span></span>  <br/> |
|<span data-ttu-id="abbe9-160">复合筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-160">Compound filter</span></span>  <br/> |[<span data-ttu-id="abbe9-161">SearchFilterCollection</span><span class="sxs-lookup"><span data-stu-id="abbe9-161">SearchFilterCollection</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="abbe9-162">And</span><span class="sxs-lookup"><span data-stu-id="abbe9-162">And</span></span>](https://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [<span data-ttu-id="abbe9-163">或</span><span class="sxs-lookup"><span data-stu-id="abbe9-163">Or</span></span>](https://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |<span data-ttu-id="abbe9-164">合并多个筛选器，以便实现更复杂的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="abbe9-164">Combines multiple filters, allowing for more complex search criteria.</span></span>  <br/> |
   
### <a name="contains-filter"></a><span data-ttu-id="abbe9-165">包含筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-165">Contains filter</span></span>

<span data-ttu-id="abbe9-166">包含筛选器是搜索字符串属性的最佳选择。</span><span class="sxs-lookup"><span data-stu-id="abbe9-166">A contains filter is the best choice for searching string properties.</span></span> <span data-ttu-id="abbe9-167">通过包含筛选器，您可以通过设置包含模式和比较模式来控制字符串匹配的各个方面，如区分大小写和空白的处理方式。</span><span class="sxs-lookup"><span data-stu-id="abbe9-167">With a contains filter, you can control aspects of string matching, like case sensitivity and how whitespace is treated, by setting the containment mode and the comparison mode.</span></span>
  
#### <a name="contains-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-168">包含 EWS 托管 API 中的筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-168">Contains filter in the EWS Managed API</span></span>
<span data-ttu-id="abbe9-169"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-169"><a name="bk_ContainsEWSMA"> </a></span></span>

<span data-ttu-id="abbe9-170">如果使用 EWS 托管 API，请使用[ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)类的[ContainmentMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx)属性设置包含模式，并使用**ContainsSubstring**类的[ComparisonMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx)属性设置比较模式。</span><span class="sxs-lookup"><span data-stu-id="abbe9-170">If you're using the EWS Managed API, you set the containment mode by using the [ContainmentMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) property of the [ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) class, and you set the comparison mode by using the [ComparisonMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) property of the **ContainsSubstring** class.</span></span> <span data-ttu-id="abbe9-171">下面的示例演示如何创建搜索筛选器，以搜索子字符串 "会议备注" 项的 "主题" 字段。</span><span class="sxs-lookup"><span data-stu-id="abbe9-171">The following example shows you how to create a search filter that searches the subject field of items for the substring "meeting notes".</span></span> <span data-ttu-id="abbe9-172">本示例忽略大小写，但不忽略空格。</span><span class="sxs-lookup"><span data-stu-id="abbe9-172">This example ignores case, but does not ignore whitespace.</span></span> 
  
```cs
// Find all items with a subject that contain the substring
// "meeting notes", regardless of case.
// Matches include:
//   - meeting notes
//   - Meeting Notes
//   - Here are my meeting notes
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

#### <a name="contains-filter-in-ews"></a><span data-ttu-id="abbe9-173">包含 EWS 中的筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-173">Contains filter in EWS</span></span>
<span data-ttu-id="abbe9-174"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-174"><a name="bk_ContainsEWSMA"> </a></span></span>

<span data-ttu-id="abbe9-175">在 EWS 中，可以使用[contains](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx)元素上的**ContainmentMode**属性设置包含模式，并使用**contains**元素上的**ContainmentComparison**属性设置比较模式。</span><span class="sxs-lookup"><span data-stu-id="abbe9-175">In EWS, you set the containment mode by using the **ContainmentMode** attribute on the [Contains](https://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) element, and you set the comparison mode by using the **ContainmentComparison** attribute on the **Contains** element.</span></span> <span data-ttu-id="abbe9-176">下面的示例演示如何创建搜索筛选器，以搜索子字符串 "会议备注" 的项目的主题字段。</span><span class="sxs-lookup"><span data-stu-id="abbe9-176">The following example shows you how to create a search filter to search the subject field of items for the substring "meeting notes".</span></span> <span data-ttu-id="abbe9-177">本示例忽略大小写，但不忽略空格。</span><span class="sxs-lookup"><span data-stu-id="abbe9-177">This example ignores case, but does not ignore whitespace.</span></span> 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a><span data-ttu-id="abbe9-178">位掩码筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-178">Bitmask filter</span></span>

<span data-ttu-id="abbe9-179">使用位掩码筛选器，可以将整数属性作为位掩码进行搜索，并返回在指定属性值中未设置特定位的结果。</span><span class="sxs-lookup"><span data-stu-id="abbe9-179">A bitmask filter enables you to search integer properties as bitmasks, and return results where specific bits are not set in the value of the specified property.</span></span>
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-180">EWS 托管 API 中的位掩码筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-180">Bitmask filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-181">下面的示例演示如何使用 EWS 托管 API 创建搜索筛选器，以返回**itemindex as**自定义属性（在 "[示例：使用搜索筛选器" 和 "EWS 托管 API"](#bk_ExampleEWSMA)一节中的 "查找项目" 一节）中具有值的所有项目（二进制中的10个）集。</span><span class="sxs-lookup"><span data-stu-id="abbe9-181">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
```cs
// Find all items with a value of the custom property that does not
// have the second bit (0010) set.
// Matches include:
//   - Property not set
//   - 1 (0001)
//   - 4 (0100)
//   - 5 (0101)
//   - 8 (1000)
SearchFilter.ExcludesBitmask bit2NotSetFilter = 
    new SearchFilter.ExcludesBitmask(customPropDefinition, 2);
```

#### <a name="bitmask-filter-in-ews"></a><span data-ttu-id="abbe9-182">EWS 中的位掩码筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-182">Bitmask filter in EWS</span></span>

<span data-ttu-id="abbe9-183">下面的示例演示如何使用 EWS 创建搜索筛选器，以返回**itemindex as**自定义属性（在本示例中的 "[使用搜索筛选器" 和 "EWS 托管 API"](#bk_ExampleEWSMA)一节中的 "查找项目" 一节）中具有值的所有项目（二进制数中的10个）设置。</span><span class="sxs-lookup"><span data-stu-id="abbe9-183">The following example shows you how to use EWS to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a><span data-ttu-id="abbe9-184">存在筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-184">Exists filter</span></span>

<span data-ttu-id="abbe9-185">存在筛选器使您能够搜索在其上设置了特定属性的项目，而不考虑该值。</span><span class="sxs-lookup"><span data-stu-id="abbe9-185">An exists filter enables you to search for items that have a specific property set on them, regardless of the value.</span></span>
  
#### <a name="exists-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-186">EWS 托管 API 中存在筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-186">Exists filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-187">下面的示例演示如何创建搜索筛选器以返回具有**itemindex as**自定义属性集的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-187">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a><span data-ttu-id="abbe9-188">在 EWS 中存在筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-188">Exists filter in EWS</span></span>

<span data-ttu-id="abbe9-189">下面的示例演示如何创建搜索筛选器以返回具有**itemindex as**自定义属性集的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-189">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a><span data-ttu-id="abbe9-190">等式筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-190">Equality filter</span></span>

<span data-ttu-id="abbe9-191">使用相等性筛选器，可以搜索指定属性的值等于或不等于特定值的所有项。</span><span class="sxs-lookup"><span data-stu-id="abbe9-191">Equality filters enable you to search for all items that have a value for the specified property that either equals a specific value or does not equal a specific value.</span></span> <span data-ttu-id="abbe9-192">要与之比较的值可以是常量值，也可以是每个项目上另一个属性的值。</span><span class="sxs-lookup"><span data-stu-id="abbe9-192">The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="equality-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-193">EWS 托管 API 中的等同性筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-193">Equality filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-194">下面的示例演示如何使用 EWS 托管 API 创建搜索筛选器，以返回所有尚未阅读的项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-194">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have not been read.</span></span>
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

<span data-ttu-id="abbe9-195">下面的示例演示如何创建搜索筛选器，以返回**itemindex as**属性中的值与项目大小不相等的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-195">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a><span data-ttu-id="abbe9-196">EWS 中的相等性筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-196">Equality filter in EWS</span></span>

<span data-ttu-id="abbe9-197">下面的示例演示如何使用 EWS 创建搜索筛选器，以返回所有尚未阅读的项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-197">The following example shows you how to use EWS to create a search filter to return all items that have not been read.</span></span>
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

<span data-ttu-id="abbe9-198">下面的示例演示如何创建搜索筛选器，以返回**itemindex as**属性中的值与项目大小不相等的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-198">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a><span data-ttu-id="abbe9-199">关系测试筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-199">Relational testing filter</span></span>

<span data-ttu-id="abbe9-200">关系测试筛选器使您可以搜索在指定属性中具有值大于（ \> ）、大于或等于（ \> =）、小于（ \< ）或小于或等于（ \< =）指定值的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-200">Relational testing filters enable you to search for all items that have a value in the specified property that is either greater than (\>), greater than or equal to (\>=), less than (\<), or less than or equal to (\<=) a specified value.</span></span> <span data-ttu-id="abbe9-201">要与之比较的值可以是常量值，也可以是每个项目上另一个属性的值。</span><span class="sxs-lookup"><span data-stu-id="abbe9-201">The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-202">EWS 托管 API 中的关系测试筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-202">Relational testing filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-203">下面的示例演示如何使用 EWS 托管 API 来创建搜索筛选器，以返回**itemindex as**属性中具有与常量值3具有指定关系的值的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-203">The following example shows you how to use the EWS Managed API to create search filters to return all items with a value in the **ItemIndex** property that has the specified relationship to the constant value 3.</span></span> 
  
```cs
// Find all items where the custom property value is > 3.
SearchFilter.IsGreaterThan greaterThanFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
// Find all items where the custom property value is >= 3.
SearchFilter.IsGreaterThanOrEqualTo greaterThanOrEqualFilter =
    new SearchFilter.IsGreaterThanOrEqualTo(customPropDefinition, ItemSchema.Size);
// Find all items where the custom property value is < 3.
SearchFilter.IsLessThan lessThanFilter =
    new SearchFilter.IsLessThan(customPropDefinition, 3);
// Find all items where the custom property value is <= 3.
SearchFilter.IsLessThanOrEqualTo lessThanOrEqualFilter =
    new SearchFilter.IsLessThanOrEqualTo(customPropDefinition, 3);
```

#### <a name="relational-testing-filter-in-ews"></a><span data-ttu-id="abbe9-204">EWS 中的关系测试筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-204">Relational testing filter in EWS</span></span>

<span data-ttu-id="abbe9-205">下面的示例演示如何使用 EWS 创建搜索筛选器，以返回**itemindex as**属性中值大于常量值3的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-205">The following example shows you how to use EWS to create a search filter to return all items with a value in the **ItemIndex** property that is greater than the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

<span data-ttu-id="abbe9-206">下面的示例演示如何创建搜索筛选器，以返回**itemindex as**属性中值大于或等于常量值3的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-206">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is greater than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

<span data-ttu-id="abbe9-207">下面的示例演示如何创建搜索筛选器，以返回**itemindex as**属性中值小于常量值3的所有项。</span><span class="sxs-lookup"><span data-stu-id="abbe9-207">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than the constant value 3.</span></span> 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

<span data-ttu-id="abbe9-208">下面的示例演示如何创建搜索筛选器，以返回**itemindex as**属性中值小于或等于常量值3的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-208">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a><span data-ttu-id="abbe9-209">Negating 筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-209">Negating filter</span></span>

<span data-ttu-id="abbe9-210">通过 negating 筛选器，您可以对其他筛选器取反，并获得相反的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="abbe9-210">A negating filter enables you to negate another filter and get the opposite search results.</span></span> <span data-ttu-id="abbe9-211">虽然其他筛选器返回与特定条件匹配的结果，但 negating 筛选器返回的结果与应用它的筛选器指定的条件不匹配。</span><span class="sxs-lookup"><span data-stu-id="abbe9-211">While other filters return results that match specific criteria, a negating filter returns results that do not match the criteria specified by the filter it is applied to.</span></span>
  
#### <a name="negating-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-212">EWS 托管 API 中的 Negating 筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-212">Negating filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-213">下面的示例演示如何使用 EWS 托管 API 创建搜索筛选器，以返回主题中不包含子字符串 "会议备注" 的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-213">The following example shows you how to use the EWS Managed API to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a><span data-ttu-id="abbe9-214">EWS 中的 Negating 筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-214">Negating filter in EWS</span></span>

<span data-ttu-id="abbe9-215">下面的示例演示如何创建搜索筛选器，以返回主题中不包含子字符串 "会议备注" 的所有项目。</span><span class="sxs-lookup"><span data-stu-id="abbe9-215">The following example shows you how to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a><span data-ttu-id="abbe9-216">复合筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-216">Compound filter</span></span>

<span data-ttu-id="abbe9-217">复合筛选器使您能够组合多个筛选器来创建更复杂的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="abbe9-217">A compound filter enables you to combine multiple filters to create more complex search criteria.</span></span> <span data-ttu-id="abbe9-218">您可以使用逻辑运算符 AND 或 or 来组合条件。</span><span class="sxs-lookup"><span data-stu-id="abbe9-218">You can combine criteria by using the logical operators AND or OR.</span></span> <span data-ttu-id="abbe9-219">通过这种方式，您可以执行搜索，如 "主题中包含 ' 会议便笺 ' 的来自 Sadie Daniels 的所有邮件"。</span><span class="sxs-lookup"><span data-stu-id="abbe9-219">In this way, you can perform searches like "all mail from Sadie Daniels that contains 'meeting notes' in the subject".</span></span>
  
#### <a name="compound-filter-in-the-ews-managed-api"></a><span data-ttu-id="abbe9-220">EWS 托管 API 中的复合筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-220">Compound filter in the EWS Managed API</span></span>

<span data-ttu-id="abbe9-221">下面的示例演示如何使用 EWS 托管 API 创建一个搜索筛选器，该搜索筛选器将返回从 Sadie Daniels 发送的所有项目，并在主题中包含 "会议说明"。</span><span class="sxs-lookup"><span data-stu-id="abbe9-221">The following example shows you how to use the EWS Managed API to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a><span data-ttu-id="abbe9-222">EWS 中的复合筛选器</span><span class="sxs-lookup"><span data-stu-id="abbe9-222">Compound filter in EWS</span></span>

<span data-ttu-id="abbe9-223">下面的示例演示如何使用 EWS 创建搜索筛选器，以返回从 Sadie Daniels 发送的所有项目，并在主题中包含 "会议说明"。</span><span class="sxs-lookup"><span data-stu-id="abbe9-223">The following example shows you how to use EWS to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
```XML
<t:And>
  <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
  <t:IsEqualTo>
    <t:FieldURI FieldURI="message:Sender" />
    <t:FieldURIOrConstant>
      <t:Constant Value="sadie@fourthcoffee.com" />
    </t:FieldURIOrConstant>
  </t:IsEqualTo>
</t:And>
```

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a><span data-ttu-id="abbe9-224">示例：使用搜索筛选器和 EWS 托管 API 查找项目</span><span class="sxs-lookup"><span data-stu-id="abbe9-224">Example: Find items by using a search filter and the EWS Managed API</span></span>
<span data-ttu-id="abbe9-225"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-225"><a name="bk_ExampleEWSMA"> </a></span></span>

<span data-ttu-id="abbe9-226">下面的 EWS 托管 API 方法使用搜索筛选器：</span><span class="sxs-lookup"><span data-stu-id="abbe9-226">The following EWS Managed API methods use search filters:</span></span>
  
- [<span data-ttu-id="abbe9-227">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="abbe9-227">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [<span data-ttu-id="abbe9-228">ExchangeService。 FindFolders</span><span class="sxs-lookup"><span data-stu-id="abbe9-228">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="abbe9-229">FindFolders</span><span class="sxs-lookup"><span data-stu-id="abbe9-229">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="abbe9-230">FindItems</span><span class="sxs-lookup"><span data-stu-id="abbe9-230">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="abbe9-231">下面的示例使用 FindItems 方法; **ExchangeService**但是，相同的规则和概念适用于所有方法。</span><span class="sxs-lookup"><span data-stu-id="abbe9-231">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to all the methods.</span></span> <span data-ttu-id="abbe9-232">在此示例中，定义了一个名为**SearchWithFilter**的方法。</span><span class="sxs-lookup"><span data-stu-id="abbe9-232">In this example, a method called **SearchWithFilter** is defined.</span></span> <span data-ttu-id="abbe9-233">它采用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、 [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象和[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)对象作为参数。</span><span class="sxs-lookup"><span data-stu-id="abbe9-233">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a [SearchFilter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) object as parameters.</span></span> <span data-ttu-id="abbe9-234">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="abbe9-234">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> <span data-ttu-id="abbe9-235">**过滤**类是所有不同搜索筛选器的基类。</span><span class="sxs-lookup"><span data-stu-id="abbe9-235">The **SearchFilter** class is the base class for all the different search filters.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data
private static Guid SearchTestGUID = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
private static ExtendedPropertyDefinition customPropDefinition =
        new ExtendedPropertyDefinition(SearchTestGUID, "ItemIndex", MapiPropertyType.Integer);
static void SearchWithFilter(ExchangeService service, WellKnownFolderName folder, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject, 
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead,
                                       customPropDefinition);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        FindItemsResults<Item> results = service.FindItems(folder, filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item.ExtendedProperties.Count > 0 &&
                 item.ExtendedProperties[0].PropertyDefinition == customPropDefinition)
            {
                Console.WriteLine("Search Index: {0}", item.ExtendedProperties[0].Value);
            }
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="abbe9-236">您可以将此函数与本文示例中所示的任何搜索筛选器结合使用。</span><span class="sxs-lookup"><span data-stu-id="abbe9-236">You can use this function with any of the search filters shown in the examples in this article.</span></span> <span data-ttu-id="abbe9-237">本示例使用复合筛选器从 Sadie Daniels 中返回收件箱中的所有项目，主题中包含 "会议备注"。</span><span class="sxs-lookup"><span data-stu-id="abbe9-237">This example uses a compound filter to return all items in the Inbox from Sadie Daniels with "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, greaterThanFilter);
SearchWithFilter(service, WellKnownFolderName.Inbox, compoundFilter);
```

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a><span data-ttu-id="abbe9-238">示例：使用搜索筛选器和 EWS 查找项目</span><span class="sxs-lookup"><span data-stu-id="abbe9-238">Example: Find an item by using a search filter and EWS</span></span>
<span data-ttu-id="abbe9-239"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-239"><a name="bk_ExampleEWS"> </a></span></span>

<span data-ttu-id="abbe9-240">下面的 EWS 操作使用搜索筛选器：</span><span class="sxs-lookup"><span data-stu-id="abbe9-240">The following EWS operations use search filters:</span></span>
  
- [<span data-ttu-id="abbe9-241">FindFolder</span><span class="sxs-lookup"><span data-stu-id="abbe9-241">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [<span data-ttu-id="abbe9-242">FindItem</span><span class="sxs-lookup"><span data-stu-id="abbe9-242">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="abbe9-243">下面的示例使用**FindItem**操作;但是，相同的规则和概念适用于这两种操作。</span><span class="sxs-lookup"><span data-stu-id="abbe9-243">The following example uses the **FindItem** operation; however, the same rules and concepts apply to both operations.</span></span> <span data-ttu-id="abbe9-244">搜索筛选器包含在 SOAP 请求的[限制](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)元素中。</span><span class="sxs-lookup"><span data-stu-id="abbe9-244">Search filters are contained in the [Restriction](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in SOAP requests.</span></span> <span data-ttu-id="abbe9-245">此示例发送一个 SOAP 请求，该请求等效于前面的 EWS 托管 API 示例中显示的搜索。</span><span class="sxs-lookup"><span data-stu-id="abbe9-245">This example sends a SOAP request that is equivalent to the search that is shown in the preceding EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
          <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
            <t:FieldURI FieldURI="item:Subject" />
            <t:Constant Value="meeting notes" />
          </t:Contains>
          <t:IsEqualTo>
            <t:FieldURI FieldURI="message:Sender" />
            <t:FieldURIOrConstant>
              <t:Constant Value="sadie@contoso.com" />
            </t:FieldURIOrConstant>
          </t:IsEqualTo>
        </t:And>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="abbe9-246">以下示例显示来自服务器的响应，包括搜索结果。</span><span class="sxs-lookup"><span data-stu-id="abbe9-246">The following example shows the response from the server, including the search results.</span></span>
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>5</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting Notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>6</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>7</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="abbe9-247">后续步骤</span><span class="sxs-lookup"><span data-stu-id="abbe9-247">Next steps</span></span>
<span data-ttu-id="abbe9-248"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="abbe9-248"><a name="bk_ExampleEWS"> </a></span></span>

<span data-ttu-id="abbe9-249">现在您已经熟悉了在基本搜索中使用搜索筛选器，您可以继续使用更高级的搜索技术。</span><span class="sxs-lookup"><span data-stu-id="abbe9-249">Now that you're familiar with using search filters in basic searches, you can move on to more advanced search techniques.</span></span>
  
- [<span data-ttu-id="abbe9-250">使用 Exchange 中的 EWS 执行分组搜索</span><span class="sxs-lookup"><span data-stu-id="abbe9-250">Perform grouped searches by using EWS in Exchange</span></span>](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="abbe9-251">使用 Exchange 中的 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="abbe9-251">Perform paged searches by using EWS in Exchange</span></span>](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="abbe9-252">另请参阅</span><span class="sxs-lookup"><span data-stu-id="abbe9-252">See also</span></span>

- [<span data-ttu-id="abbe9-253">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="abbe9-253">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="abbe9-254">在 Exchange 中使用 EWS 执行 AQS 搜索</span><span class="sxs-lookup"><span data-stu-id="abbe9-254">Perform an AQS search by using EWS in Exchange</span></span>](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="abbe9-255">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="abbe9-255">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="abbe9-256">ExchangeService。 FindFolders</span><span class="sxs-lookup"><span data-stu-id="abbe9-256">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="abbe9-257">FindFolders</span><span class="sxs-lookup"><span data-stu-id="abbe9-257">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="abbe9-258">FindItems</span><span class="sxs-lookup"><span data-stu-id="abbe9-258">Folder.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="abbe9-259">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="abbe9-259">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [<span data-ttu-id="abbe9-260">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="abbe9-260">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

