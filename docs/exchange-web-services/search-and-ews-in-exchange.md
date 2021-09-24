---
title: 搜索和交换中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: 了解如何使用 EWS 托管 API 或 EWS 在 Exchange中搜索项目。
ms.openlocfilehash: f78f4625880480e4f0d1ebb683c6e7c2c7fa83e0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524432"
---
# <a name="search-and-ews-in-exchange"></a>搜索和交换中的 EWS

了解如何使用 EWS 托管 API 或 EWS 在 Exchange中搜索项目。

这听起来是不是很熟悉？ 你最终会启动已经关闭几周的项目，并且你需要有关你的经理几周前通过电子邮件发送给你的项目的信息。 收件箱中有数百条或数千封邮件。 你是做什么工作的？ 你是否滚动浏览电子邮件，直到找到每个主题和发件人？ 或者，你是否使用最喜爱的电子邮件客户端中的搜索功能快速将所需的内容清零？

搜索可能是任何电子邮件客户端的一项必须拥有的功能。 但是，搜索可以仅用于用户搜索其邮箱。 你的应用是否需要处理属于特定时间窗口的约会？ 也许您需要报告具有特定状态的所有任务项目，或将具有特定公司名称的所有联系人移动到其他文件夹。 搜索可以帮助满足所有这些要求。

## <a name="search-basics"></a>搜索基础知识
<a name="bk_SearchBasics"> </a>

EWS 托管 API 和 EWS 提供了两种用于指定搜索的基本方法。 您可以使用搜索 [筛选器或](how-to-use-search-filters-with-ews-in-exchange.md) 查询 [字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)。 使用的方法取决于搜索背后的意图。

**表 1.搜索筛选器和搜索查询的方案**

|**如果你想要...**|**使用...**|**注意**|
|:-----|:-----|:-----|
|将搜索限制为特定属性或属性集  <br/> |搜索筛选器  <br/> |搜索筛选器提供了对哪些属性进行搜索的最佳级别的控制。 尽管通过使用 AQS 或 AQS 高级查询语法，查询字符串 (有限的一组) ，但搜索筛选器可以定位任何属性。  <br/> |
|创建具有多个条件的搜索  <br/> |搜索筛选器  <br/> |使用搜索筛选器，多个搜索条件可以与逻辑 AND 或 OR 联接，从而允许搜索，如"subject contains 'Meeting Notes' AND sender equals 'Danielie Daniels'"。 虽然查询字符串还可以联接多个搜索条件，但仅限于查询字符串支持的属性集。  <br/> |
|搜索自定义属性  <br/> |搜索筛选器  <br/> |搜索筛选器可以定位自定义属性。 查询字符串不搜索自定义属性。  <br/> |
|对字符串属性执行区分大小写的搜索  <br/> |搜索筛选器  <br/> |查询字符串搜索不区分大小写。  <br/> |
|在搜索字符串属性时控制包含模式  <br/> |搜索筛选器  <br/> |查询字符串搜索始终是子字符串搜索。 如果需要搜索特定前缀或需要完全匹配，则搜索筛选器是最佳选择。  <br/> |
|搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持使用查询字符串搜索文件夹。  <br/> |
|创建搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持使用查询字符串创建搜索文件夹。  <br/> |
|跨所有常用属性搜索  <br/> |查询字符串  <br/> |不包含 AQS 的查询字符串将搜索所有常用属性。 例如，查询字符串值"Mack Chaves"将返回 Mack Chaves 发送的所有邮件，以及正文或主题中具有"Mack Chaves"的所有邮件。  <br/> |
|基于简单的用户输入构造搜索  <br/> |查询字符串  <br/> |查询字符串是允许最终用户通过键入简单字符串进行快速搜索的最佳选择。 由于查询字符串搜索包括所有常用属性，因此结果将包含包含用户搜索词的任何项目。  <br/> |

### <a name="using-a-search-filter"></a>使用搜索筛选器

搜索筛选器为您提供了各种搜索选项，并提供了对搜索执行方式的最大控制。 您可以使用搜索筛选器执行基本相等和比较搜索，但您也可以在字符串属性的内容中搜索或进行位掩码比较。

例如，您可以使用 EWS 托管 API 中的 [SearchFilter.ContainsSubstring](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) 类搜索项目主题的内容。 本示例将创建搜索筛选器，以在主题中搜索子字符串"会议笔记"，忽略大小写。

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

您还可以搜索自定义属性。 本示例中，搜索自定义属性 **ItemIndex，** 查找大于 3 的值。

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

还可以组合多个搜索筛选器来创建更复杂的搜索。 例如，您可以使用 [SearchFilter.SearchFilterCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) 类将前两个筛选器与逻辑 AND 结合使用。

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>使用查询字符串

查询字符串提供了不同的搜索方法。 使用查询字符串搜索时，对搜索的字段以及执行搜索方式的控制较少。 这不是一件坏事！ 在某些情况下，你可能希望转换更宽的网，以便说话。

例如，您可以使用 [ExchangeService.FindItems](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) EWS 托管 API 方法搜索"会议备注"。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

如果将此搜索的结果与之前 **SearchFilter.ContainsSubstring** 搜索示例的结果进行比较，则此搜索将包含更多结果。 搜索筛选器搜索将仅返回主题中具有"会议笔记"的项目，而此搜索将返回主题、正文和其他字段中包含"会议笔记"的项目。

让我们看一下如何优化查询字符串，以更接近从搜索筛选器看到的结果。 使用 AQS，您可以将搜索限制为主题。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

这更接近，但结果仍然不同。 当您将查询字符串与多个单词一同使用时，您将获得匹配项，即使这些词不是按您指定的顺序，或者即使它们不相邻。 使用查询字符串"subject：meeting notes"，您将获得"会议笔记"、"会议备注"等的匹配项。 若要进一步优化，可以使用双引号将搜索词括起来，以指示您仅希望该短语。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>请求搜索结果中的特定属性
<a name="bk_RequestSpecific"> </a>

默认情况下，搜索结果将包含与搜索匹配的项目的所有属性。 在某些情况下，这可能是您所需的，但在大多数情况下，您的应用程序只需要一组离散的属性。 在这种情况下，应该将返回的属性集限制为仅返回应用程序所需的属性。 在下面的示例中 [，ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) 类用于将返回的属性限制为项目的主题、接收日期/时间和 ID。

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>控制搜索深度
<a name="bk_SearchDepth"> </a>

在视图上设置遍历可控制搜索的深度和范围。

**表 2.搜索遍历值**

|**遍历值**|**应用于**|**说明**|
|:-----|:-----|:-----|
|浅  <br/> |项目和文件夹  <br/> |浅表搜索仅限于要搜索的文件夹的直接子项。  <br/> |
|深  <br/> |项目 (文件夹和文件夹) 搜索文件夹  <br/> |深度搜索以递归搜索要搜索的文件夹和子文件夹。  <br/> |
|关联  <br/> |项目  <br/> |关联的搜索仅包括正在搜索的文件夹中的关联项目。 关联的项目是文件夹中的隐藏项目。  <br/> |
|SoftDeleted  <br/> |项目和文件夹  <br/> |此遍历类型已弃用。 SoftDeleted 搜索仅包括垃圾站中的项目。 转储器已被 Exchange Online 中的"[](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)可恢复的项目"文件夹、Exchange Online Office 365 的一部分以及 Exchange 2010 Exchange版本取代。  <br/> |

## <a name="managing-search-results"></a>管理搜索结果
<a name="bk_ManageSearchResults"> </a>

EWS 托管 API 和 EWS 还允许您更改搜索结果的返回方式。 可以使用视图指定结果中包括哪些属性，对结果进行排序，并分页结果，以仅返回每个响应的一组结果。 您还可以按特定字段值对结果进行分组，并指定遍历类型来控制搜索的深度。 最后，可以使用搜索文件夹创建在到达新项时动态更新的持久搜索。

### <a name="sorting"></a>排序

您可以让服务器返回已排序的结果，从而可以更轻松地按序显示或处理项目。 本示例中，将按接收日期/时间对结果进行排序，首先显示最新项目。

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>分页

使用 EWS 托管 API 或 EWS 发送搜索请求时，指定视图大小，该大小控制返回的最大项目数。 但是，服务器上与搜索匹配的项目数可能大于视图大小。 在这种情况下，服务器指示可用的项目更多。 您可以使用 [分页重复搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md) 并获取下一组结果。

例如，您可以发送视图大小为 10 的搜索请求。 服务器上可能有 15 个项目与搜索匹配，但仅返回前 10 项，以及 [FindItemsResults (指示器 \<TItem\> 。MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) 属性（如果你使用的是 EWS 托管 API) 服务器上有更多的结果）。 然后，你可以发送偏移为 10 的相同搜索，以请求接下来的 10 个项目与搜索匹配。 服务器将返回其余五项。

**图 1.分页搜索示例**

![此说明显示分页搜索。初始请求是发送 10  封邮件。第二个请求是发送接下来 10 封邮件。](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>分组

 Exchange允许您按特定字段对搜索结果进行分组。 这可以帮助将搜索结果分为多个可管理集。 例如，可以搜索"会议备注"，然后按发件人对结果进行分组。 如下图所示，返回的项目将分为多个组，其中匹配来自一个组中同一发件人的条件的所有项目，另一个组中另一个发件人的所有匹配项目，等等。

**图 2.按发件人分组的搜索结果**

![此说明显示根据发件人分组的搜索结果。](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>搜索结果文件夹
<a name="bk_SearchFolders"> </a>

通过常规搜索，将执行搜索，将结果返回到应用程序进行处理，搜索将停止存在。 搜索文件夹提供了一种使搜索持久化的方法。 对于你知道要执行多次的搜索，这是一个很好的选择。 搜索文件夹将始终打开搜索，从而允许服务器在向搜索范围添加或删除项目时更新现有 结果集，而不是重复执行相同的搜索，而是使服务器每次从头开始评估搜索。 搜索文件夹的行为与常规文件夹类似，因为它们显示为包含项目的文件夹。 区别在于，文件夹中仅包含符合与该文件夹关联的搜索条件的项目。 创建搜索文件夹后，应用程序只需检查该文件夹的内容，就可以获取最新的搜索结果。

在掌握搜索筛选器的创建过程后，创建搜索文件夹非常简单。 在下面的示例中，将创建一个搜索文件夹，以显示主题中包含"会议笔记"的所有电子邮件。

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

## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [将搜索筛选器与 EWS 一Exchange](how-to-use-search-filters-with-ews-in-exchange.md)

- [使用 EWS 执行 AQS Exchange](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 执行分页搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 执行分组Exchange](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [在搜索文件夹中使用 EWS 处理Exchange](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)

- ["可恢复的项目"文件夹](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [影响 EWS 搜索操作限制策略参数](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
