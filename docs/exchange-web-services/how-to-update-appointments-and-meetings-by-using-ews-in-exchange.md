---
title: 使用 Exchange 中的 EWS 更新约会和会议
manager: sethgros
ms.date: 12/9/2015
ms.audience: Developer
ms.assetid: 13256625-083e-4a17-8fd1-2bed1f7cc14e
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 更新约会和会议。
localization_priority: Priority
ms.openlocfilehash: 553f52e3d9c7119ee249e0e162d057e4acc993ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527605"
---
# <a name="update-appointments-and-meetings-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 更新约会和会议

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 更新约会和会议。
  
会议和约会之间的基本区别在于会议具有与会者，而约会则不是。 约会和会议既可以是单个实例，也可以是定期系列的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。 在内部，Exchange 对会议和约会使用相同的对象。 您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素来处理会议和约会。 
  
**表1。用于更新约会和会议的 EWS 托管 API 方法和 EWS 操作**

|**EWS 托管的 API 方法**|**相应的 EWS 操作**|
|:-----|:-----|
|[约会。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)<br/><br/>          [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) <br/> |
   
## <a name="update-an-appointment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新约会
<a name="bk_UpdateApptEWSMA"> </a>

下面的代码示例演示如何使用[约会对象](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)更新与约会关联的属性和[update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法将约会保存到 "日历" 文件夹中。 
  
此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。 本地变量 `appointmentId` 是与现有约会相关联的标识符。 
  
```cs
// Instantiate an appointment object by binding to it by using the ItemId.
// As a best practice, limit the properties returned to only the ones you need.
Appointment appointment = Appointment.Bind(service, appointmentId, new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End));
string oldSubject = appointment.Subject;
// Update properties on the appointment with a new subject, start time, and end time.
appointment.Subject = appointment.Subject + " moved one hour later and to the day after " + appointment.Start.DayOfWeek + "!";
appointment.Start.AddHours(25);
appointment.End.AddHours(25);
// Unless explicitly specified, the default is to use SendToAllAndSaveCopy.
// This can convert an appointment into a meeting. To avoid this,
// explicitly set SendToNone on non-meetings.
SendInvitationsOrCancellationsMode mode = appointment.IsMeeting ? 
    SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy : SendInvitationsOrCancellationsMode.SendToNone;
// Send the update request to the Exchange server.
appointment.Update(ConflictResolutionMode.AlwaysOverwrite, mode);
// Verify the update.
Console.WriteLine("Subject for the appointment was \"" + oldSubject + "\". The new subject is \"" + appointment.Subject + "\"");

```

## <a name="update-an-appointment-by-using-ews"></a>使用 EWS 更新约会
<a name="bk_UpdateApptEWS"> </a>

以下示例中的请求和响应 XML 对应于在[使用 Ews 托管 Api 更新约会](#bk_UpdateApptEWSMA)的 EWS 托管 api 代码中进行的调用。
  
下面的示例演示使用[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)操作更新约会时的请求 XML。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Tennis Lesson moved one hour later and to the day after Wednesday!</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示为响应[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)请求而返回的 XML。 为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="815" MinorBuildNumber="6" Version="V2_7" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exc
hange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
            </t:CalendarItem>
          </m:Items>
          <m:ConflictResults>
            <t:Count>0</t:Count>
          </m:ConflictResults>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </m:UpdateItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-a-meeting-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新会议
<a name="bk_UpdateMtgEWSMA"> </a>

当您更新会议时，除了将已修改的约会项目保存到 "日历" 文件夹之外，您通常还需要向与会者发送更新的会议请求。 下面的代码示例演示如何更新会议和发送会议请求。
  
此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。 本地变量 `meetingId` 是与现有约会相关联的标识符。 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet(AppointmentSchema.Subject, 
                                                                           AppointmentSchema.Location, 
                                                                           AppointmentSchema.RequiredAttendees, 
                                                                           AppointmentSchema.Resources));
string oldSubject = meeting.Subject;
// Update properties on the appointment with a new subject, location, an additional required attendee, and a resource.
meeting.Subject = "Team building exercise has moved!";
meeting.Location = "4567 Contoso Way, Redmond, OH 33333, USA";
meeting.RequiredAttendees.Add("alisa@contoso.com");
meeting.Resources.Add("dlpprojector@contoso.com");
// Send the update request to the Exchange server.
meeting.Update(ConflictResolutionMode.AlwaysOverwrite, SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy);
// Verify the update.
Console.WriteLine("Subject for the meeting was \"" + oldSubject + "\". The new subject is \"" + meeting.Subject + "\"");

```

设置[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的属性后，将会议保存到 "日历" 文件夹，并使用[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法发送更新的会议请求。 
  
调用[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法时，可以将两个枚举值之一作为参数传递： 
  
- [ConflictResolutionMode 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx)—确定如何处理客户端和服务器之间的冲突状态。 
    
- [SendInvitationsOrCancellationsMode 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsorcancellationsmode%28v=exchg.80%29.aspx)—影响会议更新请求的发送和保存。 
    
当您将[ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx)枚举值设置为**AlwaysOverwrite**时，您的会议版本将始终保存到 "日历" 文件夹中。
  
## <a name="update-a-meeting-by-using-ews"></a>使用 EWS 更新会议
<a name="bk_UpdateMtgEWS"> </a>

以下示例中的请求和响应 XML 对应于通过[使用 Ews 托管 Api 更新会议](#bk_UpdateMtgEWSMA)中的 EWS 托管 api 代码进行的调用。 
  
下面的示例演示使用[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)操作更新会议时的请求 XML。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Team building exercise has moved!</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>4567 Contoso Way, Redmond, OH 33333, USA</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack.Chaves@contoso.com</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie.Daniels@contoso.com</t:Name>
                      <t:EmailAddress>Sadie.Daniels@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:EmailAddress>alisa@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Resources" />
              <t:CalendarItem>
                <t:Resources>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:EmailAddress>dlpprojector@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:Resources>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

 下面的示例演示为响应[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)请求而返回的 XML。 为了提高可读性， **ChangeKey**和**ItemId**属性已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="815" MinorBuildNumber="6" Version="V2_7" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:UpdateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
          <m:ConflictResults>
            <t:Count>0</t:Count>
          </m:ConflictResults>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </m:UpdateItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅

- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)   
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)   
- [使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)  
- [使用 Exchange 中的 EWS 建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

