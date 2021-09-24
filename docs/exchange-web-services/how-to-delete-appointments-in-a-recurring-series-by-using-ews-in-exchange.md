---
title: 使用定期系列中的 EWS 删除定期系列中的Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: 了解如何使用 EWS 托管 API 或 EWS 在定期系列中删除Exchange。
ms.openlocfilehash: 8a68b6655c98f290d569a14dc0ac518c5d875cbe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513190"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a>使用定期系列中的 EWS 删除定期系列中的Exchange

了解如何使用 EWS 托管 API 或 EWS 在定期系列中删除Exchange。
  
您可以使用 EWS 托管 API 或 EWS 删除一系列约会或会议，或仅删除系列中的一个实例。 用于删除整个系列的过程实质上与用于删除单个事件的过程相同。 使用与用于删除单个实例约会或会议相同的 EWS 托管 API 方法或 EWS [操作](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)。 区别在于方法或操作中包含的项目 ID。 我们先看一下这两种方案是如何相同的。 
  
若要删除定期系列或定期系列中的单个事件，需要查找要删除的事件或系列，然后调用相应的方法或操作将其删除。 虽然只需删除任何类型的约会，但我们建议你使任何与会者或组织者保持最新状态，并取消用户组织的会议，并拒绝用户未组织的会议。
  
那么，这些方案会有所不同吗？ 它全部与用于调用 EWS 托管 API (的方法的 [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) 对象或 EWS 托管) API (操作请求中包含的项目 ID) 有关。 若要删除整个系列，您需要定期主控对象的 **Appointment** 对象或项目 ID。 若要删除一个匹配项，您需要该事件的 **Appointment** 对象或项目 ID。 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除定期约会

此示例假定你已对服务器Exchange身份验证，并且已获取名为 service 的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) **对象**。 _recurringItem_ 参数是定期主控对象或单个事件的 **Appointment** 对象。 _deleteEntireSeries_ 参数指示是否删除 _recurringItem_ 属于整个系列。 
  
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

为了使用此示例，您需要绑定到某个事件或定期 [主](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)控对象，然后将生成的 **Appointment** 对象传递给该方法。 请记住，如果使用 [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) 类访问约会，则生成的项目都是单个事件。 相反，如果使用 [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) 类，则生成的项目是所有定期主对象。 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a>使用 EWS 删除定期约会

使用 EWS 删除定期系列与删除单实例会议 [相同](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)。 实际上，SOAP 请求采用相同的格式。 同样，键是请求中使用的项目 ID。 如果项目 ID 对应于定期主控对象，将删除整个系列。 如果项目 ID 对应于单个匹配项，将仅删除该匹配项。
  
> [!NOTE]
> 在后续的代码示例中 **，ItemId、ChangeKey** 和 **RecurringMasterId** 属性已缩短为可读性。 
  
此示例使用 [CreateItem 操作](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 和 [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) 元素取消用户是组织者的会议。 [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx)元素的值指示要取消的项目，可以是定期主控项的项目 ID 或单个匹配项。 
  
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

此示例使用 **CreateItem 操作** 和 [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) 元素拒绝用户不是组织者的会议。 与上一示例一样 **，ReferenceItemId** 元素的值指示要拒绝的项目，可以是定期主控项的项目 ID 或单个匹配项。 
  
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

本示例使用 [DeleteItem 操作](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) 删除没有与会者的约会的单个事件。 要删除的事件由 [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) 元素指定，该元素根据定期主控项的项目 ID 和事件的索引构建。 
  
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

请注意，可以通过将 **OccurrenceItemId** 元素替换为包含匹配项的项目 ID 的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 元素获取相同的结果，如下所示。 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a>另请参阅


- [定期模式和 EWS](recurrence-patterns-and-ews.md)
    
- [使用 EWS 访问定期Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 创建定期Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [使用 EWS 更新定期系列](how-to-update-a-recurring-series-by-using-ews.md)
    
- [使用 EWS 更新定期系列Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [使用 2013 中的 EWS 创建约会Exchange会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [使用 Exchange 中的 EWS 删除约会和取消Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

