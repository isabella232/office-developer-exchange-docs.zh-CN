---
title: 使用 EWS 更新定期系列
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e61bee9-4840-4773-a0a7-47b11e1fdf59
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 修改定期系列中的约会。
ms.openlocfilehash: ecee78457d2e6f91483cf897cfb4976fbd83400c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752897"
---
# <a name="update-a-recurring-series-by-using-ews"></a><span data-ttu-id="d0e91-103">使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="d0e91-103">Update a recurring series by using EWS</span></span>

<span data-ttu-id="d0e91-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 修改定期系列中的约会。</span><span class="sxs-lookup"><span data-stu-id="d0e91-104">Learn how to modify appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d0e91-105">您可以使用 EWS 托管 API 或 EWS 通过[更新整个数据系列](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)任一，或更新一次更新定期系列。</span><span class="sxs-lookup"><span data-stu-id="d0e91-105">You can use the EWS Managed API or EWS to update a recurring series by either [updating the entire series](how-to-update-a-recurring-series-by-using-ews-in-exchange.md), or by updating a single occurrence.</span></span> <span data-ttu-id="d0e91-106">本文中，我们将讨论如何更新一次。</span><span class="sxs-lookup"><span data-stu-id="d0e91-106">In this article we'll discuss how to update a single occurrence.</span></span>
  
<span data-ttu-id="d0e91-107">修改一系列中的单个约会是非常类似于[修改单实例约会](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d0e91-107">Modifying a single appointment in a series is very similar to [modifying a single instance appointment](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="d0e91-108">使用相同的方法和操作，但不是使用您想要更改的匹配项的项 ID。</span><span class="sxs-lookup"><span data-stu-id="d0e91-108">You use the same methods and operations, but you use the item ID of the occurrence you want to change.</span></span>
  
<span data-ttu-id="d0e91-109">更改一系列中的一个匹配项时，该实例将添加到已修改的约会系列定期主控形状相关联的数组。</span><span class="sxs-lookup"><span data-stu-id="d0e91-109">When you change a single occurrence in a series, that occurrence is added to an array of modified appointments associated with the recurring master for the series.</span></span> <span data-ttu-id="d0e91-110">您可以使用[Appointment.ModifiedOccurrences](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS 托管 API 属性或[ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS 元素访问一系列中所有已修改的约会。</span><span class="sxs-lookup"><span data-stu-id="d0e91-110">You can use the [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS Managed API property or the [ModifiedOccurrences](http://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS element to access all the appointments in a series that have been modified.</span></span> 
  
## <a name="modify-a-single-occurrence-in-a-series-by-using-the-ews-managed-api"></a><span data-ttu-id="d0e91-111">使用 EWS 托管 API 修改系列中的一个匹配项</span><span class="sxs-lookup"><span data-stu-id="d0e91-111">Modify a single occurrence in a series by using the EWS Managed API</span></span>

<span data-ttu-id="d0e91-112">若要修改系列中的单个实例您：</span><span class="sxs-lookup"><span data-stu-id="d0e91-112">To modify a single instance in a series, you:</span></span>
  
1. <span data-ttu-id="d0e91-113">将绑定到想要修改的项的索引值，或具有的匹配项的 ID 的[Appointment.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)方法使用[Appointment.BindToOccurrence](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx)方法的匹配项</span><span class="sxs-lookup"><span data-stu-id="d0e91-113">Bind to the occurrence you want to modify by using either the [Appointment.BindToOccurrence](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method with the item's index value, or the [Appointment.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method with the occurrence's ID.</span></span> <span data-ttu-id="d0e91-114">从对应于匹配项， [Appointment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的[Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)属性或[OccurrenceInfo](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx)对象对应于出现[ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx)属性，您可以获取此 ID。</span><span class="sxs-lookup"><span data-stu-id="d0e91-114">You obtain this ID from either the [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) property of an [Appointment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object that corresponds to the occurrence, or from the [ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx) property of the [OccurrenceInfo](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx) object that corresponds to the occurrence.</span></span> 
    
2. <span data-ttu-id="d0e91-115">更新上的匹配项的 Appointment 对象的属性。</span><span class="sxs-lookup"><span data-stu-id="d0e91-115">Update the properties on the occurrence's Appointment object.</span></span>
    
3. <span data-ttu-id="d0e91-116">使用[Appointment.Save](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法将所做的更改保存到的匹配项的 appointment 对象。</span><span class="sxs-lookup"><span data-stu-id="d0e91-116">Save the changes to the occurrence's appointment object by using the [Appointment.Save](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="d0e91-117">下面的示例更新定期系列中的约会，并验证已修改的约会，将更新定期母版。</span><span class="sxs-lookup"><span data-stu-id="d0e91-117">The following example updates an appointment in a recurring series and verifies that the modified appointment is updated on the recurring master.</span></span> <span data-ttu-id="d0e91-118">此示例假定您具有身份验证向 Exchange 服务器，并已获取名为**服务** [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="d0e91-118">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="d0e91-119">`recurrenceMasterId`参数是相关联的定期母版的匹配项，若要修改的标识符。</span><span class="sxs-lookup"><span data-stu-id="d0e91-119">The  `recurrenceMasterId` parameter is an identifier associated with the recurring master for the occurrence to modify.</span></span> 
  
```cs
public static ItemId ModifyARecurringSeries(ExchangeService service, ItemId recurrenceMasterId)
{
    Appointment calendarItem = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    if (calendarItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        // Get the recurring master from an occurrence in a recurring series with the properties you need.
        recurrMaster = Appointment.Bind(service,
                                        recurrenceMasterId,
                                        new PropertySet(AppointmentSchema.AppointmentType,
                                                        AppointmentSchema.Subject,
                                                        AppointmentSchema.FirstOccurrence,
                                                        AppointmentSchema.LastOccurrence,
                                                        AppointmentSchema.ModifiedOccurrences,
                                                        AppointmentSchema.DeletedOccurrences));
    }
    else
    {
        Console.WriteLine("Item id was not for a recurring master.");
        return recurrenceMasterId;
    }
    // Bind to the second occurrence in the series with the properties to modify.
    Appointment occurrenceToModify = Appointment.BindToOccurrence(service,
                                                                    recurrMaster.Id,
                                                                    2,
                                                                    new PropertySet(AppointmentSchema.Location,
                                                                                    AppointmentSchema.Start,
                                                                                    AppointmentSchema.End,
                                                                                    AppointmentSchema.RequiredAttendees,
                                                                                    AppointmentSchema.Subject));
    // Update the properties you want to change.
    occurrenceToModify.Location = "Helipad of Contoso Bldg 1";
    occurrenceToModify.Start = occurrenceToModify.Start.AddDays(1);
    occurrenceToModify.End = occurrenceToModify.End.AddDays(1);
    occurrenceToModify.RequiredAttendees.Add("Contoso CEO", "sadie@contoso");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Research", "ronnie@contoso.com");
    occurrenceToModify.RequiredAttendees.Add("Contoso Head of Security", "alfred@contoso.com");
    occurrenceToModify.Subject = occurrenceToModify.Subject.ToString() + ":Mandatory";
    // Update the occurrence in your calendar folder and send meeting update requests to attendees.
    // This method call results in an UpdateItem request to EWS.
    occurrenceToModify.Update(ConflictResolutionMode.AlwaysOverwrite, SendInvitationsOrCancellationsMode.SendToAllAndSaveCopy);
    // View updated and deleted occurrences on the recurring master prior to retrieving updated information.
    Console.WriteLine("Modified Occurrences prior to updating recurring master: {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    // Update the recurring master to view the modified and deleted occurrences.
    recurrMaster = Appointment.Bind(service, recurrenceMasterId, new PropertySet(AppointmentSchema.ModifiedOccurrences,
                                                                        AppointmentSchema.DeletedOccurrences));
    // View updated and deleted occurrences on the recurring master after retrieving updated information.
    Console.WriteLine("Modified Occurrences after updating recurring master:\t {0}",
                    (recurrMaster.ModifiedOccurrences == null ? "None" : recurrMaster.ModifiedOccurrences.Count.ToString()));
    return recurrMaster.Id;            
}

```

## <a name="modify-a-single-occurrence-in-a-series-by-using-ews"></a><span data-ttu-id="d0e91-120">使用 EWS 修改系列中的一个匹配项</span><span class="sxs-lookup"><span data-stu-id="d0e91-120">Modify a single occurrence in a series by using EWS</span></span>

<span data-ttu-id="d0e91-121">修改一系列中的单个实例本质上是相同修改单实例约会。</span><span class="sxs-lookup"><span data-stu-id="d0e91-121">Modifying a single instance in a series is essentially the same as modifying a single instance appointment.</span></span> <span data-ttu-id="d0e91-122">您可以指定使用[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)或[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)元素更改的匹配项。</span><span class="sxs-lookup"><span data-stu-id="d0e91-122">You can specify the occurrence to change by using either an [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) or an [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="d0e91-123">下面的示例演示请求 XML，当您使用[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)操作更新定期约会系列中的事情。</span><span class="sxs-lookup"><span data-stu-id="d0e91-123">The following example shows the request XML when you use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to update an occurrence in a recurring series of appointments.</span></span> <span data-ttu-id="d0e91-124">为便于阅读缩短**ItemId**和**更改密钥**。</span><span class="sxs-lookup"><span data-stu-id="d0e91-124">The **ItemId** and **ChangeKey** are shortened for readability.</span></span> 
  
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
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToAllAndSaveCopy">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkA" ChangeKey="DwAAAB" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Location" />
              <t:CalendarItem>
                <t:Location>Helipad of Contoso Bldg 1</t:Location>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-03-27T19:33:00.000-07:00</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-03-27T20:33:00.000-07:00</t:End>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:RequiredAttendees" />
              <t:CalendarItem>
                <t:RequiredAttendees>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Mack@contoso.com</t:Name>
                      <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Sadie@contoso.com</t:Name>
                      <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Magdalena@contoso.com</t:Name>
                      <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso CEO</t:Name>
                      <t:EmailAddress>sadie@contoso</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Research</t:Name>
                      <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                  <t:Attendee>
                    <t:Mailbox>
                      <t:Name>Contoso Head of Security</t:Name>
                      <t:EmailAddress>alfred@contoso.com</t:EmailAddress>
                    </t:Mailbox>
                  </t:Attendee>
                </t:RequiredAttendees>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:CalendarItem>
                <t:Subject>Weekly Update Meeting:Mandatory</t:Subject>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d0e91-125">服务器响应**UpdateItem**请求使用[UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)消息，其中包括**NoError**，这表明已成功更新中的匹配项和[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值更新的约会。</span><span class="sxs-lookup"><span data-stu-id="d0e91-125">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the occurrence was updated successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the updated appointment.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0e91-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0e91-126">See also</span></span>


- [<span data-ttu-id="d0e91-127">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0e91-127">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d0e91-128">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="d0e91-128">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d0e91-129">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="d0e91-129">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="d0e91-130">在 Exchange 中使用 EWS 访问定期系列</span><span class="sxs-lookup"><span data-stu-id="d0e91-130">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d0e91-131">使用 EWS 在 Exchange 中创建定期系列</span><span class="sxs-lookup"><span data-stu-id="d0e91-131">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d0e91-132">使用 EWS 在 Exchange 中删除定期系列中的约会</span><span class="sxs-lookup"><span data-stu-id="d0e91-132">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="d0e91-133">在 Exchange 使用 EWS 更新定期系列</span><span class="sxs-lookup"><span data-stu-id="d0e91-133">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

