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
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 执行 AQS 搜索

了解如何使用 EWS 托管 API 或 EWS 应用程序中的查询字符串和 AQS 进行搜索。
  
查询字符串提供了用于表示搜索条件的[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)的替代方法。 使用查询字符串的最大优势在于，无需指定单个要搜索的属性。 您可以只提供一个值，搜索将应用于项目的所有常用字段。 您还可以使用高级查询语法（AQS）而不是简单值来优化搜索。 但是，在将查询字符串添加到工具箱之前，应注意以下限制： 
  
- **搜索特定属性的功能受限。** 在查询字符串中使用简单值进行搜索时，将对所有索引属性执行搜索。 您可以将搜索限定为特定属性，但可在 AQS 字符串中使用的属性将受到限制。 如果要搜索的属性不是可用于 AQS 的属性之一，请考虑使用搜索筛选器。 
    
- **不搜索自定义属性。** 查询字符串搜索是针对索引执行的，而自定义属性不包含在该索引中。 如果需要搜索自定义属性，请改用搜索筛选器。 
    
- **对字符串搜索的有限控制。** 查询字符串搜索始终忽略大小写，且始终为子字符串搜索。 如果要执行区分大小写、前缀或完全匹配搜索，请使用搜索筛选器。 
    
- **不适用于文件夹或搜索文件夹。** 用于搜索文件夹的 EWS 操作不支持使用查询字符串。 此外，搜索文件夹不支持查询字符串。 在这两种情况下，搜索筛选器都是唯一选项。 
    
## <a name="creating-a-query-string"></a>创建查询字符串
<a name="bk_CreateQueryString"> </a>

EWS 托管 API 和 EWS 中的查询字符串被解释为 AQS 语法的子集。 AQS 字符串由值或关键字/值对组成，由冒号（:) 分隔）。
  
`keyword:value`

如果不使用关键字指定值，将在所有索引属性中搜索值。 如果关键字与值成对出现，则关键字指定用于搜索相应值的属性。
  
**表1。支持的 AQS 关键字**

|**关键字**|**值类型**|**示例**|
|:-----|:-----|:-----|
|subject  <br/> |String  <br/> |subject： project  <br/> |
|body  <br/> |String  <br/> |正文：销售数据  <br/> |
|attachment  <br/> |String  <br/> |附件：报表  <br/> |
|更改为  <br/> |String  <br/> |to： "Sadie Daniels"  <br/> |
|发件人  <br/> |String  <br/> |发件人：希望  <br/> |
|cc  <br/> |String  <br/> |抄送： "Ronnie Sturgis"  <br/> |
|bcc  <br/> |String  <br/> |密件抄送： mack  <br/> |
|participants  <br/> |String  <br/> |参与者： sadie  <br/> |
|“类别”  <br/> |String  <br/> |类别：项目  <br/> |
|importance  <br/> |String  <br/> |importance:high  <br/> |
|kind  <br/> |项目类型  <br/> |种类：会议  <br/> |
|sent  <br/> |日期  <br/> |已发送： 12/10/2013  <br/> |
|received  <br/> |日期  <br/> |已接收：昨天  <br/> |
|hasattachment  <br/> |Boolean  <br/> |有附件： true  <br/> |
|isflagged  <br/> |Boolean  <br/> |isflagged： true  <br/> |
|isread  <br/> |Boolean  <br/> |isread： false  <br/> |
|大小  <br/> |编号  <br/> |大小： \> 5000  <br/> |
   
让我们来看看不同的值类型的工作原理。
  
### <a name="using-a-string-value-type"></a>使用字符串值类型

默认情况下，将字符串值类型搜索为不区分大小写的前缀子字符串搜索。 这意味着搜索主题： project 将匹配以下任何主题： 
  
- 项目会议笔记
    
- 您是否有项目计划？
    
- 12月销售预测
    
您可以通过将字符串括在引号中，将搜索更改为需要整个词而不是匹配的前缀。 搜索主题： "项目" 将消除匹配项列表中的 "12 月销售预测" 值。 请注意，此值仍不区分大小写。 
  
如果在查询字符串中使用多个单词，则匹配要求两个单词都显示在搜索字段中。 例如，搜索主题：项目计划将与以下任何主题匹配： 
  
- 项目计划
    
- 您是否有项目计划？
    
- 请向我发送项目计划
    
- 规划项目里程碑
    
如果将多个单词括在引号中，则会将它们视为一个短语。 搜索主题： "项目计划" 将仅与上一列表中的 "项目计划" 主题相匹配。 
  
### <a name="using-an-item-type-value-type"></a>使用项目类型值类型

您可以将以下项目类型值与**kind**关键字结合使用，以将搜索结果限制为只包含特定类型的项目，例如，电子邮件或会议请求： 
  
- 联系人    
- 文档    
- 电子邮件    
- 传真    
- im （对应于即时消息）    
- 日志    
- 会议（对应于约会和会议请求）    
- 注释    
- 公告    
- RSS 源    
- 任务    
- 语音邮件
    
### <a name="using-a-date-value-type"></a>使用日期值类型

您可以通过多种不同的方式搜索日期值类型。 最简单的是搜索特定日期。 搜索接收时间： 12/11/2013 将返回2013年12月11日收到的所有项目。 但是，也可以不太具体。 搜索接收时间： 12/11 将返回当前年份的12月11日收到的所有项目。 
  
另一种方法是使用月份名称。 您可以使用 received：12月11日、2013或12月11日搜索，以获取与接收的相同结果： 12/11/2013 和 received： 12/11。 您还可以使用 "收到：十二月" 进行搜索，以获取在当年的12月内收到的所有项目。 
  
使用一周中各天的名称也是一个选项。 搜索接收时间：星期二将返回当前周的所有星期二收到的所有项目。 
  
Date 值类型还支持用于相对于当前时间的搜索的一组关键字。 支持以下关键字：
  
- 今天  
- tomorrow
- yesterday
- this week    
- 上个星期    
- 下月    
- 过去一个月    
- 明年
    
也可以将 Date 值类型与大于或小于的关系运算符或指定为 range 运算符的范围进行比较 **。.** 例如，接收时间： \> 11/30/2013，已发送： \> = 昨天，接收时间： 12/1/2013。。今天是所有有效的查询字符串。 
  
### <a name="using-a-boolean-value-type"></a>使用布尔值类型

布尔值类型可以是 "true" 或 "false"。 这些值不区分大小写，因此 isread： false 将产生与 isread： FALSE 相同的结果。
  
### <a name="using-a-number-value-type"></a>使用数字值类型

可以将 Number 值类型搜索为精确匹配，但也可以使用大于或小于的关系运算符搜索它们。 例如，size：10000将仅返回大小正好为10000字节的项目，但 size： \> = 10000 将返回大小大于或等于10000字节的项目。 您还可以使用区域运算符（ **...**）指定一个区域。 例如，大小为： 7000. 8000 将返回大小介于7000和8000之间的项目。 
  
### <a name="using-logical-operators"></a>使用逻辑运算符

查询字符串支持下列逻辑运算符。
  
**表2。支持的逻辑运算符**

|**Operator**|**示例**|
|:-----|:-----|
|AND  <br/> |项目和 from： "Sadie Daniels"  <br/> subject：（项目和计划）  <br/> |
|OR  <br/> |主题：会议或发件人： "期望总额"  <br/> from （"Sadie Daniels" 或 "愿望总额"）  <br/> |
|NOT  <br/> |不是 from： "Ronnie Sturgis"  <br/> 已接收：不是今天  <br/> |
   
请注意，可以使用这些运算符将多个条件联接在一起，或在一个关键字/值对中联接多个值。 但是，在单个关键字/值对中联接多个值时，应使用括号将多个值括起来。 若要了解原因，请考虑从 from： "Sadie Daniels" 或 "愿望总额" 中进行搜索。 此搜索实际上被解释为以下条件：
  
- 项目来自 Sadie Daniels 或
    
- 项目在其任何索引属性中具有短语 "期望总额"。
    
相比之下，从：（"Sadie Daniels" 或 "愿望总额"）解释为： 
  
- 项目来自 Sadie Daniels 或
    
- 物料的期望总额
    
在指定多个条件但不包含逻辑运算符的情况下，默认运算符为和。 例如，"有附件： true subject：项目等效于：附件： true AND subject：项目"。
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>示例：使用查询字符串和 EWS 托管 API 查找项目
<a name="bk_ExampleEWSMA"> </a>

在此示例中，定义了一个名为**SearchWithQueryString**的方法。 它采用一个[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、一个[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象和一个代表查询字符串作为参数的**string**对象。 此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。 
  
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

您可以使用此方法在主题中搜索短语为 "项目计划" 的所有项目，如本例中所示。
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>示例：使用查询字符串和 EWS 查找项目
<a name="bk_ExampleEWS"> </a>

在此示例中，SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求使用主题中的 "项目计划" 一词查找收件箱中的所有项目。 
  
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

以下示例显示来自具有搜索结果的服务器的响应。
  
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

## <a name="see-also"></a>另请参阅

- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)    
- [在 Exchange 中将搜索筛选器与 EWS 结合使用](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService。 FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

