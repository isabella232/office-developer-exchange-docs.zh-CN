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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752778"
---
# <a name="export-items-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 导出项目

了解如何在 Exchange 使用 EWS 托管 API 或 EWS 导出约会、 电子邮件、 联系人、 任务和其他项目。
  
使用 EWS 托管 API 的 EWS 中通过多种不同的方式，您可以从 Exchange 导出项目。 您使用的选项取决于：
  
- 导出项类型。
    
- 轻微保真所需维护 Exchange 中的项目状态和导出的项之间的程度。
    
- 导出项的格式。
    
- 任何后续处理的要求。
    
- 是否要回 Exchange 导入该项目。
    
本文介绍如何使用每个不同选项的项目导出。 您可以使用任何选项批处理导出 Exchange 出的项目。
  
## <a name="export-an-item-into-a-custom-format"></a>将项目导出为自定义格式
<a name="bk_exportcustom"> </a>

您可以使用[Item.Bind](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) EWS 托管 API 方法调用的结果或解析为应用程序的要求适用于格式[执行 GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS 操作的结果。 当项目导出才能将其导入数据库、.csv 文件或其他格式或系统，则使用此选项。 您甚至可保存项目的项目 EWS XML 形式因为许多系统具有 XML 分析功能这可能有用。 我们建议您使用的**Item.Bind**方法或**GetItem**操作 （不带[Item.MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性中） 的因为导出此选项使您能够控制哪些属性。 
  
## <a name="export-items-with-full-fidelity"></a>全保真方式导出项目
<a name="bk_exportfullfidelity"> </a>

如果您想要导出项目全保真方式，您可以使用[ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS 操作。 **ExportItems**操作将每个项目导出为数据流。 此数据流不用于分析，但可以用作项目级备份可导入回 Exchange 邮箱。 虽然我们建议您在每个呼叫中包括不超过 100 个项目，您可以在每个**ExportItems**请求，包括多个项目。 因为 EWS 托管 API 不实现**ExportItems**操作，如果您使用 EWS 托管 API，您需要编写一个例程以发送 web 请求。 您可以选择使用[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法来获取有关项目的元数据，以便您能够索引和存储有关数据流信息。 
  
我们建议使用**ExportItems**操作您打算导入到 Exchange 邮箱的项目导出。 
  
下面的示例演示如何使用**ExportItems**操作。 本示例中，将被截的项标识符的可读性。 
  
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

服务器响应一个[ExportItemsResponse](http://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx)元素，包括**NoError**，这表明已成功导出项目[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的**ExportItems**请求。 响应还包括导出的项目并包含导出的内容的数据流的项 ID。 下面的示例演示 SOAP 正文包含导出的项目。
  
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

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a>使用 MIME 流导出到常见的文件格式
<a name="bk_exportfullfidelity"> </a>

您可以使用[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) EWS 托管 API 方法或[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作来获取项目的 MIME 表示形式。 由于 Exchange 不存储每个项目的 MIME 内容，它具有将每个项目的数据库表示形式转换为 MIME 流。 因为此转换会消耗大量资金，我们不建议这样做您请求大规模上的项目的 MIME 流。 另请注意 MIME 流包含一组有限的属性。您可能需要考虑的其他选项，如果属性集不包含所需的属性。 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 使用 MIME 流导出到.eml 和.mht 文件的电子邮件
<a name="bk_exportemailmime"> </a>

Outlook 和其他常见的电子邮件应用程序可以打开 EML (.eml) 文件格式。 下面的示例演示了如何使用 MIME 流，导出电子邮件并使用 MIME 流创建 EML 和 MIME HTML (.mht) 文件。 多个 web 浏览器支持的 MIME HTML 文件格式。 此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。 
  
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

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 使用 MIME 流导出到的 iCal 文件约会
<a name="bk_exporticalmime"> </a>

Outlook 和其他常见的日历应用程序可以打开 iCal (.ics) 文件格式。 下面的示例演示如何使用 MIME 流，导出为约会，并使用 MIME 流创建 iCal 文件。 请注意与 MIME 数据流，包括与会者和附件相关的属性不导出的许多属性。 您可以通过这些请求和将它们在 iCal 文件保存为私有扩展捕获从 EWS 其他属性。 这些私有扩展作为前缀与"x-"。 
  
此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。 此示例还假定您具有主题为"2015年财务投影"约会日历文件夹中。 
  
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

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 使用 MIME 流导出到一个 vCard 文件联系人
<a name="bk_exportvcardmime"> </a>

Outlook 和其他常见的联系人管理应用程序可以打开 vCard (.vcf) 文件格式。 下面的示例演示如何使用 MIME 流，导出联系人并使用 MIME 流创建电子名片。 您可以通过这些请求并将其保存捕获从 EWS 其他属性。 作为专用扩展电子名片。 这些扩展名为前缀与"x-"。 
  
此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。 
  
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
> 您不能使用**MimeContent**属性导入 vCard 文件。 您可以使用[Contact.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) EWS 托管 API 方法或[CreateItem](http://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS 操作导入联系人。 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a>使用 EWS 使用 MIME 流导出任何项目
<a name="bk_exportewsmime"> </a>

使用**GetItem**操作获取项目的 MIME 流。 以下**GetItem**请求演示如何请求的项目的 MIME 内容。 
  
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

下面的示例演示请求以获取 MIME 流的响应。 为便于阅读缩短了 MIME 流。
  
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
<a name="bk_exportfullfidelity"> </a>

导出项目之后，您可能希望若要[导入到 Exchange 的项目](how-to-import-items-by-using-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [导出和导入在 Exchange 中使用 EWS 的项目](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 导入项目](how-to-import-items-by-using-ews-in-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

