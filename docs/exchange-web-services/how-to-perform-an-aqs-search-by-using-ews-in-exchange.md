---
title: 在 Exchange 使用 EWS 执行 AQS 搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: 了解如何使用查询字符串和 AQS EWS 托管 API 或 EWS 应用程序中的搜索。
ms.openlocfilehash: dc859e24fa80cd5627477182979c9cc9527818d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752881"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="9c1ba-103">在 Exchange 使用 EWS 执行 AQS 搜索</span><span class="sxs-lookup"><span data-stu-id="9c1ba-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="9c1ba-104">了解如何使用查询字符串和 AQS EWS 托管 API 或 EWS 应用程序中的搜索。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="9c1ba-105">查询字符串提供[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)的替代项来表示搜索条件。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="9c1ba-106">使用查询字符串的最大好处是，您无需指定要搜索的一个属性。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="9c1ba-107">您可以只提供一个值，并搜索将应用于所有常用项目字段。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="9c1ba-108">您可以使用高级查询语法 (AQS) 而不是一个简单的值来改进搜索。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="9c1ba-109">但是，查询字符串具有之前将其添加到工具箱应注意以下限制：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="9c1ba-110">**有限的能够搜索特定属性。**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="9c1ba-111">在搜索查询字符串中的简单值时，搜索是针对所有索引属性执行。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="9c1ba-112">可以优化您搜索与特定的属性，但可使用 AQS 字符串中的所有属性有限。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="9c1ba-113">如果您想要搜索的属性不是一个可供 AQS 属性，请考虑使用的搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="9c1ba-114">**不搜索自定义属性。**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="9c1ba-115">查询字符串搜索索引，针对执行和自定义属性不包括在该索引。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="9c1ba-116">如果您需要搜索自定义属性，请改用的搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="9c1ba-117">**有限的控制字符串搜索。**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-117">**Limited control for string searches.**</span></span> <span data-ttu-id="9c1ba-118">查询字符串搜索始终忽略大小写，并且始终子字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="9c1ba-119">如果您想要执行区分大小写，前缀或完全匹配搜索，将使用的搜索筛选器。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="9c1ba-120">**不可用的文件夹或搜索文件夹。**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="9c1ba-121">搜索文件夹的 EWS 操作不支持使用查询字符串。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="9c1ba-122">此外，搜索文件夹不支持查询字符串。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="9c1ba-123">在这两种情况下，搜索筛选器是唯一的选项。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="9c1ba-124">创建查询字符串</span><span class="sxs-lookup"><span data-stu-id="9c1ba-124">Creating a query string</span></span>
<span data-ttu-id="9c1ba-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="9c1ba-125"></span></span>

<span data-ttu-id="9c1ba-126">EWS 托管 API 和 EWS 中的查询字符串被解释为 AQS 语法的子集。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="9c1ba-127">AQS 字符串组成值或冒号 （:） 分隔的关键字/值对。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="9c1ba-128">没有关键字指定一个值，则值会搜索索引的所有属性。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="9c1ba-129">如果值配对关键字时，关键字指定要搜索的相应值的属性。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="9c1ba-130">**表 1。支持的 AQS 关键字**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="9c1ba-131">**关键字**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-131">**Keyword**</span></span>|<span data-ttu-id="9c1ba-132">**值类型**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-132">**Value type**</span></span>|<span data-ttu-id="9c1ba-133">**示例**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c1ba-134">subject</span><span class="sxs-lookup"><span data-stu-id="9c1ba-134">subject</span></span>  <br/> |<span data-ttu-id="9c1ba-135">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-135">String</span></span>  <br/> |<span data-ttu-id="9c1ba-136">主题： 项目</span><span class="sxs-lookup"><span data-stu-id="9c1ba-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="9c1ba-137">body</span><span class="sxs-lookup"><span data-stu-id="9c1ba-137">body</span></span>  <br/> |<span data-ttu-id="9c1ba-138">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-138">String</span></span>  <br/> |<span data-ttu-id="9c1ba-139">正文： 销售图表</span><span class="sxs-lookup"><span data-stu-id="9c1ba-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="9c1ba-140">附件</span><span class="sxs-lookup"><span data-stu-id="9c1ba-140">attachment</span></span>  <br/> |<span data-ttu-id="9c1ba-141">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-141">String</span></span>  <br/> |<span data-ttu-id="9c1ba-142">附件： 报告</span><span class="sxs-lookup"><span data-stu-id="9c1ba-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="9c1ba-143">更改为</span><span class="sxs-lookup"><span data-stu-id="9c1ba-143">to</span></span>  <br/> |<span data-ttu-id="9c1ba-144">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-144">String</span></span>  <br/> |<span data-ttu-id="9c1ba-145">到:"Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="9c1ba-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="9c1ba-146">发件人</span><span class="sxs-lookup"><span data-stu-id="9c1ba-146">from</span></span>  <br/> |<span data-ttu-id="9c1ba-147">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-147">String</span></span>  <br/> |<span data-ttu-id="9c1ba-148">从： 希望</span><span class="sxs-lookup"><span data-stu-id="9c1ba-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="9c1ba-149">cc</span><span class="sxs-lookup"><span data-stu-id="9c1ba-149">cc</span></span>  <br/> |<span data-ttu-id="9c1ba-150">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-150">String</span></span>  <br/> |<span data-ttu-id="9c1ba-151">抄送:"Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="9c1ba-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="9c1ba-152">bcc</span><span class="sxs-lookup"><span data-stu-id="9c1ba-152">bcc</span></span>  <br/> |<span data-ttu-id="9c1ba-153">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-153">String</span></span>  <br/> |<span data-ttu-id="9c1ba-154">bcc:mack</span><span class="sxs-lookup"><span data-stu-id="9c1ba-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="9c1ba-155">participants</span><span class="sxs-lookup"><span data-stu-id="9c1ba-155">participants</span></span>  <br/> |<span data-ttu-id="9c1ba-156">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-156">String</span></span>  <br/> |<span data-ttu-id="9c1ba-157">参与者： sadie</span><span class="sxs-lookup"><span data-stu-id="9c1ba-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="9c1ba-158">category</span><span class="sxs-lookup"><span data-stu-id="9c1ba-158">category</span></span>  <br/> |<span data-ttu-id="9c1ba-159">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-159">String</span></span>  <br/> |<span data-ttu-id="9c1ba-160">类别： 项目</span><span class="sxs-lookup"><span data-stu-id="9c1ba-160">category:project</span></span>  <br/> |
|<span data-ttu-id="9c1ba-161">importance</span><span class="sxs-lookup"><span data-stu-id="9c1ba-161">importance</span></span>  <br/> |<span data-ttu-id="9c1ba-162">String</span><span class="sxs-lookup"><span data-stu-id="9c1ba-162">String</span></span>  <br/> |<span data-ttu-id="9c1ba-163">高重要性：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="9c1ba-164">类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-164">kind</span></span>  <br/> |<span data-ttu-id="9c1ba-165">项目类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-165">Item type</span></span>  <br/> |<span data-ttu-id="9c1ba-166">类型： 会议</span><span class="sxs-lookup"><span data-stu-id="9c1ba-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="9c1ba-167">发送</span><span class="sxs-lookup"><span data-stu-id="9c1ba-167">sent</span></span>  <br/> |<span data-ttu-id="9c1ba-168">日期</span><span class="sxs-lookup"><span data-stu-id="9c1ba-168">Date</span></span>  <br/> |<span data-ttu-id="9c1ba-169">发送： 12/10/2013年</span><span class="sxs-lookup"><span data-stu-id="9c1ba-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="9c1ba-170">接收</span><span class="sxs-lookup"><span data-stu-id="9c1ba-170">received</span></span>  <br/> |<span data-ttu-id="9c1ba-171">日期</span><span class="sxs-lookup"><span data-stu-id="9c1ba-171">Date</span></span>  <br/> |<span data-ttu-id="9c1ba-172">接收： 昨天</span><span class="sxs-lookup"><span data-stu-id="9c1ba-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="9c1ba-173">hasattachment</span><span class="sxs-lookup"><span data-stu-id="9c1ba-173">hasattachment</span></span>  <br/> |<span data-ttu-id="9c1ba-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c1ba-174">Boolean</span></span>  <br/> |<span data-ttu-id="9c1ba-175">具有附件： true</span><span class="sxs-lookup"><span data-stu-id="9c1ba-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="9c1ba-176">isflagged</span><span class="sxs-lookup"><span data-stu-id="9c1ba-176">isflagged</span></span>  <br/> |<span data-ttu-id="9c1ba-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c1ba-177">Boolean</span></span>  <br/> |<span data-ttu-id="9c1ba-178">isflagged:true</span><span class="sxs-lookup"><span data-stu-id="9c1ba-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="9c1ba-179">isread</span><span class="sxs-lookup"><span data-stu-id="9c1ba-179">isread</span></span>  <br/> |<span data-ttu-id="9c1ba-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="9c1ba-180">Boolean</span></span>  <br/> |<span data-ttu-id="9c1ba-181">isread:false</span><span class="sxs-lookup"><span data-stu-id="9c1ba-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="9c1ba-182">size</span><span class="sxs-lookup"><span data-stu-id="9c1ba-182">size</span></span>  <br/> |<span data-ttu-id="9c1ba-183">数字</span><span class="sxs-lookup"><span data-stu-id="9c1ba-183">Number</span></span>  <br/> |<span data-ttu-id="9c1ba-184">大小：\>5000</span><span class="sxs-lookup"><span data-stu-id="9c1ba-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="9c1ba-185">我们来看看不同的值类型的工作方式。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="9c1ba-186">使用字符串值类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-186">Using a string value type</span></span>

<span data-ttu-id="9c1ba-187">默认情况下不区分大小写的前缀子字符串搜索作为搜索是字符串值类型。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="9c1ba-188">这意味着，搜索主题： 项目不匹配任何以下主题：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="9c1ba-189">项目会议笔记</span><span class="sxs-lookup"><span data-stu-id="9c1ba-189">Project meeting notes</span></span>
    
- <span data-ttu-id="9c1ba-190">您是否有项目计划？</span><span class="sxs-lookup"><span data-stu-id="9c1ba-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="9c1ba-191">12 月销售计划</span><span class="sxs-lookup"><span data-stu-id="9c1ba-191">December sales projections</span></span>
    
<span data-ttu-id="9c1ba-192">您可以更改搜索需要通过括在引号的字符串的全字而不是匹配的前缀。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="9c1ba-193">主题的搜索:"项目"将不再匹配项的列表中的"年 12 月销售预测"值。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="9c1ba-194">请注意，则仍不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="9c1ba-195">如果您在查询字符串中使用多个单词，匹配将需要两个词出现在搜索字段。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="9c1ba-196">例如，搜索主题： 项目计划不匹配任何以下主题：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="9c1ba-197">项目计划</span><span class="sxs-lookup"><span data-stu-id="9c1ba-197">Project plan</span></span>
    
- <span data-ttu-id="9c1ba-198">您是否有项目计划？</span><span class="sxs-lookup"><span data-stu-id="9c1ba-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="9c1ba-199">请向我发送我们的项目的计划</span><span class="sxs-lookup"><span data-stu-id="9c1ba-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="9c1ba-200">规划项目里程碑</span><span class="sxs-lookup"><span data-stu-id="9c1ba-200">Planning project milestones</span></span>
    
<span data-ttu-id="9c1ba-201">如果将多个单词括在引号内，将被视为一个短语。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="9c1ba-202">主题的搜索:"项目计划"可以仅匹配前一列表的"项目计划"主题。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="9c1ba-203">使用项目类型的值类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-203">Using an item type value type</span></span>

<span data-ttu-id="9c1ba-204">可以用**类型**关键字使用的以下项目类型的值限制为特定类型的项目，如电子邮件或会议请求搜索结果：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="9c1ba-205">contacts</span><span class="sxs-lookup"><span data-stu-id="9c1ba-205">contacts</span></span>    
- <span data-ttu-id="9c1ba-206">文档</span><span class="sxs-lookup"><span data-stu-id="9c1ba-206">docs</span></span>    
- <span data-ttu-id="9c1ba-207">email</span><span class="sxs-lookup"><span data-stu-id="9c1ba-207">email</span></span>    
- <span data-ttu-id="9c1ba-208">传真</span><span class="sxs-lookup"><span data-stu-id="9c1ba-208">faxes</span></span>    
- <span data-ttu-id="9c1ba-209">im （对应于即时消息）</span><span class="sxs-lookup"><span data-stu-id="9c1ba-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="9c1ba-210">日志</span><span class="sxs-lookup"><span data-stu-id="9c1ba-210">journals</span></span>    
- <span data-ttu-id="9c1ba-211">会议 (对应于约会和会议请求)</span><span class="sxs-lookup"><span data-stu-id="9c1ba-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="9c1ba-212">notes</span><span class="sxs-lookup"><span data-stu-id="9c1ba-212">notes</span></span>    
- <span data-ttu-id="9c1ba-213">posts</span><span class="sxs-lookup"><span data-stu-id="9c1ba-213">posts</span></span>    
- <span data-ttu-id="9c1ba-214">rssfeeds</span><span class="sxs-lookup"><span data-stu-id="9c1ba-214">rssfeeds</span></span>    
- <span data-ttu-id="9c1ba-215">tasks</span><span class="sxs-lookup"><span data-stu-id="9c1ba-215">tasks</span></span>    
- <span data-ttu-id="9c1ba-216">语音邮件</span><span class="sxs-lookup"><span data-stu-id="9c1ba-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="9c1ba-217">使用日期值类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-217">Using a date value type</span></span>

<span data-ttu-id="9c1ba-218">您可以通过多种不同的方式搜索日期值类型。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="9c1ba-219">简单的方法是搜索特定日期。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="9c1ba-220">搜索与收到： 12/11/2013年将返回在 2013 年 12 月 11 日上收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="9c1ba-221">但是，您也可以是宽泛。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-221">However, you can also be less specific.</span></span> <span data-ttu-id="9c1ba-222">搜索与收到： 12/11 将返回年 12 月 11 当前上收到的所有项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="9c1ba-223">另一种选择是使用月份名称。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-223">Another option is to use the month names.</span></span> <span data-ttu-id="9c1ba-224">您可以搜索接收： 2013 年 12 月 11 日或年 12 月 11 收到获取相同的结果： 12/11/2013年和已接收： 12/11，分别。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="9c1ba-225">您还可以搜索与收到： 年 12 月即可接收在十二月，将当前年份内的所有项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="9c1ba-226">使用每周的星期几的名称也是一个选项。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="9c1ba-227">搜索与收到： 星期二将返回收到星期二本周的所有项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="9c1ba-228">日期值类型还支持一组关键字搜索相对于当前时间。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="9c1ba-229">支持以下关键字：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="9c1ba-230">今天</span><span class="sxs-lookup"><span data-stu-id="9c1ba-230">today</span></span>  
- <span data-ttu-id="9c1ba-231">tomorrow</span><span class="sxs-lookup"><span data-stu-id="9c1ba-231">tomorrow</span></span>
- <span data-ttu-id="9c1ba-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="9c1ba-232">yesterday</span></span>
- <span data-ttu-id="9c1ba-233">this week</span><span class="sxs-lookup"><span data-stu-id="9c1ba-233">this week</span></span>    
- <span data-ttu-id="9c1ba-234">上个星期</span><span class="sxs-lookup"><span data-stu-id="9c1ba-234">last week</span></span>    
- <span data-ttu-id="9c1ba-235">下个月</span><span class="sxs-lookup"><span data-stu-id="9c1ba-235">next month</span></span>    
- <span data-ttu-id="9c1ba-236">过去的月</span><span class="sxs-lookup"><span data-stu-id="9c1ba-236">past month</span></span>    
- <span data-ttu-id="9c1ba-237">明年</span><span class="sxs-lookup"><span data-stu-id="9c1ba-237">coming year</span></span>
    
<span data-ttu-id="9c1ba-238">此外可以与大于或更少的关系运算符比较日期值类型比，或指定范围运算符 **.** 区域。例如，接收：\>11/30/2013年发送：\>昨天、 = 和 received:12/1/2013..today 均为有效的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="9c1ba-239">使用布尔值类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-239">Using a Boolean value type</span></span>

<span data-ttu-id="9c1ba-240">布尔值类型可以是"true"或"false"。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="9c1ba-241">值不是区分大小写，因此 isread:false 将产生 isread:FALSE 相同的结果。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="9c1ba-242">使用数字值类型</span><span class="sxs-lookup"><span data-stu-id="9c1ba-242">Using a number value type</span></span>

<span data-ttu-id="9c1ba-243">可以将数字值类型搜索为完全匹配，但他们还可搜索使用关系运算符类似大于或小于比。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="9c1ba-244">例如，大小： 10000 将返回的大小为完全 10000 个字节，但大小的项目：\>= 10000 将返回具有大小大于或等于 10000 字节的项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="9c1ba-245">您可以通过使用区域运算符 （ **.**） 来指定范围。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="9c1ba-246">例如，大小： 7000..8000 将返回具有 7000 和 8000 之间的大小的项。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="9c1ba-247">使用逻辑运算符</span><span class="sxs-lookup"><span data-stu-id="9c1ba-247">Using logical operators</span></span>

<span data-ttu-id="9c1ba-248">查询字符串支持下列逻辑运算符。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="9c1ba-249">**表 2。受支持的逻辑运算符**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="9c1ba-250">**运算符**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-250">**Operator**</span></span>|<span data-ttu-id="9c1ba-251">**示例**</span><span class="sxs-lookup"><span data-stu-id="9c1ba-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c1ba-252">AND</span><span class="sxs-lookup"><span data-stu-id="9c1ba-252">AND</span></span>  <br/> |<span data-ttu-id="9c1ba-253">项目以及从:"Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="9c1ba-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="9c1ba-254">主题:(project AND plan)</span><span class="sxs-lookup"><span data-stu-id="9c1ba-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="9c1ba-255">OR</span><span class="sxs-lookup"><span data-stu-id="9c1ba-255">OR</span></span>  <br/> |<span data-ttu-id="9c1ba-256">主题： 会议或从:"跃点总数计价"</span><span class="sxs-lookup"><span data-stu-id="9c1ba-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="9c1ba-257">从: ("Sadie Daniels"或者"希望总数计价")</span><span class="sxs-lookup"><span data-stu-id="9c1ba-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="9c1ba-258">NOT</span><span class="sxs-lookup"><span data-stu-id="9c1ba-258">NOT</span></span>  <br/> |<span data-ttu-id="9c1ba-259">并非来自:"Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="9c1ba-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="9c1ba-260">接收： 不是今天</span><span class="sxs-lookup"><span data-stu-id="9c1ba-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="9c1ba-261">请注意，您可以使用这些运算符一起加入多个条件或一起加入内单个关键字/值对多个值。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="9c1ba-262">但是，当加入多个值中的单个关键字/值对，您应使用括号括在一起的多个值。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="9c1ba-263">若要了解原因，请考虑从与搜索:"Sadie Daniels"或者"总跃点"。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="9c1ba-264">实际上，此搜索被解释为以下条件：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="9c1ba-265">该项目是从 Sadie Daniels、 OR</span><span class="sxs-lookup"><span data-stu-id="9c1ba-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="9c1ba-266">项目中的任何索引属性包含短语"跃点总数计价"。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="9c1ba-267">相比之下，从: ("Sadie Daniels"或者"跃点总数计价") 将被解释为：</span><span class="sxs-lookup"><span data-stu-id="9c1ba-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="9c1ba-268">该项目是从 Sadie Daniels、 OR</span><span class="sxs-lookup"><span data-stu-id="9c1ba-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="9c1ba-269">该项目是从跃点总数计价</span><span class="sxs-lookup"><span data-stu-id="9c1ba-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="9c1ba-270">默认运算符时指定多个条件，但没有逻辑运算符包含是成和。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="9c1ba-271">例如，具有附件： true 等效具有主题： 项目： 附件： true 和主题： 项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="9c1ba-272">示例： 通过查询字符串和 EWS 托管 API 查找项目</span><span class="sxs-lookup"><span data-stu-id="9c1ba-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="9c1ba-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="9c1ba-273"></span></span>

<span data-ttu-id="9c1ba-274">本示例中，定义调用**SearchWithQueryString**的方法。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="9c1ba-275">计[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和[WellKnownFolderName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象，表示作为参数的查询字符串的**字符串**对象。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-275">It takes an [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="9c1ba-276">本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="9c1ba-277">可以使用此方法来搜索与短语主题中的"项目计划"的所有项此例中所示。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="9c1ba-278">示例： 使用查询字符串和 EWS 查找项目</span><span class="sxs-lookup"><span data-stu-id="9c1ba-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="9c1ba-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="9c1ba-279"></span></span>

<span data-ttu-id="9c1ba-280">本示例中，SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求在与短语主题中的"项目计划"收件箱中查找所有项目。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-280">In this example, a SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="9c1ba-281">下面的示例演示从搜索结果的服务器的响应。</span><span class="sxs-lookup"><span data-stu-id="9c1ba-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="9c1ba-282">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c1ba-282">See also</span></span>

- [<span data-ttu-id="9c1ba-283">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="9c1ba-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="9c1ba-284">在 Exchange 中使用 EWS 使用搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="9c1ba-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="9c1ba-285">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="9c1ba-285">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="9c1ba-286">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="9c1ba-286">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

