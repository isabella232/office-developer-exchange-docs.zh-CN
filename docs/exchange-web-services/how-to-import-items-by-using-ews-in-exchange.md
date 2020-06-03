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
# <a name="import-items-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 导入项目

了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 导入约会、电子邮件、联系人、任务和其他项目。
  
许多系统包含约会、电子邮件、联系人和任务，您可以通过多种不同的方式将这些项目导入到 Exchange 中。 在这些项目上不维护邮箱关系时，将项目导入 Exchange 非常简单。 您可以使用[项目。保存](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)EWS 托管 API 方法或[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作以在 Exchange 邮箱中创建项目。 不过，简单方法不支持所有方案;例如： 
  
- 在使用与会者（会议）导入约会时，不能维护组织者和与会者之间的关系。 这意味着会议组织者需要将会议邀请重新发送给与会者，以便在组织者和与会者之间重新建立关系。 如果约会已导入与会者的日历中，则约会将不与会议组织者的约会相关联。 与会者需要接受来自组织者的重发会议邀请，以便重新建立组织者-与会者关系。
    
- 导入分配的任务时，不会保留工作负责人的相关信息。
    
所有导入选项均可用于将项目批量导入到 Exchange。
  
## <a name="use-ews-managed-api-or-ews-item-types-to-import-an-item"></a>使用 EWS 托管 API 或 EWS 项类型导入项目
<a name="bk_importproperties"> </a>

您可以使用 EWS 托管 API 或 EWS 从其他系统中导入电子邮件、联系人、约会或任务。 根据您要导入的内容，只需根据您要导入的内容，在下列任何对象上设置源格式的[属性](properties-and-extended-properties-in-ews-in-exchange.md)。 
  
**表1。EWS 托管 API 对象和 EWS 元素**

|**EWS 托管 API 对象**|**EWS 元素**|
|:-----|:-----|
|[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[消息](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[联系人](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[联系人](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[任务](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[任务](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
使用[项目。保存](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.save%28v=exchg.80%29.aspx)EWS 托管 API 方法或[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作以执行项的导入。 当您从其他系统导入项目时，我们建议采用这种方法，因为您可以控制要导入哪些属性。 有关如何设置项目属性并保存项目的详细信息，请参阅[使用 Ews 托管 API 创建项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createewsma)或[使用 ews 创建项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_createews)。
  
## <a name="import-items-with-full-fidelity"></a>以完全保真导入项目
<a name="bk_importproperties"> </a>

您可以使用[UploadItems](https://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) EWS 操作以数据流形式上传项目。 项目的此数据流表示形式必须来自[ExportItems](https://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)操作调用的结果。 由于 EWS 托管 API 不实现**UploadItems**操作，因此如果使用 EWS 托管 api，您需要编写一个例程来发送 web 请求。 
  
这是导入已从其他 Exchange 服务器导出的项目的最简单方法。
  
在下面的示例中，将缩短标识符和**数据**元素内容以提高可读性。 
  
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

服务器使用[UploadItemsResponse](https://msdn.microsoft.com/library/93044d39-4489-456a-8cce-b6d69873348f%28Office.15%29.aspx)元素响应**UploadItems**请求，该元素包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功上载项目。 该响应还包括已上载项的项 ID。 
  
## <a name="use-the-mime-stream-to-import-from-common-file-formats"></a>使用 MIME 流从常见文件格式导入
<a name="bk_importproperties"> </a>

EWS 可以导入 .EML （.eml）和 iCal （ics）文件。 你将需要测试你的 MIME 内容，以了解 Exchange MIME 分析器如何处理你的 MIME 流的内容。 虽然使用 MIME 流非常方便，但通常更好的做法是[使用 EWS 托管 API 或 EWS 项类型导入项目](#bk_importproperties)。 下面的示例展示了如何[导入电子名片](https://code.msdn.microsoft.com/How-to-Import-vCard-Files-ffa0ff50)。
  
### <a name="use-the-ews-managed-api-to-import-an-email-from-an-eml-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 通过 MIME 流从 .EML 文件导入电子邮件

下面的示例演示如何使用 .EML 文件的内容设置[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性，然后将该电子邮件导入到邮箱中。 本示例还演示如何对导入的电子邮件设置[PidTagMessageFlags （0x0E07）](https://msdn.microsoft.com/library/office/cc839733%28v=office.15%29.aspx)扩展属性，使其不会在邮箱中显示为草稿项目。 此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户可以向 Exchange 服务器进行身份验证。 
  
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

### <a name="use-the-ews-managed-api-to-import-an-appointment-from-an-ical-file-by-using-the-mime-stream"></a>使用 EWS 托管 API 通过 MIME 流从 iCal 文件中导入约会

您可以使用 MIME 流，以 iCalendar 文件的形式导入简单约会。 您无法导入会议，这是与会者的约会，因为必须将会议组织者和与会者之间的关系设置为[Exchange 日历](calendars-and-ews-in-exchange.md)工作流的一部分。 无法在 MIME 流中捕获与会者。 
  
下面的代码示例演示如何将简单的文件导入到用户的邮箱中。
  
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

### <a name="use-ews-to-import-an-item-by-using-the-mime-stream"></a>使用 EWS 通过 MIME 流导入项目

您可以使用[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS 操作，使用 MIME 流导入 .Eml 和 iCal 项。 
  
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

## <a name="next-steps"></a>后续步骤
<a name="bk_importproperties"> </a>

将项目导入邮箱后，您可能需要[创建一个自定义文件夹来存储导入的项目](how-to-work-with-folders-by-using-ews-in-exchange.md)，或[同步您的客户端和邮箱项目](mailbox-synchronization-and-ews-in-exchange.md)。
  
## <a name="see-also"></a>另请参阅


- [使用 Exchange 中的 EWS 导出和导入项目](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 导出项目](how-to-export-items-by-using-ews-in-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    
- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)
    

