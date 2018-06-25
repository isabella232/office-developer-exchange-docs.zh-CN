---
title: 在 Exchange 中使用 EWS 使用搜索筛选器
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: 了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 的搜索筛选器。
ms.openlocfilehash: 0652c36fd610c2f9dfe22b55323b368997137e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752907"
---
# <a name="use-search-filters-with-ews-in-exchange"></a>在 Exchange 中使用 EWS 使用搜索筛选器

了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 的搜索筛选器。
  
搜索筛选器是表达您的 EWS 托管 API 或 EWS 应用程序中的搜索条件的主要工具。 建议使用搜索筛选器，而不是[查询字符串](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)中，执行下列操作：
  
- 搜索特定属性或一组属性。  
- 使用多个搜索条件进行搜索。
    
搜索筛选器是唯一的选项，如果您执行以下任一操作：
  
- 搜索自定义属性。  
- 执行区分大小写的字符串搜索。  
- 执行前缀或完全匹配字符串搜索。 
- 执行位掩码搜索。
- 搜索的特定属性设置，无论值的项目。
- 搜索文件夹。
- 创建搜索文件夹。
    
## <a name="determine-what-type-of-search-filter-you-need"></a>确定您需要哪种搜索筛选器
<a name="bk_SelectFilter"> </a>

创建搜索筛选器之前，首先确定您需要哪种类型的筛选器。 随着[SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)类 EWS 托管 API 中的后代类中的 ews[限制](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)元素的子元素以及实现的筛选类型。 
  
**表 1。搜索筛选器的类型**

|**筛选器类型**|**EWS 托管 API 类**|**EWS 元素**|**说明**|
|:-----|:-----|:-----|:-----|
|包含筛选器  <br/> |[ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[Contains](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |最佳用于字符串比较筛选器类型。 它允许您控制区分大小写，是否忽略空格，并设置包容模式。  <br/> |
|位掩码筛选器  <br/> |[ExcludesBitmask](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[不包括](http://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |允许您搜索为位掩码的整数属性并仅返回具有对应于指定的位掩码未设置位的结果。  <br/> |
|存在筛选器  <br/> |[Exists](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[Exists](http://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |返回已存在此参数，而不考虑值的指定的属性的所有项。  <br/> |
|相等筛选器  <br/> |[IsEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [IsNotEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[IsEqualTo](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [IsNotEqualTo](http://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |指定常量值或其他属性的值的指定属性的值进行比较，并返回具有相同值 （对于**IsEqualTo**筛选器） 或非同等值 （对于**IsNotEqualTo 的所有项目**筛选器)。  <br/> |
|关系测试筛选器  <br/> |[IsGreaterThan](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [IsGreaterThanOrEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [IsLessThan](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [IsLessThanOrEqualTo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[IsGreaterThan](http://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [IsGreaterThanOrEqualTo](http://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [IsLessThan](http://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [IsLessThanOrEqualTo](http://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |返回到指定的常量值或其他属性的相应关系中具有指定属性的值的所有项。 例如， **IsGreaterThan**筛选器返回的值大于指定值的指定属性中的所有项。  <br/> |
|绝对值的筛选器  <br/> |[not](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[not](http://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |否定的其他筛选器的结果。  <br/> |
|复合筛选器  <br/> |[SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[And](http://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [或](http://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |结合使用多个筛选器，允许更复杂的搜索条件。  <br/> |
   
### <a name="contains-filter"></a>包含筛选器

一个包含筛选器搜索字符串属性的最佳选择。 与包含筛选器，您可以控制方面的字符串匹配，如区分大小写和空白的处理方式，通过设置包容模式和的比较模式。
  
#### <a name="contains-filter-in-the-ews-managed-api"></a>包含 EWS 托管 API 中的筛选器
<a name="bk_ContainsEWSMA"> </a>

如果您正在使用 EWS 托管 API，可以使用[ContainsSubstring](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)类的[ContainmentMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx)属性设置的内嵌模式和使用**的[ComparisonMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx)属性设置的比较模式ContainsSubstring**类。 下面的示例演示如何创建搜索的项目的子字符串主题字段的搜索筛选器"会议笔记"。 本示例不区分大小写，但不会忽略空格。 
  
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

#### <a name="contains-filter-in-ews"></a>包含 EWS 中的筛选器
<a name="bk_ContainsEWSMA"> </a>

Ews，[包含](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx)元素中使用**ContainmentMode**属性设置包容模式和**包含**元素使用**ContainmentComparison**属性设置的比较模式。 下面的示例演示如何创建一个搜索筛选器搜索的项目"会议笔记"的子字符串主题字段。 本示例不区分大小写，但不会忽略空格。 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a>位掩码筛选器

位掩码筛选器可以搜索整数属性为位掩码，并返回结果其中中指定的属性的值未设置特定的位。
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a>EWS 托管 API 中的位掩码筛选器

下面的示例演示如何使用 EWS 托管 API 创建搜索筛选器返回具有**ItemIndex**自定义属性值的所有项目 (中定义[示例： 使用搜索筛选器和 EWS 托管 API 查找项](#bk_ExampleEWSMA)部分在本文中） 的没有设置的第二个位 (在二进制 10)。 
  
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

#### <a name="bitmask-filter-in-ews"></a>EWS 中的位掩码筛选器

下面的示例演示如何使用 EWS 创建搜索筛选器返回具有**ItemIndex**自定义属性值的所有项目 (中定义[示例： 使用搜索筛选器和 EWS 托管 API 查找项](#bk_ExampleEWSMA)本文的一节)没有设置的第二个位 (在二进制 10)。 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a>存在筛选器

存在筛选器允许您搜索具有特定属性设置它们，无论值的项目。
  
#### <a name="exists-filter-in-the-ews-managed-api"></a>存在 EWS 托管 API 中的筛选器

下面的示例演示如何创建搜索筛选器返回**ItemIndex**自定义属性设置的所有项目。 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a>存在 EWS 中的筛选器

下面的示例演示如何创建搜索筛选器返回**ItemIndex**自定义属性设置的所有项目。 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a>相等筛选器

相等筛选器允许您搜索具有特定值等于或不等于特定值的指定属性值的所有项目。 要比较的值可以是常量值或对每个项目的其他属性的值。
  
#### <a name="equality-filter-in-the-ews-managed-api"></a>EWS 托管 API 中的相等筛选器

下面的示例演示如何使用 EWS 托管 API 创建的搜索筛选器返回尚未阅读的所有项目。
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

下面的示例演示如何创建搜索筛选器返回具有值不等于项目的大小的**ItemIndex**属性中的所有项目。 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a>Ews 相等筛选器

下面的示例演示如何使用 EWS 创建搜索筛选器返回尚未阅读的所有项目。
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

下面的示例演示如何创建搜索筛选器返回具有值不等于项目的大小的**ItemIndex**属性中的所有项目。 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a>关系测试筛选器

关系测试筛选器允许您搜索具有值作为的指定属性中的所有项目大于 (\>)、 大于或等于 (\>=)，小于 (\<)，或者小于或等于 (\<=) 指定的值。 要比较的值可以是常量值或对每个项目的其他属性的值。
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a>EWS 托管 API 中的关系测试筛选器

下面的示例演示如何使用 EWS 托管 API 创建搜索筛选器中具有指定的关系的常量值 3 的**ItemIndex**属性返回的值的所有项目。 
  
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

#### <a name="relational-testing-filter-in-ews"></a>EWS 中的关系测试筛选器

下面的示例演示如何使用 EWS 创建大于 3 的常量值的**ItemIndex**属性中返回的值的所有项目的搜索筛选器。 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

下面的示例演示如何创建一个搜索筛选器返回大于或等于常量值 3 的**ItemIndex**属性中的所有项目的值。 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

下面的示例演示如何创建一个搜索筛选器小于常量值 3 的**ItemIndex**属性中返回的值的所有项目。 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

下面的示例演示如何创建一个搜索筛选器中小于或等于常量值 3 的**ItemIndex**属性返回的值的所有项目。 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a>绝对值的筛选器

Negating 筛选器可以否定另一个筛选器和获取相反的搜索结果。 尽管其他筛选器返回与特定条件匹配的结果，negating 筛选器将返回与筛选器应用于指定的条件不匹配的结果。
  
#### <a name="negating-filter-in-the-ews-managed-api"></a>绝对值 EWS 托管 API 中的筛选器

下面的示例演示如何使用 EWS 托管 API 创建的搜索筛选器返回不具有子字符串"会议笔记"主题中的所有项目。
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a>绝对值 EWS 中的筛选器

下面的示例演示如何创建搜索筛选器返回不具有子字符串"会议笔记"主题中的所有项目。
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a>复合筛选器

复合筛选器，可以合并多个筛选器创建更复杂的搜索条件。 您可以使用逻辑运算符组合条件和或 OR。 在这种方式，可以执行搜索，如"来自 Sadie Daniels 包含会议便笺主题中的所有邮件"。
  
#### <a name="compound-filter-in-the-ews-managed-api"></a>EWS 托管 API 中的复合筛选器

下面的示例演示如何使用 EWS 托管 API 创建的搜索筛选器返回 Sadie Daniels 发送的所有项，并且包含主题中的"会议笔记"。
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a>复合 EWS 中的筛选器

下面的示例演示如何使用 EWS 创建返回 Sadie Daniels 发送且包含"会议笔记"主题中的所有项的搜索筛选器。
  
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

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a>示例： 查找项目使用的搜索筛选器和 EWS 托管 API
<a name="bk_ExampleEWSMA"> </a>

以下 EWS 托管 API 方法使用搜索筛选器：
  
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
下面的示例使用**ExchangeService.FindItems**方法;但是，相同的规则和概念适用于所有方法。 本示例中，定义调用**SearchWithFilter**的方法。 它将[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、 [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象和[SearchFilter](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)对象作为参数。 本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。 **SearchFilter**类是所有的不同的搜索筛选器的基类。 
  
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

您可以使用此函数以及任何本文中示例中所示的搜索筛选器。 此示例使用复合筛选器返回的所有项目在收件箱中从 Sadie Daniels 与主题中的"会议笔记"。
  
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

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a>示例： 使用搜索筛选器和 EWS 查找项目
<a name="bk_ExampleEWS"> </a>

以下 EWS 操作使用搜索筛选器：
  
- [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
下面的示例使用**FindItem**操作;但是，相同的规则和概念适用于这两种操作。 搜索筛选器包含 SOAP 请求中的[限制](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)元素中。 本示例将 SOAP 请求，它等效于的搜索的上述 EWS 托管 API 示例所示。 
  
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

下面的示例演示从服务器中，包括搜索结果的响应。
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="next-steps"></a>后续步骤
<a name="bk_ExampleEWS"> </a>

既然您熟悉在基本搜索中使用搜索筛选器，可以将移动到更高级的搜索技术。
  
- [在 Exchange 使用 EWS 执行分组的搜索](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 执行分页的搜索](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)    
- [在 Exchange 使用 EWS 执行 AQS 搜索](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

