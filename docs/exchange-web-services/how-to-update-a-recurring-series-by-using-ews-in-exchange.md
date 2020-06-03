---
title: 在 Exchange 中使用 EWS 更新定期系列
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c922072f-ce33-4bff-97b0-1c1d0f9b880d
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 一次性更新整个定期系列。
ms.openlocfilehash: 253bc7da176a954480db97e303393fecdda54892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527612"
---
# <a name="update-a-recurring-series-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 更新定期系列

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 一次性更新整个定期系列。
  
您可以使用 EWS 托管 API 或 EWS 通过更新整个系列或[更新一次事件](how-to-update-a-recurring-series-by-using-ews.md)来更新定期系列。 在本文中，我们将讨论如何一次性更新整个系列。
  
通常情况下，更新定期系列与[修改单个约会](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)非常相似。 您可以使用相同的方法和操作，但使用系列的 "定期母版" 的项目 ID。 在某些情况下，您可能不会从定期母版开始，并且您可能需要[查找定期母版的项目 ID](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)。
  
但是，更新定期系列时需要考虑的一个关键区别：更新定期模式。 仅在定期母版中更新定期模式，并且对模式所做的更改可以添加或删除事件。 例如，如果将 "[结束](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx)日期" 属性修改为晚于当前值的日期，则会重新计算定期模式，并添加其他事件。 
  
## <a name="modify-all-occurrences-in-a-series-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 修改系列中的所有匹配项

若要修改系列中的所有匹配项，请执行以下操作：
  
1. 使用定期母版上的[BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)或 "[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)" 绑定方法绑定到系列的定期主服务器。 
    
2. 更新定期主[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象上的属性。 
    
3. 使用[save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法保存对定期母版所做的更改。 
    
以下示例更新定期系列以更改位置、添加与会者以及修改定期模式。 此示例假定在_service_参数中传递的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值进行了初始化。 _RecurringAppointment_参数是一个**约会**对象，绑定到要更新的系列的事件或定期主机。 
  
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

## <a name="modify-all-occurrences-in-a-series-by-using-ews"></a>使用 EWS 修改系列中的所有匹配项

若要修改系列中的所有匹配项，需要将[UpdateItem 操作](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)与请求的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素中的定期主控形状的项目 ID 一起使用。 请求的结构与更新单个约会的请求相同。 
  
下面的示例通过以下方式更新定期系列：
  
- 通过设置[location](https://msdn.microsoft.com/library/3fcf7133-ae1c-47b4-a187-660045f71df0%28Office.15%29.aspx)元素来更新系列的位置。 
    
- 通过设置[RequiredAttendees](https://msdn.microsoft.com/library/422f8d44-b0eb-49ca-af0f-0e22b54c78d2%28Office.15%29.aspx)元素更新与会者。 
    
- 通过设置[定期（RecurrenceType）](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx)元素更新定期。 
    
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

服务器使用包含值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素的[UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)元素进行响应，这表明更新已成功。
  
## <a name="see-also"></a>另请参阅


- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
- [使用 Exchange 中的 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [使用 EWS 更新定期系列](how-to-update-a-recurring-series-by-using-ews.md)
    
- [在 Exchange 中使用 EWS 访问定期系列](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    

