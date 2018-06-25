---
title: 使用 Exchange 2013 中的 EWS 中创建约会和会议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fdea70a4-9267-4e5d-9152-b749e2acc3b0
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建约会和会议。
ms.openlocfilehash: 1c840fac2ecca9fb51a28044dfac6299cb4fc038
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752766"
---
# <a name="create-appointments-and-meetings-by-using-ews-in-exchange-2013"></a><span data-ttu-id="4797b-103">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="4797b-103">Create appointments and meetings by using EWS in Exchange 2013</span></span>

<span data-ttu-id="4797b-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中创建约会和会议。</span><span class="sxs-lookup"><span data-stu-id="4797b-104">Learn how to create appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4797b-105">会议和约会的基本区别是，会议具有与会者，并且不约会。</span><span class="sxs-lookup"><span data-stu-id="4797b-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="4797b-106">约会和会议可以是单个实例或定期系列的一部分，但约会不包括与会者、 聊天室或资源，因为它们不需要发送一条消息。</span><span class="sxs-lookup"><span data-stu-id="4797b-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="4797b-107">内部 Exchange 使用相同的对象的会议和约会。</span><span class="sxs-lookup"><span data-stu-id="4797b-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="4797b-108">使用 EWS 托管 API[约会类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 EWS[日历项目](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx)元素以使用会议和约会。</span><span class="sxs-lookup"><span data-stu-id="4797b-108">You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="4797b-109">**表 1。EWS 托管 API 方法和用于处理约会和会议的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4797b-109">**Table 1. EWS Managed API methods and EWS operations for working with appointments and meetings**</span></span>

|<span data-ttu-id="4797b-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="4797b-110">**EWS Managed API method**</span></span>|<span data-ttu-id="4797b-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4797b-111">**EWS operation**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4797b-112">Appointment.Save</span><span class="sxs-lookup"><span data-stu-id="4797b-112">Appointment.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4797b-113">CreateItem operation，（日历项）</span><span class="sxs-lookup"><span data-stu-id="4797b-113">CreateItem operation (calendar item)</span></span>](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="4797b-114">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="4797b-114">Item.Bind</span></span>](http://msdn.microsoft.com/en-us/library/dd634410%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4797b-115">GetItem 操作 （日历项）</span><span class="sxs-lookup"><span data-stu-id="4797b-115">GetItem operation (calendar item)</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
   
## <a name="create-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="4797b-116">使用 EWS 托管 API 创建约会</span><span class="sxs-lookup"><span data-stu-id="4797b-116">Create an appointment by using the EWS Managed API</span></span>
<span data-ttu-id="4797b-117"><a name="bk_CreateApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4797b-117"></span></span>

<span data-ttu-id="4797b-118">下面的代码示例演示如何使用[Appointment 对象](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)来创建约会和[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法以将其保存到您日历文件夹中，验证已创建约会的[Item.Bind](http://msdn.microsoft.com/en-us/library/dd634410%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="4797b-118">The following code example shows how to use the [Appointment object](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) to create an appointment, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save it to your calendar folder, and the [Item.Bind](http://msdn.microsoft.com/en-us/library/dd634410%28v=exchg.80%29.aspx) method to verify that the appointment was created.</span></span> 
  
<span data-ttu-id="4797b-119">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="4797b-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

<span data-ttu-id="4797b-120">Appointment 对象上设置的属性后, 保存约会对日历文件夹使用 appointment 对象的[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="4797b-120">After setting the properties on the appointment object, you save the appointment to the calendar folder by using the appointment object's [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="4797b-121">请注意，在验证步骤中，您使用项目[Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)与约会关联验证该约会是在日历文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4797b-121">Note that in the verification step, you use the item [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the appointment to verify that the appointment is in the calendar folder.</span></span> <span data-ttu-id="4797b-122">作为最佳实践，限制返回您只需到服务器的属性，在这种情况下，约会的主题。</span><span class="sxs-lookup"><span data-stu-id="4797b-122">As a best practice, limit the properties returned by the server to only what you need — in this case, the appointment's subject.</span></span> 
  
## <a name="create-an-appointment-by-using-ews"></a><span data-ttu-id="4797b-123">使用 EWS 创建约会</span><span class="sxs-lookup"><span data-stu-id="4797b-123">Create an appointment by using EWS</span></span>
<span data-ttu-id="4797b-124"><a name="bk_CreateApptEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="4797b-124"></span></span>

<span data-ttu-id="4797b-125">请求和响应 XML 下面的示例中对应于所做的[创建约会使用 EWS 托管 API](#bk_CreateApptEWSMA)中的 EWS 托管 API 代码的呼叫。</span><span class="sxs-lookup"><span data-stu-id="4797b-125">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create an appointment by using the EWS Managed API](#bk_CreateApptEWSMA).</span></span> <span data-ttu-id="4797b-126">以及显示请求和响应验证约会项在日历文件夹中的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-126">The request and response XML that verifies that the appointment items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="4797b-127">使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation，来创建约会时，下面的示例演示请求 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-127">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an appointment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

 <span data-ttu-id="4797b-128">下面的示例显示了响应由**CreateItem**操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-128">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-129">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-129">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4797b-130">下面的示例演示的请求创建使用[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)操作时，确认约会生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-130">The following example shows the request XML that is generated when you use the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation to verify that the appointment was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-131">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-131">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
       xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
       xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

 <span data-ttu-id="4797b-132">下面的示例显示了响应由**GetItem**操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-132">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-133">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-133">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="create-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="4797b-134">使用 EWS 托管 API 创建会议</span><span class="sxs-lookup"><span data-stu-id="4797b-134">Create a meeting by using the EWS Managed API</span></span>
<span data-ttu-id="4797b-135"><a name="bk_CreateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4797b-135"></span></span>

<span data-ttu-id="4797b-136">创建会议，除了将项目保存到日历文件夹中，您通常还希望向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="4797b-136">When you create a meeting, in addition to saving an item to the calendar folder, you also typically want to send meeting requests to attendees.</span></span> <span data-ttu-id="4797b-137">下面的代码示例演示如何创建会议并发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="4797b-137">The following code example shows how to create a meeting and send meeting requests.</span></span>
  
<span data-ttu-id="4797b-138">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="4797b-138">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

<span data-ttu-id="4797b-139">[Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象上设置的属性之后, 会议将保存到日历文件夹使用[Save](http://msdn.microsoft.com/en-us/library/dd635394%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="4797b-139">After setting the properties on the [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, save the meeting to your calendar folder by using the [Save](http://msdn.microsoft.com/en-us/library/dd635394%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="4797b-140">时[SendInvitationsMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx)枚举值设置为**SendOnlyToAll**或**SendToAllAndSaveCopy**时，向与会者发送邀请。</span><span class="sxs-lookup"><span data-stu-id="4797b-140">When you set the [SendInvitationsMode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.sendinvitationsmode%28v=exchg.80%29.aspx) enumeration value to **SendOnlyToAll** or **SendToAllAndSaveCopy**, invitations are sent to attendees.</span></span>
  
<span data-ttu-id="4797b-141">使用项目与会议相关[Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)验证已保存在日历文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4797b-141">Use the item [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) associated with the meeting to verify that it was saved in the calendar folder.</span></span> <span data-ttu-id="4797b-142">作为最佳实践，限制返回的属性由服务器到仅所需-在此情况下，会议的主题。</span><span class="sxs-lookup"><span data-stu-id="4797b-142">As a best practice, limit the properties returned by the server to only what you need - in this case, the meeting's subject.</span></span> 
  
## <a name="create-a-meeting-by-using-ews"></a><span data-ttu-id="4797b-143">使用 EWS 创建会议</span><span class="sxs-lookup"><span data-stu-id="4797b-143">Create a meeting by using EWS</span></span>
<span data-ttu-id="4797b-144"><a name="bk_CreateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="4797b-144"></span></span>

<span data-ttu-id="4797b-145">请求和响应 XML 下面的示例中对应于所做的[创建会议使用 EWS 托管 API](#bk_CreateMtgEWSMA)中的 EWS 托管 API 代码的呼叫。</span><span class="sxs-lookup"><span data-stu-id="4797b-145">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Create a meeting by using the EWS Managed API](#bk_CreateMtgEWSMA).</span></span> <span data-ttu-id="4797b-146">以及显示请求和响应验证会议项目在日历文件夹中的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-146">The request and response XML that verifies that the meeting items are in the calendar folder are shown as well.</span></span>
  
<span data-ttu-id="4797b-147">使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation，创建一个会议时，下面的示例演示请求 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-147">The following example shows the request XML when you use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4797b-148">下面的示例显示了响应由**CreateItem**操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-148">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-149">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-149">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="4797b-150">下面的示例演示请求验证已创建会议时，由[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)操作生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-150">The following example shows the request XML that is generated by the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation when you verify that the meeting was created.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-151">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-151">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4797b-152">下面的示例显示了响应由**GetItem**操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="4797b-152">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4797b-153">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4797b-153">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" 
 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="4797b-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4797b-154">See also</span></span>

- [<span data-ttu-id="4797b-155">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4797b-155">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)  
- [<span data-ttu-id="4797b-156">在 Exchange 使用 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="4797b-156">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="4797b-157">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="4797b-157">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="4797b-158">删除约会，并在 Exchange 使用 EWS 取消会议</span><span class="sxs-lookup"><span data-stu-id="4797b-158">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="4797b-159">建议在 Exchange 使用 EWS 的新的会议时间</span><span class="sxs-lookup"><span data-stu-id="4797b-159">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

