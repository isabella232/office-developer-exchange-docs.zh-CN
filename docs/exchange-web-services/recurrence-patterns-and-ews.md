---
title: 定期模式和 EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: 了解定期模式和 Exchange 中的定期Exchange。
ms.openlocfilehash: fcd6cf847efedd3bc48a26ad7866a0221de59371
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541586"
---
# <a name="recurrence-patterns-and-ews"></a>定期模式和 EWS

了解定期模式和 Exchange 中的定期Exchange。
  
定期系列是按照定义的模式重复的约会或会议。 定期系列可以具有特定的发生次数，也可以无限重复。 此外，定期系列可能具有不遵循其余事件模式的异常，并且可能具有从模式中删除的事件。 您可以使用 EWS 托管 API 和 EWS 处理定期系列及其关联的日历项目。
  
## <a name="recurring-calendar-items"></a>定期日历项目

所有日历项目分为以下四个类别之一：
  
- 非定期日历项目
    
- 定期主母版
    
- 系列中发生次数
    
- 系列中已修改的匹配项，称为异常
    
本文将介绍属于定期系列的三种类型的日历项目。
  
了解定期系列如何在 Exchange 服务器上实现。 服务器在日历中仅创建一个实际项目（称为定期主控事件）而不是为定期系列中每个事件创建一个不同的项目。 定期主控文件的格式与非定期约会非常相似，并添加定期模式信息。 然后，服务器使用名为展开定期模式，根据客户端对约会信息的请求生成事件。 这些生成的事件不会永久存储在服务器上。 了解这一点非常重要，因为搜索日历项目的方式决定了您收到的信息以及是否发生扩展。
  
## <a name="recurrence-patterns"></a>定期模式

实现扩展的定期系列的关键部分是定期模式。 该定期模式位于定期主控文件上，并描述了一组根据定期主控母版的日期和时间计算发生次数的条件。
  
**表 1.可用的定期模式**

|**EWS 托管 API 类**|**EWS 元素**|**示例**|
|:-----|:-----|:-----|
|[Recurrence.DailyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[DailyRecurrence](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |每天重复一次。  <br/> 每隔一天重复一次。  <br/> |
|[Recurrence.MonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteMonthlyRecurrence](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |每月的第 10 天重复一次。  <br/> 每隔一个月在每月的第二十一天重复一次。  <br/> |
|[Recurrence.RelativeMonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeMonthlyRecurrence](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |在每月的第二个星期二重复。  <br/> 每三个月在每月的第三个星期四重复一次。  <br/> |
|[Recurrence.RelativeYearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeYearlyRecurrence](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |在每年 8 月的第一个星期一重复。  <br/> |
|[Recurrence.WeeklyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[WeeklyRecurrence](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |每周一重复一次。  <br/> 每隔一周每星期二和星期四重复一次。  <br/> |
|[Recurrence.YearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteYearlyRecurrence](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |在每年 9 月 1 日重复。  <br/> |
   
事件的另一条重要信息是定期模式何时结束。 这可表示为一组发生次数、结束日期或没有结束时间。
  
**表 2.用于定期系列结束的选项**

|**EWS 托管 API 方法/属性**|**EWS 元素**|**说明**|
|:-----|:-----|:-----|
|[Recurrence.NumberOfOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[NumberedRecurrence](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |此属性或元素的值指定发生次数。  <br/> |
|[Recurrence.EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[EndDateRecurrence](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |系列中的最后一次事件是此属性或元素指定的日期或之前。  <br/> |
|[Recurrence.HasEnd](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [Recurrence.NeverEnds](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[NoEndRecurrence](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |系列没有结束。  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a>展开的视图与非展开视图

在 EWS 托管 API (中对 **CalendarView** 元素使用 **FindAppointments** 方法) 调用扩展过程。  这将在约会中隐藏定期结果集约会，而是显示该定期系列的展开视图。 属于日历视图参数的定期主控事件的发生次数和例外均包括在结果集。 相反，将 EWS 托管 API (中的 **FindItems** 方法或 **FindItem** 操作与 EWS) 中的 **IndexedPageItemView** 或 **FractionalPageItemView** 元素一同使用，不会调用扩展过程，并且不包括事件和异常。 让我们看一个比较这两种方法的示例。 
  
**表 3.用于查找约会的方法和操作**

|**EWS 托管的 API 方法**|**EWS 操作**|**扩展系列？**|**结果中包含的项目**|
|:-----|:-----|:-----|:-----|
|[ExchangeService.FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |使用[CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)元素的[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作  <br/> |是  <br/> |非定期约会、定期系列的单个事件以及定期系列的例外  <br/> |
|[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |使用[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)元素的[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作  <br/> |否  <br/> |非定期约会和定期主约会  <br/> |
   
小马刚刚将她的人注册为球队。 团队每周三上午 8：30 练习，从 7 月 2 日开始，最后一次练习在 8 月 6 日。 为了忘记实践，一位小马向日历添加了定期约会，以提醒她。
  
**表 4.小马的定期约会**

|**约会字段**|**值**|
|:-----|:-----|
|主题  <br/> |球队实践  <br/> |
|开始  <br/> |2014 年 7 月 2 日上午 8：30  <br/> |
|End  <br/> |2014 年 7 月 2 日上午 10：00  <br/> |
|递归  <br/> |每周三  <br/> |
|最后一次出现  <br/> |2014 年 8 月 6 日上午 8：30  <br/> |
   
快速查看日历可发现团队总共将拥有六个实践。 但是，日历中不存在六个不同的约会项目。 相反，只有一个代表系列的定期主约会。
  
现在，让我们看一看在在 7 月发生的在一月，在一位小马的日历上查找约会。 下面的代码示例使用 Exchange 托管 API 中的 **FindItems** 方法生成一个不展开的一个在一起显示一位用户日历的视图。 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

该代码将生成以下包含[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素的[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

服务器的响应仅包括单个项目，即定期主控服务器，由 **RecurringMaster** 的 [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素值指示。 ItemId 元素[](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的值已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

现在，让我们与展开的视图进行比较。 下面的代码示例使用 EWS 托管 API 中的 **FindAppointments** 方法创建一个"一对一"的日历的展开视图。 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

此代码生成以下包含[CalendarView 元素的 FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作请求。 [](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

此时，服务器响应包括五次事件，每个事件针对 7 月的每个星期三发生一次。 这些项目 [上的 CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) 元素都有一个 **Occurrence 值**。 请注意，响应中不存在定期主机。 ItemId [元素](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 的值已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
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
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

在您具有定期主控事件、事件或异常后，您始终可以 [检索其他相关项目](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)。 如果发生或出现异常，您可以检索定期主控服务器，反之亦然。
  
## <a name="working-with-recurring-calendar-items"></a>使用定期日历项目

使用与用于处理非定期日历项目相同的方法和操作处理定期系列。 区别在于，根据你用于调用这些方法或操作的项目，你采取的操作可以应用于整个系列，也可以只应用于一个事件。 [对定期主](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)控文件采取的操作将应用于系列中发生的所有事件，而对单个事件[](how-to-update-a-recurring-series-by-using-ews.md)或异常采取的操作将仅适用于该发生或异常。 
  
## <a name="in-this-section"></a>本节内容

- [使用 EWS 访问定期系列Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 创建定期Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 删除定期系列中的约会Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 更新定期系列](how-to-update-a-recurring-series-by-using-ews.md)
    
- [使用 EWS 更新定期系列Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [使用 Exchange 中的 EWS 获取约会和Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

