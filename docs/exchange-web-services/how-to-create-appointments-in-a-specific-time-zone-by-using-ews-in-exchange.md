---
title: 使用特定时区中的 EWS 创建Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: 了解如何使用 EWS 托管 API 或 EWS 在特定的时区创建Exchange。
ms.openlocfilehash: 589c72982fdda568170468c376b8a6d9f598aa36
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521142"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>使用特定时区中的 EWS 创建Exchange

了解如何使用 EWS 托管 API 或 EWS 在特定的时区创建Exchange。
  
在日历上创建约会或会议Exchange，用于指定开始时间和结束时间时区将保存为约会的创建时区。 该时区还用于解释未指定显式[](time-zones-and-ews-in-exchange.md)时区的日期和时间值，因此了解指定时区的选项非常重要。
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 在不同时区创建约会

使用 EWS 托管 API 创建约会或会议时，有三个选项用于指定时区：
  
- 若要使用执行 EWS 托管 API 的计算机的时区，在创建 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象时不要指定时区。 
    
- 若要在所有日期/时间属性（包括创建新约会或会议时的属性）使用特定时区，请为 **ExchangeService** 对象的构造函数指定时区。 
    
- 若要使用与 [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) 属性中指定的时区不同的时区，请使用 [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) 和 [Appointment.EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) 属性。 
    
    > [!NOTE]
    > **EndTimeZone** 属性仅在 [ExchangeService.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性设置为 **Exchange2010** 或更高版本时可用。 如果不可用，则 **设置 StartTimeZone** 适用于约会的开始时间和结束时间。 
  
在下面的示例中，EWS 托管 API 用于创建三个约会。 每个约会都设置为从现在（在未指定时区）的下午 1：00 开始，一小时后结束。 第一个约会使用默认的 EWS 托管 API 行为在客户端计算机的时区创建。 第二个使用 **Appointment.StartTimeZone** 和 **Appointment.EndTimeZone** 属性在中央时区创建。 第三个通过使用 **ExchangeService.TimeZone** 属性在"Mountain"时区创建。 
  
```cs
using Microsoft.Exchange.WebServices.Data;
using System.Security;
static void CreateAppointments(string userEmail, SecureString userPass)
{
    // *****************************************************
    // Create an appointment using the client computer's time zone.
    // *****************************************************
    // Do not specify a time zone when creating the ExchangeService.
    ExchangeService clientTZService = new ExchangeService(ExchangeVersion.Exchange2010);
    clientTZService.Credentials = new NetworkCredential(userEmail, userPass);
    clientTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment clientTZAppt = new Appointment(clientTZService);
    clientTZAppt.Subject = "Appointment created using client time zone";
    clientTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", clientTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    DateTime startTime = new DateTime(DateTime.Now.Year, DateTime.Now.Month, DateTime.Now.Day + 2);
    startTime = startTime.AddHours(13);
    clientTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    DateTime endTime = startTime.AddHours(1);
    clientTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        clientTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Central time zone by
    // using the StartTimeZone property.
    // *****************************************************
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Create the appointment.
    Appointment centralTZAppt = new Appointment(clientTZService);
    centralTZAppt.Subject = "Appointment created using Central time zone";
    centralTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", centralTZ.DisplayName));
    // Set the time zone on the appointment.
    centralTZAppt.StartTimeZone = centralTZ;
    centralTZAppt.EndTimeZone = centralTZ;
    // Set the start time to 1:00 PM two days from today.
    centralTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    centralTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        centralTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Mountain time zone by
    // using the ExchangeService.TimeZone property.
    // *****************************************************
    // Specify the Mountain time zone when creating the ExchangeService.
    TimeZoneInfo mountainTZ = TimeZoneInfo.FindSystemTimeZoneById("Mountain Standard Time");
    ExchangeService mountainTZService = new ExchangeService(ExchangeVersion.Exchange2010, mountainTZ);
    mountainTZService.Credentials = new NetworkCredential(userEmail, userPass);
    mountainTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment mountainTZAppt = new Appointment(mountainTZService);
    mountainTZAppt.Subject = "Appointment created using Mountain time zone";
    mountainTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", mountainTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    mountainTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    mountainTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        mountainTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
}
```

当此示例在在东部时区配置的客户端计算机上执行时，从在东部时区配置的客户端查看其创建的三个约会时，它们分别在下午 1：00、下午 2：00 和下午 3：00 显示。
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>使用 EWS 在不同时区创建约会

使用 EWS 创建约会或会议时，有三个选项用于指定时区：
  
- 若要使用协调世界时 (UTC) ，请不要在[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)操作请求中包括[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素[、MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)元素 (Exchange 2007) 或[StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)和[EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素 (Exchange 2010 及更高版本) 。 
    
- 若要在所有日期/时间属性（包括创建新约会或会议时的属性）使用特定时区，请指定[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)操作请求中[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素中的时区。 
    
- 若要使用与[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素中指定的时区不同的时区，在[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)操作请求中包括[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素[、MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)元素 (Exchange 2007) 或[StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)和[EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素 (Exchange 2010 及更高版本) 。 
    
下面的示例 [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 请求使用 UTC 创建约会。 请注意 **，TimeZoneContext** 元素 **、StartTimeZone** 元素和 **EndTimeZone** 元素不存在。 **Start** 和 **End** 元素值以 UTC 表示。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using UTC</t:Subject>
          <t:Body BodyType="HTML">Time zone: UTC</t:Body>
          <t:Start>2014-06-07T17:00:00.000Z</t:Start>
          <t:End>2014-06-07T18:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

下面的示例 [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 请求使用 **StartTimeZone** 和 **EndTimeZone** 元素指定约会的中心时区。 请注意 **，TimeZoneContext** 元素不存在。 但是，如果存在 **，StartTimeZone** 和 **EndTimeZone** 元素的值将替代其值。 同样 **，Start** 和 **End** 元素值以 UTC 表示。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Central time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-06:00) Central Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T18:00:00.000Z</t:Start>
          <t:End>2014-06-07T19:00:00.000Z</t:End>
          <t:StartTimeZone Id="Central Standard Time" />
          <t:EndTimeZone Id="Central Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

以下示例 [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 请求将 **TimeZoneContext** 元素设置到"Mountain"时区。 请注意 **，StartTimeZone 和** **EndTimeZone 元素** 不存在。 同样 **，Start** 和 **End** 元素值以 UTC 表示。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Mountain Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Mountain time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-07:00) Mountain Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T19:00:00.000Z</t:Start>
          <t:End>2014-06-07T20:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

从在东部时区配置的客户端查看由以前的 EWS 示例请求创建的三个约会时，它们分别出现在下午 1：00、下午 2：00 和下午 3：00。
  
## 

现在，你已了解如何创建特定时区的约会，您可能想要将现有约会的时区[](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)更新为其他时区。 
  
## <a name="see-also"></a>另请参阅


- [时区和 Exchange 中的 EWS](time-zones-and-ews-in-exchange.md)
    
- [使用约会中的 EWS 更新约会的Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [使用 2013 中的 EWS 创建约会Exchange会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

