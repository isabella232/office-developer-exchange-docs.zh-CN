---
title: 在 Exchange 中使用 EWS 删除定期系列中的约会
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 删除定期系列中的约会。
ms.openlocfilehash: 5646a30d218ed4d795044aefe5efea1399d19a79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528123"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 删除定期系列中的约会

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 删除定期系列中的约会。
  
您可以使用 EWS 托管 API 或 EWS 删除一系列约会或会议，或仅删除系列中的一个实例。 用于删除整个系列的过程基本上与用于删除单个事件的过程相同。 使用与[删除单个实例约会或会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)时使用的相同的 EWS 托管 API 方法或 ews 操作。 不同之处在于方法或操作中包含的项 ID。 首先，我们来看看这两个方案是相同的。 
  
若要在定期系列中删除定期系列或单个事件，需要查找要删除的具体值或系列，然后调用相应的方法或操作将其删除。 虽然您可以简单地删除任何类型的约会，但我们建议您将任何与会者或组织者保持为最新，并取消用户已组织的会议并拒绝用户未组织的会议。
  
应用场景的不同之处是什么？ 这是关于用于调用方法（对于 EWS 托管 API）或包含在操作请求中的项目 ID （对于 EWS）的[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象。 若要删除整个系列，则需要定期母版的**约会**对象或项目 ID。 若要删除单个事件，需要使用**约会**对象或项目 ID 进行匹配。 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除定期约会

此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。 _RecurringItem_参数是定期母版或单个事件的**约会**对象。 _DeleteEntireSeries_参数指示是否删除_recurringItem_所属的整个系列。 
  
```cs
public static bool DeleteRecurringItem(ExchangeService service, Appointment recurringItem, bool deleteEntireSeries)
{
    Appointment appointmentToDelete = null;
    // If the item is a single appointment, fail.
    if (recurringItem.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        if (!deleteEntireSeries)
        {
            // The item is the recurring master, so deleting it will delete
            // the entire series. The caller indicated that the entire series
            // should not be deleted, so fail.
            Console.WriteLine("ERROR: The item to delete is the recurring master of the series. Deleting it will delete the entire series.");
            return false;
        }
        else
        {
            appointmentToDelete = recurringItem;
        }
    }
    else
    {
        if (deleteEntireSeries)
        {
            // The item passed is not the recurring master, but the caller
            // wants to delete the entire series. Bind to the recurring
            // master to delete it.
            try
            {
                appointmentToDelete = Appointment.BindToRecurringMaster(service, recurringItem.Id);
            }
            catch (Exception ex)
            {
                Console.WriteLine("ERROR: {0}", ex.Message);
                return false;
            }
        }
        else
        {
            // The item passed is not the recurring master, but the caller
            // only wants to delete the occurrence, so just
            // delete the passed item.
            appointmentToDelete = recurringItem;
        }
    }
    if (appointmentToDelete != null)
    {
        // Remove the item, depending on the scenario. 
        if (appointmentToDelete.IsMeeting)
        {
            CalendarActionResults results;
            // If it's a meeting and the user is the organizer, cancel it.
            // Determine this by testing the AppointmentState bitmask for 
            // the presence of the second bit. This bit indicates that the appointment
            // was received, which means that someone sent it to the user. Therefore,
            // they're not the organizer.
            int isReceived = 2;
            if ((appointmentToDelete.AppointmentState &amp; isReceived) == 0)
            {
                results = appointmentToDelete.CancelMeeting("Cancelling this meeting.");
                return true;
            }
            // If it's a meeting and the user is not the organizer, decline it.
            else
            {
                results = appointmentToDelete.Decline(true);
                return true;
            }
        }
        else
        {
            // The item isn't a meeting, so just delete it.
            appointmentToDelete.Delete(DeleteMode.MoveToDeletedItems);
            return true;
        }
    }
    return false;
}
```

若要使用此示例，您需要[绑定到事件或定期母版](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)，并将生成的**约会**对象传递给方法。 请记住，如果通过使用[CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)类访问约会，则生成的项目全部为单个事件。 相反，如果使用[ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)类，则生成的项目将是所有定期主控形状。 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>使用 EWS 删除定期约会

使用 EWS 删除定期系列与[删除单实例会议](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)相同。 事实上，SOAP 请求采用相同的格式。 此外，键是请求中使用的项 ID。 如果项目 ID 对应于定期母版，则整个系列将被删除。 如果项目 ID 对应于单个事件，则仅删除该事件。
  
> [!NOTE]
> 在下面的代码示例中，将缩短**ItemId**、 **ChangeKey**和**RecurringMasterId**属性以提高可读性。 
  
本示例将[CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx)与[CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx)元素一起使用，以取消用户为其组织者的会议。 [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx)元素的值指示要取消的项，可以是定期母版或单个事件的项目 ID。 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:NewBodyContent BodyType="HTML">Cancelling this meeting.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

本示例将**CreateItem 操作**与[DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx)元素一起使用，以拒绝用户不是其组织者的会议。 如上面的示例中所示， **ReferenceItemId**元素的值指示要拒绝的项目，可以是定期主实例或单个事件的项目 ID。 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:DeclineItem>
          <t:ReferenceItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
        </t:DeclineItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

此示例使用[DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)删除不包含与会者的约会的单个事件。 要删除的匹配项由[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx)元素指定，该元素由定期主控形状的项 ID 和事件发生的索引构成。 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

请注意，您可以通过将**OccurrenceItemId**元素替换为包含发生事件的项 ID 的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素来获取相同的结果，如图所示。 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>另请参阅


- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
- [在 Exchange 中使用 EWS 访问定期系列](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 创建定期系列](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 更新定期系列](how-to-update-a-recurring-series-by-using-ews.md)
    
- [在 Exchange 中使用 EWS 更新定期系列](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

