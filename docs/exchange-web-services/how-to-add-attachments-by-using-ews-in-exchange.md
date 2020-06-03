---
title: 使用 Exchange 中的 EWS 添加附件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 0cbce436-2ae6-4fcc-bd8b-f517a0724e55
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，创建包含附件的新项目，或向现有项目添加附件。
localization_priority: Priority
ms.openlocfilehash: fa98eb437d1289f25cfb827b6fa9b351d842bd40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528263"
---
# <a name="add-attachments-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 添加附件

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，创建包含附件的新项目，或向现有项目添加附件。
  
您可以使用 EWS 托管 API 或 EWS 将文件附件或项目附件添加到新项目或现有项目中。 如果使用 EWS 托管 API，则可以使用相同的方法将附件添加到新项目或现有项目中;但是，如果您使用的是文件或项目附件，则此方法会更改。 相反，如果使用 EWS，则可以使用相同的操作将文件或项目附件添加到项目中，但如果要将附件添加到新项目或现有项目中，则该操作会更改。
  
**表1。用于添加附件的 EWS 托管 API 方法和 EWS 操作**

|**任务**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|将文件附件添加到新的或现有的电子邮件  <br/> |[AttachmentCollection.AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |新电子邮件的[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)  <br/> 要添加到现有电子邮件中的[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)  <br/> |
|将项目附件添加到新的或现有的电子邮件  <br/> |[AttachmentCollection.AddItemAttachment](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx) <br/> |新电子邮件的[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)  <br/> 要添加到现有电子邮件中的[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建包含文件和项目附件的电子邮件
<a name="bk_createattachewsma"> </a>

下面的代码示例演示如何通过以下方式创建包含多个文件附件和项目附件的电子邮件： 
  
1. 使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建电子邮件。 
    
2. 使用 AddFileAttachment 和[AttachmentCollection](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx)方法将附件添加到邮件中。 [AttachmentCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) 
    
3. 使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法将邮件发送给收件人，并将邮件保存在 "已发送邮件" 文件夹中。 
    
此代码示例演示使用 EWS 托管 API 将文件附件添加到项目的四种方式：
  
- 通过使用完全限定的文件位置。
    
- 通过使用完全限定的文件位置和新的附件名称。
    
- 通过使用字节数组。
    
- 使用流。
    
请注意，此示例中的项目附件是在电子邮件的同一时间创建的。 若要将现有电子邮件添加为项目附件，请参阅[使用 MimeContent 和 EWS 托管 API 将现有项目添加到新电子邮件](#bk_addexistingemailewsma)。
  
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
public static void CreateEmailWithAttachments(ExchangeService service)
{
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Message with Attachments";
    message.Body = "This message contains four file attachments 
        and one message item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    message.ToRecipients.Add("ronnie@contoso.com");
    // Add a file attachment by using the fully qualified location of the file. 
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // Add a file attachment by using the fully qualified string name, 
    // and specify the name of the attachment as it will appear in the email.
    // The new name of the file attachment is SecondAttachment.txt.
    message.Attachments.AddFileAttachment("SecondAttachment.txt", "C:\\temp\\FileAttachment2.txt");
    // Add a file attachment by using a byte array.
    // In this example, theBytes is the byte array that represents the content of the image file to attach.
    byte[] theBytes = File.ReadAllBytes("C:\\Temp\\Tulips.jpg");
    // The byte array file attachment is named ThirdAttachment.jpg.
    message.Attachments.AddFileAttachment("ThirdAttachment.jpg", theBytes);
    // Add a file attachment by using a stream.
    FileStream theStream = new FileStream("C:\\temp\\FileAttachment4.txt", FileMode.OpenOrCreate);
    // The streamed file attachment is named FourthAttachment.txt.
    message.Attachments.AddFileAttachment("FourthAttachment.txt", theStream);
    // Add an email message as an item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Name = "Attached Message Item";
    itemAttachment.Item.Subject = "Message Item Subject";
    itemAttachment.Item.Body = "Message Item Body";
    itemAttachment.Item.ToRecipients.Add("sadie@contoso.com");
    itemAttachment.Item.ToRecipients.Add("ronnie@contoso.com");
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a>使用 EWS 创建包含文件和项目附件的电子邮件
<a name="bk_createattachews"> </a>

下面的代码示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作创建包含四个文件附件和一个项目附件的电子邮件。 这也是在您[创建包含文件和项目附件的电子邮件](#bk_createattachewsma)时，EWS 托管 API 发送的 XML 请求之一。
  
请注意，此示例中的项目附件是在电子邮件的同一时间创建的。 若要将现有电子邮件添加为项目附件，请参阅[使用 MimeContent 和 EWS 托管 API 将现有项目添加到新电子邮件](#bk_addexistingemailewsma)。
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Message with Attachments</t:Subject>
          <t:Body BodyType="HTML">This message contains four file attachments 
              and one message item attachment.</t:Body>
          <t:Attachments>
            <t:FileAttachment>
              <t:Name>FileAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>SecondAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>VGhpcyBpcyB0aGUgc2Vjb25kIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>ThirdAttachment.jpg</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>nAoAXNIZMVEZs5GKhdzRcLH/9k=</t:Content>
            </t:FileAttachment>
            <t:FileAttachment>
              <t:Name>FourthAttachment.txt</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:IsContactPhoto>false</t:IsContactPhoto>
              <t:Content>obWVudC4=…</t:Content>
            </t:FileAttachment>
            <t:ItemAttachment>
              <t:Name>Attached Message Item</t:Name>
              <t:IsInline>false</t:IsInline>
              <t:Message>
                <t:Subject>Message Item Subject</t:Subject>
                <t:Body BodyType="HTML">Message Item Body</t:Body>
                <t:ToRecipients>
                  <t:Mailbox>
                    <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                  <t:Mailbox>
                    <t:EmailAddress>mack@contoso.com</t:EmailAddress>
                  </t:Mailbox>
                </t:ToRecipients>
              </t:Message>
            </t:ItemAttachment>
          </t:Attachments>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
            <t:Mailbox>
              <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值为**NoError**，表示已成功创建电子邮件和附件。 新创建的邮件的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)和每个附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值也包含在响应中。 为了提高可读性，某些属性的值已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="upV4AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXuktU" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="6ts3NuI=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="gOIZx1I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="esRan5I=" />
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="t7sU6s=" />
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="XgDCggM=" />
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

若要[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)，请调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a>使用 MimeContent 和 EWS 托管 API 将现有项添加到新电子邮件
<a name="bk_addexistingemailewsma"> </a>

若要将现有项目作为项目附件添加到另一个项目，您需要创建新的项目附件并将现有项目的内容复制到新项目中。 可通过 2 种方法执行此操作： 
  
1. 如果您使用的是电子邮件，则可以将[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性的值从电子邮件复制到新创建的项目附件中。 在此过程中，您将丢失一些属性，如后续标志和类别，但它对标准电子邮件非常有用。 
    
2. 如果您需要所有项目类型的完全保真，则可以绑定到现有项目并将所有属性和扩展属性复制到新的附件中。
    
下面的代码示例演示了第一种方法，即将**MimeContent**复制到新项附件中。 下面的示例展示了如何修改代码以使用第二种方法的过程。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过 Exchange 服务器的身份验证，并且**itemid**是要附加的项的[itemid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) 。 
  
```cs
public static void CreateEmailExistingItem(ExchangeService service, ItemId itemId)
{        
    // This method results in a GetItem call to EWS.
    EmailMessage msgToAttach = EmailMessage.Bind(service,itemId, 
        new PropertySet(ItemSchema.MimeContent, ItemSchema.Subject));
    // Create an email message and set properties on the message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Message with Item Attachment (MimeContent)";
    message.Body = "The attachment to this message was created by copying
        the MimeContent from the original message and adding it to a new item attachment.";
    message.ToRecipients.Add("sadie@contoso.com");
    // Add an email message item attachment and set properties on the item.
    ItemAttachment<EmailMessage> itemAttachment = message.Attachments.AddItemAttachment<EmailMessage>();
    itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
    itemAttachment.Name = msgToAttach.Subject;
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

若要修改此示例以将现有项的每个属性复制到新项附件中，请执行以下操作： 
  
1. 将属性集更改为包含**PropertySet**以及所需的任何其他属性或扩展属性。 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. 删除以下行，因为您不需要**MimeContent**属性。 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. 对每个要从现有项目复制到新附件的属性重复此代码行。 请勿将**ItemId**复制到新项目附件中，因为这是只读属性。 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. 将附件上的[PidTagMessageFlags](https://msdn.microsoft.com/library/cc839733.aspx) （0x0E070003）属性设置为 "**已发送**"。
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a>使用 MimeContent 和 EWS 将现有项添加到新电子邮件中
<a name="bk_addexistingemailews"> </a>

有两种方法可将现有项添加到新项： 
  
1. 如果您使用的是电子邮件，则可以将[MimeContent](https://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx)元素的值从电子邮件复制到新创建的项目附件中。 在此过程中，您将丢失一些属性，如后续标志和类别，但它对标准电子邮件非常有用。 
    
2. 如果您需要所有项目类型的完全保真，则可以绑定到现有项目并将所有属性和扩展属性复制到新的附件中。
    
下面的代码示例演示如何使用**MimeContent**元素将原始项的内容复制到新项附件的**MimeContent**值中。 此示例使用以下操作： 
  
1. [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) —获取将成为新邮件的项目附件的邮件的**MimeContent**和[主题](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)。 
    
2. [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) —创建新的电子邮件。 
    
3. [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)—使用由**GetItem**操作检索到的**MimeContent**和**主题**来创建新附件。 
    
4. [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) —发送和保存邮件。 
    
该示例首先检索现有项的**MimeContent**和**主题**。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:MimeContent" />
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="jCrTAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示电子邮件已成功检索，以及电子邮件的**MimeContent**和**主题**。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="944"
                         MinorBuildNumber="11"
                         Version="V2_12"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
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
              <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
              <t:ItemId Id="jCrTAAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi+7u" />
              <t:Subject>Play tennis?</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

接下来，调用**CreateItem**操作以创建新的电子邮件。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Message with Item Attachment (MimeContent)</t:Subject>
          <t:Body BodyType="HTML">The attachment to this message was created by copying the MimeContent from the original message and adding it to a new item attachment.</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>primary@contoso1000.onmicrosoft.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示已成功创建电子邮件。
  
接下来，使用**MimeContent**和**GetItem**操作检索到的**主题**创建新的项目附件。 使用**CreateItem**响应中返回的**ItemId**值填充[ParentItemId](https://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx)元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateAttachment>
      <m:ParentItemId Id="jDKsAAA=" />
      <m:Attachments>
        <t:ItemAttachment>
          <t:Name>Play tennis?</t:Name>
          <t:IsInline>false</t:IsInline>
          <t:Message>
            <t:MimeContent CharacterSet="UTF-8">tDQe/Eo=…</t:MimeContent>
          </t:Message>
        </t:ItemAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件响应**CreateAttachment**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，这表示附件已成功创建，以及新创建的附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) 。 
  
现在已创建新邮件，并且已附加项目，您可以通过调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="jDKsAAA="
                  ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAZi/q/" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **SendItemResponse** 邮件响应 [SendItem](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**，表示电子邮件已成功发送。
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建带有内嵌附件的电子邮件
<a name="bk_createinlineattachewsma"> </a>

下面的代码示例演示如何通过以下方式创建包含内联附件的电子邮件：
  
1. 使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建电子邮件。 
    
2. 将[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)属性设置为包含内联附件的 HTML 正文。 
    
3. 使用 AddFileAttachment 方法可将附件添加到邮件中。 [AttachmentCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) 
    
4. 使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法将邮件发送给收件人，并将邮件保存在 "已发送邮件" 文件夹中。 
    
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
public static void CreateEmailWithInlineAttachment(ExchangeService service)
{
    // Create the HTML body with the content identifier of the attachment.
    string html = @"<html>
                        <head>
                        </head>
                        <body>
                        <img width=100 height=100 id=""1"" src=""cid:Party.jpg"">
                        </body>
                        </html>";
         
    // Create the email message.
    EmailMessage message = new EmailMessage(service);
    message.Subject = "Inline Attachment";
    message.Body = new MessageBody(BodyType.HTML, html);
    message.ToRecipients.Add("sadie@contoso.com");
    // Add the attachment to the local copy of the email message.
    string file = @"C:\Temp\Party.jpg";
    message.Attachments.AddFileAttachment("Party.jpg", file);
    message.Attachments[0].IsInline = true;
    message.Attachments[0].ContentId = "Party.jpg";
         
    // Send the mail and save a copy in the Sent Items folder.
    // This method results in a CreateItem and SendItem call to EWS.
    message.SendAndSaveCopy();
}
```

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a>使用 EWS 创建带有内嵌附件的电子邮件
<a name="bk_createinlineattachewsma"> </a>

下面的代码示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作创建包含内联文件附件的电子邮件。 [Body](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx)元素的**office.mailboxenums.bodytype**属性指示内容为 HTML 格式，并包含图像源。 这也是当您使用 EWS 托管 API[创建带有内嵌附件的电子邮件](#bk_createinlineattachewsma)时，EWS 托管 api 发送的 XML 请求之一。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:Items>
        <t:Message>
          <t:Subject>Inline Attachment</t:Subject>
          <t:Body BodyType="HTML">
            &amp;lt;html&amp;gt;
            &amp;lt;head&amp;gt;
            &amp;lt;/head&amp;gt;
            &amp;lt;body&amp;gt;
            &amp;lt;img width=100 height=100 id="1" src="cid:Party.jpg"&amp;gt;
            &amp;lt;/body&amp;gt;
            &amp;lt;/html&amp;gt;
          </t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。 
  
若要[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)，请调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 将附件添加到现有电子邮件
<a name="bk_createinlineattachewsma"> </a>

下面的代码示例演示如何通过以下方式向现有电子邮件添加附件： 
  
1. 使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法可绑定到现有电子邮件。 
    
2. 使用**AddFileAttachment**方法将文件附件添加到邮件中。 
    
3. 通过调用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存更新。 
    
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```XML
public static void AddAttachmentToExisting(ExchangeService service, ItemId itemId)
{
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId);
    message.Attachments.AddFileAttachment("C:\\temp\\FileAttachment.txt");
    // This method results in a CreateAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a>使用 EWS 将附件添加到现有电子邮件
<a name="bk_createinlineattachewsma"> </a>

下面的代码示例演示如何使用[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作将文件附件添加到现有电子邮件中。 这也是当您使用 EWS 托管 API[将附件添加到现有电子邮件](#bk_createinlineattachewsma)中时，EWS 托管 api 发送的 XML 请求之一。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateAttachment>
      <m:ParentItemId Id="uqE2AAA=" />
      <m:Attachments>
        <t:FileAttachment>
          <t:Name>FileAttachment.txt</t:Name>
          <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
        </t:FileAttachment>
      </m:Attachments>
    </m:CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件响应**CreateAttachment**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，这表示附件已成功创建，以及新创建的附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) 。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="yRLhCh8="
                              RootItemId="uqE2AAA="
                              RootItemChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcf" />
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:CreateAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅


- [附件和 EWS Exchange 中](attachments-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 添加附件](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 删除附件](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 获取附件](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

