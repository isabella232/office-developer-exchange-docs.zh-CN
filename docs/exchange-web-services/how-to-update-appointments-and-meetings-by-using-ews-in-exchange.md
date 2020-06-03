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
# <a name="update-appointments-and-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="76e4e-103">使用 Exchange 中的 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-103">Update appointments and meetings by using EWS in Exchange</span></span>

<span data-ttu-id="76e4e-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 更新约会和会议。</span><span class="sxs-lookup"><span data-stu-id="76e4e-104">Learn how to update appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="76e4e-105">会议和约会之间的基本区别在于会议具有与会者，而约会则不是。</span><span class="sxs-lookup"><span data-stu-id="76e4e-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="76e4e-106">约会和会议既可以是单个实例，也可以是定期系列的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。</span><span class="sxs-lookup"><span data-stu-id="76e4e-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="76e4e-107">在内部，Exchange 对会议和约会使用相同的对象。</span><span class="sxs-lookup"><span data-stu-id="76e4e-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="76e4e-108">您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素来处理会议和约会。</span><span class="sxs-lookup"><span data-stu-id="76e4e-108">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="76e4e-109">**表1。用于更新约会和会议的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="76e4e-109">**Table 1. EWS Managed API method and EWS operations for updating appointments and meetings**</span></span>

|<span data-ttu-id="76e4e-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="76e4e-110">**EWS Managed API method**</span></span>|<span data-ttu-id="76e4e-111">**相应的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="76e4e-111">**Corresponding EWS operations**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76e4e-112">约会。更新</span><span class="sxs-lookup"><span data-stu-id="76e4e-112">Appointment.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="76e4e-113">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="76e4e-113">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)<br/><br/>          [<span data-ttu-id="76e4e-114">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="76e4e-114">UpdateItemResponse</span></span>](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) <br/> |
   
## <a name="update-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="76e4e-115">使用 EWS 托管 API 更新约会</span><span class="sxs-lookup"><span data-stu-id="76e4e-115">Update an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="76e4e-116"><a name="bk_UpdateApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="76e4e-116"><a name="bk_UpdateApptEWSMA"> </a></span></span>

<span data-ttu-id="76e4e-117">下面的代码示例演示如何使用[约会对象](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)更新与约会关联的属性和[update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法将约会保存到 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="76e4e-117">The following code example shows how to use the [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) to update properties associated with an appointment and the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method to save the appointment to your calendar folder.</span></span> 
  
<span data-ttu-id="76e4e-118">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="76e4e-118">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="76e4e-119">本地变量 `appointmentId` 是与现有约会相关联的标识符。</span><span class="sxs-lookup"><span data-stu-id="76e4e-119">The local variable  `appointmentId` is an identifier associated with an existing appointment.</span></span> 
  
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

## <a name="update-an-appointment-by-using-ews"></a><span data-ttu-id="76e4e-120">使用 EWS 更新约会</span><span class="sxs-lookup"><span data-stu-id="76e4e-120">Update an appointment by using EWS</span></span>
<span data-ttu-id="76e4e-121"><a name="bk_UpdateApptEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="76e4e-121"><a name="bk_UpdateApptEWS"> </a></span></span>

<span data-ttu-id="76e4e-122">以下示例中的请求和响应 XML 对应于在[使用 Ews 托管 Api 更新约会](#bk_UpdateApptEWSMA)的 EWS 托管 api 代码中进行的调用。</span><span class="sxs-lookup"><span data-stu-id="76e4e-122">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Update an appointment by using the EWS Managed API](#bk_UpdateApptEWSMA).</span></span>
  
<span data-ttu-id="76e4e-123">下面的示例演示使用[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)操作更新约会时的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="76e4e-123">The following example shows the request XML when you use the [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) operation to update an appointment.</span></span> 
  
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

<span data-ttu-id="76e4e-124">下面的示例演示为响应[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)请求而返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="76e4e-124">The following example shows the XML that is returned in response to an [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="76e4e-125">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="76e4e-125">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
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

## <a name="update-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="76e4e-126">使用 EWS 托管 API 更新会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-126">Update a meeting by using the EWS Managed API</span></span>
<span data-ttu-id="76e4e-127"><a name="bk_UpdateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="76e4e-127"><a name="bk_UpdateMtgEWSMA"> </a></span></span>

<span data-ttu-id="76e4e-128">当您更新会议时，除了将已修改的约会项目保存到 "日历" 文件夹之外，您通常还需要向与会者发送更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="76e4e-128">When you update a meeting, in addition to saving the modified appointment item to the calendar folder, you also typically want to send updated meeting requests to attendees.</span></span> <span data-ttu-id="76e4e-129">下面的代码示例演示如何更新会议和发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="76e4e-129">The following code example shows how to update a meeting and send meeting requests.</span></span>
  
<span data-ttu-id="76e4e-130">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="76e4e-130">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="76e4e-131">本地变量 `meetingId` 是与现有约会相关联的标识符。</span><span class="sxs-lookup"><span data-stu-id="76e4e-131">The local variable  `meetingId` is an identifier that is associated with an existing appointment.</span></span> 
  
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

<span data-ttu-id="76e4e-132">设置[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的属性后，将会议保存到 "日历" 文件夹，并使用[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法发送更新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="76e4e-132">After setting the properties on the [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, save the meeting to your calendar folder and send updated meeting requests by using the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="76e4e-133">调用[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)方法时，可以将两个枚举值之一作为参数传递：</span><span class="sxs-lookup"><span data-stu-id="76e4e-133">You can pass in one of two enumeration values as parameters when you call the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) method:</span></span> 
  
- <span data-ttu-id="76e4e-134">[ConflictResolutionMode 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx)—确定如何处理客户端和服务器之间的冲突状态。</span><span class="sxs-lookup"><span data-stu-id="76e4e-134">[ConflictResolutionMode enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) — Determines how conflicting states between client and server are handled.</span></span> 
    
- <span data-ttu-id="76e4e-135">[SendInvitationsOrCancellationsMode 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsorcancellationsmode%28v=exchg.80%29.aspx)—影响会议更新请求的发送和保存。</span><span class="sxs-lookup"><span data-stu-id="76e4e-135">[SendInvitationsOrCancellationsMode enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsorcancellationsmode%28v=exchg.80%29.aspx) — Affects the sending and saving of meeting update requests.</span></span> 
    
<span data-ttu-id="76e4e-136">当您将[ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx)枚举值设置为**AlwaysOverwrite**时，您的会议版本将始终保存到 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="76e4e-136">When you set the [ConflictResolutionMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.conflictresolutionmode%28v=exchg.80%29.aspx) enumeration value to **AlwaysOverwrite**, your version of the meeting will always be saved to the calendar folder.</span></span>
  
## <a name="update-a-meeting-by-using-ews"></a><span data-ttu-id="76e4e-137">使用 EWS 更新会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-137">Update a meeting by using EWS</span></span>
<span data-ttu-id="76e4e-138"><a name="bk_UpdateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="76e4e-138"><a name="bk_UpdateMtgEWS"> </a></span></span>

<span data-ttu-id="76e4e-139">以下示例中的请求和响应 XML 对应于通过[使用 Ews 托管 Api 更新会议](#bk_UpdateMtgEWSMA)中的 EWS 托管 api 代码进行的调用。</span><span class="sxs-lookup"><span data-stu-id="76e4e-139">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Update a meeting by using the EWS Managed API](#bk_UpdateMtgEWSMA).</span></span> 
  
<span data-ttu-id="76e4e-140">下面的示例演示使用[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)操作更新会议时的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="76e4e-140">The following example shows the request XML when you use the [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) operation to update a meeting.</span></span> 
  
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

 <span data-ttu-id="76e4e-141">下面的示例演示为响应[UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx)请求而返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="76e4e-141">The following example shows the XML that is returned in response to an [UpdateItem](https://msdn.microsoft.com/library/34643d58-2743-45b0-a08d-bff6dc1da61d%28Office.15%29.aspx) request.</span></span> <span data-ttu-id="76e4e-142">为了提高可读性， **ChangeKey**和**ItemId**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="76e4e-142">The **ChangeKey** and **ItemId** attributes have been shortened for readability.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="76e4e-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76e4e-143">See also</span></span>

- [<span data-ttu-id="76e4e-144">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="76e4e-144">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)   
- [<span data-ttu-id="76e4e-145">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-145">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)   
- [<span data-ttu-id="76e4e-146">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-146">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="76e4e-147">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="76e4e-147">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="76e4e-148">使用 Exchange 中的 EWS 建议新的会议时间</span><span class="sxs-lookup"><span data-stu-id="76e4e-148">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

