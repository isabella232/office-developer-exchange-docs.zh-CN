---
title: 搜索和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9fa5b836-857e-401d-9450-51e7dbc69104
description: 了解如何使用 EWS 托管 API 或 EWS 在 Exchange 搜索的项目。
ms.openlocfilehash: da24258ba94b842fa97fff92148620344c939f05
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753014"
---
# <a name="search-and-ews-in-exchange"></a>搜索和 Exchange 中的 EWS

了解如何使用 EWS 托管 API 或 EWS 在 Exchange 搜索的项目。
  
这听起来熟悉？ 最后，您刚开始您已拖延周，该项目，您需要有关您的经理发送您在以前的电子邮件周内的项目的信息。 收件箱中有成百上千或许消息的数目。 你是做什么工作的？ 滚动电子邮件扫描每个主题和发件人，直到找到它？ 或者您使用的搜索功能您喜欢的电子邮件客户端中快速零，在您需要哪种产品？
  
搜索无疑任何电子邮件客户端必须功能。 但是，可用于搜索远不止使用户可以搜索其邮箱。 您的应用程序是否需要处理在特定时间范围内的约会？ 也许您需要报告所有任务项目的特定状态，或将用特定的公司名称的所有联系人都移动到另一个文件夹。 搜索可帮助进行所有这些要求。
  
## <a name="search-basics"></a>搜索基础知识
<a name="bk_SearchBasics"> </a>

EWS 托管 API 和 EWS 提供两种基本方法用于指定搜索。 您可以使用[查询字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)或[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)。 所用的方法取决于您的搜索背后用途。
  
**表 1。搜索筛选器和搜索查询方案**

|**如果您希望...**|**使用...**|**备注**|
|:-----|:-----|:-----|
|将搜索限制为特定属性或一组属性  <br/> |搜索筛选器  <br/> |搜索筛选器提供最佳级别的控制哪些要搜索的属性。 虽然查询字符串可以使用高级查询语法 (AQS) 确定目标一组有限的属性，可以指定搜索筛选器的目标任何属性。  <br/> |
|创建具有多个条件的搜索  <br/> |搜索筛选器  <br/> |与搜索筛选器，可以与逻辑混用 And 或 Or，如"主题包含会议便笺和发件人等于 Sadie Daniels'"搜索允许一起加入多个搜索条件。 虽然查询字符串也可以加入多个搜索条件，它们是限制为查询字符串支持的属性集。  <br/> |
|搜索自定义属性  <br/> |搜索筛选器  <br/> |搜索筛选器可以指定自定义属性的目标。 查询字符串不搜索自定义属性。  <br/> |
|执行区分大小写的搜索字符串属性  <br/> |搜索筛选器  <br/> |查询字符串搜索不区分大小写。  <br/> |
|搜索字符串属性时控制包容模式  <br/> |搜索筛选器  <br/> |查询字符串搜索始终是子字符串搜索。 如果您需要以搜索特定前缀，或需要完全匹配，则搜索筛选器是最佳选择。  <br/> |
|搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持搜索文件夹的查询字符串。  <br/> |
|创建搜索文件夹  <br/> |搜索筛选器  <br/> |EWS 不支持的查询字符串创建搜索文件夹。  <br/> |
|搜索所有常用属性  <br/> |查询字符串  <br/> |不包含 AQS 查询字符串将搜索所有常用的属性。 例如，"Mack Chaves"的查询字符串值将返回所有由 Mack Chaves 以及正文或主题中具有"Mack Chaves"的任何邮件发送的邮件。  <br/> |
|构建基于简单的用户输入的搜索  <br/> |查询字符串  <br/> |查询字符串是非常好的选择允许最终用户如何快速搜索通过键入以下内容中的简单的字符串。 由于查询字符串搜索包括所有常用的属性，结果将包含任何项目包含用户的搜索词。  <br/> |
   
### <a name="using-a-search-filter"></a>使用搜索筛选器

搜索筛选器为您提供了各种搜索选项和最大程度的控制如何执行搜索。 您可以使用搜索筛选器执行基本的等价和比较搜索，但也可以在字符串属性的内容中搜索或位掩码比较。
  
例如，您可以通过使用 EWS 托管 API 中的[SearchFilter.ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)类搜索项目的主题的内容。 本示例中，创建的搜索筛选器来搜索子字符串"会议注意，"忽略大小写的主题。 
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

您还可以对自定义属性进行搜索。 本示例中， **ItemIndex**的自定义属性值大于 3 搜索。 
  
```cs
Guid MyAppGuid = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
ExtendedPropertyDefinition customPropDefinition =
    new ExtendedPropertyDefinition(MyAppGuid, "ItemIndex", MapiPropertyType.Integer); 
SearchFilter.IsGreaterThan customPropFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
```

您还可以结合多个搜索筛选器创建更复杂的搜索。 例如，可以通过使用[SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx)类与逻辑 AND 组合以前的两个筛选器。 
  
```cs
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, customPropFilter);
```

### <a name="using-a-query-string"></a>使用查询字符串

查询字符串提供不同的方法来搜索。 您必须对要搜索的字段和使用查询字符串搜索时如何执行搜索较少控制。 不，它是错误 ！ 在某些情况下，您可能想要强制转换宽 net，这样说。
  
例如，您也可以通过使用[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/jj223808%28v=exchg.80%29.aspx) EWS 托管 API 方法搜索"会议笔记"。 
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "meeting notes", view);
```

如果比较结果**SearchFilter.ContainsSubstring**搜索示例前面的此搜索结果，此搜索将包含更多结果。 搜索筛选器搜索将返回此搜索将返回具有主题、 正文和其他字段中的"会议笔记"的项时，有"会议笔记"主题中的项目。 
  
我们来看一下如何可以优化的查询字符串以获取更接近于您的搜索筛选器中看到的结果。 使用 AQS，您可以限制对主题的搜索。
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:meeting notes", view);
```

这是靠近，但结果仍然不完全相同。 使用查询字符串的多个词语，当您将看到匹配项，或即使单词不按顺序指定，即使它们不是彼此相邻。 带有查询字符串"subject： 会议笔记"中，您将获取匹配进行"会议注释"、"会议中的注释"，依此类推。 以便进一步，您可以用双引号括起来，以指示您希望该短语只环绕的搜索词。
  
```cs
FindItemsResults<Item> results = service.FindItems(folder, "subject:\"meeting notes\"", view);
```

## <a name="requesting-specific-properties-in-search-results"></a>在搜索结果中请求特定属性
<a name="bk_RequestSpecific"> </a>

默认情况下，搜索结果将包含符合搜索的项目上的所有属性。 在某些情况下这可能是所需的但在大多数情况下您的应用程序只需要一组不同的属性。 在这种情况下，您应限制了一组属性返回对属性仅应用程序的需求。 在以下示例中，[属性查看](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)类用于限制为主题，返回的属性收到，日期/时间和项的 ID。 
  
```cs
ItemView view = new ItemView(10);
// Creating a new PropertySet with this constructor includes 
// ItemSchema.Id.
view.PropertySet = new PropertySet(ItemSchema.Subject, ItemSchema.DateTimeReceived);
```

## <a name="controlling-search-depth"></a>控制搜索深度
<a name="bk_SearchDepth"> </a>

在视图中设置遍历控制的深度和搜索范围。 
  
**表 2。搜索遍历值**

|**遍历值**|**适用于**|**说明**|
|:-----|:-----|:-----|
|浅  <br/> |项目和文件夹  <br/> |浅表搜索被限制为要搜索的文件夹的直接子级。  <br/> |
|深  <br/> |（仅与搜索文件夹） 项和文件夹  <br/> |深入搜索以递归方式搜索所搜索的文件夹和子文件夹。  <br/> |
|关联  <br/> |项目  <br/> |关联的搜索仅包括相关的项，从要搜索的文件夹。 关联的项目的文件夹中的隐藏的项目。  <br/> |
|带有 SoftDeleted  <br/> |项目和文件夹  <br/> |此遍历类型已被弃用。 带有 SoftDeleted 搜索仅包含项目中的转储程序。 转储程序已由[Recoverable Items Folder](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx(Office.15).aspx) in Exchange Online、 Exchange Online 作为 Office 365 的一部分和版本的 Exchange 启动与 Exchange 2010 取代。  <br/> |
   
## <a name="managing-search-results"></a>管理搜索结果
<a name="bk_ManageSearchResults"> </a>

EWS 托管 API 和 EWS 还允许您更改搜索结果如何返回。 可以使用视图指定在结果中包含哪些属性、 排序结果，和页上的搜索结果仅得到每响应的结果集数。 您还可以通过指定遍历类型分组按特定字段值和控件的深度的搜索结果。 最后，您可以使用搜索文件夹创建新项目到达时动态更新的持久搜索。
  
### <a name="sorting"></a>排序

您可以获取服务器返回排序的结果，可以更加轻松地显示或处理顺序中的项目。 本示例中，将按收到与最新项目正在第一个日期/时间排序结果。
  
```cs
view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
```

### <a name="paging"></a>Paging

当您使用 EWS 托管 API 或 EWS 发送搜索请求时，您可以指定视图大小，用于控制返回的项的最大数目。 但是，在服务器上的匹配您的搜索的项目数可能大于视图大小。 在这种情况下，服务器指示项目可用。 您可以[使用分页重复搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)并获取下一组结果。 
  
例如，您可以发送搜索请求视图大小为 10。 可能会出现在服务器上的 15 项匹配您的搜索，但您只获得的前 10 个，以及指示符 ( [FindItemsResults\<TItem\>。MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx)属性，如果您使用 EWS 托管 API) 的服务器上有更多结果。 您然后可以发送和偏移量为 10，以匹配您的搜索的接下来的 10 项请求相同的搜索。 服务器将返回剩余的五个项目。 
  
**图 1。分页的搜索示例**

![此说明显示分页搜索。初始请求是发送 10  封邮件。第二个请求是发送接下来 10 封邮件。](media/Ex15_Search_PagedSearch.png)
  
### <a name="grouping"></a>分组

 Exchange 使您能够将搜索结果分组依据的特定字段。 这可以帮助拆分到更易于管理设置的搜索结果。 例如，您可以搜索"会议笔记"并按发件人结果进行分组。 下图中所示，则返回的项将分隔成组，所有符合来自合一相同的发件人的条件的项目进行分组，来自另一个组中的另一个发件人的所有匹配项等等。 
  
**图 2。按发件人分组的搜索结果**

![此说明显示根据发件人分组的搜索结果。](media/Ex15_Search_GroupedResults.png)
  
## <a name="search-folders"></a>搜索文件夹
<a name="bk_SearchFolders"> </a>

使用正则搜索中，执行搜索、 结果返回到你的应用程序处理和搜索将不再存在。 搜索文件夹提供一种方法，以使搜索持久。 这是选项非常适合于您知道您需要多次执行的搜索。 而不是重复执行相同的搜索，从而导致服务器评估从头搜索每次时，搜索文件夹使始终打开、 允许服务器以更新现有结果从搜索范围删除或设置为项目添加到搜索。 搜索文件夹操作类似于普通文件夹，它们显示为包含字样项目的文件夹。 不同之处在于，在文件夹中包含的唯一项是那些符合搜索条件的与文件夹关联。 创建搜索文件夹后，您的应用程序可以获取最新搜索结果，只需通过检查该文件夹的内容。
  
创建搜索文件夹是简单，当您掌握了创建搜索筛选器。 在以下示例中，创建搜索文件夹显示主题包含"会议笔记"的所有电子邮件。
  
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

- [在 Exchange 中使用 EWS 使用搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 执行 AQS 搜索](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 执行分页的搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 执行分组的搜索](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 使用搜索文件夹](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [可恢复的项目文件夹](http://technet.microsoft.com/en-us/library/ee364755%28v=exchg.150%29.aspx(Office.15).aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [影响 EWS 的限制策略参数搜索操作](ews-throttling-in-exchange.md#bk_ThrottlingSearch)
    

