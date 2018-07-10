---
title: 通过在 Exchange 使用 EWS 特定时区中创建约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中特定时区创建约会。
ms.openlocfilehash: 1725498847f89a417b62a06fb8a3109af5c4deb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752767"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a><span data-ttu-id="523ec-103">通过在 Exchange 使用 EWS 特定时区中创建约会</span><span class="sxs-lookup"><span data-stu-id="523ec-103">Create appointments in a specific time zone by using EWS in Exchange</span></span>

<span data-ttu-id="523ec-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中特定时区创建约会。</span><span class="sxs-lookup"><span data-stu-id="523ec-104">Learn how to create appointments in specific time zones by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="523ec-105">当创建了 Exchange 日历约会或会议后，用于指定的开始和结束时间的时区另存为约会创建所在的时区。</span><span class="sxs-lookup"><span data-stu-id="523ec-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="523ec-106">该时区是还用于[解释不具有指定的显式时区的日期和时间值](time-zones-and-ews-in-exchange.md)，因此很重要了解您的选项以指定时区。</span><span class="sxs-lookup"><span data-stu-id="523ec-106">That time zone is also used to [interpret date and time values that do not have an explicit time zone specified](time-zones-and-ews-in-exchange.md), so it is important to understand your options to specify the time zone.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a><span data-ttu-id="523ec-107">使用 EWS 托管 API 位于不同时区创建约会</span><span class="sxs-lookup"><span data-stu-id="523ec-107">Creating appointments in different time zones by using the EWS Managed API</span></span>

<span data-ttu-id="523ec-108">创建约会或会议使用 EWS 托管 API 时，可以针对指定时区的三个选项：</span><span class="sxs-lookup"><span data-stu-id="523ec-108">When creating appointments or meetings using the EWS Managed API, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="523ec-109">若要使用的计算机所在的时区执行您 EWS 托管 API 时，不指定时区时创建[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="523ec-109">To use the time zone of the computer where your EWS Managed API is executing, do not specify a time zone when creating the [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object.</span></span> 
    
- <span data-ttu-id="523ec-110">若要使用的所有日期/时间属性的某个特定的时区，包括属性时创建一个新的约会或会议，时区中指定**ExchangeService**对象的构造函数。</span><span class="sxs-lookup"><span data-stu-id="523ec-110">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the constructor for the **ExchangeService** object.</span></span> 
    
- <span data-ttu-id="523ec-111">若要使用比[ExchangeService.TimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性中指定一个不同的时区，使用[Appointment.StartTimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx)和[Appointment.EndTimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="523ec-111">To use a different time zone than the one specified in the [ExchangeService.TimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property, use the [Appointment.StartTimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) and [Appointment.EndTimeZone](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) properties.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="523ec-112">当[ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性设置为**Exchange2010**或更高版本， **EndTimeZone**属性才可用。</span><span class="sxs-lookup"><span data-stu-id="523ec-112">The **EndTimeZone** property is only available when the [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property is set to **Exchange2010** or later.</span></span> <span data-ttu-id="523ec-113">如果不可用，设置**StartTimeZone**适用于约会的开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="523ec-113">If it is not available, setting the **StartTimeZone** applies to both the start and end times of the appointment.</span></span> 
  
<span data-ttu-id="523ec-114">在以下示例中，使用 EWS 托管 API 创建三个约会。</span><span class="sxs-lookup"><span data-stu-id="523ec-114">In the following example, the EWS Managed API is used to create three appointments.</span></span> <span data-ttu-id="523ec-115">每个约会是设置为在启动 1:00 从现在起，两天中未指定的时区和结束一小时更高版本。</span><span class="sxs-lookup"><span data-stu-id="523ec-115">Each appointment is set to start at 1:00 PM two days from now, in an unspecified time zone, and end one hour later.</span></span> <span data-ttu-id="523ec-116">通过使用默认 EWS 托管 API 行为情况下，在客户端计算机时区创建的第一个约会。</span><span class="sxs-lookup"><span data-stu-id="523ec-116">The first appointment is created in the client computer's time zone by using default EWS Managed API behavior.</span></span> <span data-ttu-id="523ec-117">通过使用**Appointment.StartTimeZone**和**Appointment.EndTimeZone**属性情况下，在中央所在的时区创建第二个。</span><span class="sxs-lookup"><span data-stu-id="523ec-117">The second is created in the Central time zone by using the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="523ec-118">第三个山地时间区域中创建使用**ExchangeService.TimeZone**属性。</span><span class="sxs-lookup"><span data-stu-id="523ec-118">The third is created in the Mountain time zone by using the **ExchangeService.TimeZone** property.</span></span> 
  
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

<span data-ttu-id="523ec-119">本示例在东部时区，配置客户端计算机上执行和查看从客户端配置在东部时区，其显示在 1:00，它会创建三个约会时 2:00 和下午 3:00，分别。</span><span class="sxs-lookup"><span data-stu-id="523ec-119">When this example is executed on a client computer configured in the Eastern time zone, and the three appointments it creates are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a><span data-ttu-id="523ec-120">使用 EWS 不同时区中创建约会</span><span class="sxs-lookup"><span data-stu-id="523ec-120">Creating appointments in different time zones by using EWS</span></span>

<span data-ttu-id="523ec-121">创建约会或会议使用 EWS 时，可以针对指定时区的三个选项：</span><span class="sxs-lookup"><span data-stu-id="523ec-121">When creating appointments or meetings using EWS, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="523ec-122">若要使用协调世界时 (UTC)，不包括[TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素、 [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)元素 (仅在 Exchange 2007 中)，或[StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)和[EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素 (Exchange 2010 及更高版本) 中[CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="523ec-122">To use Coordinated Universal Time (UTC), do not include a [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="523ec-123">若要使用的所有日期/时间属性的某个特定的时区，包括属性时创建一个新的约会或会议，某个时区的元素中指定[TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) [CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求中。</span><span class="sxs-lookup"><span data-stu-id="523ec-123">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="523ec-124">若要使用与[TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素中指定不同的时区，包括[TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素、 [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx)元素 (仅在 Exchange 2007 中) 或[StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx)和[EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx)元素 （Exchange 2010 及更高版本) [CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求中。</span><span class="sxs-lookup"><span data-stu-id="523ec-124">To use a different time zone than the one specified in the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, include a [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
<span data-ttu-id="523ec-125">以下示例[CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求创建约会使用 UTC。</span><span class="sxs-lookup"><span data-stu-id="523ec-125">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request creates an appointment using UTC.</span></span> <span data-ttu-id="523ec-126">请注意**TimeZoneContext**元素、 **StartTimeZone**元素和**EndTimeZone**元素不存在。</span><span class="sxs-lookup"><span data-stu-id="523ec-126">Notice that the **TimeZoneContext** element, the **StartTimeZone** element, and the **EndTimeZone** element are absent.</span></span> <span data-ttu-id="523ec-127">以 UTC 表示**Start**和**End**元素的值。</span><span class="sxs-lookup"><span data-stu-id="523ec-127">The **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="523ec-128">以下示例[CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求使用的**StartTimeZone**和**EndTimeZone**元素来指定约会中央所在的时区。</span><span class="sxs-lookup"><span data-stu-id="523ec-128">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment.</span></span> <span data-ttu-id="523ec-129">请注意**TimeZoneContext**元素不存在。</span><span class="sxs-lookup"><span data-stu-id="523ec-129">Notice that the **TimeZoneContext** element is absent.</span></span> <span data-ttu-id="523ec-130">但是，如果它已存在， **StartTimeZone**和**EndTimeZone**元素的值会覆盖它的值。</span><span class="sxs-lookup"><span data-stu-id="523ec-130">However, if it were present, the values of the **StartTimeZone** and **EndTimeZone** elements would override its value.</span></span> <span data-ttu-id="523ec-131">同样，以 UTC 表示**Start**和**End**元素的值。</span><span class="sxs-lookup"><span data-stu-id="523ec-131">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="523ec-132">以下示例[CreateItem operation，](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求将**TimeZoneContext**元素设置为山地所在的时区。</span><span class="sxs-lookup"><span data-stu-id="523ec-132">The following example [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request sets the **TimeZoneContext** element to the Mountain time zone.</span></span> <span data-ttu-id="523ec-133">请注意的**StartTimeZone**和**EndTimeZone**元素不存在。</span><span class="sxs-lookup"><span data-stu-id="523ec-133">Notice that the **StartTimeZone** and **EndTimeZone** elements are absent.</span></span> <span data-ttu-id="523ec-134">同样，以 UTC 表示**Start**和**End**元素的值。</span><span class="sxs-lookup"><span data-stu-id="523ec-134">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="523ec-135">从客户端配置在东部时区，其显示在 1:00，查看以前的 EWS 示例请求创建的三个约会时 2:00 和下午 3:00，分别。</span><span class="sxs-lookup"><span data-stu-id="523ec-135">When the three appointments created by the previous EWS example requests are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## 

<span data-ttu-id="523ec-136">既然您知道如何在特定时间区域中创建约会，您可能希望为另一个[更新现有约会上的时区](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="523ec-136">Now that you know how to create appointments in specific time zones, you might want to [update the time zones on existing appointments](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) to a different one.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="523ec-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="523ec-137">See also</span></span>


- [<span data-ttu-id="523ec-138">时区和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="523ec-138">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="523ec-139">在 Exchange 使用 EWS 更新约会所在的时区</span><span class="sxs-lookup"><span data-stu-id="523ec-139">Update the time zone for an appointment by using EWS in Exchange</span></span>](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="523ec-140">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="523ec-140">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

