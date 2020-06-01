---
title: 使用 Exchange 中的 EWS 创建全天事件
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建全天事件。
ms.openlocfilehash: 6be638c17cc0e0c86fa6b4217169aa7259dfd4aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456862"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a><span data-ttu-id="dbbf4-103">使用 Exchange 中的 EWS 创建全天事件</span><span class="sxs-lookup"><span data-stu-id="dbbf4-103">Create all-day events by using EWS in Exchange</span></span>

<span data-ttu-id="dbbf4-104">了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建全天事件。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-104">Learn how to create all-day events by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="dbbf4-105">全天事件提供了一种表示整天或几天内发生的事情（例如，假日或假期）的方法。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-105">All-day events provide a way to represent something that happens for an entire day or multiple days—for example, a holiday, or vacation days.</span></span> <span data-ttu-id="dbbf4-106">使用 EWS 托管 API 或 EWS 创建全天事件是一个快照。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-106">Creating all-day events with the EWS Managed API or EWS is a snap.</span></span> <span data-ttu-id="dbbf4-107">这就像[创建约会](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)，但有一些小的变化。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-107">It's just like [creating appointments](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), but with a few small changes.</span></span>
  
## <a name="setting-start-and-end-times"></a><span data-ttu-id="dbbf4-108">设置开始时间和结束时间</span><span class="sxs-lookup"><span data-stu-id="dbbf4-108">Setting start and end times</span></span>

<span data-ttu-id="dbbf4-109">根据定义，全天事件将在特定日期的午夜开始，并在稍后结束24小时（或24小时的多个小时）。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-109">By definition, all-day events start at midnight on a specific day, and end 24 hours (or a multiple of 24 hours) later.</span></span> <span data-ttu-id="dbbf4-110">但是，EWS 托管 API 和 EWS 允许您在创建全天事件时指定午夜以外的时间。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-110">However, the EWS Managed API and EWS allow you to specify times other than midnight when creating all day events.</span></span> <span data-ttu-id="dbbf4-111">如果你不知道这些时间在服务器上的翻译方式，这可能会导致意外行为。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-111">This can lead to unintended behavior if you're not aware of how these times get translated on the server.</span></span>
  
<span data-ttu-id="dbbf4-112">收到请求以创建新的全天事件（在[请求或约会的时区](time-zones-and-ews-in-exchange.md)中）开始和/或结束时间时，这些时间将根据以下规则调整为相应时区中的午夜：</span><span class="sxs-lookup"><span data-stu-id="dbbf4-112">When a request is received to create a new all-day event with non-midnight (in the [time zone of the request or appointment](time-zones-and-ews-in-exchange.md)) start and/or end times, those times get adjusted to midnight in the appropriate time zone according to the following rules:</span></span>
  
- <span data-ttu-id="dbbf4-113">非午夜开始时间将调整为指定的时间之前的午夜。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-113">Non-midnight start times are adjusted to the midnight prior to the time specified.</span></span> <span data-ttu-id="dbbf4-114">例如，1:00 年6月6日下午6点调整为 12:00 AM。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-114">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 6.</span></span>
    
- <span data-ttu-id="dbbf4-115">在指定的时间之后，非午夜结束时间将调整为午夜。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-115">Non-midnight end times are adjusted to the midnight after the time specified.</span></span> <span data-ttu-id="dbbf4-116">例如，1:00 年6月6日在6月7日调整为 12:00 AM。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-116">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 7.</span></span>
    
<span data-ttu-id="dbbf4-117">因此，您创建的全天事件始终包含您指定的开始时间和结束时间，但可能会因班次转到午夜而在用户日历上声明额外的时间。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-117">So the all-day event that you create is always inclusive of the start and end time that you specify, but might claim additional time on the user's calendar due to the shift to midnight.</span></span> <span data-ttu-id="dbbf4-118">由于服务器会将开始时间和结束时间调整为午夜，因此建议您在午夜指定开始时间和结束时间以避免对时间的任何意外更改。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-118">Because the server will adjust the start and end time to midnight, we recommend that you specify your start and end time at midnight to avoid any unintended changes to the times.</span></span>
  
<span data-ttu-id="dbbf4-119">创建全天事件时，考虑时区也是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-119">It's also important to consider time zones when creating all-day events.</span></span> <span data-ttu-id="dbbf4-120">由于 Exchange server 在请求或约会的时区中强制执行午夜的开始和结束时间，因此在为不同时区配置的客户端中查看该全天事件可能会产生意外的结果。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-120">Because the Exchange server enforces a midnight start and end time in the time zone of the request or appointment, viewing that all-day event in a client configured for a different time zone can yield unexpected results.</span></span> <span data-ttu-id="dbbf4-121">根据客户端的不同，它可能会显示为包含您不打算包含的额外天数的全天事件，也可能不会完全显示为全天事件。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-121">Depending on the client, it might appear as an all-day event with extra days that you did not intend to include, or it might not appear as an all-day event altogether.</span></span> <span data-ttu-id="dbbf4-122">因此，我们建议您在创建全天事件时尽可能使用用户的首选时区。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-122">Because of this, we recommend that you use the user's preferred time zone whenever possible when you create all-day events.</span></span>
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a><span data-ttu-id="dbbf4-123">使用 EWS 托管 API 创建全天事件</span><span class="sxs-lookup"><span data-stu-id="dbbf4-123">Create an all-day event by using the EWS Managed API</span></span>

<span data-ttu-id="dbbf4-124">下面的示例演示如何使用 EWS 托管 API 创建一个全天事件，_从起始日期参数指定_的日期开始，并持续_numDays_参数指定的天数。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-124">The following example shows how to use the EWS Managed API to create an all-day event, starting on the date specified by the  _startDate_ parameter and lasting for the number of days specified by the  _numDays_ parameter.</span></span> <span data-ttu-id="dbbf4-125">请注意，将在[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx)属性指定的时区中创建约会。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-125">Note that the appointment will be created in the time zone specified by the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="dbbf4-126">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值对在_Service_参数中传递的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-126">This example assumes that the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values for the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a><span data-ttu-id="dbbf4-127">使用 EWS 创建全天事件</span><span class="sxs-lookup"><span data-stu-id="dbbf4-127">Create an all-day event by using EWS</span></span>

<span data-ttu-id="dbbf4-128">以下示例显示了用于创建全天事件的 EWS [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)请求。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-128">The following example shows an EWS [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request to create an all-day event.</span></span> <span data-ttu-id="dbbf4-129">约会在东部时区中创建，如[TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx)元素所示。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-129">The appointment is created in the Eastern time zone, as indicated by the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="dbbf4-130">请注意， [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx)和[End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx)元素的值的时间部分均为04：00Z，这将在夏令时转换为东部时区中的午夜。</span><span class="sxs-lookup"><span data-stu-id="dbbf4-130">Notice that the time portion of the values of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) elements are both 04:00Z, which converts to midnight in the Eastern time zone during daylight saving time.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="dbbf4-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbbf4-131">See also</span></span>


- [<span data-ttu-id="dbbf4-132">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="dbbf4-132">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="dbbf4-133">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="dbbf4-133">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="dbbf4-134">时区和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="dbbf4-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    

