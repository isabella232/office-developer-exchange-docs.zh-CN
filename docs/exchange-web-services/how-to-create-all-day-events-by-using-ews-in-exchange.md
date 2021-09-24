---
title: 使用 Exchange 中的 EWS 创建全天事件
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建全天事件。
ms.openlocfilehash: 8769999907df46f519355a36fdf409f9ad347330
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521219"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 创建全天事件

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建全天事件。
  
全天事件提供了一种表示全天或多天所发生事件（例如，假日或休假日）的方法。 使用 EWS 托管 API 或 EWS 创建全天事件非常贴靠。 这就像创建 [约会一样](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)，但只需进行一些小更改。
  
## <a name="setting-start-and-end-times"></a>设置开始时间和结束时间

根据定义，全天事件从特定一天的午夜开始，在 24 小时或 24 小时之后结束 (24 小时) 结束。 但是，EWS 托管 API 和 EWS 允许您在创建全天事件时指定除午夜外的时间。 如果您不知道如何在服务器上翻译这些时间，这可能会导致意外行为。
  
当收到以非午夜 (在请求或约会 [) ](time-zones-and-ews-in-exchange.md) 开始时间和/或结束时间时区创建一个新的全天事件的请求时，根据以下规则，这些时间将调整到相应时区的午夜：
  
- 非午夜开始时间在指定的时间之前调整到午夜。 例如，6 月 6 日晚上 1：00 将调整为 6 月 6 日上午 12：00。
    
- 非午夜结束时间调整为指定时间后午夜。 例如，6 月 6 日晚上 1：00 将调整为 6 月 7 日上午 12：00。
    
因此，您创建的全天事件始终包含您指定的开始时间和结束时间，但可能会由于转移到午夜而声明用户日历的额外时间。 由于服务器将开始时间和结束时间调整为午夜，因此建议您指定午夜的开始时间和结束时间，以避免对时间进行任何意外更改。
  
创建全天事件时考虑时区也很重要。 由于 Exchange 服务器在请求或约会的时区强制执行午夜开始时间和结束时间，因此查看为不同时区配置的客户端中的全天事件会产生意外结果。 根据客户端，它可能显示为包含您不想包含的额外天数的全天事件，或者可能完全不会显示为全天事件。 因此，我们建议你在创建全天事件时尽可能使用用户的首选时区。
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建全天事件

下面的示例演示如何使用 EWS 托管 API 创建全天事件，从  _startDate_ 参数指定的日期开始，持续  _numDays_ 参数指定的天数。 请注意，将在 [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) 属性指定的时区创建约会。 此示例假定服务参数中传递的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象已使用[Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和 Url 属性的有效值[进行了](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)初始化。 
  
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

以下示例显示用于创建全天事件的 EWS [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 操作请求。 约会在东部时区创建，由 [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) 元素指示。 请注意 [，Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) 和 [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) 元素的值的时间部分是 04：00Z，在夏令时期间，在东部时区转换为午夜。 
  
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
    

