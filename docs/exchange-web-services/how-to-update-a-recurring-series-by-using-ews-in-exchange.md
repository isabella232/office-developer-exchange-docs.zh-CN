---
title: 在 Exchange 使用 EWS 更新定期系列
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c922072f-ce33-4bff-97b0-1c1d0f9b880d
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 一次更新整个定期系列。
ms.openlocfilehash: 03f414845674bfcacca62ef96fdb84f8b8823920
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752882"
---
# <a name="update-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="81324-103">在 Exchange 使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="81324-103">Update a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="81324-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 一次更新整个定期系列。</span><span class="sxs-lookup"><span data-stu-id="81324-104">Learn how to update an entire recurring series at once by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="81324-105">您可以使用 EWS 托管 API 或 EWS 通过更新整个数据系列，或[更新一次](how-to-update-a-recurring-series-by-using-ews.md)更新定期系列。</span><span class="sxs-lookup"><span data-stu-id="81324-105">You can use the EWS Managed API or EWS to update a recurring series by either updating the entire series, or by [updating a single occurrence](how-to-update-a-recurring-series-by-using-ews.md).</span></span> <span data-ttu-id="81324-106">本文中，我们将讨论如何同时更新整个数据系列。</span><span class="sxs-lookup"><span data-stu-id="81324-106">In this article we'll discuss how to update the entire series at once.</span></span>
  
<span data-ttu-id="81324-107">一般情况下，更新定期系列是非常类似于[修改一个约会](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="81324-107">In general, updating a recurring series is very similar to [modifying a single appointment](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="81324-108">使用相同的方法和操作，但您使用的数据系列的定期主项目 ID。</span><span class="sxs-lookup"><span data-stu-id="81324-108">You use the same methods and operations, but you use the item ID of the series' recurring master.</span></span> <span data-ttu-id="81324-109">在某些情况下您可能无法启动与定期主控形状，您可能需要[查找定期主控形状的项 ID](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="81324-109">In some cases you might not start with the recurring master, and you might need to [find the item ID for the recurring master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="81324-110">但是，没有更新定期系列时要考虑的主要区别之一： 更新定期模式。</span><span class="sxs-lookup"><span data-stu-id="81324-110">However, there is one key difference to consider when updating a recurring series: updating the recurrence pattern.</span></span> <span data-ttu-id="81324-111">更新定期模式仅可能与定期主控形状，并且与模式更改可以添加或删除发生次数。</span><span class="sxs-lookup"><span data-stu-id="81324-111">Updating the recurrence pattern is only possible with the recurring master, and changes to the pattern can add or remove occurrences.</span></span> <span data-ttu-id="81324-112">例如，如果您修改将[Recurrence.EndDate](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx)属性设为日期晚于其当前值，定期模式几，并且可能添加其他发生次数。</span><span class="sxs-lookup"><span data-stu-id="81324-112">For example, if you modify the [Recurrence.EndDate](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) property to a date later than its current value, the recurrence pattern is reevaluated, and additional occurrences might be added.</span></span> 
  
## <a name="modify-all-occurrences-in-a-series-by-using-the-ews-managed-api"></a><span data-ttu-id="81324-113">使用 EWS 托管 API 修改一系列中的所有实例</span><span class="sxs-lookup"><span data-stu-id="81324-113">Modify all occurrences in a series by using the EWS Managed API</span></span>

<span data-ttu-id="81324-114">修改一系列中的所有实例您：</span><span class="sxs-lookup"><span data-stu-id="81324-114">To modify all occurrences in a series you:</span></span>
  
1. <span data-ttu-id="81324-115">通过对定期主使用[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)或[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)方法绑定到数据系列的定期母版。</span><span class="sxs-lookup"><span data-stu-id="81324-115">Bind to the recurring master for the series by using the [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) or [Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method on a recurring master.</span></span> 
    
2. <span data-ttu-id="81324-116">更新对母版页的定期[约会](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="81324-116">Update the properties on the recurring master [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object.</span></span> 
    
3. <span data-ttu-id="81324-117">使用[Appointment.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法将所做的更改保存到定期主控形状。</span><span class="sxs-lookup"><span data-stu-id="81324-117">Save the changes to the recurring master by using the [Appointment.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="81324-118">下面的示例更新定期系列更改位置，添加一个与会者，并修改定期模式。</span><span class="sxs-lookup"><span data-stu-id="81324-118">The following example updates a recurring series to change the location, add an attendee, and modify the recurrence pattern.</span></span> <span data-ttu-id="81324-119">本示例假定_服务_参数中传递的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象已初始化与中的[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。</span><span class="sxs-lookup"><span data-stu-id="81324-119">This example assumes that the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> <span data-ttu-id="81324-120">_定期约会_参数是绑定到匹配项或要更新的数据系列的定期主**约会**对象。</span><span class="sxs-lookup"><span data-stu-id="81324-120">The  _recurringAppointment_ parameter is an **Appointment** object bound to either an occurrence or the recurring master for the series to be updated.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
public static bool UpdateRecurringSeries(ExchangeService service, Appointment recurringAppointment)
{
    Appointment recurringMaster = null;
    // If the item is a single appointment, fail.
    if (recurringAppointment.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringAppointment.AppointmentType != AppointmentType.RecurringMaster)
    {
        // If an occurrence was passed in, bind to the master.
        try
        {
            // This method results in a call to EWS.
            recurringMaster = Appointment.BindToRecurringMaster(service, recurringAppointment.Id);
        }
        catch (Exception ex)
        {
            Console.WriteLine("Couldn't bind to master: {0}", ex.Message);
            return false;
        }
    }
    else
    {
        // Bind to the appointment to load all properties.
        // This method results in a call to EWS.
        recurringMaster = Appointment.Bind(service, recurringAppointment.Id);
    }
    // Basic updates. These kinds of updates are the same
    // as if you were updating a single appointment.
    // Update the location. All occurrences will update to this new location.
    recurringMaster.Location = "Conference Room 2";
    // Add an attendee.
    Attendee newAttendee = new Attendee("sadie@contoso.com");
    recurringMaster.RequiredAttendees.Add(newAttendee);
    // Changes to the recurrence. This is only applicable to a recurring
    // master.
    // If the series has an end date, extend the series to add two more occurrences.
    if (recurringMaster.Recurrence.HasEnd)
    {
        // NumberOfOccurrences is only set if the user created the
        // appointment with a set number of occurrences.
        // Otherwise, there's a start and end date.
        if (recurringMaster.Recurrence.NumberOfOccurrences != null)
        {
            recurringMaster.Recurrence.NumberOfOccurrences += 2;
        }
        else
        {
            // This is a bit more complicated if you want to add two more
            // occurrences. You need to calculate a new end date.
            Type recurrenceType = recurringMaster.Recurrence.GetType();
            switch (recurrenceType.Name)
            {
                case "DailyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(2);
                    break;
                case "WeeklyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddDays(14);
                    break;
                case "YearlyPattern":
                    recurringMaster.Recurrence.EndDate =
                        recurringMaster.Recurrence.EndDate.Value.AddYears(2);
                    break;
                default:
                    // Do nothing here. There are other recurrence
                    // types but for simplicity, these aren't covered.
                    break;
            }
        }
    }
    else
    {
        // If it has no end, set an end date to 2 weeks from today.
        recurringMaster.Recurrence.EndDate = DateTime.Now.AddDays(14);
    }
    // Update the series.
    try
    {
        // This method results in a call to EWS.
        recurringMaster.Update(ConflictResolutionMode.AutoResolve);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating series: {0}", ex.Message);
        return false;
    }
    return true;
}
```

## <a name="modify-all-occurrences-in-a-series-by-using-ews"></a><span data-ttu-id="81324-121">使用 EWS 修改一系列中的所有实例</span><span class="sxs-lookup"><span data-stu-id="81324-121">Modify all occurrences in a series by using EWS</span></span>

<span data-ttu-id="81324-122">若要修改在一系列中的所有匹配项，您需要使用请求中的[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素中的定期主机的项 ID [UpdateItem 操作](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="81324-122">To modify all occurrences in a series, you need to use the [UpdateItem operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) with the item ID of the recurring master in the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element in the request.</span></span> <span data-ttu-id="81324-123">请求更新一个约会相同请求的结构。</span><span class="sxs-lookup"><span data-stu-id="81324-123">The structure of the request is the same as a request to update a single appointment.</span></span> 
  
<span data-ttu-id="81324-124">下面的示例更新按以下方式定期系列：</span><span class="sxs-lookup"><span data-stu-id="81324-124">The following example updates the recurring series in the following ways:</span></span>
  
- <span data-ttu-id="81324-125">通过设置[位置](http://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx)元素来更新数据系列的位置。</span><span class="sxs-lookup"><span data-stu-id="81324-125">Updates the location of the series by setting the [Location](http://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx) element.</span></span> 
    
- <span data-ttu-id="81324-126">通过设置[RequiredAttendees](http://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx)元素更新与会者。</span><span class="sxs-lookup"><span data-stu-id="81324-126">Updates the attendees by setting the [RequiredAttendees](http://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx) element.</span></span> 
    
- <span data-ttu-id="81324-127">更新定期通过设置[定期 (RecurrenceType)](http://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="81324-127">Updates the recurrence by setting the [Recurrence (RecurrenceType)](http://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) element.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Conference Room 2</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie Daniels</t:Name>
                      <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Recurrence" />
              <t:CalendarItem>
                <t:Recurrence>
                  <t:WeeklyRecurrence>
                    <t:Interval>1</t:Interval>
                    <t:DaysOfWeek>Tuesday</t:DaysOfWeek>
                  </t:WeeklyRecurrence>
                  <t:EndDateRecurrence>
                    <t:StartDate>2014-05-06</t:StartDate>
                    <t:EndDate>2014-06-22-04:00</t:EndDate>
                  </t:EndDateRecurrence>
                </t:Recurrence>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:MeetingTimeZone" />
              <t:CalendarItem>
                <t:MeetingTimeZone TimeZoneName="Pacific Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="81324-128">服务器响应一个[UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)元素，包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的值为**NoError**，这表明已成功更新。</span><span class="sxs-lookup"><span data-stu-id="81324-128">The server responds with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) element that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element with a value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81324-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81324-129">See also</span></span>


- [<span data-ttu-id="81324-130">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="81324-130">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="81324-131">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="81324-131">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="81324-132">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="81324-132">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="81324-133">使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="81324-133">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="81324-134">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="81324-134">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    

