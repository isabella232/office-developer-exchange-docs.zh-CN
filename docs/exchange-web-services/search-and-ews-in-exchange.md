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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463832"
---
# <a name="search-and-ews-in-exchange"></a>搜索和交换中的 EWS

了解如何使用 EWS 托管 API 或 EWS 搜索 Exchange 中的项目。

这听起来是不是很熟悉？ 最终，您将开始为每周准备好的项目，并需要您的经理在电子邮件周前向您发送的项目的相关信息。 您的收件箱中有成百上千封邮件。 你是做什么工作的？ 您是否要浏览电子邮件扫描每个主题和发件人，直到找到它？ 您喜欢的电子邮件客户端中的搜索功能是否在您需要的内容中快速零地可用？

搜索可能对任何电子邮件客户端都是必需的功能。 但除了让用户能够搜索其邮箱之外，还可以使用搜索。 您的应用程序是否需要处理特定时间窗口内的约会？ 您可能需要报告具有特定状态的所有任务项目，或将具有特定公司名称的所有联系人移动到其他文件夹。 搜索可帮助满足所有这些要求。

## <a name="search-basics"></a>搜索基础知识
<a name="bk_SearchBasics"> </a>

EWS 托管 API 和 EWS 提供两种用于指定搜索的基本方法。 您可以使用[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)或[查询字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)。 您使用的方法取决于搜索背后的意图。

**表1。搜索筛选器和搜索查询的方案**

|**如果您想要 .。。**|**使用 .。。**|**注释**|
|:-----|:-----|:-----|
|将搜索限制为特定属性或一组属性  <br/> |搜索筛选器  <br/> |搜索筛选器提供了对哪些属性进行搜索的最佳控制级别。 尽管查询字符串可以使用高级查询语法（AQS）以一组有限的属性为目标，但搜索筛选器可以以任何属性为目标。  <br/> |
|使用多个条件创建搜索  <br/> |搜索筛选器  <br/> |使用搜索筛选器，可以将多个搜索条件与逻辑用 and 或 Or 联接在一起，从而允许搜索（如 "subject 包含 ' 会议说明 '" 和 "发件人" 等于 "Sadie Daniels"）。 尽管查询字符串也可以加入多个搜索条件，但它们仅限于查询字符串支持的一组属性。  <br/> |
|搜索自定义属性  <br/> |搜索筛选器  <br/> |搜索筛选器可以设定自定义属性。 查询字符串不搜索自定义属性。  <br/> |
|对字符串属性执行区分大小写的搜索  <br/> |搜索筛选器  <br/> |查询字符串搜索不区分大小写。  <br/> |
|在搜索字符串属性时控制包含模式  <br/> |搜索筛选器  <br/> |查询字符串搜索始终是子字符串搜索。 如果您需要搜索特定的前缀，或需要完全匹配项，则搜索筛选器是最佳选择。  <br/> |
|搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持搜索包含查询字符串的文件夹。  <br/> |
|创建搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持使用查询字符串创建搜索文件夹。  <br/> |
|跨所有常用属性搜索  <br/> |查询字符串  <br/> |不包含 AQS 的查询字符串将在所有常用属性中进行搜索。 例如，查询字符串值 "Mack Chaves" 将返回 Mack Chaves 发送的所有邮件，以及正文或主题中包含 "Mack Chaves" 的所有邮件。  <br/> |
|根据简单的用户输入构建搜索  <br/> |查询字符串  <br/> |查询字符串是允许最终用户通过键入一个简单字符串来执行快速搜索的理想选择。 由于查询字符串搜索包含所有常用的属性，因此结果将包含任何包含用户搜索词的项目。  <br/> |

### <a name="using-a-search-filter"></a>使用搜索筛选器

搜索筛选器为您提供了大量搜索选项，以及对如何执行搜索的最大程度的控制。 您可以使用搜索筛选器执行基本的相等性和比较搜索，但您也可以在字符串属性的内容中进行搜索或执行位掩码比较。

例如，可以使用 EWS 托管 API 中的[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)类搜索项目主题的内容。 在此示例中，将创建搜索筛选器，以搜索主题中的子字符串 "会议备注"，忽略大小写。

```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

您还可以对自定义属性进行搜索。 在此示例中，将在自定义属性**itemindex as**中搜索大于3的值。

```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer);
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

您还可以将多个搜索筛选器组合起来，以创建更复杂的搜索。 例如，可以使用[过滤](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx)类将前两个筛选器与逻辑 AND 组合。

```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>使用查询字符串

查询字符串提供了不同的搜索方法。 您对搜索的字段的控制程度较低，并且您在使用查询字符串搜索时如何执行搜索。 但这不是一件好事！ 在某些情况下，您可能需要转换为较宽的网，以便于讲话。

例如，您可以使用[ExchangeService](https://msdn.microsoft.com/library/jj223808%28v=exchg.80%29.aspx) EWS 托管 API 方法搜索 "会议备注"。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

如果将此搜索的结果与之前的**过滤**搜索示例的结果进行比较，则此搜索将包含更多结果。 搜索筛选器搜索将仅返回主题中包含 "会议备注" 的项目，而此搜索将返回主题、正文和其他域中包含 "会议备注" 的项目。

我们来看看如何优化查询字符串以更接近您从搜索筛选器中看到的结果。 使用 AQS，您可以将搜索限制到主题。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

这一点更接近，但结果仍不完全相同。 当您使用包含多个单词的查询字符串时，将会得到匹配项，即使这些单词的顺序不是您指定的顺序，甚至它们彼此之间并不相邻。 在查询字符串 "subject：会议笔记" 中，您将获得与 "会议备注"、"会议中的笔记" 等的匹配项。 若要进一步优化，可以将搜索词封装在双引号中，以表明您只需要该短语。

```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>在搜索结果中请求特定属性
<a name="bk_RequestSpecific"> </a>

默认情况下，搜索结果将包含与搜索匹配的项目的所有属性。 在某些情况下，这可能是您想要的内容，但在大多数情况下，应用程序只需要一组离散的属性。 在这种情况下，您应该限制仅返回给您的应用程序需要的属性的属性集。 在下面的示例中， [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)类用于将返回的属性限制为主题、收到的日期/时间以及项目的 ID。

```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>控制搜索深度
<a name="bk_SearchDepth"> </a>

设置视图上的遍历控制搜索的深度和范围。

**表2。搜索遍历值**

|**遍历值**|**应用于**|**说明**|
|:-----|:-----|:-----|
|浅  <br/> |项目和文件夹  <br/> |浅表搜索仅限于要搜索的文件夹的子文件夹。  <br/> |
|深  <br/> |项目（仅与搜索文件夹一起使用）和文件夹  <br/> |深度搜索以递归方式搜索要搜索的文件夹和子文件夹。  <br/> |
|相应  <br/> |项目  <br/> |关联的搜索仅包含要搜索的文件夹中的关联项。 关联项是文件夹中的隐藏项。  <br/> |
|SoftDeleted  <br/> |项目和文件夹  <br/> |此遍历类型已被弃用。 SoftDeleted 搜索仅包含转储程序中的项目。 转储程序已替换为 exchange Online 中的 "[可恢复的项目" 文件夹](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)、exchange Online 作为 Office 365 的一部分以及从 exchange 2010 开始的 exchange 版本。  <br/> |

## <a name="managing-search-results"></a>管理搜索结果
<a name="bk_ManageSearchResults"> </a>

EWS 托管 API 和 EWS 还允许您更改搜索结果的返回方式。 您可以使用视图来指定结果中包含哪些属性，对结果进行排序，并将结果分页，使其仅返回每个响应的一组结果数。 您还可以按特定字段值对结果进行分组，并通过指定遍历类型来控制搜索的深度。 最后，您可以使用搜索文件夹创建持久搜索，这些搜索将随着新项目的到达而动态更新。

### <a name="sorting"></a>排序

您可以让服务器返回已排序结果，这样可以更轻松地按顺序显示或处理项目。 在此示例中，将按接收到的日期/时间对结果进行排序，并将最新的项排在最前面。

```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>分页

当您使用 EWS 托管 API 或 EWS 发送搜索请求时，您可以指定视图大小，这将控制返回的最大项目数。 但是，与您的搜索匹配的服务器上的项目数可能大于视图大小。 在这种情况下，服务器指示有更多的可用项目。 您可以[使用分页来重复搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)，并获取下一组结果。

例如，您可以发送视图大小为10的搜索请求。 服务器上可能有15个与您的搜索匹配的项目，但您只会返回前10个和一个指示符（FindItemsResults） [ \<TItem\> 。MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx)属性（如果使用的是 EWS 托管 API）在服务器上有更多结果。 然后，您可以使用偏移量10发送相同的搜索，以询问接下来的10个符合搜索条件的项目。 服务器将返回剩余的五个项目。

**图1。分页搜索示例**

![此说明显示分页搜索。 初始请求是发送 10  封邮件。 第二个请求是发送接下来 10 封邮件。](media/Ex15_Search_PagedSearch.png)

### <a name="grouping"></a>分组

 Exchange 使您能够按特定字段对搜索结果进行分组。 这可帮助将搜索结果分解为更易于管理的集。 例如，您可以搜索 "会议笔记" 并按发件人对结果进行分组。 如下图所示，返回的项目将分成多个组，其中所有项目都与一个组中的同一发件人的条件相匹配，其他组中其他发件人的所有匹配项，等等。

**图2。按发件人分组的搜索结果**

![此说明显示根据发件人分组的搜索结果。](media/Ex15_Search_GroupedResults.png)

## <a name="search-folders"></a>搜索文件夹
<a name="bk_SearchFolders"> </a>

使用常规搜索时，将执行搜索，并将结果返回给您的应用程序进行处理，并且该搜索将不再存在。 搜索文件夹提供了一种使搜索持久的方法。 对于您知道需要多次执行的搜索，这是一个很好的选择。 搜索文件夹将始终打开搜索文件夹，而不是重复执行相同的搜索，从而使服务器每次都从头开始评估搜索，从而允许服务器更新现有结果集，因为在搜索范围中添加或删除项目。 搜索文件夹的作用类似于常规文件夹，因为它们显示为包含项目的文件夹。 区别在于，文件夹中包含的唯一项目是与与该文件夹相关联的搜索条件相匹配的项目。 在创建搜索文件夹之后，您的应用程序可以通过检查该文件夹的内容来获取最新的搜索结果。

创建搜索筛选器时，创建 "搜索文件夹" 非常简单。 在以下示例中，将创建一个搜索文件夹，以显示包含 "会议备注" 的主题的所有电子邮件。

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

- [在 Exchange 中将搜索筛选器与 EWS 结合使用](how-to-use-search-filters-with-ews-in-exchange.md)

- [在 Exchange 中使用 EWS 执行 AQS 搜索](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 执行分页搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 执行分组搜索](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 处理搜索文件夹](how-to-work-with-search-folders-by-using-ews-in-exchange.md)

## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)

- ["可恢复的项目" 文件夹](https://docs.microsoft.com/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder)

- [ExchangeService。 FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)

- [影响 EWS 搜索操作的限制策略参数](ews-throttling-in-exchange.md#throttling-policy-parameters-that-affect-ews-search-operations)
