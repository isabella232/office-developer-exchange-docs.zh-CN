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
# <a name="delete-appointments-and-cancel-meetings-by-using-ews-in-exchange"></a><span data-ttu-id="95a46-103">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="95a46-103">Delete appointments and cancel meetings by using EWS in Exchange</span></span>

<span data-ttu-id="95a46-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 删除约会和会议。</span><span class="sxs-lookup"><span data-stu-id="95a46-104">Learn how to delete appointments and meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="95a46-105">会议和约会之间的基本区别在于会议具有与会者，而约会则不是。</span><span class="sxs-lookup"><span data-stu-id="95a46-105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="95a46-106">约会和会议既可以是单个实例，也可以是定期系列的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。</span><span class="sxs-lookup"><span data-stu-id="95a46-106">Both appointments and meetings can be single instances or part of a recurring series, but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span> <span data-ttu-id="95a46-107">在内部，Exchange 对会议和约会使用相同的对象。</span><span class="sxs-lookup"><span data-stu-id="95a46-107">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="95a46-108">您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx)元素来处理会议和约会。</span><span class="sxs-lookup"><span data-stu-id="95a46-108">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/Title Topic ID Project Name Writer Editor Publish Preview.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="95a46-109">**表1。用于删除约会和会议的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="95a46-109">**Table 1. EWS Managed API methods and EWS operations for deleting appointments and meetings**</span></span>

|<span data-ttu-id="95a46-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="95a46-110">**EWS Managed API method**</span></span>|<span data-ttu-id="95a46-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="95a46-111">**EWS Operation**</span></span>|<span data-ttu-id="95a46-112">**功能**</span><span class="sxs-lookup"><span data-stu-id="95a46-112">**What it does**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95a46-113">约会. 删除</span><span class="sxs-lookup"><span data-stu-id="95a46-113">Appointment.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="95a46-114">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="95a46-114">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |<span data-ttu-id="95a46-115">删除约会。</span><span class="sxs-lookup"><span data-stu-id="95a46-115">Deletes an appointment.</span></span>  <br/> |
|[<span data-ttu-id="95a46-116">约会. 删除</span><span class="sxs-lookup"><span data-stu-id="95a46-116">Appointment.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="95a46-117">CreateItem （日历项目）</span><span class="sxs-lookup"><span data-stu-id="95a46-117">CreateItem (calendar item)</span></span>](../web-service-reference/createitem-operation-calendar-item.md) <br/> |<span data-ttu-id="95a46-118">删除会议。</span><span class="sxs-lookup"><span data-stu-id="95a46-118">Deletes a meeting.</span></span>  <br/> |
   
<span data-ttu-id="95a46-119">请注意，使用 EWS 删除约会时，可以使用[DeleteItem](../web-service-reference/deleteitem-operation.md)操作，但在删除会议时，将使用[CreateItem](../web-service-reference/createitem-operation-calendar-item.md)操作。</span><span class="sxs-lookup"><span data-stu-id="95a46-119">Note that when you delete an appointment by using EWS, you use the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation, but when you delete a meeting, you use the [CreateItem](../web-service-reference/createitem-operation-calendar-item.md) operation.</span></span> <span data-ttu-id="95a46-120">这可能看起来 counterintuitive，但这是因为您必须创建一个会议响应对象才能向与会者发送会议取消邮件。</span><span class="sxs-lookup"><span data-stu-id="95a46-120">This might seem counterintuitive, but it is because you have to create a meeting response object to send meeting cancellation messages to attendees.</span></span> 

<span data-ttu-id="95a46-121"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="95a46-121"><a name="bk_DeleteApptEWSMA"> </a></span></span>

## <a name="delete-an-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="95a46-122">使用 EWS 托管 API 删除约会</span><span class="sxs-lookup"><span data-stu-id="95a46-122">Delete an appointment by using the EWS Managed API</span></span>

<span data-ttu-id="95a46-123">下面的代码示例演示如何使用[delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)方法从 "日历" 文件夹中删除约会，并使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法通过在 "已删除邮件" 文件夹中查找约会来验证是否已将其删除。</span><span class="sxs-lookup"><span data-stu-id="95a46-123">The following code example shows how to use the [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method to delete an appointment from your calendar folder, and the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method to verify that the appointment was deleted by looking for it in the Deleted Items folder.</span></span> 
  
<span data-ttu-id="95a46-124">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="95a46-124">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="95a46-125">本地变量 `appointmentId` 是与现有约会相关联的标识符。</span><span class="sxs-lookup"><span data-stu-id="95a46-125">The local variable  `appointmentId` is an identifier associated with an existing appointment.</span></span> 
  
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

<span data-ttu-id="95a46-126">本示例演示如何通过验证 "已删除项目" 文件夹中第一项的主题与已删除约会的主题相匹配，来验证是否已删除约会的简单方法。</span><span class="sxs-lookup"><span data-stu-id="95a46-126">This example shows a simple way to verify that the appointment was deleted, by verifying that the subject of the first item in the Deleted Items folder matches that of the deleted appointment.</span></span> <span data-ttu-id="95a46-127">如何选择验证是否已删除约会将根据您的应用程序的需要而有所不同。</span><span class="sxs-lookup"><span data-stu-id="95a46-127">How you choose to verify that your appointment was deleted will vary based the needs of your application.</span></span>
  
<span data-ttu-id="95a46-128">正如您所看到的，删除约会非常简单，并且几乎可以预期。</span><span class="sxs-lookup"><span data-stu-id="95a46-128">As you can see, deleting an appointment is straightforward and pretty much what you might expect.</span></span> <span data-ttu-id="95a46-129">注释当您创建 "已删除邮件" 文件夹中的约会项目与 "日历" 文件夹中的 "约会" 项目具有不同的 ItemId 时的验证步骤。</span><span class="sxs-lookup"><span data-stu-id="95a46-129">Note when you create your verification step that the appointment item in the Deleted Items folder has a different ItemId than the appointment item in the calendar folder.</span></span> <span data-ttu-id="95a46-130">该项目将被复制和删除，而不只是移到 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="95a46-130">The item is copied and deleted rather than simply moved to the Deleted Items folder.</span></span> 
  
## <a name="delete-an-appointment-by-using-ews"></a><span data-ttu-id="95a46-131">使用 EWS 删除约会</span><span class="sxs-lookup"><span data-stu-id="95a46-131">Delete an appointment by using EWS</span></span>
<span data-ttu-id="95a46-132"><a name="bk_DeleteApptEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="95a46-132"><a name="bk_DeleteApptEWSMA"> </a></span></span>

<span data-ttu-id="95a46-133">以下示例中的请求和响应 XML 对应于通过[使用 EWS 托管 Api 删除约会](#bk_DeleteApptEWSMA)中的 EWS 托管 api 代码进行的调用。</span><span class="sxs-lookup"><span data-stu-id="95a46-133">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete an appointment by using the EWS Managed API](#bk_DeleteApptEWSMA).</span></span> <span data-ttu-id="95a46-134">同时还会显示用于验证约会项目是否位于 "已删除邮件" 文件夹中的请求和响应 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-134">The request and response XML that verifies that the appointment item is in the Deleted Items folder is shown as well.</span></span>
  
<span data-ttu-id="95a46-135">下面的示例演示用于删除约会的[DeleteItem](../web-service-reference/deleteitem-operation.md)操作的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-135">The following example shows the request XML for the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation to delete an appointment.</span></span> 
  
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

<span data-ttu-id="95a46-136">下面的示例演示由[DeleteItem](../web-service-reference/deleteitem-operation.md)操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-136">The following example shows the response XML that is returned by the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation.</span></span> <span data-ttu-id="95a46-137">为提高可读性，将缩短**ItemId**和**ChangeKey**属性。</span><span class="sxs-lookup"><span data-stu-id="95a46-137">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="95a46-138">下面的示例演示[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作的请求 XML，该操作检索 "已删除邮件" 文件夹中的第一项，以便将项目的主题与已删除的约会对象的主题进行比较。</span><span class="sxs-lookup"><span data-stu-id="95a46-138">The following example shows the request XML for the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
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

<span data-ttu-id="95a46-139">下面的示例演示在验证步骤中由[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作返回的响应 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-139">The following example shows the response XML that is returned by the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95a46-140">为提高可读性，将缩短**ItemId**和**ChangeKey**属性。</span><span class="sxs-lookup"><span data-stu-id="95a46-140">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="95a46-141"><a name="bk_DeleteMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="95a46-141"><a name="bk_DeleteMtgEWSMA"> </a></span></span>

## <a name="delete-a-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="95a46-142">使用 EWS 托管 API 删除会议</span><span class="sxs-lookup"><span data-stu-id="95a46-142">Delete a meeting by using the EWS Managed API</span></span>

<span data-ttu-id="95a46-143">当您删除会议时，除了从 "日历" 文件夹中删除约会项目之外，您可能还需要向与会者发送会议取消通知。</span><span class="sxs-lookup"><span data-stu-id="95a46-143">When you delete a meeting, in addition to removing the appointment item from the calendar folder, you might also want to send meeting cancellations to attendees.</span></span> <span data-ttu-id="95a46-144">您可以使用以下三种方法取消会议：</span><span class="sxs-lookup"><span data-stu-id="95a46-144">You can use the following three methods to cancel a meeting:</span></span>
  
- [<span data-ttu-id="95a46-145">约会. 删除</span><span class="sxs-lookup"><span data-stu-id="95a46-145">Appointment.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="95a46-146">CancelMeeting</span><span class="sxs-lookup"><span data-stu-id="95a46-146">Appointment.CancelMeeting</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="95a46-147">CancelMeetingMessage</span><span class="sxs-lookup"><span data-stu-id="95a46-147">CancelMeetingMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)
    
<span data-ttu-id="95a46-148">您选择的方法取决于您在取消邮件中需要提供的详细信息级别。</span><span class="sxs-lookup"><span data-stu-id="95a46-148">The method that you choose depends on the level of detail you need to provide in your cancellation message.</span></span> <span data-ttu-id="95a46-149">[CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)通过将更新的邮件作为参数传递，使您能够轻松地更新取消邮件。</span><span class="sxs-lookup"><span data-stu-id="95a46-149">[Appointment.CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) makes it easy to update the cancellation message by passing an updated message as a parameter.</span></span> <span data-ttu-id="95a46-150">[CancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx)允许您在发送取消前修改邮件的属性，以便您可以执行类似请求回执的操作。</span><span class="sxs-lookup"><span data-stu-id="95a46-150">[CancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.cancelmeetingmessage%28v=exchg.80%29.aspx) allows you to modify properties on your message before sending a cancellation, so you can do things like request a receipt.</span></span> 
  
<span data-ttu-id="95a46-151">本节中的代码示例演示了删除会议和发送会议取消的不同方法。</span><span class="sxs-lookup"><span data-stu-id="95a46-151">The code examples in this section show the different ways to delete a meeting and send meeting cancellations.</span></span> <span data-ttu-id="95a46-152">此示例假定您已通过 Exchange 服务器的身份验证，并获取了名为 "**服务**" 的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="95a46-152">The examples assume that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="95a46-153">本地变量 `meetingId` 是与现有会议关联的标识符，其中目标用户是会议组织者。</span><span class="sxs-lookup"><span data-stu-id="95a46-153">The local variable  `meetingId` is an identifier associated with an existing meeting where the target user is the meeting organizer.</span></span> 
  
<span data-ttu-id="95a46-154">下面的代码示例演示如何使用[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)delete 方法删除会议。</span><span class="sxs-lookup"><span data-stu-id="95a46-154">The following code example shows how to delete a meeting by using the [Appointment.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
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

<span data-ttu-id="95a46-155">下面的代码示例演示如何使用[CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)方法删除会议。</span><span class="sxs-lookup"><span data-stu-id="95a46-155">The following code example shows how to delete a meeting by using the [CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Instantiate an appointment object by binding to it using the ItemId.
// As a best practice, limit the properties returned to only the Appointment ID.
Appointment meeting = Appointment.Bind(service, meetingId, new PropertySet());
// Delete the meeting by using the CancelMeeting method.
meeting.CancelMeeting("The outdoor meeting has been cancelled due to hailstorms.");

```

<span data-ttu-id="95a46-156">下面的代码示例演示如何使用[CreateCancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx)方法删除会议。</span><span class="sxs-lookup"><span data-stu-id="95a46-156">The following code example shows how to delete a meeting by using the [Appointment.CreateCancelMeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.createcancelmeetingmessage%28v=exchg.80%29.aspx) method.</span></span> 
  
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

## <a name="delete-a-meeting-by-using-ews"></a><span data-ttu-id="95a46-157">使用 EWS 删除会议</span><span class="sxs-lookup"><span data-stu-id="95a46-157">Delete a meeting by using EWS</span></span>
<span data-ttu-id="95a46-158"><a name="bk_EWSDeleteApptAndMeeting"> </a></span><span class="sxs-lookup"><span data-stu-id="95a46-158"><a name="bk_EWSDeleteApptAndMeeting"> </a></span></span>

<span data-ttu-id="95a46-159">以下示例中的请求和响应 XML 对应于通过使用 "[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)" 的[ews 托管 api，通过使用 ews 托管 api 在删除会议时删除会议](#bk_DeleteMtgEWSMA)中的 ews 托管 api 代码进行的调用。</span><span class="sxs-lookup"><span data-stu-id="95a46-159">The request and response XML in the following examples correspond to calls made by the EWS Managed API code in [Delete a meeting by using the EWS Managed API](#bk_DeleteMtgEWSMA) by using the [Appointment.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="95a46-160">下面的示例演示使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作向与会者发送取消邮件和删除会议时的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-160">The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to send cancellation messages to attendees and delete a meeting.</span></span> 
  
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

<span data-ttu-id="95a46-161">下面的示例演示为响应用于删除会议的[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作请求而返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-161">The following example shows the XML that is returned in response to a [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation request used to delete a meeting.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95a46-162">为提高可读性，将缩短**ItemId**和**ChangeKey**属性。</span><span class="sxs-lookup"><span data-stu-id="95a46-162">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

<span data-ttu-id="95a46-163">下面的示例演示[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作的请求 XML，该操作检索 "已删除邮件" 文件夹中的第一项，以便将项目的主题与已删除的约会对象的主题进行比较。</span><span class="sxs-lookup"><span data-stu-id="95a46-163">The following example shows the request XML for the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation that retrieves the first item in the Deleted Items folder in order to compare the item's subject with that of the deleted appointment object.</span></span> 
  
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

<span data-ttu-id="95a46-164">下面的示例演示在验证步骤中由[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作返回的 XML。</span><span class="sxs-lookup"><span data-stu-id="95a46-164">The following example shows the XML that is returned by the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation during the verification step.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="95a46-165">为了提高可读性， **Id**和**ChangeKey**属性被缩短。</span><span class="sxs-lookup"><span data-stu-id="95a46-165">The **Id** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="95a46-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95a46-166">See also</span></span>

- [<span data-ttu-id="95a46-167">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="95a46-167">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)    
- [<span data-ttu-id="95a46-168">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="95a46-168">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)  
- [<span data-ttu-id="95a46-169">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="95a46-169">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="95a46-170">使用 Exchange 中的 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="95a46-170">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)  
- [<span data-ttu-id="95a46-171">使用 Exchange 中的 EWS 建议新的会议时间</span><span class="sxs-lookup"><span data-stu-id="95a46-171">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="95a46-172">使用 Exchange 中的 EWS 建议新的会议时间</span><span class="sxs-lookup"><span data-stu-id="95a46-172">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    

