---
title: 在 Exchange 使用 EWS 导入项目
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd3d3221-c98e-4fa0-81f0-77f733d2f432
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 导入约会、 电子邮件、 联系人、 任务和其他项目。
ms.openlocfilehash: c09c96eff455b7584b084e71b937853abfde731d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752836"
---
# <a name="import-items-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 导入项目

了解如何在 Exchange 使用 EWS 托管 API 或 EWS 导入约会、 电子邮件、 联系人、 任务和其他项目。
  
许多系统包含约会、 电子邮件、 联系人和任务，并且可以这些项目导入 Exchange 中通过多种不同的方式。 邮箱关系不维护这些项目时，将项目导入 Exchange 非常简单。 您可以使用[Item.Save](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS 托管 API 方法或[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作在 Exchange 邮箱中创建项目。 简单的做法不支持所有方案，但是;例如： 
  
- 导入与与会者 （会议） 的约会时，您不能维护组织者和与会者之间的关系。 这意味着会议组织者将需要将会议邀请重新发送给与会者，才能重新建立组织者和与会者之间的关系。 如果约会已导入与会者的日历，约会将不与会议组织者的约会。 与会者将需要重新建立组织者 attendee 关系以接受从组织者重发的会议邀请。
    
- 导入分配的任务时，则不会保留 assignees 有关的信息。
    
所有导入选项可用于到 Exchange 批量导入项目。
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>使用 EWS 托管 API 或 EWS 项目导入项目的类型
<a name="bk_importproperties"> </a>

您可以使用 EWS 托管 API 或 EWS 从其他系统导入电子邮件、 联系人、 约会或任务。 只需将[属性](properties-and-extended-properties-in-ews-in-exchange.md)从源格式设置的下列对象，具体取决于您正在导入任何。 
  
**表 1。EWS 托管 API 对象和 EWS 元素**

|**EWS 托管 API 对象**|**EWS 元素**|
|:-----|:-----|
|[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Contact](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[约会](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[任务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[任务](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
使用[Item.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx) EWS 托管 API 方法或[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作执行导入的项目。 正在导项目入来自其他系统中，因为您有时必须通过该属性获取导入的控件时，我们建议此方法。 有关如何在项目上设置属性，然后保存项目的详细信息，请参阅[创建通过使用 EWS 托管 API 的项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma)或[创建使用 EWS 的项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews)。
  
## <a name="import-items-with-full-fidelity"></a>全保真方式导入项目
<a name="bk_importproperties"> </a>

您可以使用[UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS 操作将上载一个项目作为数据流。 此数据流表示形式项目必须来自[ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)操作调用的结果。 因为 EWS 托管 API 不实现**UploadItems**操作，如果您使用 EWS 托管 API，您需要编写一个例程以发送 web 请求。 
  
这是导入已从另一个 Exchange 服务器中导出的项目的最简单方式。
  
在以下示例中，为便于阅读缩短标识符和**数据**元素内容。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xmlns:xsd="http://www.w3.org/2001/XMLSchema"
      xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
      xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

服务器响应的包括**NoError**，这表明项目已成功上载[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值与[UploadItemsResponse](http://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx)元素**UploadItems**请求。 响应还包括上载的项的项 ID。 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>使用要导入从常用文件格式的 MIME 流
<a name="bk_importproperties"> </a>

EML (.eml) 和 iCal (.ics) 文件，可以导入 EWS。 您需要测试您的 MIME 内容，以查看 Exchange MIME 分析程序处理的 MIME 流内容的方式。 虽然使用 MIME 的流为方便，但会[使用 EWS 托管 API 或 EWS 项目导入项目的类型](#bk_importproperties)通常更好。 下面是若要[导入电子名片](http://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50)的示例。
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 使用 MIME 流从 EML 文件中导入电子邮件

下面的示例演示如何将 EML 文件的内容与[MimeContent](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性设置，然后导入邮箱的电子邮件。 本示例还演示了如何设置[PidTagMessageFlags (0x0E07)](http://msdn.microsoft.com/en-us/library/office/cc839733%28v=office.15%29.aspx)扩展属性导入电子邮件，以便它没有显示作为草稿项的邮箱中。 此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以验证到 Exchange 服务器。 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 从 iCal 文件导入约会，使用 MIME 流

您可以使用 MIME 流导入 iCalendar 文件的窗体中的简单约会。 无法导入会议，因为要设置为[Exchange 日历](calendars-and-ews-in-exchange.md)工作流的一部分会议组织者和与会者之间的关系是与与会者的约会。 与会者无法捕获 MIME 用于将 stream 中。 
  
下面的代码示例演示如何简单.ics 文件导入到用户的邮箱。
  
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

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a>使用 EWS 使用 MIME 流导入项目

您可以使用[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作使用其 MIME 流导入 EML 和 iCal 的项。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="next-steps"></a>后续步骤
<a name="bk_importproperties"> </a>

项目导入邮箱后，您可能要[创建自定义文件夹来存储您导入的项目](how-to-work-with-folders-by-using-ews-in-exchange.md)，或[同步客户端和邮箱项目](mailbox-synchronization-and-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [导出和导入在 Exchange 中使用 EWS 的项目](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 导出项目](how-to-export-items-by-using-ews-in-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

