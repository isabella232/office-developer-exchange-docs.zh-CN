---
title: 搜索和交换中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: 了解如何使用 EWS 托管 API 或 EWS 搜索 Exchange 中的项目。
ms.openlocfilehash: d35cc74ab2fa79530ac09256e315a780023d833b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463832"
---
# <a name="search-and-ews-in-exchange"></a><span data-ttu-id="5f060-103">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="5f060-103">Search and EWS in Exchange</span></span>

<span data-ttu-id="5f060-104">了解如何使用 EWS 托管 API 或 EWS 搜索 Exchange 中的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-104">Find out how to search for items in Exchange by using the EWS Managed API or EWS.</span></span>

<span data-ttu-id="5f060-105">这听起来是不是很熟悉？</span><span class="sxs-lookup"><span data-stu-id="5f060-105">Does this sound familiar?</span></span> <span data-ttu-id="5f060-106">最终，您将开始为每周准备好的项目，并需要您的经理在电子邮件周前向您发送的项目的相关信息。</span><span class="sxs-lookup"><span data-stu-id="5f060-106">You're finally starting that project you've been putting off for weeks, and you need information about the project that your manager sent you in email weeks ago.</span></span> <span data-ttu-id="5f060-107">您的收件箱中有成百上千封邮件。</span><span class="sxs-lookup"><span data-stu-id="5f060-107">Your Inbox has hundreds or perhaps thousands of messages in it.</span></span> <span data-ttu-id="5f060-108">你是做什么工作的？</span><span class="sxs-lookup"><span data-stu-id="5f060-108">What do you do?</span></span> <span data-ttu-id="5f060-109">您是否要浏览电子邮件扫描每个主题和发件人，直到找到它？</span><span class="sxs-lookup"><span data-stu-id="5f060-109">Do you scroll through your email scanning each subject and sender until you find it?</span></span> <span data-ttu-id="5f060-110">您喜欢的电子邮件客户端中的搜索功能是否在您需要的内容中快速零地可用？</span><span class="sxs-lookup"><span data-stu-id="5f060-110">Or do you use the search feature in your favorite email client to quickly zero in on what you need?</span></span>

<span data-ttu-id="5f060-111">搜索可能对任何电子邮件客户端都是必需的功能。</span><span class="sxs-lookup"><span data-stu-id="5f060-111">Search is arguably a must-have feature for any email client.</span></span> <span data-ttu-id="5f060-112">但除了让用户能够搜索其邮箱之外，还可以使用搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-112">But search can be used for a lot more than just enabling users to search their mailbox.</span></span> <span data-ttu-id="5f060-113">您的应用程序是否需要处理特定时间窗口内的约会？</span><span class="sxs-lookup"><span data-stu-id="5f060-113">Does your app need to process appointments that fall within specific time windows?</span></span> <span data-ttu-id="5f060-114">您可能需要报告具有特定状态的所有任务项目，或将具有特定公司名称的所有联系人移动到其他文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-114">Maybe you need to report on all task items with a specific status, or move all contacts with a specific company name to a different folder.</span></span> <span data-ttu-id="5f060-115">搜索可帮助满足所有这些要求。</span><span class="sxs-lookup"><span data-stu-id="5f060-115">Search can help with all of these requirements.</span></span>

## <a name="search-basics"></a><span data-ttu-id="5f060-116">搜索基础知识</span><span class="sxs-lookup"><span data-stu-id="5f060-116">Search basics</span></span>
<span data-ttu-id="5f060-117"><a name="bk_SearchBasics"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-117"><a name="bk_SearchBasics"> </a></span></span>

<span data-ttu-id="5f060-118">EWS 托管 API 和 EWS 提供两种用于指定搜索的基本方法。</span><span class="sxs-lookup"><span data-stu-id="5f060-118">The EWS Managed API and EWS offer two basic methods for specifying a search.</span></span> <span data-ttu-id="5f060-119">您可以使用[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)或[查询字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="5f060-119">You can use a [search filter](how-to-use-search-filters-with-ews-in-exchange.md) or a [query string](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="5f060-120">您使用的方法取决于搜索背后的意图。</span><span class="sxs-lookup"><span data-stu-id="5f060-120">The method you use depends on the intent behind your search.</span></span>

<span data-ttu-id="5f060-121">**表1。搜索筛选器和搜索查询的方案**</span><span class="sxs-lookup"><span data-stu-id="5f060-121">**Table 1. Scenarios for search filters and search queries**</span></span>

|<span data-ttu-id="5f060-122">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="5f060-122">**If you want to…**</span></span>|<span data-ttu-id="5f060-123">**使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="5f060-123">**Use a…**</span></span>|<span data-ttu-id="5f060-124">**备注**</span><span class="sxs-lookup"><span data-stu-id="5f060-124">**Notes**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f060-125">将搜索限制为特定属性或一组属性</span><span class="sxs-lookup"><span data-stu-id="5f060-125">Limit your search to a specific property or set of properties</span></span>  <br/> |<span data-ttu-id="5f060-126">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-126">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-127">搜索筛选器提供了对哪些属性进行搜索的最佳控制级别。</span><span class="sxs-lookup"><span data-stu-id="5f060-127">Search filters provide the best level of control over which properties are searched.</span></span> <span data-ttu-id="5f060-128">尽管查询字符串可以使用高级查询语法（AQS）以一组有限的属性为目标，但搜索筛选器可以以任何属性为目标。</span><span class="sxs-lookup"><span data-stu-id="5f060-128">Although query strings can target a limited set of properties by using Advanced Query Syntax (AQS), search filters can target any property.</span></span>  <br/> |
|<span data-ttu-id="5f060-129">使用多个条件创建搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-129">Create searches with multiple criteria</span></span>  <br/> |<span data-ttu-id="5f060-130">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-130">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-131">使用搜索筛选器，可以将多个搜索条件与逻辑用 and 或 Or 联接在一起，从而允许搜索（如 "subject 包含 ' 会议说明 '" 和 "发件人" 等于 "Sadie Daniels"）。</span><span class="sxs-lookup"><span data-stu-id="5f060-131">With search filters, multiple search criteria can be joined together with logical ANDs or ORs, allowing for searches like "subject contains 'Meeting Notes' AND sender equals 'Sadie Daniels'".</span></span> <span data-ttu-id="5f060-132">尽管查询字符串也可以加入多个搜索条件，但它们仅限于查询字符串支持的一组属性。</span><span class="sxs-lookup"><span data-stu-id="5f060-132">Although query strings can also join multiple search criteria, they are limited to the set of properties supported by query strings.</span></span>  <br/> |
|<span data-ttu-id="5f060-133">搜索自定义属性</span><span class="sxs-lookup"><span data-stu-id="5f060-133">Search custom properties</span></span>  <br/> |<span data-ttu-id="5f060-134">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-134">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-135">搜索筛选器可以设定自定义属性。</span><span class="sxs-lookup"><span data-stu-id="5f060-135">Search filters can target custom properties.</span></span> <span data-ttu-id="5f060-136">查询字符串不搜索自定义属性。</span><span class="sxs-lookup"><span data-stu-id="5f060-136">Query strings do not search custom properties.</span></span>  <br/> |
|<span data-ttu-id="5f060-137">对字符串属性执行区分大小写的搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-137">Perform a case sensitive search of string properties</span></span>  <br/> |<span data-ttu-id="5f060-138">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-138">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-139">查询字符串搜索不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="5f060-139">Query string searches are not case sensitive.</span></span>  <br/> |
|<span data-ttu-id="5f060-140">在搜索字符串属性时控制包含模式</span><span class="sxs-lookup"><span data-stu-id="5f060-140">Control the containment mode when searching string properties</span></span>  <br/> |<span data-ttu-id="5f060-141">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-141">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-142">查询字符串搜索始终是子字符串搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-142">Query string searches are always substring searches.</span></span> <span data-ttu-id="5f060-143">如果您需要搜索特定的前缀，或需要完全匹配项，则搜索筛选器是最佳选择。</span><span class="sxs-lookup"><span data-stu-id="5f060-143">If you need to search for specific prefixes, or require exact matches, a search filter is the best choice.</span></span>  <br/> |
|<span data-ttu-id="5f060-144">搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-144">Search for folders</span></span>  <br/> |<span data-ttu-id="5f060-145">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-145">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-146">EWS 不支持搜索包含查询字符串的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-146">EWS does not support searching for folders with a query string.</span></span>  <br/> |
|<span data-ttu-id="5f060-147">创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-147">Create a search folder</span></span>  <br/> |<span data-ttu-id="5f060-148">搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-148">Search filter</span></span>  <br/> |<span data-ttu-id="5f060-149">EWS 不支持使用查询字符串创建搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-149">EWS does not support creating search folders with a query string.</span></span>  <br/> |
|<span data-ttu-id="5f060-150">跨所有常用属性搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-150">Search across all commonly used properties</span></span>  <br/> |<span data-ttu-id="5f060-151">查询字符串</span><span class="sxs-lookup"><span data-stu-id="5f060-151">Query string</span></span>  <br/> |<span data-ttu-id="5f060-152">不包含 AQS 的查询字符串将在所有常用属性中进行搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-152">Query strings that do not contain AQS will search across all commonly used properties.</span></span> <span data-ttu-id="5f060-153">例如，查询字符串值 "Mack Chaves" 将返回 Mack Chaves 发送的所有邮件，以及正文或主题中包含 "Mack Chaves" 的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="5f060-153">For example, a query string value of "Mack Chaves" will return all messages sent by Mack Chaves as well as any messages that have "Mack Chaves" in the body or subject.</span></span>  <br/> |
|<span data-ttu-id="5f060-154">根据简单的用户输入构建搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-154">Construct a search based on simple user input</span></span>  <br/> |<span data-ttu-id="5f060-155">查询字符串</span><span class="sxs-lookup"><span data-stu-id="5f060-155">Query string</span></span>  <br/> |<span data-ttu-id="5f060-156">查询字符串是允许最终用户通过键入一个简单字符串来执行快速搜索的理想选择。</span><span class="sxs-lookup"><span data-stu-id="5f060-156">A query string is a great choice for allowing an end user to do a quick search by typing in a simple string.</span></span> <span data-ttu-id="5f060-157">由于查询字符串搜索包含所有常用的属性，因此结果将包含任何包含用户搜索词的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-157">Because a query string search includes all commonly used properties, the results will contain any items that contain the user's search terms.</span></span>  <br/> |

### <a name="using-a-search-filter"></a><span data-ttu-id="5f060-158">使用搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="5f060-158">Using a search filter</span></span>

<span data-ttu-id="5f060-159">搜索筛选器为您提供了大量搜索选项，以及对如何执行搜索的最大程度的控制。</span><span class="sxs-lookup"><span data-stu-id="5f060-159">Search filters give you a wide range of search options and the greatest degree of control over how the search is performed.</span></span> <span data-ttu-id="5f060-160">您可以使用搜索筛选器执行基本的相等性和比较搜索，但您也可以在字符串属性的内容中进行搜索或执行位掩码比较。</span><span class="sxs-lookup"><span data-stu-id="5f060-160">You can use search filters to perform basic equality and comparison searches, but you can also search within the contents of string properties or do bitmask comparisons.</span></span>

<span data-ttu-id="5f060-161">例如，可以使用 EWS 托管 API 中的[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)类搜索项目主题的内容。</span><span class="sxs-lookup"><span data-stu-id="5f060-161">For example, you can search the contents of the subject of items by using the [SearchFilter.ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) class in the EWS Managed API.</span></span> <span data-ttu-id="5f060-162">在此示例中，将创建搜索筛选器，以搜索主题中的子字符串 "会议备注"，忽略大小写。</span><span class="sxs-lookup"><span data-stu-id="5f060-162">In this example, a search filter is created to search the subject for the substring "meeting notes", ignoring case.</span></span>

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

<span data-ttu-id="5f060-163">您还可以对自定义属性进行搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-163">You can also search against custom properties.</span></span> <span data-ttu-id="5f060-164">在此示例中，将在自定义属性**itemindex as**中搜索大于3的值。</span><span class="sxs-lookup"><span data-stu-id="5f060-164">In this example, the custom property **ItemIndex** is searched for values greater than 3.</span></span>

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

<span data-ttu-id="5f060-165">您还可以将多个搜索筛选器组合起来，以创建更复杂的搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-165">You can also combine multiple search filters to create more complex searches.</span></span> <span data-ttu-id="5f060-166">例如，可以使用[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx)类将前两个筛选器与逻辑 AND 组合。</span><span class="sxs-lookup"><span data-stu-id="5f060-166">For example, you can combine the previous two filters with a logical AND by using the [SearchFilter.SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) class.</span></span>

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a><span data-ttu-id="5f060-167">使用查询字符串</span><span class="sxs-lookup"><span data-stu-id="5f060-167">Using a query string</span></span>

<span data-ttu-id="5f060-168">查询字符串提供了不同的搜索方法。</span><span class="sxs-lookup"><span data-stu-id="5f060-168">Query strings provide a different approach to search.</span></span> <span data-ttu-id="5f060-169">您对搜索的字段的控制程度较低，并且您在使用查询字符串搜索时如何执行搜索。</span><span class="sxs-lookup"><span data-stu-id="5f060-169">You have less control over the fields that are searched and how the search is performed when you use a query string search.</span></span> <span data-ttu-id="5f060-170">但这不是一件好事！</span><span class="sxs-lookup"><span data-stu-id="5f060-170">Not that that's a bad thing!</span></span> <span data-ttu-id="5f060-171">在某些情况下，您可能需要转换为较宽的网，以便于讲话。</span><span class="sxs-lookup"><span data-stu-id="5f060-171">In some cases, you might want to cast a wider net, so to speak.</span></span>

<span data-ttu-id="5f060-172">例如，您可以使用[ExchangeService](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) EWS 托管 API 方法搜索 "会议备注"。</span><span class="sxs-lookup"><span data-stu-id="5f060-172">For example, you can search for "meeting notes" by using the [ExchangeService.FindItems](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) EWS Managed API method.</span></span>

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

<span data-ttu-id="5f060-173">如果将此搜索的结果与之前的**过滤**搜索示例的结果进行比较，则此搜索将包含更多结果。</span><span class="sxs-lookup"><span data-stu-id="5f060-173">If you compare the results of this search to the results of the **SearchFilter.ContainsSubstring** search example earlier, this search will contain more results.</span></span> <span data-ttu-id="5f060-174">搜索筛选器搜索将仅返回主题中包含 "会议备注" 的项目，而此搜索将返回主题、正文和其他域中包含 "会议备注" 的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-174">The search filter search will return only items that have "meeting notes" in the subject, while this search will return items that have "meeting notes" in the subject, body, and other fields.</span></span>

<span data-ttu-id="5f060-175">我们来看看如何优化查询字符串以更接近您从搜索筛选器中看到的结果。</span><span class="sxs-lookup"><span data-stu-id="5f060-175">Let's take a look at how you can refine the query string to get closer to the results you see from the search filter.</span></span> <span data-ttu-id="5f060-176">使用 AQS，您可以将搜索限制到主题。</span><span class="sxs-lookup"><span data-stu-id="5f060-176">Using AQS, you can limit your search to the subject.</span></span>

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

<span data-ttu-id="5f060-177">这一点更接近，但结果仍不完全相同。</span><span class="sxs-lookup"><span data-stu-id="5f060-177">This is closer, but the results are still not quite the same.</span></span> <span data-ttu-id="5f060-178">当您使用包含多个单词的查询字符串时，将会得到匹配项，即使这些单词的顺序不是您指定的顺序，甚至它们彼此之间并不相邻。</span><span class="sxs-lookup"><span data-stu-id="5f060-178">When you use a query string with multiple words, you will get matches even if the words are not in the order you specify, or even if they're not adjacent to each other.</span></span> <span data-ttu-id="5f060-179">在查询字符串 "subject：会议笔记" 中，您将获得与 "会议备注"、"会议中的笔记" 等的匹配项。</span><span class="sxs-lookup"><span data-stu-id="5f060-179">With the query string "subject:meeting notes", you will get matches for "meeting notes", "notes from the meeting", and so on.</span></span> <span data-ttu-id="5f060-180">若要进一步优化，可以将搜索词封装在双引号中，以表明您只需要该短语。</span><span class="sxs-lookup"><span data-stu-id="5f060-180">To further refine, you can wrap the search terms in double quotes to indicate that you want that phrase only.</span></span>

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a><span data-ttu-id="5f060-181">在搜索结果中请求特定属性</span><span class="sxs-lookup"><span data-stu-id="5f060-181">Requesting specific properties in search results</span></span>
<span data-ttu-id="5f060-182"><a name="bk_RequestSpecific"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-182"><a name="bk_RequestSpecific"> </a></span></span>

<span data-ttu-id="5f060-183">默认情况下，搜索结果将包含与搜索匹配的项目的所有属性。</span><span class="sxs-lookup"><span data-stu-id="5f060-183">By default, search results will contain all properties on the items that match the search.</span></span> <span data-ttu-id="5f060-184">在某些情况下，这可能是您想要的内容，但在大多数情况下，应用程序只需要一组离散的属性。</span><span class="sxs-lookup"><span data-stu-id="5f060-184">In some cases this might be what you want, but in most cases your application only requires a discrete set of properties.</span></span> <span data-ttu-id="5f060-185">在这种情况下，您应该限制仅返回给您的应用程序需要的属性的属性集。</span><span class="sxs-lookup"><span data-stu-id="5f060-185">In this case, you should limit the set of properties that are returned to only the properties your application needs.</span></span> <span data-ttu-id="5f060-186">在下面的示例中， [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)类用于将返回的属性限制为主题、收到的日期/时间以及项目的 ID。</span><span class="sxs-lookup"><span data-stu-id="5f060-186">In the following example, the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) class is used to limit the returned properties to the subject, date/time received, and ID of the items.</span></span>

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a><span data-ttu-id="5f060-187">控制搜索深度</span><span class="sxs-lookup"><span data-stu-id="5f060-187">Controlling search depth</span></span>
<span data-ttu-id="5f060-188"><a name="bk_SearchDepth"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-188"><a name="bk_SearchDepth"> </a></span></span>

<span data-ttu-id="5f060-189">设置视图上的遍历控制搜索的深度和范围。</span><span class="sxs-lookup"><span data-stu-id="5f060-189">Setting the traversal on the view controls the depth and scope of the search.</span></span>

<span data-ttu-id="5f060-190">**表2。搜索遍历值**</span><span class="sxs-lookup"><span data-stu-id="5f060-190">**Table 2. Search traversal values**</span></span>

|<span data-ttu-id="5f060-191">**遍历值**</span><span class="sxs-lookup"><span data-stu-id="5f060-191">**Traversal value**</span></span>|<span data-ttu-id="5f060-192">**应用于**</span><span class="sxs-lookup"><span data-stu-id="5f060-192">**Applies to**</span></span>|<span data-ttu-id="5f060-193">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f060-193">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f060-194">浅</span><span class="sxs-lookup"><span data-stu-id="5f060-194">Shallow</span></span>  <br/> |<span data-ttu-id="5f060-195">项目和文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-195">Items and Folders</span></span>  <br/> |<span data-ttu-id="5f060-196">浅表搜索仅限于要搜索的文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-196">Shallow searches are limited to direct children of the folder being searched.</span></span>  <br/> |
|<span data-ttu-id="5f060-197">深</span><span class="sxs-lookup"><span data-stu-id="5f060-197">Deep</span></span>  <br/> |<span data-ttu-id="5f060-198">项目（仅与搜索文件夹一起使用）和文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-198">Items (only with search folders) and Folders</span></span>  <br/> |<span data-ttu-id="5f060-199">深度搜索以递归方式搜索要搜索的文件夹和子文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-199">Deep searches recursively search the folder being searched and subfolders.</span></span>  <br/> |
|<span data-ttu-id="5f060-200">相应</span><span class="sxs-lookup"><span data-stu-id="5f060-200">Associated</span></span>  <br/> |<span data-ttu-id="5f060-201">项目</span><span class="sxs-lookup"><span data-stu-id="5f060-201">Items</span></span>  <br/> |<span data-ttu-id="5f060-202">关联的搜索仅包含要搜索的文件夹中的关联项。</span><span class="sxs-lookup"><span data-stu-id="5f060-202">Associated searches only include associated items from the folder being searched.</span></span> <span data-ttu-id="5f060-203">关联项是文件夹中的隐藏项。</span><span class="sxs-lookup"><span data-stu-id="5f060-203">Associated items are hidden items within the folder.</span></span>  <br/> |
|<span data-ttu-id="5f060-204">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="5f060-204">SoftDeleted</span></span>  <br/> |<span data-ttu-id="5f060-205">项目和文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-205">Items and Folders</span></span>  <br/> |<span data-ttu-id="5f060-206">此遍历类型已被弃用。</span><span class="sxs-lookup"><span data-stu-id="5f060-206">This traversal type is deprecated.</span></span> <span data-ttu-id="5f060-207">SoftDeleted 搜索仅包含转储程序中的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-207">SoftDeleted searches only include items that are in the dumpster.</span></span> <span data-ttu-id="5f060-208">转储程序已替换为 exchange Online 中的 "[可恢复的项目" 文件夹](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)、exchange Online 作为 Office 365 的一部分以及从 exchange 2010 开始的 exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="5f060-208">The dumpster has been replaced by the [Recoverable Items Folder](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder) in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2010.</span></span>  <br/> |

## <a name="managing-search-results"></a><span data-ttu-id="5f060-209">管理搜索结果</span><span class="sxs-lookup"><span data-stu-id="5f060-209">Managing search results</span></span>
<span data-ttu-id="5f060-210"><a name="bk_ManageSearchResults"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-210"><a name="bk_ManageSearchResults"> </a></span></span>

<span data-ttu-id="5f060-211">EWS 托管 API 和 EWS 还允许您更改搜索结果的返回方式。</span><span class="sxs-lookup"><span data-stu-id="5f060-211">The EWS Managed API and EWS also allow you to change how your search results are returned.</span></span> <span data-ttu-id="5f060-212">您可以使用视图来指定结果中包含哪些属性，对结果进行排序，并将结果分页，使其仅返回每个响应的一组结果数。</span><span class="sxs-lookup"><span data-stu-id="5f060-212">You can use views to specify which properties are included in the results, sort results, and page your results to only get back a set number of results per response.</span></span> <span data-ttu-id="5f060-213">您还可以按特定字段值对结果进行分组，并通过指定遍历类型来控制搜索的深度。</span><span class="sxs-lookup"><span data-stu-id="5f060-213">You can also group results by specific field values and control the depth of a search by specifying a traversal type.</span></span> <span data-ttu-id="5f060-214">最后，您可以使用搜索文件夹创建持久搜索，这些搜索将随着新项目的到达而动态更新。</span><span class="sxs-lookup"><span data-stu-id="5f060-214">Finally, you can use search folders to create persistent searches that are updated dynamically as new items arrive.</span></span>

### <a name="sorting"></a><span data-ttu-id="5f060-215">排序</span><span class="sxs-lookup"><span data-stu-id="5f060-215">Sorting</span></span>

<span data-ttu-id="5f060-216">您可以让服务器返回已排序结果，这样可以更轻松地按顺序显示或处理项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-216">You can get the server to return sorted results, which can make it easier to display or process items in order.</span></span> <span data-ttu-id="5f060-217">在此示例中，将按接收到的日期/时间对结果进行排序，并将最新的项排在最前面。</span><span class="sxs-lookup"><span data-stu-id="5f060-217">In this example, the results will be sorted by the date/time received, with the newest items being first.</span></span>

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a><span data-ttu-id="5f060-218">分页</span><span class="sxs-lookup"><span data-stu-id="5f060-218">Paging</span></span>

<span data-ttu-id="5f060-219">当您使用 EWS 托管 API 或 EWS 发送搜索请求时，您可以指定视图大小，这将控制返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="5f060-219">When you send a search request by using the EWS Managed API or EWS, you specify a view size, which controls the maximum number of items returned.</span></span> <span data-ttu-id="5f060-220">但是，与您的搜索匹配的服务器上的项目数可能大于视图大小。</span><span class="sxs-lookup"><span data-stu-id="5f060-220">However, the number of items on the server that match your search might be larger than the view size.</span></span> <span data-ttu-id="5f060-221">在这种情况下，服务器指示有更多的可用项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-221">In this case, the server indicates that more items are available.</span></span> <span data-ttu-id="5f060-222">您可以[使用分页来重复搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)，并获取下一组结果。</span><span class="sxs-lookup"><span data-stu-id="5f060-222">You can [use paging to repeat your search](how-to-perform-paged-searches-by-using-ews-in-exchange.md) and get the next set of results.</span></span>

<span data-ttu-id="5f060-223">例如，您可以发送视图大小为10的搜索请求。</span><span class="sxs-lookup"><span data-stu-id="5f060-223">For example, you can send a search request with a view size of 10.</span></span> <span data-ttu-id="5f060-224">服务器上可能有15个与您的搜索匹配的项目，但您只会返回前10个和一个指示符（FindItemsResults） [ \<TItem\> 。MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx)属性（如果使用的是 EWS 托管 API）在服务器上有更多结果。</span><span class="sxs-lookup"><span data-stu-id="5f060-224">There might be 15 items on the server that match your search, but you will only get back the first 10, along with an indicator (the [FindItemsResults\<TItem\>.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property if you're using the EWS Managed API) that there are more results on the server.</span></span> <span data-ttu-id="5f060-225">然后，您可以使用偏移量10发送相同的搜索，以询问接下来的10个符合搜索条件的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-225">You can then send the same search with an offset of 10 to ask for the next 10 items that match your search.</span></span> <span data-ttu-id="5f060-226">服务器将返回剩余的五个项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-226">The server will return the remaining five items.</span></span>

<span data-ttu-id="5f060-227">**图1。分页搜索示例**</span><span class="sxs-lookup"><span data-stu-id="5f060-227">**Figure 1. Paged search example**</span></span>

![此说明显示分页搜索。](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a><span data-ttu-id="5f060-231">分组</span><span class="sxs-lookup"><span data-stu-id="5f060-231">Grouping</span></span>

 <span data-ttu-id="5f060-232">Exchange 使您能够按特定字段对搜索结果进行分组。</span><span class="sxs-lookup"><span data-stu-id="5f060-232">Exchange enables you to group search results by a specific field.</span></span> <span data-ttu-id="5f060-233">这可帮助将搜索结果分解为更易于管理的集。</span><span class="sxs-lookup"><span data-stu-id="5f060-233">This can help break up search results into more manageable sets.</span></span> <span data-ttu-id="5f060-234">例如，您可以搜索 "会议笔记" 并按发件人对结果进行分组。</span><span class="sxs-lookup"><span data-stu-id="5f060-234">For example, you can search for "meeting notes" and group the results by sender.</span></span> <span data-ttu-id="5f060-235">如下图所示，返回的项目将分成多个组，其中所有项目都与一个组中的同一发件人的条件相匹配，其他组中其他发件人的所有匹配项，等等。</span><span class="sxs-lookup"><span data-stu-id="5f060-235">As shown in the following figure, the items returned will be separated into groups, with all the items that match the criteria from the same sender in one group, all the matching items from another sender in another group, and so on.</span></span>

<span data-ttu-id="5f060-236">**图2。按发件人分组的搜索结果**</span><span class="sxs-lookup"><span data-stu-id="5f060-236">**Figure 2. Search results grouped by sender**</span></span>

![此说明显示根据发件人分组的搜索结果。](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a><span data-ttu-id="5f060-238">搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-238">Search folders</span></span>
<span data-ttu-id="5f060-239"><a name="bk_SearchFolders"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-239"><a name="bk_SearchFolders"> </a></span></span>

<span data-ttu-id="5f060-240">使用常规搜索时，将执行搜索，并将结果返回给您的应用程序进行处理，并且该搜索将不再存在。</span><span class="sxs-lookup"><span data-stu-id="5f060-240">With a regular search, the search is executed, the results are returned to your application for processing, and the search ceases to exist.</span></span> <span data-ttu-id="5f060-241">搜索文件夹提供了一种使搜索持久的方法。</span><span class="sxs-lookup"><span data-stu-id="5f060-241">Search folders provide a way to make a search persistent.</span></span> <span data-ttu-id="5f060-242">对于您知道需要多次执行的搜索，这是一个很好的选择。</span><span class="sxs-lookup"><span data-stu-id="5f060-242">This is a great option for searches that you know you will want to execute multiple times.</span></span> <span data-ttu-id="5f060-243">搜索文件夹将始终打开搜索文件夹，而不是重复执行相同的搜索，从而使服务器每次都从头开始评估搜索，从而允许服务器更新现有结果集，因为在搜索范围中添加或删除项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-243">Rather than executing the same search repeatedly, causing the server to evaluate the search from scratch each time, a search folder makes a search always on, allowing the server to update the existing result set as items are added to or removed from the search scope.</span></span> <span data-ttu-id="5f060-244">搜索文件夹的作用类似于常规文件夹，因为它们显示为包含项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5f060-244">Search folders act like regular folders, in that they appear as folders that have items in them.</span></span> <span data-ttu-id="5f060-245">区别在于，文件夹中包含的唯一项目是与与该文件夹相关联的搜索条件相匹配的项目。</span><span class="sxs-lookup"><span data-stu-id="5f060-245">The difference is that the only items contained in the folder are those that match the search criteria that are associated with the folder.</span></span> <span data-ttu-id="5f060-246">在创建搜索文件夹之后，您的应用程序可以通过检查该文件夹的内容来获取最新的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="5f060-246">After a search folder is created, your application can get up-to-date results of the search just by checking the contents of the folder.</span></span>

<span data-ttu-id="5f060-247">创建搜索筛选器时，创建 "搜索文件夹" 非常简单。</span><span class="sxs-lookup"><span data-stu-id="5f060-247">Creating a search folder is simple when you've mastered creating search filters.</span></span> <span data-ttu-id="5f060-248">在以下示例中，将创建一个搜索文件夹，以显示包含 "会议备注" 的主题的所有电子邮件。</span><span class="sxs-lookup"><span data-stu-id="5f060-248">In the following example, a search folder is created to show all email with a subject that contains "meeting notes".</span></span>

```cs
static void CreateSearchFolder(ExchangeService service)
{
    SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
        "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "Meeting Notes";
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    searchFolder.SearchParameters.SearchFilter = subjectFilter;
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="in-this-section"></a><span data-ttu-id="5f060-249">本节内容</span><span class="sxs-lookup"><span data-stu-id="5f060-249">In this section</span></span>
<span data-ttu-id="5f060-250"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="5f060-250"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="5f060-251">在 Exchange 中将搜索筛选器与 EWS 结合使用</span><span class="sxs-lookup"><span data-stu-id="5f060-251">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)

- [<span data-ttu-id="5f060-252">在 Exchange 中使用 EWS 执行 AQS 搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-252">Perform an AQS search by using EWS in Exchange</span></span>](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [<span data-ttu-id="5f060-253">使用 Exchange 中的 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-253">Perform paged searches by using EWS in Exchange</span></span>](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [<span data-ttu-id="5f060-254">使用 Exchange 中的 EWS 执行分组搜索</span><span class="sxs-lookup"><span data-stu-id="5f060-254">Perform grouped searches by using EWS in Exchange</span></span>](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [<span data-ttu-id="5f060-255">使用 Exchange 中的 EWS 处理搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-255">Work with search folders by using EWS in Exchange</span></span>](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a><span data-ttu-id="5f060-256">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f060-256">See also</span></span>


- [<span data-ttu-id="5f060-257">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="5f060-257">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)

- [<span data-ttu-id="5f060-258">"可恢复的项目" 文件夹</span><span class="sxs-lookup"><span data-stu-id="5f060-258">Recoverable Items Folder</span></span>](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [<span data-ttu-id="5f060-259">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="5f060-259">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [<span data-ttu-id="5f060-260">影响 EWS 搜索操作的限制策略参数</span><span class="sxs-lookup"><span data-stu-id="5f060-260">Throttling policy parameters that affect EWS search operations</span></span>](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
