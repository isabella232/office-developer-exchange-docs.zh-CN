---
title: 使用 Exchange 中的 EWS 创建全天事件
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建全天事件。
ms.openlocfilehash: 6be638c17cc0e0c86fa6b4217169aa7259dfd4aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456862"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 创建全天事件

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建全天事件。
  
全天事件提供了一种表示整天或几天内发生的事情（例如，假日或假期）的方法。 使用 EWS 托管 API 或 EWS 创建全天事件是一个快照。 这就像[创建约会](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)，但有一些小的变化。
  
## <a name="setting-start-and-end-times"></a>设置开始时间和结束时间

根据定义，全天事件将在特定日期的午夜开始，并在稍后结束24小时（或24小时的多个小时）。 但是，EWS 托管 API 和 EWS 允许您在创建全天事件时指定午夜以外的时间。 如果你不知道这些时间在服务器上的翻译方式，这可能会导致意外行为。
  
收到请求以创建新的全天事件（在[请求或约会的时区](time-zones-and-ews-in-exchange.md)中）开始和/或结束时间时，这些时间将根据以下规则调整为相应时区中的午夜：
  
- 非午夜开始时间将调整为指定的时间之前的午夜。 例如，1:00 年6月6日下午6点调整为 12:00 AM。
    
- 在指定的时间之后，非午夜结束时间将调整为午夜。 例如，1:00 年6月6日在6月7日调整为 12:00 AM。
    
因此，您创建的全天事件始终包含您指定的开始时间和结束时间，但可能会因班次转到午夜而在用户日历上声明额外的时间。 由于服务器会将开始时间和结束时间调整为午夜，因此建议您在午夜指定开始时间和结束时间以避免对时间的任何意外更改。
  
创建全天事件时，考虑时区也是非常重要的。 由于 Exchange server 在请求或约会的时区中强制执行午夜的开始和结束时间，因此在为不同时区配置的客户端中查看该全天事件可能会产生意外的结果。 根据客户端的不同，它可能会显示为包含您不打算包含的额外天数的全天事件，也可能不会完全显示为全天事件。 因此，我们建议您在创建全天事件时尽可能使用用户的首选时区。
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建全天事件

下面的示例演示如何使用 EWS 托管 API 创建一个全天事件，_从起始日期参数指定_的日期开始，并持续_numDays_参数指定的天数。 请注意，将在[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性指定的时区中创建约会。 此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值对在_Service_参数中传递的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象进行了初始化。 
  
```cs
static void CreateAllDayAppointment(ExchangeService service, DateTime startDate, int numDays)
{
    // Best practice is to set the start date to midnight
    // on the first day of the all-day event.
    DateTime startDateMidnight = startDate.Date;
    // The end date should be midnight on the first day
    // after the event.
    DateTime endDateMidnight = startDateMidnight.AddDays(numDays);
    Appointment allDayEvent = new Appointment(service);
    // Set IsAllDayEvent to true.
    allDayEvent.IsAllDayEvent = true;
    // Set other properties.
    allDayEvent.Subject = "Vacation";
    allDayEvent.LegacyFreeBusyStatus = LegacyFreeBusyStatus.OOF;
    allDayEvent.Start = startDateMidnight;
    allDayEvent.End = endDateMidnight;
    // Save the appointment.
    try
    {
        allDayEvent.Save(WellKnownFolderName.Calendar, SendInvitationsMode.SendToNone);
        Console.WriteLine("All day event created.");
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving all day event: {0}", ex.Message);
    }
}
```

## <a name="create-an-all-day-event-by-using-ews"></a>使用 EWS 创建全天事件

以下示例显示了用于创建全天事件的 EWS [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求。 约会在东部时区中创建，如[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素所示。 请注意， [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx)元素的值的时间部分均为04：00Z，这将在夏令时转换为东部时区中的午夜。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Vacation</t:Subject>
          <t:Start>2014-06-09T04:00:00.000Z</t:Start>
          <t:End>2014-06-10T04:00:00.000Z</t:End>
          <t:IsAllDayEvent>true</t:IsAllDayEvent>
          <t:LegacyFreeBusyStatus>OOF</t:LegacyFreeBusyStatus>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [时区和 Exchange 中的 EWS](time-zones-and-ews-in-exchange.md)
    

