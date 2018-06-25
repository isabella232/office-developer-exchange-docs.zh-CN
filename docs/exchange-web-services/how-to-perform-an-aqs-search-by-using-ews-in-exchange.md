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
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 执行 AQS 搜索

了解如何使用查询字符串和 AQS EWS 托管 API 或 EWS 应用程序中的搜索。
  
查询字符串提供[搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)的替代项来表示搜索条件。 使用查询字符串的最大好处是，您无需指定要搜索的一个属性。 您可以只提供一个值，并搜索将应用于所有常用项目字段。 您可以使用高级查询语法 (AQS) 而不是一个简单的值来改进搜索。 但是，查询字符串具有之前将其添加到工具箱应注意以下限制： 
  
- **有限的能够搜索特定属性。** 在搜索查询字符串中的简单值时，搜索是针对所有索引属性执行。 可以优化您搜索与特定的属性，但可使用 AQS 字符串中的所有属性有限。 如果您想要搜索的属性不是一个可供 AQS 属性，请考虑使用的搜索筛选器。 
    
- **不搜索自定义属性。** 查询字符串搜索索引，针对执行和自定义属性不包括在该索引。 如果您需要搜索自定义属性，请改用的搜索筛选器。 
    
- **有限的控制字符串搜索。** 查询字符串搜索始终忽略大小写，并且始终子字符串搜索。 如果您想要执行区分大小写，前缀或完全匹配搜索，将使用的搜索筛选器。 
    
- **不可用的文件夹或搜索文件夹。** 搜索文件夹的 EWS 操作不支持使用查询字符串。 此外，搜索文件夹不支持查询字符串。 在这两种情况下，搜索筛选器是唯一的选项。 
    
## <a name="creating-a-query-string"></a>创建查询字符串
<a name="bk_CreateQueryString"> </a>

EWS 托管 API 和 EWS 中的查询字符串被解释为 AQS 语法的子集。 AQS 字符串组成值或冒号 （:） 分隔的关键字/值对。
  
`keyword:value`

没有关键字指定一个值，则值会搜索索引的所有属性。 如果值配对关键字时，关键字指定要搜索的相应值的属性。
  
**表 1。支持的 AQS 关键字**

|**关键字**|**值类型**|**示例**|
|:-----|:-----|:-----|
|subject  <br/> |String  <br/> |主题： 项目  <br/> |
|body  <br/> |String  <br/> |正文： 销售图表  <br/> |
|附件  <br/> |String  <br/> |附件： 报告  <br/> |
|更改为  <br/> |String  <br/> |到:"Sadie Daniels"  <br/> |
|发件人  <br/> |String  <br/> |从： 希望  <br/> |
|cc  <br/> |String  <br/> |抄送:"Ronnie Sturgis"  <br/> |
|bcc  <br/> |String  <br/> |bcc:mack  <br/> |
|participants  <br/> |String  <br/> |参与者： sadie  <br/> |
|category  <br/> |String  <br/> |类别： 项目  <br/> |
|importance  <br/> |String  <br/> |高重要性：  <br/> |
|类型  <br/> |项目类型  <br/> |类型： 会议  <br/> |
|发送  <br/> |日期  <br/> |发送： 12/10/2013年  <br/> |
|接收  <br/> |日期  <br/> |接收： 昨天  <br/> |
|hasattachment  <br/> |Boolean  <br/> |具有附件： true  <br/> |
|isflagged  <br/> |Boolean  <br/> |isflagged:true  <br/> |
|isread  <br/> |Boolean  <br/> |isread:false  <br/> |
|size  <br/> |数字  <br/> |大小：\>5000  <br/> |
   
我们来看看不同的值类型的工作方式。
  
### <a name="using-a-string-value-type"></a>使用字符串值类型

默认情况下不区分大小写的前缀子字符串搜索作为搜索是字符串值类型。 这意味着，搜索主题： 项目不匹配任何以下主题： 
  
- 项目会议笔记
    
- 您是否有项目计划？
    
- 12 月销售计划
    
您可以更改搜索需要通过括在引号的字符串的全字而不是匹配的前缀。 主题的搜索:"项目"将不再匹配项的列表中的"年 12 月销售预测"值。 请注意，则仍不区分大小写。 
  
如果您在查询字符串中使用多个单词，匹配将需要两个词出现在搜索字段。 例如，搜索主题： 项目计划不匹配任何以下主题： 
  
- 项目计划
    
- 您是否有项目计划？
    
- 请向我发送我们的项目的计划
    
- 规划项目里程碑
    
如果将多个单词括在引号内，将被视为一个短语。 主题的搜索:"项目计划"可以仅匹配前一列表的"项目计划"主题。 
  
### <a name="using-an-item-type-value-type"></a>使用项目类型的值类型

可以用**类型**关键字使用的以下项目类型的值限制为特定类型的项目，如电子邮件或会议请求搜索结果： 
  
- contacts    
- 文档    
- email    
- 传真    
- im （对应于即时消息）    
- 日志    
- 会议 (对应于约会和会议请求)    
- notes    
- posts    
- rssfeeds    
- tasks    
- 语音邮件
    
### <a name="using-a-date-value-type"></a>使用日期值类型

您可以通过多种不同的方式搜索日期值类型。 简单的方法是搜索特定日期。 搜索与收到： 12/11/2013年将返回在 2013 年 12 月 11 日上收到的所有项目。 但是，您也可以是宽泛。 搜索与收到： 12/11 将返回年 12 月 11 当前上收到的所有项目。 
  
另一种选择是使用月份名称。 您可以搜索接收： 2013 年 12 月 11 日或年 12 月 11 收到获取相同的结果： 12/11/2013年和已接收： 12/11，分别。 您还可以搜索与收到： 年 12 月即可接收在十二月，将当前年份内的所有项目。 
  
使用每周的星期几的名称也是一个选项。 搜索与收到： 星期二将返回收到星期二本周的所有项目。 
  
日期值类型还支持一组关键字搜索相对于当前时间。 支持以下关键字：
  
- 今天  
- tomorrow
- yesterday
- this week    
- 上个星期    
- 下个月    
- 过去的月    
- 明年
    
此外可以与大于或更少的关系运算符比较日期值类型比，或指定范围运算符 **.** 区域。例如，接收：\>11/30/2013年发送：\>昨天、 = 和 received:12/1/2013..today 均为有效的查询字符串。 
  
### <a name="using-a-boolean-value-type"></a>使用布尔值类型

布尔值类型可以是"true"或"false"。 值不是区分大小写，因此 isread:false 将产生 isread:FALSE 相同的结果。
  
### <a name="using-a-number-value-type"></a>使用数字值类型

可以将数字值类型搜索为完全匹配，但他们还可搜索使用关系运算符类似大于或小于比。 例如，大小： 10000 将返回的大小为完全 10000 个字节，但大小的项目：\>= 10000 将返回具有大小大于或等于 10000 字节的项目。 您可以通过使用区域运算符 （ **.**） 来指定范围。 例如，大小： 7000..8000 将返回具有 7000 和 8000 之间的大小的项。 
  
### <a name="using-logical-operators"></a>使用逻辑运算符

查询字符串支持下列逻辑运算符。
  
**表 2。受支持的逻辑运算符**

|**运算符**|**示例**|
|:-----|:-----|
|AND  <br/> |项目以及从:"Sadie Daniels"  <br/> 主题:(project AND plan)  <br/> |
|OR  <br/> |主题： 会议或从:"跃点总数计价"  <br/> 从: ("Sadie Daniels"或者"希望总数计价")  <br/> |
|NOT  <br/> |并非来自:"Ronnie Sturgis"  <br/> 接收： 不是今天  <br/> |
   
请注意，您可以使用这些运算符一起加入多个条件或一起加入内单个关键字/值对多个值。 但是，当加入多个值中的单个关键字/值对，您应使用括号括在一起的多个值。 若要了解原因，请考虑从与搜索:"Sadie Daniels"或者"总跃点"。 实际上，此搜索被解释为以下条件：
  
- 该项目是从 Sadie Daniels、 OR
    
- 项目中的任何索引属性包含短语"跃点总数计价"。
    
相比之下，从: ("Sadie Daniels"或者"跃点总数计价") 将被解释为： 
  
- 该项目是从 Sadie Daniels、 OR
    
- 该项目是从跃点总数计价
    
默认运算符时指定多个条件，但没有逻辑运算符包含是成和。 例如，具有附件： true 等效具有主题： 项目： 附件： true 和主题： 项目。
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a>示例： 通过查询字符串和 EWS 托管 API 查找项目
<a name="bk_ExampleEWSMA"> </a>

本示例中，定义调用**SearchWithQueryString**的方法。 计[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和[WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)对象，表示作为参数的查询字符串的**字符串**对象。 本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。 
  
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

可以使用此方法来搜索与短语主题中的"项目计划"的所有项此例中所示。
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a>示例： 使用查询字符串和 EWS 查找项目
<a name="bk_ExampleEWS"> </a>

本示例中，SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)请求在与短语主题中的"项目计划"收件箱中查找所有项目。 
  
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

下面的示例演示从搜索结果的服务器的响应。
  
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

## <a name="see-also"></a>另请参阅

- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)    
- [在 Exchange 中使用 EWS 使用搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

