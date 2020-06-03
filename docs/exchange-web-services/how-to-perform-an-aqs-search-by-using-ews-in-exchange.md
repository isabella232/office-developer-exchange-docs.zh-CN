---
title: 在 Exchange 中使用 EWS 执行 AQS 搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: 了解如何使用 EWS 托管 API 或 EWS 应用程序中的查询字符串和 AQS 进行搜索。
localization_priority: Priority
ms.openlocfilehash: 9f611a8d90c6baf0f307897735c6366c82bb63c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455714"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="3b2bf-103">在 Exchange 中使用 EWS 执行 AQS 搜索</span><span class="sxs-lookup"><span data-stu-id="3b2bf-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="3b2bf-104">了解如何使用 EWS 托管 API 或 EWS 应用程序中的查询字符串和 AQS 进行搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="3b2bf-105">查询字符串提供了用于表示搜索条件的[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)的替代方法。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="3b2bf-106">使用查询字符串的最大优势在于，无需指定单个要搜索的属性。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="3b2bf-107">您可以只提供一个值，搜索将应用于项目的所有常用字段。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="3b2bf-108">您还可以使用高级查询语法（AQS）而不是简单值来优化搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="3b2bf-109">但是，在将查询字符串添加到工具箱之前，应注意以下限制：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="3b2bf-110">**搜索特定属性的功能受限。**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="3b2bf-111">在查询字符串中使用简单值进行搜索时，将对所有索引属性执行搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="3b2bf-112">您可以将搜索限定为特定属性，但可在 AQS 字符串中使用的属性将受到限制。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="3b2bf-113">如果要搜索的属性不是可用于 AQS 的属性之一，请考虑使用搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="3b2bf-114">**不搜索自定义属性。**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="3b2bf-115">查询字符串搜索是针对索引执行的，而自定义属性不包含在该索引中。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="3b2bf-116">如果需要搜索自定义属性，请改用搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="3b2bf-117">**对字符串搜索的有限控制。**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-117">**Limited control for string searches.**</span></span> <span data-ttu-id="3b2bf-118">查询字符串搜索始终忽略大小写，且始终为子字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="3b2bf-119">如果要执行区分大小写、前缀或完全匹配搜索，请使用搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="3b2bf-120">**不适用于文件夹或搜索文件夹。**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="3b2bf-121">用于搜索文件夹的 EWS 操作不支持使用查询字符串。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="3b2bf-122">此外，搜索文件夹不支持查询字符串。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="3b2bf-123">在这两种情况下，搜索筛选器都是唯一选项。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="3b2bf-124">创建查询字符串</span><span class="sxs-lookup"><span data-stu-id="3b2bf-124">Creating a query string</span></span>
<span data-ttu-id="3b2bf-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="3b2bf-125"><a name="bk_CreateQueryString"> </a></span></span>

<span data-ttu-id="3b2bf-126">EWS 托管 API 和 EWS 中的查询字符串被解释为 AQS 语法的子集。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="3b2bf-127">AQS 字符串由值或关键字/值对组成，由冒号（:) 分隔）。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="3b2bf-128">如果不使用关键字指定值，将在所有索引属性中搜索值。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="3b2bf-129">如果关键字与值成对出现，则关键字指定用于搜索相应值的属性。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="3b2bf-130">**表1。支持的 AQS 关键字**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="3b2bf-131">**关键字**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-131">**Keyword**</span></span>|<span data-ttu-id="3b2bf-132">**值类型**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-132">**Value type**</span></span>|<span data-ttu-id="3b2bf-133">**示例**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b2bf-134">subject</span><span class="sxs-lookup"><span data-stu-id="3b2bf-134">subject</span></span>  <br/> |<span data-ttu-id="3b2bf-135">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-135">String</span></span>  <br/> |<span data-ttu-id="3b2bf-136">subject： project</span><span class="sxs-lookup"><span data-stu-id="3b2bf-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="3b2bf-137">body</span><span class="sxs-lookup"><span data-stu-id="3b2bf-137">body</span></span>  <br/> |<span data-ttu-id="3b2bf-138">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-138">String</span></span>  <br/> |<span data-ttu-id="3b2bf-139">正文：销售数据</span><span class="sxs-lookup"><span data-stu-id="3b2bf-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="3b2bf-140">attachment</span><span class="sxs-lookup"><span data-stu-id="3b2bf-140">attachment</span></span>  <br/> |<span data-ttu-id="3b2bf-141">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-141">String</span></span>  <br/> |<span data-ttu-id="3b2bf-142">附件：报表</span><span class="sxs-lookup"><span data-stu-id="3b2bf-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="3b2bf-143">更改为</span><span class="sxs-lookup"><span data-stu-id="3b2bf-143">to</span></span>  <br/> |<span data-ttu-id="3b2bf-144">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-144">String</span></span>  <br/> |<span data-ttu-id="3b2bf-145">to： "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="3b2bf-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="3b2bf-146">发件人</span><span class="sxs-lookup"><span data-stu-id="3b2bf-146">from</span></span>  <br/> |<span data-ttu-id="3b2bf-147">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-147">String</span></span>  <br/> |<span data-ttu-id="3b2bf-148">发件人：希望</span><span class="sxs-lookup"><span data-stu-id="3b2bf-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="3b2bf-149">cc</span><span class="sxs-lookup"><span data-stu-id="3b2bf-149">cc</span></span>  <br/> |<span data-ttu-id="3b2bf-150">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-150">String</span></span>  <br/> |<span data-ttu-id="3b2bf-151">抄送： "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="3b2bf-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="3b2bf-152">bcc</span><span class="sxs-lookup"><span data-stu-id="3b2bf-152">bcc</span></span>  <br/> |<span data-ttu-id="3b2bf-153">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-153">String</span></span>  <br/> |<span data-ttu-id="3b2bf-154">密件抄送： mack</span><span class="sxs-lookup"><span data-stu-id="3b2bf-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="3b2bf-155">participants</span><span class="sxs-lookup"><span data-stu-id="3b2bf-155">participants</span></span>  <br/> |<span data-ttu-id="3b2bf-156">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-156">String</span></span>  <br/> |<span data-ttu-id="3b2bf-157">参与者： sadie</span><span class="sxs-lookup"><span data-stu-id="3b2bf-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="3b2bf-158">“类别”</span><span class="sxs-lookup"><span data-stu-id="3b2bf-158">category</span></span>  <br/> |<span data-ttu-id="3b2bf-159">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-159">String</span></span>  <br/> |<span data-ttu-id="3b2bf-160">类别：项目</span><span class="sxs-lookup"><span data-stu-id="3b2bf-160">category:project</span></span>  <br/> |
|<span data-ttu-id="3b2bf-161">importance</span><span class="sxs-lookup"><span data-stu-id="3b2bf-161">importance</span></span>  <br/> |<span data-ttu-id="3b2bf-162">String</span><span class="sxs-lookup"><span data-stu-id="3b2bf-162">String</span></span>  <br/> |<span data-ttu-id="3b2bf-163">importance:high</span><span class="sxs-lookup"><span data-stu-id="3b2bf-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="3b2bf-164">kind</span><span class="sxs-lookup"><span data-stu-id="3b2bf-164">kind</span></span>  <br/> |<span data-ttu-id="3b2bf-165">项目类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-165">Item type</span></span>  <br/> |<span data-ttu-id="3b2bf-166">种类：会议</span><span class="sxs-lookup"><span data-stu-id="3b2bf-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="3b2bf-167">sent</span><span class="sxs-lookup"><span data-stu-id="3b2bf-167">sent</span></span>  <br/> |<span data-ttu-id="3b2bf-168">日期</span><span class="sxs-lookup"><span data-stu-id="3b2bf-168">Date</span></span>  <br/> |<span data-ttu-id="3b2bf-169">已发送： 12/10/2013</span><span class="sxs-lookup"><span data-stu-id="3b2bf-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="3b2bf-170">received</span><span class="sxs-lookup"><span data-stu-id="3b2bf-170">received</span></span>  <br/> |<span data-ttu-id="3b2bf-171">日期</span><span class="sxs-lookup"><span data-stu-id="3b2bf-171">Date</span></span>  <br/> |<span data-ttu-id="3b2bf-172">已接收：昨天</span><span class="sxs-lookup"><span data-stu-id="3b2bf-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="3b2bf-173">hasattachment</span><span class="sxs-lookup"><span data-stu-id="3b2bf-173">hasattachment</span></span>  <br/> |<span data-ttu-id="3b2bf-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="3b2bf-174">Boolean</span></span>  <br/> |<span data-ttu-id="3b2bf-175">有附件： true</span><span class="sxs-lookup"><span data-stu-id="3b2bf-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="3b2bf-176">isflagged</span><span class="sxs-lookup"><span data-stu-id="3b2bf-176">isflagged</span></span>  <br/> |<span data-ttu-id="3b2bf-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="3b2bf-177">Boolean</span></span>  <br/> |<span data-ttu-id="3b2bf-178">isflagged： true</span><span class="sxs-lookup"><span data-stu-id="3b2bf-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="3b2bf-179">isread</span><span class="sxs-lookup"><span data-stu-id="3b2bf-179">isread</span></span>  <br/> |<span data-ttu-id="3b2bf-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="3b2bf-180">Boolean</span></span>  <br/> |<span data-ttu-id="3b2bf-181">isread： false</span><span class="sxs-lookup"><span data-stu-id="3b2bf-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="3b2bf-182">大小</span><span class="sxs-lookup"><span data-stu-id="3b2bf-182">size</span></span>  <br/> |<span data-ttu-id="3b2bf-183">编号</span><span class="sxs-lookup"><span data-stu-id="3b2bf-183">Number</span></span>  <br/> |<span data-ttu-id="3b2bf-184">大小： \> 5000</span><span class="sxs-lookup"><span data-stu-id="3b2bf-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="3b2bf-185">让我们来看看不同的值类型的工作原理。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="3b2bf-186">使用字符串值类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-186">Using a string value type</span></span>

<span data-ttu-id="3b2bf-187">默认情况下，将字符串值类型搜索为不区分大小写的前缀子字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="3b2bf-188">这意味着搜索主题： project 将匹配以下任何主题：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="3b2bf-189">项目会议笔记</span><span class="sxs-lookup"><span data-stu-id="3b2bf-189">Project meeting notes</span></span>
    
- <span data-ttu-id="3b2bf-190">您是否有项目计划？</span><span class="sxs-lookup"><span data-stu-id="3b2bf-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="3b2bf-191">12月销售预测</span><span class="sxs-lookup"><span data-stu-id="3b2bf-191">December sales projections</span></span>
    
<span data-ttu-id="3b2bf-192">您可以通过将字符串括在引号中，将搜索更改为需要整个词而不是匹配的前缀。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="3b2bf-193">搜索主题： "项目" 将消除匹配项列表中的 "12 月销售预测" 值。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="3b2bf-194">请注意，此值仍不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="3b2bf-195">如果在查询字符串中使用多个单词，则匹配要求两个单词都显示在搜索字段中。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="3b2bf-196">例如，搜索主题：项目计划将与以下任何主题匹配：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="3b2bf-197">项目计划</span><span class="sxs-lookup"><span data-stu-id="3b2bf-197">Project plan</span></span>
    
- <span data-ttu-id="3b2bf-198">您是否有项目计划？</span><span class="sxs-lookup"><span data-stu-id="3b2bf-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="3b2bf-199">请向我发送项目计划</span><span class="sxs-lookup"><span data-stu-id="3b2bf-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="3b2bf-200">规划项目里程碑</span><span class="sxs-lookup"><span data-stu-id="3b2bf-200">Planning project milestones</span></span>
    
<span data-ttu-id="3b2bf-201">如果将多个单词括在引号中，则会将它们视为一个短语。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="3b2bf-202">搜索主题： "项目计划" 将仅与上一列表中的 "项目计划" 主题相匹配。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="3b2bf-203">使用项目类型值类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-203">Using an item type value type</span></span>

<span data-ttu-id="3b2bf-204">您可以将以下项目类型值与**kind**关键字结合使用，以将搜索结果限制为只包含特定类型的项目，例如，电子邮件或会议请求：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="3b2bf-205">联系人</span><span class="sxs-lookup"><span data-stu-id="3b2bf-205">contacts</span></span>    
- <span data-ttu-id="3b2bf-206">文档</span><span class="sxs-lookup"><span data-stu-id="3b2bf-206">docs</span></span>    
- <span data-ttu-id="3b2bf-207">电子邮件</span><span class="sxs-lookup"><span data-stu-id="3b2bf-207">email</span></span>    
- <span data-ttu-id="3b2bf-208">传真</span><span class="sxs-lookup"><span data-stu-id="3b2bf-208">faxes</span></span>    
- <span data-ttu-id="3b2bf-209">im （对应于即时消息）</span><span class="sxs-lookup"><span data-stu-id="3b2bf-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="3b2bf-210">日志</span><span class="sxs-lookup"><span data-stu-id="3b2bf-210">journals</span></span>    
- <span data-ttu-id="3b2bf-211">会议（对应于约会和会议请求）</span><span class="sxs-lookup"><span data-stu-id="3b2bf-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="3b2bf-212">注释</span><span class="sxs-lookup"><span data-stu-id="3b2bf-212">notes</span></span>    
- <span data-ttu-id="3b2bf-213">公告</span><span class="sxs-lookup"><span data-stu-id="3b2bf-213">posts</span></span>    
- <span data-ttu-id="3b2bf-214">RSS 源</span><span class="sxs-lookup"><span data-stu-id="3b2bf-214">rssfeeds</span></span>    
- <span data-ttu-id="3b2bf-215">任务</span><span class="sxs-lookup"><span data-stu-id="3b2bf-215">tasks</span></span>    
- <span data-ttu-id="3b2bf-216">语音邮件</span><span class="sxs-lookup"><span data-stu-id="3b2bf-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="3b2bf-217">使用日期值类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-217">Using a date value type</span></span>

<span data-ttu-id="3b2bf-218">您可以通过多种不同的方式搜索日期值类型。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="3b2bf-219">最简单的是搜索特定日期。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="3b2bf-220">搜索接收时间： 12/11/2013 将返回2013年12月11日收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="3b2bf-221">但是，也可以不太具体。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-221">However, you can also be less specific.</span></span> <span data-ttu-id="3b2bf-222">搜索接收时间： 12/11 将返回当前年份的12月11日收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="3b2bf-223">另一种方法是使用月份名称。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-223">Another option is to use the month names.</span></span> <span data-ttu-id="3b2bf-224">您可以使用 received：12月11日、2013或12月11日搜索，以获取与接收的相同结果： 12/11/2013 和 received： 12/11。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="3b2bf-225">您还可以使用 "收到：十二月" 进行搜索，以获取在当年的12月内收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="3b2bf-226">使用一周中各天的名称也是一个选项。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="3b2bf-227">搜索接收时间：星期二将返回当前周的所有星期二收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="3b2bf-228">Date 值类型还支持用于相对于当前时间的搜索的一组关键字。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="3b2bf-229">支持以下关键字：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="3b2bf-230">今天</span><span class="sxs-lookup"><span data-stu-id="3b2bf-230">today</span></span>  
- <span data-ttu-id="3b2bf-231">tomorrow</span><span class="sxs-lookup"><span data-stu-id="3b2bf-231">tomorrow</span></span>
- <span data-ttu-id="3b2bf-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="3b2bf-232">yesterday</span></span>
- <span data-ttu-id="3b2bf-233">this week</span><span class="sxs-lookup"><span data-stu-id="3b2bf-233">this week</span></span>    
- <span data-ttu-id="3b2bf-234">上个星期</span><span class="sxs-lookup"><span data-stu-id="3b2bf-234">last week</span></span>    
- <span data-ttu-id="3b2bf-235">下月</span><span class="sxs-lookup"><span data-stu-id="3b2bf-235">next month</span></span>    
- <span data-ttu-id="3b2bf-236">过去一个月</span><span class="sxs-lookup"><span data-stu-id="3b2bf-236">past month</span></span>    
- <span data-ttu-id="3b2bf-237">明年</span><span class="sxs-lookup"><span data-stu-id="3b2bf-237">coming year</span></span>
    
<span data-ttu-id="3b2bf-238">也可以将 Date 值类型与大于或小于的关系运算符或指定为 range 运算符的范围进行比较 **。.** 例如，接收时间： \> 11/30/2013，已发送： \> = 昨天，接收时间： 12/1/2013。。今天是所有有效的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="3b2bf-239">使用布尔值类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-239">Using a Boolean value type</span></span>

<span data-ttu-id="3b2bf-240">布尔值类型可以是 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="3b2bf-241">这些值不区分大小写，因此 isread： false 将产生与 isread： FALSE 相同的结果。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="3b2bf-242">使用数字值类型</span><span class="sxs-lookup"><span data-stu-id="3b2bf-242">Using a number value type</span></span>

<span data-ttu-id="3b2bf-243">可以将 Number 值类型搜索为精确匹配，但也可以使用大于或小于的关系运算符搜索它们。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="3b2bf-244">例如，size：10000将仅返回大小正好为10000字节的项目，但 size： \> = 10000 将返回大小大于或等于10000字节的项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="3b2bf-245">您还可以使用区域运算符（ **...**）指定一个区域。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="3b2bf-246">例如，大小为： 7000. 8000 将返回大小介于7000和8000之间的项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="3b2bf-247">使用逻辑运算符</span><span class="sxs-lookup"><span data-stu-id="3b2bf-247">Using logical operators</span></span>

<span data-ttu-id="3b2bf-248">查询字符串支持下列逻辑运算符。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="3b2bf-249">**表2。支持的逻辑运算符**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="3b2bf-250">**Operator**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-250">**Operator**</span></span>|<span data-ttu-id="3b2bf-251">**示例**</span><span class="sxs-lookup"><span data-stu-id="3b2bf-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b2bf-252">AND</span><span class="sxs-lookup"><span data-stu-id="3b2bf-252">AND</span></span>  <br/> |<span data-ttu-id="3b2bf-253">项目和 from： "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="3b2bf-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="3b2bf-254">subject：（项目和计划）</span><span class="sxs-lookup"><span data-stu-id="3b2bf-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="3b2bf-255">OR</span><span class="sxs-lookup"><span data-stu-id="3b2bf-255">OR</span></span>  <br/> |<span data-ttu-id="3b2bf-256">主题：会议或发件人： "期望总额"</span><span class="sxs-lookup"><span data-stu-id="3b2bf-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="3b2bf-257">from （"Sadie Daniels" 或 "愿望总额"）</span><span class="sxs-lookup"><span data-stu-id="3b2bf-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="3b2bf-258">NOT</span><span class="sxs-lookup"><span data-stu-id="3b2bf-258">NOT</span></span>  <br/> |<span data-ttu-id="3b2bf-259">不是 from： "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="3b2bf-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="3b2bf-260">已接收：不是今天</span><span class="sxs-lookup"><span data-stu-id="3b2bf-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="3b2bf-261">请注意，可以使用这些运算符将多个条件联接在一起，或在一个关键字/值对中联接多个值。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="3b2bf-262">但是，在单个关键字/值对中联接多个值时，应使用括号将多个值括起来。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="3b2bf-263">若要了解原因，请考虑从 from： "Sadie Daniels" 或 "愿望总额" 中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="3b2bf-264">此搜索实际上被解释为以下条件：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="3b2bf-265">项目来自 Sadie Daniels 或</span><span class="sxs-lookup"><span data-stu-id="3b2bf-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="3b2bf-266">项目在其任何索引属性中具有短语 "期望总额"。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="3b2bf-267">相比之下，从：（"Sadie Daniels" 或 "愿望总额"）解释为：</span><span class="sxs-lookup"><span data-stu-id="3b2bf-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="3b2bf-268">项目来自 Sadie Daniels 或</span><span class="sxs-lookup"><span data-stu-id="3b2bf-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="3b2bf-269">物料的期望总额</span><span class="sxs-lookup"><span data-stu-id="3b2bf-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="3b2bf-270">在指定多个条件但不包含逻辑运算符的情况下，默认运算符为和。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="3b2bf-271">例如，"有附件： true subject：项目等效于：附件： true AND subject：项目"。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="3b2bf-272">示例：使用查询字符串和 EWS 托管 API 查找项目</span><span class="sxs-lookup"><span data-stu-id="3b2bf-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="3b2bf-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="3b2bf-273"><a name="bk_ExampleEWSMA"> </a></span></span>

<span data-ttu-id="3b2bf-274">在此示例中，定义了一个名为**SearchWithQueryString**的方法。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="3b2bf-275">它采用一个[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、一个[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象和一个代表查询字符串作为参数的**string**对象。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-275">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="3b2bf-276">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
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

<span data-ttu-id="3b2bf-277">您可以使用此方法在主题中搜索短语为 "项目计划" 的所有项目，如本例中所示。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="3b2bf-278">示例：使用查询字符串和 EWS 查找项目</span><span class="sxs-lookup"><span data-stu-id="3b2bf-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="3b2bf-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="3b2bf-279"><a name="bk_ExampleEWS"> </a></span></span>

<span data-ttu-id="3b2bf-280">在此示例中，SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求使用主题中的 "项目计划" 一词查找收件箱中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-280">In this example, a SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
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
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3b2bf-281">以下示例显示来自具有搜索结果的服务器的响应。</span><span class="sxs-lookup"><span data-stu-id="3b2bf-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="3b2bf-282">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3b2bf-282">See also</span></span>

- [<span data-ttu-id="3b2bf-283">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="3b2bf-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="3b2bf-284">在 Exchange 中将搜索筛选器与 EWS 结合使用</span><span class="sxs-lookup"><span data-stu-id="3b2bf-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="3b2bf-285">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="3b2bf-285">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="3b2bf-286">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="3b2bf-286">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

