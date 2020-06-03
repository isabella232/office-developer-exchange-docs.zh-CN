---
title: 使用 Exchange 2013 中的 EWS 创建约会和会议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: fdea70a4-9267-4e5d-9152-b749e2acc3b0
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建约会和会议。
localization_priority: Priority
ms.openlocfilehash: b617519b839fb5ad310fbcaf6fae065f71f0f165
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528228"
---
# <a name="create-appointments-and-meetings-by-using-ews-in-exchange-2013"></a><span data-ttu-id="7505f-103">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="7505f-103">Create appointments and meetings by using EWS in Exchange 2013</span></span>

<span data-ttu-id="7505f-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建约会和会议。</span><span class="sxs-lookup"><span data-stu-id="7505f-104">Learn how to create appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="7505f-105">会议和约会之间的基本区别在于会议具有与会者，而约会则不是。</span><span class="sxs-lookup"><span data-stu-id="7505f-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="7505f-106">约会和会议既可以是单个实例，也可以是定期系列的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。</span><span class="sxs-lookup"><span data-stu-id="7505f-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="7505f-107">在内部，Exchange 对会议和约会使用相同的对象。</span><span class="sxs-lookup"><span data-stu-id="7505f-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="7505f-108">您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx)元素来处理会议和约会。</span><span class="sxs-lookup"><span data-stu-id="7505f-108">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="7505f-109">**表1。用于处理约会和会议的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="7505f-109">**Table 1. EWS Managed API methods and EWS operations for working with appointments and meetings**</span></span>

|<span data-ttu-id="7505f-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="7505f-110">**EWS Managed API method**</span></span>|<span data-ttu-id="7505f-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="7505f-111">**EWS operation**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7505f-112">约会. 保存</span><span class="sxs-lookup"><span data-stu-id="7505f-112">Appointment.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7505f-113">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="7505f-113">CreateItem operation (calendar item)</span></span>](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="7505f-114">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="7505f-114">Item.Bind</span></span>](https://msdn.microsoft.com/library/dd634410%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7505f-115">GetItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="7505f-115">GetItem operation (calendar item)</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
   
## <a name="create-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="7505f-116">使用 EWS 托管 API 创建约会</span><span class="sxs-lookup"><span data-stu-id="7505f-116">Create an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="7505f-117"><a name="bk_CreateApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="7505f-117"><a name="bk_CreateApptEWSMA"> </a></span></span>

<span data-ttu-id="7505f-118">下面的代码示例演示如何使用[约会对象](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)创建约会、[保存方法以](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)将其保存到 "日历" 文件夹，以及用于验证约会是否已创建的[Item 方法。](https://msdn.microsoft.com/library/dd634410%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7505f-118">The following code example shows how to use the [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) to create an appointment, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save it to your calendar folder, and the [Item.Bind](https://msdn.microsoft.com/library/dd634410%28v=exchg.80%29.aspx) method to verify that the appointment was created.</span></span> 
  
<span data-ttu-id="7505f-119">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="7505f-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
Appointment appointment = new Appointment(service);
// Set the properties on the appointment object to create the appointment.
appointment.Subject = "Tennis lesson";
appointment.Body = "Focus on backhand this week.";
appointment.Start = DateTime.Now.AddDays(2);
appointment.End = appointment.Start.AddHours(1);
appointment.Location = "Tennis club";
appointment.ReminderDueBy = DateTime.Now;
// Save the appointment to your calendar.
appointment.Save(SendInvitationsMode.SendToNone);
// Verify that the appointment was created by using the appointment's item ID.
Item item = Item.Bind(service, appointment.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nAppointment created: " + item.Subject + "\n");

```

<span data-ttu-id="7505f-120">设置约会对象上的属性后，可以使用约会对象的[save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法将约会保存到 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="7505f-120">After setting the properties on the appointment object, you save the appointment to the calendar folder by using the appointment object's [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="7505f-121">请注意，在验证步骤中，使用与约会关联的项目[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)来验证约会是否在 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="7505f-121">Note that in the verification step, you use the item [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the appointment to verify that the appointment is in the calendar folder.</span></span> <span data-ttu-id="7505f-122">作为最佳实践，应将服务器返回的属性限制为仅为您需要的内容，在此示例中为约会的主题。</span><span class="sxs-lookup"><span data-stu-id="7505f-122">As a best practice, limit the properties returned by the server to only what you need — in this case, the appointment's subject.</span></span> 
  
## <a name="create-an-appointment-by-using-ews"></a><span data-ttu-id="7505f-123">使用 EWS 创建约会</span><span class="sxs-lookup"><span data-stu-id="7505f-123">Create an appointment by using EWS</span></span>
<span data-ttu-id="7505f-124"><a name="bk_CreateApptEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7505f-124"><a name="bk_CreateApptEWS"> </a></span></span>

<span data-ttu-id="7505f-125">以下示例中的请求和响应 XML 对应于通过[使用 Ews 托管 Api 创建约会](#bk_CreateApptEWSMA)中的 EWS 托管 api 代码进行的调用。</span><span class="sxs-lookup"><span data-stu-id="7505f-125">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create an appointment by using the EWS Managed API](#bk_CreateApptEWSMA).</span></span> <span data-ttu-id="7505f-126">同时还会显示用于验证约会项目是否位于 "日历" 文件夹中的请求和响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-126">The request and response XML that verifies that the appointment items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="7505f-127">下面的示例演示使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建约会时的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-127">The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an appointment.</span></span> 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Tennis lesson</t:Subject>
          <t:Body BodyType="HTML">Focus on backhand this week.</t:Body>
          <t:ReminderDueBy>2013-09-19T14:37:10.732-07:00</t:ReminderDueBy>
          <t:Start>2013-09-21T19:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Tennis club</t:Location>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

 <span data-ttu-id="7505f-128">下面的示例演示由**CreateItem**操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-128">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-129">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-129">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="7505f-130">下面的示例演示在使用[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)操作来验证约会是否已创建时生成的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-130">The following example shows the request XML that is generated when you use the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation to verify that the appointment was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-131">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-131">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="7505f-132">下面的示例演示由**GetItem**操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-132">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-133">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-133">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Tennis lesson</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="create-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="7505f-134">使用 EWS 托管 API 创建会议</span><span class="sxs-lookup"><span data-stu-id="7505f-134">Create a meeting by using the EWS Managed API</span></span>
<span data-ttu-id="7505f-135"><a name="bk_CreateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="7505f-135"><a name="bk_CreateMtgEWSMA"> </a></span></span>

<span data-ttu-id="7505f-136">在创建会议时，除了将项目保存到 "日历" 文件夹之外，您通常还需要向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="7505f-136">When you create a meeting, in addition to saving an item to the calendar folder, you also typically want to send meeting requests to attendees.</span></span> <span data-ttu-id="7505f-137">下面的代码示例演示如何创建会议并发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="7505f-137">The following code example shows how to create a meeting and send meeting requests.</span></span>
  
<span data-ttu-id="7505f-138">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="7505f-138">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
```cs
Appointment meeting = new Appointment(service);
// Set the properties on the meeting object to create the meeting.
meeting.Subject = "Team building exercise";
meeting.Body = "Let's learn to really work as a team and then have lunch!";
meeting.Start = DateTime.Now.AddDays(2);            
meeting.End = meeting.Start.AddHours(4);
meeting.Location = "Conference Room 12";
meeting.RequiredAttendees.Add("Mack@contoso.com");
meeting.RequiredAttendees.Add("Sadie@contoso.com");
meeting.OptionalAttendees.Add("Magdalena@contoso.com");
meeting.ReminderMinutesBeforeStart = 60;
// Save the meeting to the Calendar folder and send the meeting request.
meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
// Verify that the meeting was created.
Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
Console.WriteLine("\nMeeting created: " + item.Subject + "\n");

```

<span data-ttu-id="7505f-139">在设置了[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的属性后，使用[save](https://msdn.microsoft.com/library/dd635394%28v=exchg.80%29.aspx)方法将会议保存到 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="7505f-139">After setting the properties on the [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, save the meeting to your calendar folder by using the [Save](https://msdn.microsoft.com/library/dd635394%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="7505f-140">当您将[SendInvitationsMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx)枚举值设置为**SendOnlyToAll**或**SendToAllAndSaveCopy**时，会向与会者发送邀请。</span><span class="sxs-lookup"><span data-stu-id="7505f-140">When you set the [SendInvitationsMode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) enumeration value to **SendOnlyToAll** or **SendToAllAndSaveCopy**, invitations are sent to attendees.</span></span>
  
<span data-ttu-id="7505f-141">使用与会议关联的项目[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)验证会议是否保存在 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="7505f-141">Use the item [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the meeting to verify that it was saved in the calendar folder.</span></span> <span data-ttu-id="7505f-142">作为最佳实践，请将服务器返回的属性限制为仅限您需要的内容-在此示例中为会议的主题。</span><span class="sxs-lookup"><span data-stu-id="7505f-142">As a best practice, limit the properties returned by the server to only what you need - in this case, the meeting's subject.</span></span> 
  
## <a name="create-a-meeting-by-using-ews"></a><span data-ttu-id="7505f-143">使用 EWS 创建会议</span><span class="sxs-lookup"><span data-stu-id="7505f-143">Create a meeting by using EWS</span></span>
<span data-ttu-id="7505f-144"><a name="bk_CreateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="7505f-144"><a name="bk_CreateMtgEWS"> </a></span></span>

<span data-ttu-id="7505f-145">以下示例中的请求和响应 XML 对应于通过[使用 Ews 托管 Api 创建会议](#bk_CreateMtgEWSMA)中的 EWS 托管 api 代码进行的调用。</span><span class="sxs-lookup"><span data-stu-id="7505f-145">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create a meeting by using the EWS Managed API](#bk_CreateMtgEWSMA).</span></span> <span data-ttu-id="7505f-146">同时显示了确认会议项目是否位于 "日历" 文件夹中的请求和响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-146">The request and response XML that verifies that the meeting items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="7505f-147">下面的示例演示使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建会议时的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-147">The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting.</span></span> 
  
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
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2013-09-21T16:00:00.000Z</t:Start>
          <t:End>2013-09-21T20:00:00.000Z</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie.Daniels@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:OptionalAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena.Kemp@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:OptionalAttendees>
          <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7505f-148">下面的示例演示由**CreateItem**操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-148">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-149">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-149">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="7505f-150">下面的示例演示在验证会议是否已创建时由[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)操作生成的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-150">The following example shows the request XML that is generated by the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation when you verify that the meeting was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-151">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-151">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```xml
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7505f-152">下面的示例演示由**GetItem**操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="7505f-152">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7505f-153">为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="7505f-153">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
              <t:Subject>Team building exercise</t:Subject>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="7505f-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7505f-154">See also</span></span>

- [<span data-ttu-id="7505f-155">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7505f-155">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)  
- [<span data-ttu-id="7505f-156">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="7505f-156">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="7505f-157">使用 Exchange 中的 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="7505f-157">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="7505f-158">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="7505f-158">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="7505f-159">使用 Exchange 中的 EWS 建议新的会议时间</span><span class="sxs-lookup"><span data-stu-id="7505f-159">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

