---
title: 使用 Exchange 中的 EWS 导入项目
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 导入约会、电子邮件、联系人、任务和其他项目。
ms.openlocfilehash: bc874c667c31beb4e59a305626247488cb1a1781
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527983"
---
# <a name="import-items-by-using-ews-in-exchange"></a><span data-ttu-id="ea03c-103">使用 Exchange 中的 EWS 导入项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-103">Import items by using EWS in Exchange</span></span>

<span data-ttu-id="ea03c-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 导入约会、电子邮件、联系人、任务和其他项目。</span><span class="sxs-lookup"><span data-stu-id="ea03c-104">Learn how to import appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ea03c-105">许多系统包含约会、电子邮件、联系人和任务，您可以通过多种不同的方式将这些项目导入到 Exchange 中。</span><span class="sxs-lookup"><span data-stu-id="ea03c-105">Many systems contain appointments, emails, contacts, and tasks, and you can import those items into Exchange in a number of different ways.</span></span> <span data-ttu-id="ea03c-106">在这些项目上不维护邮箱关系时，将项目导入 Exchange 非常简单。</span><span class="sxs-lookup"><span data-stu-id="ea03c-106">Importing items into Exchange is simple when mailbox relationships aren't maintained on those items.</span></span> <span data-ttu-id="ea03c-107">您可以使用[项目。保存](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)EWS 托管 API 方法或[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作以在 Exchange 邮箱中创建项目。</span><span class="sxs-lookup"><span data-stu-id="ea03c-107">You can use the [Item.Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to create the items in an Exchange mailbox.</span></span> <span data-ttu-id="ea03c-108">不过，简单方法不支持所有方案;例如：</span><span class="sxs-lookup"><span data-stu-id="ea03c-108">The simple approach does not support all scenarios, however; for example:</span></span> 
  
- <span data-ttu-id="ea03c-109">在使用与会者（会议）导入约会时，不能维护组织者和与会者之间的关系。</span><span class="sxs-lookup"><span data-stu-id="ea03c-109">You cannot maintain the relationship between organizers and attendees when importing appointments with attendees (meetings).</span></span> <span data-ttu-id="ea03c-110">这意味着会议组织者需要将会议邀请重新发送给与会者，以便在组织者和与会者之间重新建立关系。</span><span class="sxs-lookup"><span data-stu-id="ea03c-110">This means that the meeting organizer will need to resend meeting invites to attendees in order to reestablish the relationship between the organizer and attendees.</span></span> <span data-ttu-id="ea03c-111">如果约会已导入与会者的日历中，则约会将不与会议组织者的约会相关联。</span><span class="sxs-lookup"><span data-stu-id="ea03c-111">If the appointment was imported into an attendee's calendar, the appointment will not be related to the meeting organizer's appointment.</span></span> <span data-ttu-id="ea03c-112">与会者需要接受来自组织者的重发会议邀请，以便重新建立组织者-与会者关系。</span><span class="sxs-lookup"><span data-stu-id="ea03c-112">The attendees will need to accept the resent meeting invite from the organizer in order to reestablish the organizer-attendee relationship.</span></span>
    
- <span data-ttu-id="ea03c-113">导入分配的任务时，不会保留工作负责人的相关信息。</span><span class="sxs-lookup"><span data-stu-id="ea03c-113">Information about the assignees is not preserved when assigned tasks are imported.</span></span>
    
<span data-ttu-id="ea03c-114">所有导入选项均可用于将项目批量导入到 Exchange。</span><span class="sxs-lookup"><span data-stu-id="ea03c-114">All the import options can be used to batch import items into Exchange.</span></span>
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a><span data-ttu-id="ea03c-115">使用 EWS 托管 API 或 EWS 项类型导入项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-115">Use EWS Managed API or EWS item types to import an item</span></span>
<span data-ttu-id="ea03c-116"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="ea03c-116"><a name="bk_importproperties"> </a></span></span>

<span data-ttu-id="ea03c-117">您可以使用 EWS 托管 API 或 EWS 从其他系统中导入电子邮件、联系人、约会或任务。</span><span class="sxs-lookup"><span data-stu-id="ea03c-117">You can use the EWS Managed API or EWS to import emails, contacts, appointments, or tasks from other systems.</span></span> <span data-ttu-id="ea03c-118">根据您要导入的内容，只需根据您要导入的内容，在下列任何对象上设置源格式的[属性](properties-and-extended-properties-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="ea03c-118">Just set the [properties ](properties-and-extended-properties-in-ews-in-exchange.md) from your source format on any of the following objects, depending on what you're importing.</span></span> 
  
<span data-ttu-id="ea03c-119">**表1。EWS 托管 API 对象和 EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="ea03c-119">**Table 1. EWS Managed API objects and EWS elements**</span></span>

|<span data-ttu-id="ea03c-120">**EWS 托管 API 对象**</span><span class="sxs-lookup"><span data-stu-id="ea03c-120">**EWS Managed API object**</span></span>|<span data-ttu-id="ea03c-121">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="ea03c-121">**EWS element**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea03c-122">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="ea03c-122">EmailMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ea03c-123">消息</span><span class="sxs-lookup"><span data-stu-id="ea03c-123">Message</span></span>](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="ea03c-124">联系人</span><span class="sxs-lookup"><span data-stu-id="ea03c-124">Contact</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ea03c-125">联系人</span><span class="sxs-lookup"><span data-stu-id="ea03c-125">Contact</span></span>](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="ea03c-126">约会</span><span class="sxs-lookup"><span data-stu-id="ea03c-126">Appointment</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ea03c-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ea03c-127">CalendarItem</span></span>](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[<span data-ttu-id="ea03c-128">任务</span><span class="sxs-lookup"><span data-stu-id="ea03c-128">Task</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ea03c-129">任务</span><span class="sxs-lookup"><span data-stu-id="ea03c-129">Task</span></span>](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="ea03c-130">使用[项目。保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)EWS 托管 API 方法或[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作以执行项的导入。</span><span class="sxs-lookup"><span data-stu-id="ea03c-130">Use the [Item.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to perform the import of items.</span></span> <span data-ttu-id="ea03c-131">当您从其他系统导入项目时，我们建议采用这种方法，因为您可以控制要导入哪些属性。</span><span class="sxs-lookup"><span data-stu-id="ea03c-131">We recommend this approach when you're importing items from other systems because you have control over which properties get imported.</span></span> <span data-ttu-id="ea03c-132">有关如何设置项目属性并保存项目的详细信息，请参阅[使用 Ews 托管 API 创建项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma)或[使用 ews 创建项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews)。</span><span class="sxs-lookup"><span data-stu-id="ea03c-132">For more information about how to set properties on items and then save the item, see [Create an item by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma) or [Create an item by using EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews).</span></span>
  
## <a name="import-items-with-full-fidelity"></a><span data-ttu-id="ea03c-133">以完全保真导入项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-133">Import items with full fidelity</span></span>
<span data-ttu-id="ea03c-134"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="ea03c-134"><a name="bk_importproperties"> </a></span></span>

<span data-ttu-id="ea03c-135">您可以使用[UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS 操作以数据流形式上传项目。</span><span class="sxs-lookup"><span data-stu-id="ea03c-135">You can use the [UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS operation to upload an item as a data stream.</span></span> <span data-ttu-id="ea03c-136">项目的此数据流表示形式必须来自[ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)操作调用的结果。</span><span class="sxs-lookup"><span data-stu-id="ea03c-136">This data stream representation of an item has to come from the results of an [ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) operation call.</span></span> <span data-ttu-id="ea03c-137">由于 EWS 托管 API 不实现**UploadItems**操作，因此如果使用 EWS 托管 api，您需要编写一个例程来发送 web 请求。</span><span class="sxs-lookup"><span data-stu-id="ea03c-137">Because the EWS Managed API does not implement the **UploadItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> 
  
<span data-ttu-id="ea03c-138">这是导入已从其他 Exchange 服务器导出的项目的最简单方法。</span><span class="sxs-lookup"><span data-stu-id="ea03c-138">This is the easiest way to import items that have been exported from another Exchange server.</span></span>
  
<span data-ttu-id="ea03c-139">在下面的示例中，将缩短标识符和**数据**元素内容以提高可读性。</span><span class="sxs-lookup"><span data-stu-id="ea03c-139">In the following example, the identifiers and the **Data** element content are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1"/>
  </soap:Header>
  <soap:Body>
    <m:UploadItems>
      <m:Items>
        <t:Item CreateAction="CreateNew">
          <t:ParentFolderId  Id="AAMkADEzOTE7kV0AAA=" ChangeKey="AQAAAA=="/>
          <t:Data>AQAAAAgAAAAAAQAAAAADABZADQASDkANABMO</t:Data>
        </t:Item>
      </m:Items>
    </m:UploadItems>
  </soap:Body>
</soap:Envelope>
```

服务器使用[UploadItemsResponse](https://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx)元素响应**UploadItems**请求，该元素包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功上载项目。 <span data-ttu-id="ea03c-141">该响应还包括已上载项的项 ID。</span><span class="sxs-lookup"><span data-stu-id="ea03c-141">The response also includes the item ID of the uploaded item.</span></span> 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a><span data-ttu-id="ea03c-142">使用 MIME 流从常见文件格式导入</span><span class="sxs-lookup"><span data-stu-id="ea03c-142">Use the MIME stream to import from common file formats</span></span>
<span data-ttu-id="ea03c-143"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="ea03c-143"><a name="bk_importproperties"> </a></span></span>

<span data-ttu-id="ea03c-144">EWS 可以导入 .EML （.eml）和 iCal （ics）文件。</span><span class="sxs-lookup"><span data-stu-id="ea03c-144">EWS can import EML (.eml) and iCal (.ics) files.</span></span> <span data-ttu-id="ea03c-145">你将需要测试你的 MIME 内容，以了解 Exchange MIME 分析器如何处理你的 MIME 流的内容。</span><span class="sxs-lookup"><span data-stu-id="ea03c-145">You'll want to test your MIME content to see how the Exchange MIME parser handles the content of your MIME stream.</span></span> <span data-ttu-id="ea03c-146">虽然使用 MIME 流非常方便，但通常更好的做法是[使用 EWS 托管 API 或 EWS 项类型导入项目](#bk_importproperties)。</span><span class="sxs-lookup"><span data-stu-id="ea03c-146">Although using the MIME stream is convenient, it is typically better to [Use EWS Managed API or EWS item types to import an item](#bk_importproperties).</span></span> <span data-ttu-id="ea03c-147">下面的示例展示了如何[导入电子名片](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50)。</span><span class="sxs-lookup"><span data-stu-id="ea03c-147">Here's an example of how to [import a vCard](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50).</span></span>
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a><span data-ttu-id="ea03c-148">使用 EWS 托管 API 通过 MIME 流从 .EML 文件导入电子邮件</span><span class="sxs-lookup"><span data-stu-id="ea03c-148">Use the EWS Managed API to import an email from an EML file by using the MIME stream</span></span>

<span data-ttu-id="ea03c-149">下面的示例演示如何使用 .EML 文件的内容设置[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性，然后将该电子邮件导入到邮箱中。</span><span class="sxs-lookup"><span data-stu-id="ea03c-149">The following example shows how to set the [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property with the contents of an EML file and then import the email into a mailbox.</span></span> <span data-ttu-id="ea03c-150">本示例还演示如何对导入的电子邮件设置[PidTagMessageFlags （0x0E07）](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx)扩展属性，使其不会在邮箱中显示为草稿项目。</span><span class="sxs-lookup"><span data-stu-id="ea03c-150">This example also shows how to set the [PidTagMessageFlags (0x0E07)](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx) extended property on an imported email so that it doesn't appear in the mailbox as a draft item.</span></span> <span data-ttu-id="ea03c-151">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以向 Exchange 服务器进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="ea03c-151">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void UploadMIMEEmail(ExchangeService service)
{
    EmailMessage email = new EmailMessage(service);
    
    string emlFileName = @"C:\import\email.eml";
    using (FileStream fs = new FileStream(emlFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .eml file to the MimeContent property.
        email.MimeContent = new MimeContent("UTF-8", bytes);
    }
    
    // Indicate that this email is not a draft. Otherwise, the email will appear as a 
    // draft to clients.
    ExtendedPropertyDefinition PR_MESSAGE_FLAGS_msgflag_read = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
    email.SetExtendedProperty(PR_MESSAGE_FLAGS_msgflag_read, 1);
    // This results in a CreateItem call to EWS. The email will be saved in the Inbox folder.
    email.Save(WellKnownFolderName.Inbox);
}
```

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="ea03c-152">使用 EWS 托管 API 通过 MIME 流从 iCal 文件中导入约会</span><span class="sxs-lookup"><span data-stu-id="ea03c-152">Use the EWS Managed API to import an appointment from an iCal file by using the MIME stream</span></span>

<span data-ttu-id="ea03c-153">您可以使用 MIME 流，以 iCalendar 文件的形式导入简单约会。</span><span class="sxs-lookup"><span data-stu-id="ea03c-153">You can import simple appointments in the form of iCalendar files by using the MIME stream.</span></span> <span data-ttu-id="ea03c-154">您无法导入会议，这是与会者的约会，因为必须将会议组织者和与会者之间的关系设置为[Exchange 日历](calendars-and-ews-in-exchange.md)工作流的一部分。</span><span class="sxs-lookup"><span data-stu-id="ea03c-154">You can't import meetings, which are appointments with attendees, because the relationship between meeting organizers and attendees has to be set as part of the [Exchange calendaring](calendars-and-ews-in-exchange.md) workflow.</span></span> <span data-ttu-id="ea03c-155">无法在 MIME 流中捕获与会者。</span><span class="sxs-lookup"><span data-stu-id="ea03c-155">Attendees cannot be captured in the MIME stream.</span></span> 
  
<span data-ttu-id="ea03c-156">下面的代码示例演示如何将简单的文件导入到用户的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="ea03c-156">The following code example shows you how to import a simple .ics file into a user's mailbox.</span></span>
  
```cs
private static void UploadMIMEAppointment(ExchangeService service)
{
    Appointment appointment = new Appointment(service);
    string iCalFileName = @"C:\import\appointment.ics";
    using (FileStream fs = new FileStream(iCalFileName, FileMode.Open, FileAccess.Read))
    {
        byte[] bytes = new byte[fs.Length];
        int numBytesToRead = (int)fs.Length;
        int numBytesRead = 0;
        while (numBytesToRead > 0)
        {
            int n = fs.Read(bytes, numBytesRead, numBytesToRead);
            if (n == 0)
                break;
            numBytesRead += n;
            numBytesToRead -= n;
        }
        // Set the contents of the .ics file to the MimeContent property.
        appointment.MimeContent = new MimeContent("UTF-8", bytes);
    }
    // This results in a CreateItem call to EWS. 
    appointment.Save(WellKnownFolderName.Calendar);
}
```

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a><span data-ttu-id="ea03c-157">使用 EWS 通过 MIME 流导入项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-157">Use EWS to import an item by using the MIME stream</span></span>

<span data-ttu-id="ea03c-158">您可以使用[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作，使用 MIME 流导入 .Eml 和 iCal 项。</span><span class="sxs-lookup"><span data-stu-id="ea03c-158">You can use the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation to import EML and iCal items by using their MIME stream.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body >
    <m:CreateItem>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </m:SavedItemFolderId> 
        <m:Items>
        <t:Message>
          <t:MimeContent CharacterSet="UTF-8">
            <!-- Insert MIME content here-->
          </t:MimeContent>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="ea03c-159">后续步骤</span><span class="sxs-lookup"><span data-stu-id="ea03c-159">Next steps</span></span>
<span data-ttu-id="ea03c-160"><a name="bk_importproperties"> </a></span><span class="sxs-lookup"><span data-stu-id="ea03c-160"><a name="bk_importproperties"> </a></span></span>

<span data-ttu-id="ea03c-161">将项目导入邮箱后，您可能需要[创建一个自定义文件夹来存储导入的项目](how-to-work-with-folders-by-using-ews-in-exchange.md)，或[同步您的客户端和邮箱项目](mailbox-synchronization-and-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="ea03c-161">After you import items into a mailbox, you might want to [create a custom folder to store your imported items](how-to-work-with-folders-by-using-ews-in-exchange.md), or [synchronize your client and mailbox items](mailbox-synchronization-and-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ea03c-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ea03c-162">See also</span></span>


- [<span data-ttu-id="ea03c-163">使用 Exchange 中的 EWS 导出和导入项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-163">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ea03c-164">使用 Exchange 中的 EWS 导出项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-164">Export items by using EWS in Exchange</span></span>](how-to-export-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ea03c-165">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="ea03c-165">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="ea03c-166">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="ea03c-166">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

