---
title: 使用 EWS 更新定期系列
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7e61bee9-4840-4773-a0a7-47b11e1fdf59
description: 了解如何使用 EWS 托管 API 或 EWS 在定期系列中修改Exchange。
ms.openlocfilehash: 3b9260bf271581a9a47fcad36d35f48e9845eb91
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521073"
---
# <a name="update-a-recurring-series-by-using-ews"></a>使用 EWS 更新定期系列

了解如何使用 EWS 托管 API 或 EWS 在定期系列中修改Exchange。
  
您可以使用 EWS 托管 API 或 EWS 通过更新整个系列或更新[](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)单个事件来更新定期系列。 本文将讨论如何更新单个事件。
  
修改系列中的单个约会与修改单个实例 [约会非常相似](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。 使用相同的方法和操作，但使用要更改的事件的项目 ID。
  
在更改系列中的单个事件时，该匹配项将添加到与系列的定期主约会关联的已修改约会数组中。 可以使用 [Appointment.ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) EWS 托管 API 属性或 [ModifiedOccurrences](https://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) EWS 元素访问系列中已修改的所有约会。 
  
## <a name="modify-a-single-occurrence-in-a-series-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 修改系列中的单个事件

若要修改系列中的单个实例，需要：
  
1. 绑定到要修改的事件，方法是将 [Appointment.BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) 方法与项目的索引值一同使用，或 [将 Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) 方法与事件的 ID 一同使用。 从对应于事件的[Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)属性，或者从对应于事件的[OccurrenceInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.occurrenceinfo%28v=exchg.80%29.aspx)对象的[ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.occurrenceinfo.itemid%28v=exchg.80%29.aspx)属性获取此 ID。 
    
2. 更新事件的 Appointment 对象的属性。
    
3. 使用 [Appointment.Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) 方法保存对约会对象的更改。 
    
以下示例更新定期系列中的约会，并验证已修改的约会是否更新在定期主控上。 此示例假定你已对服务器Exchange身份验证，并且已获取名为 service 的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) **对象**。 参数  `recurrenceMasterId` 是一个与定期主机相关联的标识符，用于修改事件。 
  
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

## <a name="modify-a-single-occurrence-in-a-series-by-using-ews"></a>使用 EWS 修改系列中的单个事件

修改系列中的单个实例本质上与修改单个实例约会相同。 可以使用 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 或 [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) 元素指定要更改的事件。 
  
以下示例显示使用 [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) 操作更新定期约会系列中的事件时的请求 XML。 **ItemId** 和 **ChangeKey** 已缩短为可读性。 
  
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

服务器使用 [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)消息响应 **UpdateItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值（指示事件已成功更新）和更新的约会的 [ItemId。](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 
  
## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 更新约会和Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
- [通过使用 EWS 访问定期系列Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 创建定期Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 删除定期系列中的约会Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 更新定期系列Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

