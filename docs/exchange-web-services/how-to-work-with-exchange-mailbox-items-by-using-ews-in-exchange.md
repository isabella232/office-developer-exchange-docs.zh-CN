---
title: 通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: 本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除项目。
ms.openlocfilehash: e70ac499da57faa60b4bcb6082648b23d1a7e791
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752908"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a>通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除项目。
  
您可以使用 EWS 托管 API 或 EWS 处理邮箱中的项目。 可以使用泛型项  EWS 托管 API [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象或 EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) 类型  来执行一些操作（获取某项或使用项的标识符删除项）；但是，大多数情况下您需要使用 [强类型项](folders-and-items-in-ews-in-exchange.md#bk_item)执行获取或更新操作，因为您将需要访问特定于强类型项的属性。 

例如，您无法使用泛型项检索某个项包含开始日期和结束日期的项 - 您需要一个 EWS 托管 API [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) 对象或 EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) 类型来执行此操作。 如果您正在使用 EWS 托管 API，您总是需要创建强类型项，因为泛型 **Item** 类没有构造函数。 如果您正在处理非强类型项，您始终可以使用基 **Item** 类来处理该项。 
  
**表 1. 用于处理项的 EWS 托管 API 方法和 EWS 操作**

|**若要...**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|创建泛型项  <br/> |无。您只能通过使用 EWS 托管 API 创建特定项类型；不能创建泛型项。  <br/> |[CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|获取项  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|更新项  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|删除项  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
在本文中，您将了解到何时可以使用泛型基类以及何时需要使用强类型项来完成您的任务。代码示例将演示如何使用基类，以及不能使用基类或它不符合您需求时应该怎么做。
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建项
<a name="bk_createewsma"> </a>

EWS 托管 API 没有公共构造函数用于 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 类，因此您必须使用您想要创建的特定项类型的构造函数来创建项。例如，使用 [EmailMessage 类构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx)来创建新的电子邮件，以及使用 [Contact 类构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)创建新联系人。同样，服务器从不在响应中返回泛型 **Item** 对象；所有泛型项作为 **EmailMessage** 对象返回。 
  
当您确定要创建的项的类型时，您只需几个步骤便可完成任务。所有项类型的步骤类似：
  
1. 初始化其中一个 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 类的新实例，使用 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象作为参数。 
    
2. 设置项上的属性。架构对于每个项类型不同，所以不同的项可用的属性不同。
    
3. 保存该项，或保存并发送该项。
    
例如，您可以创建 [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象，设置 [Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)、[Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) 和 [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) 属性，然后通过使用 [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法发送它。 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

若要了解如何使用 EWS 托管 API 创建会议或约会项目，请参阅[创建约会和会议使用 EWS 在 Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)。
  
## <a name="create-an-item-by-using-ews"></a>使用 EWS 创建项
<a name="bk_createews"> </a>

可以通过使用 EWS 创建泛型项或强类型项。所有项类型的步骤类似：
  
1. 使用 [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) 操作在 Exchange 存储中创建项。 
    
2. 使用 [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) 元素包含要创建的一个或多个项。 
    
3. 设置项上的属性。
    
例如，您可以创建电子邮件并通过在下面的示例中使用代码来发送电子邮件。这也是在您调用 [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法时 EWS 托管 API 发送的 XML 请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。 
  
若要了解如何使用 EWS 创建会议或约会项目，请参阅[创建约会和会议使用 EWS 在 Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)。
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取项
<a name="bk_getewsma"> </a>

若要使用 EWS 托管 API 来获取项目，如果您知道要检索的项的 [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) ，您只需调用该项上的一个 [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 方法，则会检索到该项。最佳做法是建议您限制仅返回所需的属性。此示例返回项 **Id** 属性和 **Subject** 属性。 
  
此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

如果您正在搜索满足特定条件的项，请执行以下操作：
  
1. 绑定到包含要获取的项的文件夹。
    
2. 实例化 [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) 或 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) 过滤要返回的项。 
    
3. 实例化 [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) 或 [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) 对象指定要返回的项数。 
    
4. 调用 [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 或 [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法。 
    
例如，如果您想要检索收件箱中未读的电子邮件，请在下面的示例中使用代码。此示例使用 **SearchFilterCollection** 将 **FindItems** 方法的结果限制为未读邮件，并限制 **ItemView** 以将结果限制为一个项。此特定代码仅适用于 [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象，因为 [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) 值属于 **SearchFilter** 。 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

或者，您可以使用 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 限制搜索结果，如以下代码示例中所示。此示例使用 [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法来检索在接下来的 30 天中发生的最多五个约会。当然，此代码仅适用于日历项。 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

请注意，服务器在 **Bind** 方法响应中返回的信息不同于服务器为 **FindItem** 或 **FindAppointment** 方法响应返回的信息。 **Bind** 方法可返回所有架构化属性，而 **FindItem** 和 **FindAppointment** 方法不会返回所有架构化属性。所以如果需要完全访问项，您将需要使用 **Bind** 方法。如果您不具备要检索的项的项 **Id** ，请使用 **FindItem** 或 **FindAppointment** 方法来检索 ID，然后使用 **Bind** 方法来检索所需的属性。 
  
若要了解如何使用 EWS 托管 API 获取会议或约会项目，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="get-an-item-by-using-ews"></a>使用 EWS 获取项
<a name="bk_getews"> </a>

如果您知道要检索的项的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)，您可以通过使用 [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) 操作获取项。 
  
下面的示例演示 XML 请求通过特定 [ItemId](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) 获取某项的 **"主题"**。这也是当在 [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 上调用 **Bind** 方法时 EWS 托管 API 发送的 XML 请求。为了方便读取，已缩短一些属性和元素的值。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

以下示例显示了服务器在处理 **GetItem** 操作后返回的 XML 响应。该响应指示项已成功检索。为了方便读取，已缩短某些属性和元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

如果您不知道要检索的项的 **ItemId**，您可以使用 [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) 操作来查找该项。为了使用 **FindItem** 操作，必须首先标识要搜索的文件夹。您可以通过使用其 **DistinguinguishedFolderName** 或使用 [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 标识该文件夹。您可以使用 [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) 或 [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作来获取您需要的 **FolderId**。然后使用 **FindItem** 操作来搜索该文件夹中与搜索筛选器匹配的结果。与 EWS 托管 API 不同，EWS 不提供单独的约会查找操作。 **FindItem** 操作会检索所有类型的项。 
  
下面的示例演示 XML **FindItem** 操作请求发送到服务器以查找在接下来的 30 天内出现的日历文件夹中的约会。为了方便读取，已缩短一些属性和元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

服务器通过包含 **NoError** 的 [ResponseCode](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) 值的 [ FindItemResponse ](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 消息响应 **FindItem** 请求，该值指示操作已成功完成。如果任意日历项符合过滤条件，则它们将会包括在响应中。
  
请注意，服务器在 **GetItem** 操作响应中返回的信息不同于服务器在 **FindItem** 或 **FindAppointment** 操作响应中返回的信息。 **GetItem** 方法可返回所有架构化属性，而 **FindItem** 和 **FindAppointment** 操作不会返回所有架构化属性。所以，如果您需要对项进行完全访问，您将需要使用 **GetItem** 操作。如果您不具备要检索的项的 **ItemId**，请使用 **FindItem** 或 **FindAppointment** 操作来检索 **ItemId**，然后使用 **GetItem** 操作来检索所需的元素。 
  
若要了解如何使用 EWS 获取会议或约会项目，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新项
<a name="bk_updateewsma"> </a>

通过 EWS 托管 API 更新项的步骤对于所有项类型是相似的；但是，项属性对于每种项类型是不同的，[Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) 方法具有许多可选择的过载方法。要更新项，请执行以下操作： 
  
1. 使用 [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 方法获取最新版本的项，除非已经拥有该项。若要更新特定于某个强类型项的属性，您需要绑定到该项类型。若要更新可用的泛型项类型上可用的属性，您可以绑定到 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象。 
    
2. 更新项上的属性。
    
3. 调用 **Update** 方法。 
    
例如，可以使用泛型项类型更新某个电子邮件的主题，如下面的示例代码中所示。
  
此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

若要了解如何使用 EWS 托管 API 更新会议或约会项目，请参阅[更新约会和会议使用 EWS 在 Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="update-an-item-by-using-ews"></a>使用 EWS 更新项
<a name="bk_updateews"> </a>

要通过 EWS 更新某项，请执行以下操作：
  
1. 使用 [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) 操作获取最新版本的项，除非已拥有该项。 
    
2. 使用 [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) 操作来指定字段，以更新并将新值分配给这些字段。 
    
下面的示例显示了发送给服务器以更新电子邮件 **"主题"** 值的 XML [UpdateItem](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) 操作请求。为了方便读取，已缩短一些属性和元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **UpdateItemResponse** 邮件响应 [UpdateItem](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) 请求，该邮件中包括 [NoError](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 的 **ResponseCode** 值，该值表示项更新成功。
  
若要了解如何使用 EWS 更新会议或约会项目，请参阅[更新约会和会议使用 EWS 在 Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除项
<a name="bk_deleteewsma"> </a>

您可以通过将项移动到已删除项文件夹或垃圾站来删除项。如果您知道要删除的项的 [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)，只需调用该项的 [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) 方法。 
  
如果您需要在删除项之前找到它，请执行以下操作：
  
1. 调用 [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 或 [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法找到要删除的项。 
    
1. 实例化 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) 并将其限制为要返回的属性，或者使用 [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) 查找特定项。 
    
2. 实例化 [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) 或 [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) 指定要返回的项数。 
    
2. 调用 [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) 方法。 
    
例如，下面的代码演示如何将电子邮件移动到已删除项文件夹。
  
此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

有关删除项的更多详细信息，请参阅[通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)。 若要了解如何使用 EWS 托管 API 删除会议或约会项目，请参阅[删除约会和取消在 Exchange 使用 EWS 的会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)。
  
## <a name="delete-an-item-by-using-ews"></a>使用 EWS 删除项
<a name="bk_deleteews"> </a>

您可以通过使用 [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) 操作删除项。 
  
下面的示例显示了发送给服务器以将电子邮件移动到已删除项文件夹的 XML 请求。为了方便读取，已缩短一些属性和元素的值。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **DeleteItemResponse** 邮件响应 [DeleteItem](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) 请求，该邮件中包括 [NoError](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 的 **ResponseCode** 值，该值表示项删除成功。
  
有关删除项的更多详细信息，请参阅[通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)。 若要了解如何使用 EWS 删除会议或约会项目，请参阅[删除约会和取消在 Exchange 使用 EWS 的会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)。
  
## <a name="move-or-copy-items-to-another-mailbox"></a>将项移动或复制到另一个邮箱
<a name="bk_movecopybtnmailboxes"> </a>

您可以使用 [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) 和 [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) 操作在邮件之间移动或复制项。若要了解更多信息，请参阅 [导出和导入 Exchange 中使用 EWS 的项目](exporting-and-importing-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅

- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)    
- [在 Exchange 使用 EWS 使用文件夹](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)
    

