---
title: 在 Exchange 中使用 EWS 作为代理访问日历
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来以委派方式访问日历。
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528291"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 作为代理访问日历

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来以委派方式访问日历。
  
您可以使用 EWS 托管 API 或 EWS 为用户委派对邮箱所有者的日历文件夹的访问权限。 然后，代理可以代表邮箱所有者创建会议请求、创建约会、响应会议请求以及检索、更新和删除邮箱所有者的 "日历" 文件夹中的会议，具体取决于他们的权限。
  
作为代理，您可以使用相同的方法和操作来访问邮箱所有者的 "日历" 文件夹，以便访问自己的 "日历" 文件夹。 主要区别在于，必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)来查找或创建日历项目或日历子文件夹，然后在确定项目 id 或文件夹 id 之后，可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除项目。 
  
**表1。用于将日历作为代理访问的 EWS 托管 API 方法和 EWS 操作**

|**如果您想要 .。。**|**使用此 EWS 托管 API 方法 .。。**|**使用此 EWS 操作 .。。**|
|:-----|:-----|:-----|
|以代理人的形式创建会议或约会  <br/> |在[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的情况下[保存。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|将多个会议或约会创建为代理人  <br/> |**FolderId**参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[CreateItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|搜索或查找作为代理的约会或会议  <br/> |**FolderId**参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[FindItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|将约会或会议作为代理获取  <br/> |[约会. 绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|将约会或会议更新为代理人  <br/> |接[下来是约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) [。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|将约会或会议作为代理删除  <br/> |接下来为 "约会" 的 "先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)"。[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> 在本文的代码示例中，primary@contoso.com 是邮箱所有者。 
  
## <a name="prerequisite-tasks"></a>先决条件任务
<a name="bk_prereq"> </a>

在用户可以将邮箱所有者的日历文件夹作为代理访问之前，必须将该用户[添加为具有](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的 "日历" 文件夹权限的代理。 
  
代理必须将邮箱附加到其帐户，才能更新邮箱所有者的日历。
  
如果代理只需要处理会议请求和响应，则可以将该代理添加到 "日历" 文件夹中，并使用默认的[MeetingRequestsDeliveryScope "DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS 托管 API 枚举值" 或 " [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) ews 元素值**DelegatesAndSendInformationToMe** " 将请求发送给邮箱所有者，并将信息消息发送给邮箱所有者。 然后，无需授予代理对邮箱所有者的收件箱文件夹的访问权限。 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 将会议或约会创建为代理人
<a name="bk_createewsma"> </a>

使用 EWS 托管 API，您可以使用代理用户的服务对象为邮箱所有者创建日历项目。 本示例演示如何使用[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法创建会议并向与会者发送会议请求。 
  
本示例假定**服务**是代理的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且已为委派授予对邮箱所有者的 "日历" 文件夹的适当权限。 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

请注意，保存项目时， [save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法调用必须标识邮箱所有者的 "日历" 文件夹。 如果未指定邮箱所有者的 "日历" 文件夹，则会将会议请求保存到代理的日历中，而不是邮箱所有者的 "日历" 文件夹中。 您可以通过两种方式将邮箱所有者的 "日历" 文件夹包含在**Save**方法调用中。 建议使用[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)和邮箱所有者的 SMTP 地址实例化[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)对象的新实例。 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

不过，您还可以先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)到 "日历" 文件夹，然后在**Save**方法调用中使用该文件夹的 ID。 但请注意，这会导致额外的 EWS 调用。 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>使用 EWS 创建会议或约会作为代理人
<a name="bk_createews"> </a>

EWS 使您可以使用委派用户的服务对象为邮箱所有者创建日历项目。 本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建会议并向与会者发送会议请求。 
  
这也是当您使用**Save**方法以[代理的形式创建会议或约会](#bk_createewsma)时，EWS 托管 API 发送的 XML 请求。
  
为简洁起见，已从以下示例中删除了 SOAP 标头。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功创建会议。 该响应还包含新创建的会议的项目 ID。
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 将会议或约会搜索为代理人
<a name="bk_searchewsma"> </a>

若要搜索会议，必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法之一，以便您可以指定邮箱所有者的 "日历" 文件夹。 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

在**FindItems**调用返回带有 ID 的响应之后，您可以使用 id 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该会议，而无需指定邮箱所有者的 SMTP 地址。 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a>使用 EWS 作为代理人搜索会议或约会
<a name="bk_searchews"> </a>

通过 EWS，您可以使用代理用户的服务对象来搜索符合一组搜索条件的约会和会议。 本示例演示如何使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作在邮箱所有者的 "日历" 文件夹中查找包含主题中包含 "建筑物" 一词的会议。 
  
这也是当您使用**FindItem**方法将[会议或约会作为代理搜索](#bk_searchewsma)时，EWS 托管 API 发送的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)邮件响应**FindItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功完成搜索。 响应包含符合搜索条件的任何约会或会议的[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) 。 在这种情况下，仅找到一个会议。 
  
为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

现在，您已拥有满足**条件的符合**条件，您可以使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该会议，而无需指定邮箱所有者的 SMTP 地址。 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取、更新或删除日历项目为代理人
<a name="bk_geteswma"> </a>

您可以使用 EWS 托管 API 来获取、更新或删除会议或约会，方式与您在不使用代理访问时执行这些操作的方式相同。 唯一的区别是，服务对象是代表委派用户的。 **Bind**方法调用中包含的项目 ID 在邮箱所有者的 "日历" 文件夹中唯一标识邮箱存储中的项目。 
  
**表2。用于将约会和会议作为代理使用的 EWS 托管 API 方法**

|**任务**|**EWS 托管的 API 方法**|**代码示例**|
|:-----|:-----|:-----|
|获取约会或会议  <br/> |[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|更新约会或会议  <br/> |先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 更新会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|删除约会或会议  <br/> |先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 删除会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a>使用 EWS 获取、更新或删除日历项目作为代理人
<a name="bk_getews"> </a>

您可以使用 EWS 获取、更新或删除会议或约会，方式与您在不使用代理访问时执行这些操作的方式相同。 唯一的区别是，服务对象是代表委派用户的。 [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)方法调用中包含的项目 ID 在邮箱所有者的 "日历" 文件夹中唯一标识邮箱存储中的项目。 
  
**表3。将约会和会议作为代理使用的 EWS 操作**

|**任务**|**EWS 操作**|**代码示例**|
|:-----|:-----|:-----|
|获取约会或会议  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[使用 EWS 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|更新约会或会议  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[使用 EWS 更新会议](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|删除约会或会议  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a>另请参阅

- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)   
- [使用 Exchange 中的 EWS 添加和删除委派](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [使用 Exchange 中的 EWS 为另一个用户设置文件夹权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    

