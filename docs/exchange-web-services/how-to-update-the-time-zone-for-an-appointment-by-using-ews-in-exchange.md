---
title: 在 Exchange 使用 EWS 更新约会所在的时区
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 更新现有约会或会议的时区。
ms.openlocfilehash: 535eb9f546d9a4353408579f3a24750f32237699
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752894"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a><span data-ttu-id="df6a6-103">在 Exchange 使用 EWS 更新约会所在的时区</span><span class="sxs-lookup"><span data-stu-id="df6a6-103">Update the time zone for an appointment by using EWS in Exchange</span></span>

<span data-ttu-id="df6a6-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 更新现有约会或会议的时区。</span><span class="sxs-lookup"><span data-stu-id="df6a6-104">Learn how to update the time zone for an existing appointment or meeting by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="df6a6-105">当创建了 Exchange 日历约会或会议后，用于指定的开始和结束时间的时区另存为约会创建所在的时区。</span><span class="sxs-lookup"><span data-stu-id="df6a6-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="df6a6-106">您可以通过使用 EWS 托管 API 或 EWS 更改该所在的时区。</span><span class="sxs-lookup"><span data-stu-id="df6a6-106">You can change that time zone by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="df6a6-107">但是，更改约会上的时区具有对约会的开始和结束时间其他效果。</span><span class="sxs-lookup"><span data-stu-id="df6a6-107">However, changing the time zone on an appointment has other effects on the start and end time of the appointment.</span></span>
  
<span data-ttu-id="df6a6-108">时间值存储在 Exchange 服务器以协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="df6a6-108">Time values are stored on the Exchange server in Coordinate Universal Time (UTC).</span></span> <span data-ttu-id="df6a6-109">因此，如果约会设置为 1:00 (13:00) 在启动在东部时区 (UTC-05:00)，值为 6:00 (18:00) 存储在服务器上，假定该时区在其标准时间阶段。</span><span class="sxs-lookup"><span data-stu-id="df6a6-109">So if an appointment is set to start at 1:00 PM (13:00) in the Eastern time zone (UTC-05:00), that value is stored as 6:00 PM (18:00) on the server, assuming that the time zone is in its standard time phase.</span></span> <span data-ttu-id="df6a6-110">时在其他时区查看该约会时，添加或从 UTC 值来确定特定于所在的时区的时间中减去适当的小时数。</span><span class="sxs-lookup"><span data-stu-id="df6a6-110">When that appointment is viewed in other time zones, the appropriate number of hours is added or subtracted from the UTC value to determine the time zone-specific time.</span></span> <span data-ttu-id="df6a6-111">例如，如果约会开始时间 1:00 在东部 (下午 6:00 UTC)，并查看来自客户端在太平洋时区 (UTC-08:00)，时区特定开始时间，为该客户端将为 10:00 (18:00-08:00)。</span><span class="sxs-lookup"><span data-stu-id="df6a6-111">For example, if an appointment has a start time at 1:00 PM Eastern (6:00 PM UTC), and is viewed from a client in the Pacific time zone (UTC-08:00), the time-zone specific start time for that client would be 10:00 AM (18:00 - 08:00).</span></span>
  
<span data-ttu-id="df6a6-112">更新时所在的时区的约会不更新开始和结束时间的情况下，服务器将更新保留为相同的特定于所在的时区的时间的开始和结束时间在服务器上存储的 UTC 值。</span><span class="sxs-lookup"><span data-stu-id="df6a6-112">When you update the time zone of the appointment without updating the start and end time, the server updates the UTC values stored on the server to keep the start and end time as the same time zone-specific times.</span></span> <span data-ttu-id="df6a6-113">例如，假设 1:00 东部约会。</span><span class="sxs-lookup"><span data-stu-id="df6a6-113">For example, consider the 1:00 PM Eastern appointment.</span></span> <span data-ttu-id="df6a6-114">作为 18:00 UTC 的服务器上存储的时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-114">The time is stored as 18:00 UTC on the server.</span></span> <span data-ttu-id="df6a6-115">如果约会的时区更改为太平洋时区，服务器会转移到 1:00 的开始时间太平洋 (21:00 UTC)。</span><span class="sxs-lookup"><span data-stu-id="df6a6-115">If the time zone of the appointment is changed to the Pacific time zone, the server shifts the start time to 1:00 PM Pacific (21:00 UTC).</span></span>
  
<span data-ttu-id="df6a6-116">您可以通过显式设置的开始和结束时间来更改此行为。</span><span class="sxs-lookup"><span data-stu-id="df6a6-116">You can change this behavior by explicitly setting the start and end times.</span></span>
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="df6a6-117">使用 EWS 托管 API 更新现有约会上的时区</span><span class="sxs-lookup"><span data-stu-id="df6a6-117">Updating the time zone on an existing appointment by using the EWS Managed API</span></span>

<span data-ttu-id="df6a6-118">以下示例中，在 EWS 托管 API 用于通过更新的**Appointment.StartTimeZone**和**Appointment.EndTimeZone**属性更新为中央所在的时区的现有约会上的时区。</span><span class="sxs-lookup"><span data-stu-id="df6a6-118">In the following example, the EWS Managed API is used to update the time zone on an existing appointment to the Central time zone by updating the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="df6a6-119">如果_shiftAppointnment_参数设置为**true**，代码不明确设置的开始和结束时间在约会。</span><span class="sxs-lookup"><span data-stu-id="df6a6-119">If the  _shiftAppointnment_ parameter is set to **true**, the code does not explicitly set the start and end times on the appointment.</span></span> <span data-ttu-id="df6a6-120">在这种情况下，服务器将 shift 的开始和结束时间，以使其保持在新的时区中相同的相对于所在的时区的时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-120">In this case, the server will shift the start and end times to keep them at the same time zone-relative times in the new time zone.</span></span> <span data-ttu-id="df6a6-121">如果设置为**false**，则代码将转换显式可在 UTC 保留同时约会的开始和结束的时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-121">If set to **false**, the code converts the start and end times explicitly to keep the appointment at the same time in UTC.</span></span> 

<span data-ttu-id="df6a6-122">本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。</span><span class="sxs-lookup"><span data-stu-id="df6a6-122">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="df6a6-123">该示例用于更新约会的开始，在 1:00 东部和在下午 2:00 结束东部，与_shiftAppointment_参数设置为 true，则和[ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性设置为东部时区、 输出看起来如下所示。</span><span class="sxs-lookup"><span data-stu-id="df6a6-123">When the example is used to update an appointment that starts at 1:00 PM Eastern and ends at 2:00 PM Eastern, with the  _shiftAppointment_ parameter set to true, and the [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property set to the Eastern time zone, the output looks like the following.</span></span> 
  
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

<span data-ttu-id="df6a6-124">该示例使用_shiftAppointment_参数设置为 false，与和重新设置为东部时区的**TimeZone**属性更新了同一约会时, 的输出如下所稍有不同。</span><span class="sxs-lookup"><span data-stu-id="df6a6-124">When the example is used to update the same appointment with the  _shiftAppointment_ parameter set to false, and with the **TimeZone** property again set to the Eastern time zone, the output looks a little different.</span></span> 
  
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

<span data-ttu-id="df6a6-125">请注意，不会更改的开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-125">Notice that the start and end times did not change.</span></span> <span data-ttu-id="df6a6-126">这是因为时间以东部时间正在解释区域 （因为**TimeZone**属性设置为东部时区），和时间值已更新，以防止约会从进行切换。</span><span class="sxs-lookup"><span data-stu-id="df6a6-126">This is because the times are being interpreted in the Eastern time zone (because the **TimeZone** property is set to the Eastern time zone), and the time values were updated to prevent the appointment from shifting.</span></span> 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a><span data-ttu-id="df6a6-127">使用 EWS 更新现有约会上的时区</span><span class="sxs-lookup"><span data-stu-id="df6a6-127">Updating the time zone on an existing appointment by using EWS</span></span>

<span data-ttu-id="df6a6-128">以下示例 EWS [UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)请求更新对约会所在的时区。</span><span class="sxs-lookup"><span data-stu-id="df6a6-128">The following example EWS [UpdateItem operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request updates the time zone on an appointment.</span></span> <span data-ttu-id="df6a6-129">本示例仅更新[StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)和[EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素，以便服务器将 shift 以使其保持在同一时间区域相对时间中新的时区的约会的开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-129">This example only updates the [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone.</span></span> <span data-ttu-id="df6a6-130">为便于阅读将被截**ItemId**元素的值。</span><span class="sxs-lookup"><span data-stu-id="df6a6-130">The value of the **ItemId** element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="df6a6-131">以下示例请求更新所在的时区的约会，并通过显式设置的**开始**和**结束**元素日还更新的开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="df6a6-131">The following example request updates the time zone of the appointment, and also updates the start and end times by explicitly setting the **Start** and **End** elements.</span></span> <span data-ttu-id="df6a6-132">为便于阅读将被截**ItemId**元素的值。</span><span class="sxs-lookup"><span data-stu-id="df6a6-132">The value of the **ItemId** element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="df6a6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df6a6-133">See also</span></span>

- [<span data-ttu-id="df6a6-134">时区和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="df6a6-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)   
- [<span data-ttu-id="df6a6-135">通过在 Exchange 使用 EWS 特定时区中创建约会</span><span class="sxs-lookup"><span data-stu-id="df6a6-135">Create appointments in a specific time zone by using EWS in Exchange</span></span>](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="df6a6-136">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="df6a6-136">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

