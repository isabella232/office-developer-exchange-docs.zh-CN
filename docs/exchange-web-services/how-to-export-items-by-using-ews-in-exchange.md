---
title: 使用 Exchange 中的 EWS 导出项目
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: e93ee68c-e134-4469-9070-fba404d46cb4
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 导出约会、电子邮件、联系人、任务和其他项目。
localization_priority: Priority
ms.openlocfilehash: a01c9487821958b06ec162f2aee27e2d2804eaaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455882"
---
# <a name="export-items-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 导出项目

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 导出约会、电子邮件、联系人、任务和其他项目。
  
您可以使用 EWS 托管 API 或 EWS 以多种不同的方式从 Exchange 中导出项目。 所使用的选项取决于：
  
- 导出的项目类型。
    
- 要在 Exchange 中的项目状态和导出的项目之间保持的保真度的程度。
    
- 导出的项目的格式。
    
- 任何后续处理要求。
    
- 是否要将项目导回 Exchange。
    
本文向您介绍如何使用每个不同的选项来导出项目。 您可以使用任何选项将项目批量导出到 Exchange 之外。
  
## <a name="export-an-item-into-a-custom-format"></a>将项目导出为自定义格式
<a name="bk_exportcustom"> </a>

您可以使用项目的结果[。绑定](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma)EWS 托管 API 方法调用或将[GetItem](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) EWS 操作的结果分析为符合应用程序要求的格式。 导出项目时使用此选项，将其导入数据库、.csv 文件或其他格式或系统。 您甚至可以将项目保存为项目 EWS XML 的形式，这很有用，因为很多系统具有 XML 分析功能。 建议使用 GetItem 方法或**GetItem**操作（不包含[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性），因为此选项可控制导出哪些**属性。** 
  
## <a name="export-items-with-full-fidelity"></a>以完全保真导出项目
<a name="bk_exportfullfidelity"> </a>

如果要以全保真方式导出项目，您可以使用[ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) EWS 操作。 **ExportItems**操作将每个项目导出为数据流。 此数据流不用于分析，但可用作可以导入回 Exchange 邮箱的项目级备份。 您可以在每个**ExportItems**请求中包含多个项目，尽管我们建议在每个调用中包含的项目不超过100个。 由于 EWS 托管 API 不实现**ExportItems**操作，因此如果使用 EWS 托管 api，您需要编写一个例程来发送 web 请求。 您可以选择使用[item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法来获取有关项目的元数据，以便您可以索引和存储有关数据流的信息。 
  
建议使用**ExportItems**操作导出计划导入到 Exchange 邮箱的项目。 
  
下面的示例演示如何使用**ExportItems**操作。 在此示例中，将缩短项目标识符以提高可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

服务器使用[ExportItemsResponse](https://msdn.microsoft.com/library/ef44354b-fbdb-4f7c-b6bd-b27f56a1d018%28Office.15%29.aspx)元素响应**ExportItems**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功导出项目。 该响应还包括导出项的项 ID 和包含导出内容的数据流。 下面的示例演示包含导出项的 SOAP 正文。
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:ExportItemsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="use-the-mime-stream-to-export-into-common-file-formats"></a>使用 MIME 流导出到常见文件格式
<a name="bk_exportfullfidelity"> </a>

您可以使用[项目。绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)EWS 托管 API 方法或[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS 操作，以获取项目的 MIME 表示形式。 由于 Exchange 不存储每个项目的 MIME 内容，因此必须将每个项目的数据库表示形式转换为 MIME 流。 由于这种转换成本较高，因此我们建议您不要为较大的项目请求 MIME 流。 另请注意，MIME 流包含一组有限的属性;如果属性集不包含所需的属性，则可能需要考虑其他选项。 
  
### <a name="use-the-ews-managed-api-to-export-an-email-into-an-eml-and-mht-file-by-using-the-mime-stream"></a>使用 EWS 托管 API，通过 MIME 流将电子邮件导出到 .eml 和 .mht 文件中
<a name="bk_exportemailmime"> </a>

Outlook 和其他常见的电子邮件应用程序可以打开 .EML （.eml）文件格式。 下面的示例演示如何使用 MIME 流导出电子邮件，并使用 MIME 流创建 .EML 和 MIME HTML （.mht）文件。 许多 web 浏览器都支持 MIME HTML 文件格式。 此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以向 Exchange 服务器进行身份验证。 
  
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

### <a name="use-the-ews-managed-api-to-export-an-appointment-into-an-ical-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 将约会导出到 iCal 文件中，方法是使用 MIME 流
<a name="bk_exporticalmime"> </a>

Outlook 和其他常见的日历应用程序可以打开 iCal （ics）文件格式。 下面的示例演示如何使用 MIME 流导出约会，并使用 MIME 流创建 iCal 文件。 请注意，许多属性不会与 MIME 流一起导出，包括与会者和与附件相关的属性。 通过请求这些属性并将其作为专用扩展名保存在 iCal 文件中，可以从 EWS 捕获其他属性。 这些专用扩展名以 "x-" 为前缀。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以向 Exchange 服务器进行身份验证。 本示例还假设您在 "日历" 文件夹中有一个主题为 "2015 财务预测" 的约会。 
  
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

### <a name="use-the-ews-managed-api-to-export-a-contact-into-a-vcard-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 将联系人导出到 vCard 文件中，方法是使用 MIME 流
<a name="bk_exportvcardmime"> </a>

Outlook 和其他常见的联系人管理应用程序都可以打开 vCard （.vcf）文件格式。 下面的示例演示如何使用 MIME 流导出联系人，并使用 MIME 流创建电子名片。 通过请求这些属性并将其保存在中，可以从 EWS 捕获其他属性。 作为私人分机的电子名片。 这些扩展名以 "x-" 为前缀。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以向 Exchange 服务器进行身份验证。 
  
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
> 您不能使用**MimeContent**属性导入 vCard 文件。 您可以使用联系人导入联系人[。保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx)EWS 托管 API 方法或[CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) EWS 操作。 
  
### <a name="use-ews-to-export-any-item-by-using-the-mime-stream"></a>使用 EWS 导出任何项目，方法是使用 MIME 流
<a name="bk_exportewsmime"> </a>

使用**GetItem**操作可获取项目的 MIME 流。 以下**GetItem**请求显示如何请求项目的 MIME 内容。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

下面的示例演示对获取 MIME 流的请求的响应。 为了提高可读性，MIME 流已缩短。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="893" 
                         MinorBuildNumber="17" 
                         Version="V2_10" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

导出项目后，您可能需要将[项目导入到 Exchange](how-to-import-items-by-using-ews-in-exchange.md)中。
  
## <a name="see-also"></a>另请参阅


- [使用 Exchange 中的 EWS 导出和导入项目](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 导入项目](how-to-import-items-by-using-ews-in-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

