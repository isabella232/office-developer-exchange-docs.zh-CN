---
title: 使用约会中的 EWS 更新约会的Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: 了解如何使用现有约会或会议中的 EWS 托管 API 或 EWS 更新Exchange。
ms.openlocfilehash: 525feb1c7e37914ef4105312e89af8f1a8cf856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521065"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>使用约会中的 EWS 更新约会的Exchange

了解如何使用现有约会或会议中的 EWS 托管 API 或 EWS 更新Exchange。
  
在日历上创建约会或会议Exchange，用于指定开始时间和结束时间时区将保存为约会的创建时区。 可以使用 EWS 托管 API 或 EWS 更改该时区。 但是，更改约会的时区对约会的开始时间和结束时间有其他影响。
  
时间值以协调世界时 Exchange UTC 值 (服务器) 。 因此，如果约会设置为在东部时区 (UTC-05：00) 的下午 1：00 (13：00) 开始，则该值将存储在服务器上的下午 6：00 (18：00) ，假定时区处于其标准时间阶段。 在其他时区查看该约会时，将从 UTC 值中添加或减去相应的小时数以确定特定于时区的时间。 例如， 如果约会的开始时间为 UTC ( (6：00 PM) ，并且从太平洋时区 (UTC-08：00) 的客户端查看，该客户端的时区特定开始时间为上午 10：00 (18：00 - 08：00) 。
  
更新约会的时区而不更新开始时间和结束时间时，服务器将更新服务器上存储的 UTC 值，使开始时间和结束时间与特定于时区的时间保持相同。 例如，考虑下午 1：00 的东部约会。 时间在服务器上存储为 18：00 UTC。 如果约会的时区更改为太平洋时区，服务器将开始时间改为太平洋时间下午 1：00 (21：00 UTC) 。
  
可以通过显式设置开始时间和结束时间来更改此行为。
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新现有约会的时区

在下面的示例中，EWS 托管 API 用于通过更新 **Appointment.StartTimeZone** 和 **Appointment.EndTimeZone** 属性将现有约会的时区更新到中央时区。 如果  _shiftAppointnment_ 参数设置为 **true，** 则代码不会显式设置约会的开始时间和结束时间。 在这种情况下，服务器将切换开始时间和结束时间，以使它们处于新时区中相对于时区的同一时间。 如果设置为 **false，** 代码将显式转换开始时间和结束时间，以将约会同时保留为 UTC。 

此示例假定 **ExchangeService** 对象已使用 [凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)的有效值和 [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 属性进行了初始化。 
  
```cs
static void UpdateAppointmentTimeZone(ExchangeService service, ItemId apptId, bool shiftAppointment)
{
    PropertySet includeTimeZones = new PropertySet(AppointmentSchema.Subject,
                                                   AppointmentSchema.Start,
                                                   AppointmentSchema.ReminderDueBy,
                                                   AppointmentSchema.End,
                                                   AppointmentSchema.StartTimeZone,
                                                   AppointmentSchema.EndTimeZone);
    Appointment apptToUpdate;
    // Load the existing appointment.
    // This will result in a call to EWS.
    try
    {
        apptToUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("Before update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptToUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptToUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptToUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptToUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptToUpdate.EndTimeZone.DisplayName);
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Update the time zones on the appointment.
    apptToUpdate.StartTimeZone = centralTZ;
    apptToUpdate.EndTimeZone = centralTZ;
    if (!shiftAppointment)
    {
        // Set the start and end times explicitly so that the appointment
        // will start and end at the same UTC time.
        // Convert the times to then Central time zone. This
        // will keep them at the same time in UTC.
        // For example, 1:00 PM Eastern becomes 12:00 PM Central.
        DateTime newStartTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.Start, centralTZ);
        DateTime newEndTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.End, centralTZ);
        apptToUpdate.Start = newStartTime;
        apptToUpdate.End = newEndTime;
    }
    try
    {
        // Save the changes. This will result in a call to EWS.
        apptToUpdate.Update(ConflictResolutionMode.AlwaysOverwrite, 
            SendInvitationsOrCancellationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating appointment: {0}", ex.Message);
        return;
    }
    // Now rebind to the appointment to get the new values.
    Appointment apptAfterUpdate;
    
    try
    {
        // This will result in a call to EWS.
        apptAfterUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("After update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptAfterUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptAfterUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptAfterUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptAfterUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptAfterUpdate.EndTimeZone.DisplayName);
}
```

当此示例用于更新从东部时间下午 1：00 开始，下午 2：00 结束的约会  _，shiftAppointment_ 参数设置为 [true，ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) 属性设置为东部时区时，输出如下所示。 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 2:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 2:00:00 PM
  End: 6/20/2014 3:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

当此示例用于更新同一约会时  _，shiftAppointment_ 参数设置为 false，并且 **TimeZone** 属性再次设置为东部时区时，输出看起来会有所不同。 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

请注意，开始时间和结束时间不会更改。 这是因为时间是在东部时区 (因为 **TimeZone** 属性设置为东部时区) ，并且更新了时间值以防止约会转移。 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>使用 EWS 更新现有约会上的时区

下面的示例 EWS [UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) 请求更新约会的时区。 此示例仅更新 [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) 和 [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) 元素，因此服务器将切换约会的开始时间和结束时间，以将约会保持新时区中相对于时区的同一时间。 ItemId 元素的值为可读性而缩短。 
  
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
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

以下示例请求更新约会的时区，并且通过显式设置 Start 和 End 元素来更新 **开始时间** 和 **结束** 时间。 ItemId 元素的值为可读性而缩短。 
  
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
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-06-20T17:00:00.000Z</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-06-20T18:00:00.000Z</t:End>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅

- [时区和 Exchange 中的 EWS](time-zones-and-ews-in-exchange.md)   
- [使用特定时区中的 EWS 创建Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [使用 Exchange 中的 EWS 更新约会和Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

