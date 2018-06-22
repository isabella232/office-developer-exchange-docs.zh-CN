---
title: 在 Exchange 使用 EWS 导出项目
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 导出约会、 电子邮件、 联系人、 任务和其他项目。
ms.openlocfilehash: 65b5b2ef1eba66877d5b6f6c3d4237a26a254196
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752778"
---
# <a name="export-items-by-using-ews-in-exchange"></a><span data-ttu-id="c7c39-103">在 Exchange 使用 EWS 导出项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-103">Export items by using EWS in Exchange</span></span>

<span data-ttu-id="c7c39-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 导出约会、 电子邮件、 联系人、 任务和其他项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-104">Learn how to export appointments, emails, contacts, tasks, and other items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="c7c39-105">使用 EWS 托管 API 的 EWS 中通过多种不同的方式，您可以从 Exchange 导出项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-105">You can export items from Exchange by using the EWS Managed API or EWS in a number of different ways.</span></span> <span data-ttu-id="c7c39-106">您使用的选项取决于：</span><span class="sxs-lookup"><span data-stu-id="c7c39-106">The option you use depends on:</span></span>
  
- <span data-ttu-id="c7c39-107">导出项类型。</span><span class="sxs-lookup"><span data-stu-id="c7c39-107">The item type that is exported.</span></span>
    
- <span data-ttu-id="c7c39-108">轻微保真所需维护 Exchange 中的项目状态和导出的项之间的程度。</span><span class="sxs-lookup"><span data-stu-id="c7c39-108">The degree of fidelity that you want maintained between the item state in Exchange and the exported item.</span></span>
    
- <span data-ttu-id="c7c39-109">导出项的格式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-109">The format of the exported item.</span></span>
    
- <span data-ttu-id="c7c39-110">任何后续处理的要求。</span><span class="sxs-lookup"><span data-stu-id="c7c39-110">Any post-processing requirements.</span></span>
    
- <span data-ttu-id="c7c39-111">是否要回 Exchange 导入该项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-111">Whether you want to import the item back into Exchange.</span></span>
    
<span data-ttu-id="c7c39-112">本文介绍如何使用每个不同选项的项目导出。</span><span class="sxs-lookup"><span data-stu-id="c7c39-112">This article shows you how to use each of the different options to export items.</span></span> <span data-ttu-id="c7c39-113">您可以使用任何选项批处理导出 Exchange 出的项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-113">You can use any option to batch export items out of Exchange.</span></span>
  
## <a name="export-an-item-into-a-custom-format"></a><span data-ttu-id="c7c39-114">将项目导出为自定义格式</span><span class="sxs-lookup"><span data-stu-id="c7c39-114">Export an item into a custom format</span></span>
<span data-ttu-id="c7c39-115"><a name="bk_exportcustom"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-115"></span></span>

<span data-ttu-id="c7c39-116">您可以使用[Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS 托管 API 方法调用的结果或解析为应用程序的要求适用于格式[执行 GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS 操作的结果。</span><span class="sxs-lookup"><span data-stu-id="c7c39-116">You can use the results of an [Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS Managed API method call or parse the results of a [GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS operation into a format that works with your application requirements.</span></span> <span data-ttu-id="c7c39-117">当项目导出才能将其导入数据库、.csv 文件或其他格式或系统，则使用此选项。</span><span class="sxs-lookup"><span data-stu-id="c7c39-117">Use this option when you are exporting items in order to import them into a database, .csv file, or another format or system.</span></span> <span data-ttu-id="c7c39-118">您甚至可保存项目的项目 EWS XML 形式因为许多系统具有 XML 分析功能这可能有用。</span><span class="sxs-lookup"><span data-stu-id="c7c39-118">You can even save the item in the form of the item EWS XML, which can be useful because many systems have XML parsing capability.</span></span> <span data-ttu-id="c7c39-119">我们建议您使用的**Item.Bind**方法或**GetItem**操作 （不带[Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性中） 的因为导出此选项使您能够控制哪些属性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-119">We recommend that you use the **Item.Bind** method or the **GetItem** operation (without the [Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property) because this option gives you control over which properties are exported.</span></span> 
  
## <a name="export-items-with-full-fidelity"></a><span data-ttu-id="c7c39-120">全保真方式导出项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-120">Export items with full fidelity</span></span>
<span data-ttu-id="c7c39-121"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-121"></span></span>

<span data-ttu-id="c7c39-122">如果您想要导出项目全保真方式，您可以使用[ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS 操作。</span><span class="sxs-lookup"><span data-stu-id="c7c39-122">If you want to export items with full fidelity, you can use the [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="c7c39-123">**ExportItems**操作将每个项目导出为数据流。</span><span class="sxs-lookup"><span data-stu-id="c7c39-123">The **ExportItems** operation exports each item as a data stream.</span></span> <span data-ttu-id="c7c39-124">此数据流不用于分析，但可以用作项目级备份可导入回 Exchange 邮箱。</span><span class="sxs-lookup"><span data-stu-id="c7c39-124">This data stream is not for parsing, but can be used as an item-level backup that can be imported back into an Exchange mailbox.</span></span> <span data-ttu-id="c7c39-125">虽然我们建议您在每个呼叫中包括不超过 100 个项目，您可以在每个**ExportItems**请求，包括多个项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-125">You can include many items in each **ExportItems** request, although we recommend that you include no more than 100 items in each call.</span></span> <span data-ttu-id="c7c39-126">因为 EWS 托管 API 不实现**ExportItems**操作，如果您使用 EWS 托管 API，您需要编写一个例程以发送 web 请求。</span><span class="sxs-lookup"><span data-stu-id="c7c39-126">Because the EWS Managed API does not implement the **ExportItems** operation, if you use the EWS Managed API, you'll need to write a routine to send the web requests.</span></span> <span data-ttu-id="c7c39-127">您可以选择使用[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法来获取有关项目的元数据，以便您能够索引和存储有关数据流信息。</span><span class="sxs-lookup"><span data-stu-id="c7c39-127">You can optionally use the [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get metadata about the item so that you can index and store information about the data stream.</span></span> 
  
<span data-ttu-id="c7c39-128">我们建议使用**ExportItems**操作您打算导入到 Exchange 邮箱的项目导出。</span><span class="sxs-lookup"><span data-stu-id="c7c39-128">We recommend that you use the **ExportItems** operation to export items that you plan to import into an Exchange mailbox.</span></span> 
  
<span data-ttu-id="c7c39-129">下面的示例演示如何使用**ExportItems**操作。</span><span class="sxs-lookup"><span data-stu-id="c7c39-129">The following example shows how to use the **ExportItems** operation.</span></span> <span data-ttu-id="c7c39-130">本示例中，将被截的项标识符的可读性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-130">In this example, the item identifier is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:ExportItems>
      <m:ItemIds>
        <t:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA="/>
      </m:ItemIds>
    </m:ExportItems>
  </soap:Body>
</soap:Envelope>
```

服务器响应一个[ExportItemsResponse](http://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx)元素，包括**NoError**，这表明已成功导出项目[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的**ExportItems**请求。 响应还包括导出的项目并包含导出的内容的数据流的项 ID。 <span data-ttu-id="c7c39-133">下面的示例演示 SOAP 正文包含导出的项目。</span><span class="sxs-lookup"><span data-stu-id="c7c39-133">The following example shows the SOAP body that contains the exported item.</span></span>
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:ExportItemsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:ItemId Id="AAMkAGYzZjZmRiUsidkC+NAAAAY89GAAA=" ChangeKey="FwAAAA=="/>
        <m:Data>
          AQAAAAgAAAAAAAAALgBlAHgAdABlAHMAdAAuAG0AaQBjAHIAbwBzAG8AZgB0AC4A
          cgAyAEAAYQB1AGoAaQBuAGcALQBkAG8AbQAuAGUAeAB0AGUAcwB0AC4AbQBpAGMAcgBvAHMA
          bwBmAHQALgBjAG8AbQAAAAMAADkAAAAAAwD+DwYAAAADAARAAwACQAMADkA=
        </m:Data>
      </m:ExportItemsResponseMessage>
     </m:ResponseMessages>
  </m:ExportItemsResponse>
</s:Body>
```

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a><span data-ttu-id="c7c39-134">使用 MIME 流导出到常见的文件格式</span><span class="sxs-lookup"><span data-stu-id="c7c39-134">Use the MIME stream to export into common file formats</span></span>
<span data-ttu-id="c7c39-135"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-135"></span></span>

<span data-ttu-id="c7c39-136">您可以使用[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作来获取项目的 MIME 表示形式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-136">You can use the [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS Managed API method or the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get a MIME representation of an item.</span></span> <span data-ttu-id="c7c39-137">由于 Exchange 不存储每个项目的 MIME 内容，它具有将每个项目的数据库表示形式转换为 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="c7c39-137">Because Exchange doesn't store the MIME content of each item, it has to convert the database representation of each item into the MIME stream.</span></span> <span data-ttu-id="c7c39-138">因为此转换会消耗大量资金，我们不建议这样做您请求大规模上的项目的 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="c7c39-138">Because this conversion is costly, we do not recommend that you request the MIME stream for items on a large scale.</span></span> <span data-ttu-id="c7c39-139">另请注意 MIME 流包含一组有限的属性。您可能需要考虑的其他选项，如果属性集不包含所需的属性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-139">Also note that the MIME stream contains a limited set of properties; you might have to consider other options if the property set doesn't contain the properties you need.</span></span> 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a><span data-ttu-id="c7c39-140">使用 EWS 托管 API 使用 MIME 流导出到.eml 和.mht 文件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="c7c39-140">Use the EWS Managed API to export an email into an .eml and .mht file by using the MIME stream</span></span>
<span data-ttu-id="c7c39-141"><a name="bk_exportemailmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-141"></span></span>

<span data-ttu-id="c7c39-142">Outlook 和其他常见的电子邮件应用程序可以打开 EML (.eml) 文件格式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-142">Outlook and other common email applications can open the EML (.eml) file format.</span></span> <span data-ttu-id="c7c39-143">下面的示例演示了如何使用 MIME 流，导出电子邮件并使用 MIME 流创建 EML 和 MIME HTML (.mht) 文件。</span><span class="sxs-lookup"><span data-stu-id="c7c39-143">The following example shows you how you can export an email by using the MIME stream, and use the MIME stream to create an EML and a MIME HTML (.mht) file.</span></span> <span data-ttu-id="c7c39-144">多个 web 浏览器支持的 MIME HTML 文件格式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-144">Many web browsers support the MIME HTML file format.</span></span> <span data-ttu-id="c7c39-145">此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7c39-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void ExportMIMEEmail(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    { 
        PropertySet props = new PropertySet(EmailMessageSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = EmailMessage.Bind(service, item.Id, props);
                
        string emlFileName = @"C:\export\email.eml";
        string mhtFileName = @"C:\export\email.mht";
        // Save as .eml.
        using (FileStream fs = new FileStream(emlFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
        // Save as .mht.
        using (FileStream fs = new FileStream(mhtFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a><span data-ttu-id="c7c39-146">使用 EWS 托管 API 使用 MIME 流导出到的 iCal 文件约会</span><span class="sxs-lookup"><span data-stu-id="c7c39-146">Use the EWS Managed API to export an appointment into an iCal file by using the MIME stream</span></span>
<span data-ttu-id="c7c39-147"><a name="bk_exporticalmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-147"></span></span>

<span data-ttu-id="c7c39-148">Outlook 和其他常见的日历应用程序可以打开 iCal (.ics) 文件格式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-148">Outlook and other common calendar applications can open the iCal (.ics) file format.</span></span> <span data-ttu-id="c7c39-149">下面的示例演示如何使用 MIME 流，导出为约会，并使用 MIME 流创建 iCal 文件。</span><span class="sxs-lookup"><span data-stu-id="c7c39-149">The following example shows you how to export an appointment by using the MIME stream, and use the MIME stream to create an iCal file.</span></span> <span data-ttu-id="c7c39-150">请注意与 MIME 数据流，包括与会者和附件相关的属性不导出的许多属性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-150">Note that many properties are not exported with the MIME stream, including attendees and attachment-related properties.</span></span> <span data-ttu-id="c7c39-151">您可以通过这些请求和将它们在 iCal 文件保存为私有扩展捕获从 EWS 其他属性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-151">You can capture other properties from EWS by requesting them and saving them in the iCal file as private extensions.</span></span> <span data-ttu-id="c7c39-152">这些私有扩展作为前缀与"x-"。</span><span class="sxs-lookup"><span data-stu-id="c7c39-152">These private extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="c7c39-153">此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7c39-153">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> <span data-ttu-id="c7c39-154">此示例还假定您具有主题为"2015年财务投影"约会日历文件夹中。</span><span class="sxs-lookup"><span data-stu-id="c7c39-154">This example also assumes that you have an appointment with the subject "2015 Financial Projections" in the calendar folder.</span></span> 
  
```cs
private static void ExportMIMEAppointment(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Calendar);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly); 
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems("subject:'2015 Financial Projections'", view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(AppointmentSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Appointment.Bind(service, item.Id, props);
        string iCalFileName = @"C:\export\appointment.ics";
        // Save as .ics.
        using (FileStream fs = new FileStream(iCalFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a><span data-ttu-id="c7c39-155">使用 EWS 托管 API 使用 MIME 流导出到一个 vCard 文件联系人</span><span class="sxs-lookup"><span data-stu-id="c7c39-155">Use the EWS Managed API to export a contact into a vCard file by using the MIME stream</span></span>
<span data-ttu-id="c7c39-156"><a name="bk_exportvcardmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-156"></span></span>

<span data-ttu-id="c7c39-157">Outlook 和其他常见的联系人管理应用程序可以打开 vCard (.vcf) 文件格式。</span><span class="sxs-lookup"><span data-stu-id="c7c39-157">Outlook and other common contact management applications can open the vCard (.vcf) file format.</span></span> <span data-ttu-id="c7c39-158">下面的示例演示如何使用 MIME 流，导出联系人并使用 MIME 流创建电子名片。</span><span class="sxs-lookup"><span data-stu-id="c7c39-158">The following example shows you how to export a contact by using the MIME stream, and use the MIME stream to create a vCard.</span></span> <span data-ttu-id="c7c39-159">您可以通过这些请求并将其保存捕获从 EWS 其他属性。</span><span class="sxs-lookup"><span data-stu-id="c7c39-159">You can capture other properties from EWS by requesting them and saving them in the .</span></span> <span data-ttu-id="c7c39-160">作为专用扩展电子名片。</span><span class="sxs-lookup"><span data-stu-id="c7c39-160">vCard as private extensions.</span></span> <span data-ttu-id="c7c39-161">这些扩展名为前缀与"x-"。</span><span class="sxs-lookup"><span data-stu-id="c7c39-161">These extensions are prefixed with "x-".</span></span> 
  
<span data-ttu-id="c7c39-162">此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7c39-162">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that the user can authenticate to an Exchange server.</span></span> 
  
```cs
private static void ExportMIMEContact(ExchangeService service)
{
    Folder inbox = Folder.Bind(service, WellKnownFolderName.Contacts);
    ItemView view = new ItemView(1);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly);
    // This results in a FindItem call to EWS.
    FindItemsResults<Item> results = inbox.FindItems(view);
    foreach (var item in results)
    {
        PropertySet props = new PropertySet(ContactSchema.MimeContent);
        // This results in a GetItem call to EWS.
        var email = Contact.Bind(service, item.Id, props);
        string vcfFileName = @"C:\export\contact.vcf";
        // Save as .vcf.
        using (FileStream fs = new FileStream(vcfFileName, FileMode.Create, FileAccess.Write))
        {
            fs.Write(email.MimeContent.Content, 0, email.MimeContent.Content.Length);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="c7c39-163">您不能使用**MimeContent**属性导入 vCard 文件。</span><span class="sxs-lookup"><span data-stu-id="c7c39-163">You cannot import vCard files by using the **MimeContent** property.</span></span> <span data-ttu-id="c7c39-164">您可以使用[Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS 托管 API 方法或[CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS 操作导入联系人。</span><span class="sxs-lookup"><span data-stu-id="c7c39-164">You can import contacts by using the [Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS Managed API method or the [CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS operation.</span></span> 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a><span data-ttu-id="c7c39-165">使用 EWS 使用 MIME 流导出任何项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-165">Use EWS to export any item by using the MIME stream</span></span>
<span data-ttu-id="c7c39-166"><a name="bk_exportewsmime"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-166"></span></span>

<span data-ttu-id="c7c39-167">使用**GetItem**操作获取项目的 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="c7c39-167">Use the **GetItem** operation to get the MIME stream of an item.</span></span> <span data-ttu-id="c7c39-168">以下**GetItem**请求演示如何请求的项目的 MIME 内容。</span><span class="sxs-lookup"><span data-stu-id="c7c39-168">The following **GetItem** request shows how to request the MIME content of an item.</span></span> 
  
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
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c7c39-169">下面的示例演示请求以获取 MIME 流的响应。</span><span class="sxs-lookup"><span data-stu-id="c7c39-169">The following example shows the response to a request to get the MIME stream.</span></span> <span data-ttu-id="c7c39-170">为便于阅读缩短了 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="c7c39-170">The MIME stream has been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
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
              <t:MimeContent CharacterSet="UTF-8">UmVjZ6IGZyb2b2suY29y5hMzgwZTA1YtDQo=</t:MimeContent>
              <t:ItemId Id="AAMkADEzYjJkLTYxMwB8GqYicWAAA=" ChangeKey="CQAAABzXv"/>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## 
<span data-ttu-id="c7c39-171"><a name="bk_exportfullfidelity"> </a></span><span class="sxs-lookup"><span data-stu-id="c7c39-171"></span></span>

<span data-ttu-id="c7c39-172">导出项目之后，您可能希望若要[导入到 Exchange 的项目](how-to-import-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="c7c39-172">After exporting items, you might want to [import items into Exchange](how-to-import-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7c39-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7c39-173">See also</span></span>


- [<span data-ttu-id="c7c39-174">导出和导入在 Exchange 中使用 EWS 的项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-174">Exporting and importing items by using EWS in Exchange</span></span>](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c7c39-175">在 Exchange 使用 EWS 导入项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-175">Import items by using EWS in Exchange</span></span>](how-to-import-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c7c39-176">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="c7c39-176">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c7c39-177">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c7c39-177">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

