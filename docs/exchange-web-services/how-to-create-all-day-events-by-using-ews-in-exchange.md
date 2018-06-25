---
title: 使用 EWS 在 Exchange 中创建全天事件
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建全天事件。
ms.openlocfilehash: 0547fdf0ca92ba0648caeb5de6940d90d2a8ff46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752757"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange 中创建全天事件

了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建全天事件。
  
全天事件提供一种方式来表示内容的整个一天或多个日期发生 — 例如假日或假期天。 使用 EWS 托管 API 或 EWS 创建全天事件是管理单元。 它是一样[创建约会](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)，但有一些细微改动。
  
## <a name="setting-start-and-end-times"></a>设置开始和结束时间

根据定义，全天事件在特定日期，并结束 24 小时 （或 24 小时的倍数） 上的午夜开始更高版本。 但是，EWS 托管 API 和 EWS 允许您指定时间午夜之外创建全天事件时。 如果您不知道这些时间获取如何在服务器上进行转换，则会导致意外的行为。
  
当收到请求创建一个新的全天事件 （[所在的时区的请求或约会](time-zones-and-ews-in-exchange.md)） 中的非午夜开始和/或结束时间时，这些时间获取调整为中根据以下规则适当的时区的午夜：
  
- 非午夜开始时间将调整到之前指定的时间午夜。 例如，1:00 年 6 月 6 获取调整为上年 6 月 6 日上午 12:00。
    
- 为指定时间后午夜调整非午夜结束时间。 例如，1:00 年 6 月 6 获取调整为上 6 月 7 日上午 12:00。
    
因此始终 inclusive of 指定，但可能在声明更多时间的开始和结束时间是全天事件创建的用户的日历截止到午夜转移。 由于服务器将调整午夜开始和结束时间，我们建议您指定开始和结束时间午夜以避免时间任何意外的更改。
  
也很重要创建全天事件时，应考虑的时区。 Exchange server 强制执行午夜开始和结束时间的请求或约会的时区，因为在配置不同时区的客户端中查看该全天事件可以产生意外的结果。 根据客户端，它可能显示为与额外的几天所不打算包括，或它可能不显示为全天事件完全全天事件。 因此，我们建议您在创建全天事件时使用用户的首选的所在的时区尽可能。
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建全天事件

下面的示例演示如何使用 EWS 托管 API 创建的全天事件， _startDate_参数指定和持续的天数_numDays_参数指定在日期开始。 请注意，将[ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性指定的时区中创建约会。 本示例假定_服务_参数中传递的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象已初始化的[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。 
  
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

下面的示例演示创建全天事件的 EWS [CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求。 指示由[TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素，则在东部时区，创建约会。 请注意， [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[End](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx)元素的值的时间部分这两个 04:00Z，将转换为午夜在东部时区期间夏时制。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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
    
- [使用 Exchange 2013 中的 EWS 中创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [时区和 Exchange 中的 EWS](time-zones-and-ews-in-exchange.md)
    

