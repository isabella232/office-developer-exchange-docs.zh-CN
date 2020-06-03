---
title: 使用 Exchange 中的 EWS 删除约会和取消会议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 42412265-3968-468a-a8c2-7e8af3c6deb9
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 删除约会和会议。
localization_priority: Priority
ms.openlocfilehash: 6a2fdaa357f4088da4bbd0643187d05a5bc51c0c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528130"
---
# <a name="delete-appointments-and-cancel-meetings-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 删除约会和取消会议

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 删除约会和会议。
  
会议和约会之间的基本区别在于会议具有与会者，而约会则不是。 约会和会议既可以是单个实例，也可以是定期系列的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。 在内部，Exchange 对会议和约会使用相同的对象。 您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx)元素来处理会议和约会。 
  
**表1。用于删除约会和会议的 EWS 托管 API 方法和 EWS 操作**

|**EWS 托管的 API 方法**|**EWS 操作**|**功能**|
|:-----|:-----|:-----|
|[约会. 删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |删除约会。  <br/> |
|[约会. 删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[CreateItem （日历项目）](../web-service-reference/createitem-operation-calendar-item.md) <br/> |删除会议。  <br/> |
   
请注意，使用 EWS 删除约会时，可以使用[DeleteItem](../web-service-reference/deleteitem-operation.md)操作，但在删除会议时，将使用[CreateItem](../web-service-reference/createitem-operation-calendar-item.md)操作。 这可能看起来 counterintuitive，但这是因为您必须创建一个会议响应对象才能向与会者发送会议取消邮件。 

<a name="bk_DeleteApptEWSMA"> </a>

## <a name="delete-an-appointment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除约会

下面的代码示例演示如何使用[delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)方法从 "日历" 文件夹中删除约会，并使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法通过在 "已删除邮件" 文件夹中查找约会来验证是否已将其删除。 
  
此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。 本地变量 `appointmentId` 是与现有约会相关联的标识符。 
  
```cs
// Instantiate an appointment object by binding to it by using the ItemId.
// As a best practice, limit the properties returned to only the ones you need.
Appointment appointment = Appointment.Bind(service, appointmentId, new PropertySet());
// Delete the appointment. Note that the item ID will change when the item is moved to the Deleted Items folder.
appointment.Delete(DeleteMode.MoveToDeletedItems);
// Verify that the appointment has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The appointment " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

本示例演示如何通过验证 "已删除项目" 文件夹中第一项的主题与已删除约会的主题相匹配，来验证是否已删除约会的简单方法。 如何选择验证是否已删除约会将根据您的应用程序的需要而有所不同。
  
正如您所看到的，删除约会非常简单，并且几乎可以预期。 注释当您创建 "已删除邮件" 文件夹中的约会项目与 "日历" 文件夹中的 "约会" 项目具有不同的 ItemId 时的验证步骤。 该项目将被复制和删除，而不只是移到 "已删除邮件" 文件夹。 
  
## <a name="delete-an-appointment-by-using-ews"></a>使用 EWS 删除约会
<a name="bk_DeleteApptEWSMA"> </a>

以下示例中的请求和响应 XML 对应于通过[使用 EWS 托管 Api 删除约会](#bk_DeleteApptEWSMA)中的 EWS 托管 api 代码进行的调用。 同时还会显示用于验证约会项目是否位于 "已删除邮件" 文件夹中的请求和响应 XML。
  
下面的示例演示用于删除约会的[DeleteItem](../web-service-reference/deleteitem-operation.md)操作的请求 XML。 
  
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
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示由[DeleteItem](../web-service-reference/deleteitem-operation.md)操作返回的响应 XML。 为提高可读性，将缩短**ItemId**和**ChangeKey**属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </m:DeleteItemResponse>
  </s:Body>
</s:Envelope>

```

下面的示例演示[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作的请求 XML，该操作检索 "已删除邮件" 文件夹中的第一项，以便将项目的主题与已删除的约会对象的主题进行比较。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages
" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示在验证步骤中由[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作返回的响应 XML。 
  
> [!NOTE]
> 为提高可读性，将缩短**ItemId**和**ChangeKey**属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10748" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA=" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Tennis lesson</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

<a name="bk_DeleteMtgEWSMA"> </a>

## <a name="delete-a-meeting-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除会议

当您删除会议时，除了从 "日历" 文件夹中删除约会项目之外，您可能还需要向与会者发送会议取消通知。 您可以使用以下三种方法取消会议：
  
- [约会. 删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)
    
- [CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)
    
- [CancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)
    
您选择的方法取决于您在取消邮件中需要提供的详细信息级别。 [CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)通过将更新的邮件作为参数传递，使您能够轻松地更新取消邮件。 [CancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)允许您在发送取消前修改邮件的属性，以便您可以执行类似请求回执的操作。 
  
本节中的代码示例演示了删除会议和发送会议取消的不同方法。 此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。 本地变量 `meetingId` 是与现有会议关联的标识符，其中目标用户是会议组织者。 
  
下面的代码示例演示如何使用[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)delete 方法删除会议。 
  
```cs
// Instantiate an appointment object for the meeting by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
            
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the Delete method.
meeting.Delete(DeleteMode.MoveToDeletedItems, SendCancellationsMode.SendToAllAndSaveCopy);
// Verify that the meeting has been deleted by looking for a matching subject in the Deleted Items folder's first entry.
ItemView itemView = new ItemView(1);
itemView.Traversal = ItemTraversal.Shallow;
// Just retrieve the properties you need.
itemView.PropertySet = new PropertySet(ItemSchema.Id, ItemSchema.ParentFolderId, ItemSchema.Subject);
// Note that the FindItems method results in a call to EWS.
FindItemsResults<Item> deletedItems = service.FindItems(WellKnownFolderName.DeletedItems, itemView);
Item deletedItem = deletedItems.First();
Folder parentFolder = Folder.Bind(service, deletedItem.ParentFolderId, new PropertySet(FolderSchema.DisplayName));
Console.WriteLine("The meeting " + "\"" + deletedItem.Subject + "\"" + " is now in the " + parentFolder.DisplayName + " folder.");

```

下面的代码示例演示如何使用[CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)方法删除会议。 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CancelMeeting method.
meeting.CancelMeeting("The outdoor meeting has been cancelled due to hailstorms.");

```

下面的代码示例演示如何使用[CreateCancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx)方法删除会议。 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CreateCancelMeetingMessage method.
CancelMeetingMessage cancelMessage = meeting.CreateCancelMeetingMessage();
cancelMessage.Body = new MessageBody("The outdoor meeting has been canceled due to hailstorms.");
cancelMessage.IsReadReceiptRequested = true;
cancelMessage.SendAndSaveCopy();

```

## <a name="delete-a-meeting-by-using-ews"></a>使用 EWS 删除会议
<a name="bk_EWSDeleteApptAndMeeting"> </a>

以下示例中的请求和响应 XML 对应于通过使用 "[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)" 的[ews 托管 api，通过使用 ews 托管 api 在删除会议时删除会议](#bk_DeleteMtgEWSMA)中的 ews 托管 api 代码进行的调用。 
  
下面的示例演示使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作向与会者发送取消邮件和删除会议时的请求 XML。 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkA" ChangeKey="DwAAA" />
          <t:NewBodyContent BodyType="HTML">The outdoor meeting has been canceled due to hailstorms.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示为响应用于删除会议的[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作请求而返回的 XML。 
  
> [!NOTE]
> 为提高可读性，将缩短**ItemId**和**ChangeKey**属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
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

下面的示例演示[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作的请求 XML，该操作检索 "已删除邮件" 文件夹中的第一项，以便将项目的主题与已删除的约会对象的主题进行比较。 
  
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
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemId" />
          <t:FieldURI FieldURI="item:ParentFolderId" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示在验证步骤中由[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作返回的 XML。 
  
> [!NOTE]
> 为了提高可读性， **Id**和**ChangeKey**属性被缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="800" MinorBuildNumber="5" Version="V2_6" 
 xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
 xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="10750" IncludesLastItemInRange="false">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkA" ChangeKey="DwAAA" />
                <t:ParentFolderId Id="AAMkA" ChangeKey="AQAAA" />
                <t:Subject>Team building exercise</t:Subject>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a>另请参阅

- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)    
- [使用 Exchange 2013 中的 EWS 创建约会和会议](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [使用 Exchange 中的 EWS 更新约会和会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [使用 Exchange 中的 EWS 建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) 
- [使用 Exchange 中的 EWS 建议新的会议时间](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

