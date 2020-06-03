---
title: 在 Exchange 中使用 EWS 发送电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 5290fafe-8b51-4275-a27e-baf497fc969c
description: 本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解在 Exchange 中如何使用 EWS 托管 API 或 EWS 发送新的或草稿电子邮件，或者发送延迟的电子邮件。
localization_priority: Priority
ms.openlocfilehash: b73327cc69db37028c0508af788bf5294e79206a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527724"
---
# <a name="send-email-messages-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 发送电子邮件

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解在 Exchange 中如何使用 EWS 托管 API 或 EWS 发送新的或草稿电子邮件，或者发送延迟的电子邮件。
  
不论您使用的是 EWS 托管 API 还是 EWS，您都可以通过两种方式发送电子邮件。您可以发送现有邮件，如存储在"草稿"文件夹中的邮件，也可以一步创建和发送电子邮件。不论您是立即发送邮件，还是发送延迟邮件，用于发送邮件的方法和操作均相同。
  
**表 1. 用于发送电子邮件的 EWS 托管 API 方法和 EWS 操作**

|**任务**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|发送新的电子邮件  <br/> |[EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|发送现有电子邮件  <br/> |[EmailMessage.Send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) <br/> |[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> |
   
## <a name="send-a-new-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 发送新的电子邮件
<a name="bk_sendnewewsma"> </a>

以下代码示例介绍如何使用 [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象创建电子邮件，使用 [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法将邮件发送给收件人并将邮件保存在"已发送邮件"文件夹中。 
  
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
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
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "' and saved in the SendItems folder.");
```

## <a name="send-a-new-email-message-by-using-ews"></a>使用 EWS 发送新的电子邮件
<a name="bk_sendnewews"> </a>

以下代码示例介绍如何使用 [MessageDisposition](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 值为 **SendAndSaveCopy** 的 **CreateItem** 操作创建电子邮件、将邮件发送给收件人并将邮件保存在"已发送邮件"文件夹中。这也是当您 [发送新的电子邮件](#bk_sendnewewsma)时 EWS 托管 API 发送的 XML 请求。
  
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

服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。 
  
## <a name="send-a-draft-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 发送草稿电子邮件
<a name="bk_senddraftewsma"> </a>

以下代码示例介绍如何发送存储在"草稿"文件夹中的邮件，如[使用 EWS 托管的 API 创建一封电子邮件](email-and-ews-in-exchange.md#bk_createewsma)中所示。首先，使用 [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 方法检索邮件，然后使用 [Send](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) 方法发送电子邮件，如以下代码示例中所示。请注意，此方法不会将已发送的邮件保存在"已发送邮件"文件夹中。 
  
在这种情况下，会将 [EmailMessageSchema.Subject](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) 和 [EmailMessageSchema.ToRecipients](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) 属性添加到 [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)，以便值可以包含在控制台输出中。 
  
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// As a best practice, create a property set that limits the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
// Send the email message.
// This method call results in a SendItem call to EWS.
message.Send();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "'.");
```

## <a name="send-a-draft-email-message-by-using-ews"></a>使用 EWS 发送草稿电子邮件
<a name="bk_senddraftews"> </a>

以下代码示例介绍如何发送之前存储在"草稿"文件夹中的邮件，如[使用 EWS 创建一封电子邮件](email-and-ews-in-exchange.md#bk_createews)中所示。首先，使用 [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) 操作检索要发送的电子邮件。然后使用 [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) 操作将电子邮件发送给收件人并将其保存在"已发送邮件"文件夹中。 
  
第一封邮件 **GetItem** 请求邮件指定要绑定到的草稿电子邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)，[ItemShape](https://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx) 元素中的元素限制要包含在 **GetItem** 响应中的结果。 **ItemShape** 元素的 [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) 为 **IdOnly**，[AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) 元素包括项目架构中的 [Subject](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) 属性和邮件架构中的 **ToRecipients** 属性的 **FieldURI** 值，这意味着在响应中仅向客户端返回 **ItemId**、[Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) 和 [ToRecipients](https://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) 元素。有关限制调用中返回的值的详细信息以及 **BaseShape** 元素的含义，请参阅 [属性集和响应形状在 EWS 在 Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md)。
  
这也是调用 [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 方法时 EWS 托管 API 发送的 XML 请求。某些属性和元素的值已缩短，以方便读取。 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

以下示例显示了服务器在处理 **GetItem** 操作后返回的 XML 响应。响应指示电子邮件已成功检索，且包括所请求的 **Subject** 和 **ToRecipient** 元素。某些属性和元素的值已缩短，以方便读取。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="842"
                         MinorBuildNumber="10"
                         Version="V2_8"
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
              <t:ItemId Id="AAMkADE4="
                        ChangeKey="CQAAABYA" />
              <t:Subject>Project priorities</t:Subject>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>sadie@contoso.com</t:Name>
                  <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                  <t:MailboxType>OneOff</t:MailboxType>
                </t:Mailbox>
              </t:ToRecipients>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

第二封邮件 **SendItem** 请求邮件指定要发送的电子邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 以及 [SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx)，后者指定了已发送的邮件将保存到哪个文件夹中。
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4="
                  ChangeKey="CQAAABYA" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 **SendItemResponse** 邮件响应 [SendItem](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**，表示电子邮件已成功发送。
  
## <a name="send-a-delayed-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 发送延迟的电子邮件
<a name="bk_senddelayedewsma"> </a>

以下代码示例介绍如何使用 [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象创建电子邮件，如何使用 [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) 类创建 [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx) (0x3FEF0040) 属性的属性定义，如何使用 [SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法发送延迟的邮件并将邮件保存在"已发送邮件"文件夹中。 
  
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// Create a new email message. 
EmailMessage message = new EmailMessage(service);
// Specify the email recipient and subject. 
message.ToRecipients.Add("sadie@contoso.com");
message.Subject = "Delayed email";
// Identify the extended property that can be used to specify when to send the email. 
ExtendedPropertyDefinition PidTagDeferredSendTime = new ExtendedPropertyDefinition(16367, MapiPropertyType.SystemTime);
// Set the time that will be used to specify when the email is sent. 
// In this example, the email will be sent one minute after the next line executes, 
// provided that the message.SendAndSaveCopy request is processed by the server within one minute. 
string sendTime = DateTime.Now.AddMinutes(1).ToUniversalTime().ToString();
// Specify when to send the email by setting the value of the extended property. 
message.SetExtendedProperty(PidTagDeferredSendTime, sendTime);
// Specify the email body. 
StringBuilder str = new StringBuilder();
str.AppendLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
str.AppendLine("The email message will be sent at: " + sendTime + ".");
message.Body = str.ToString();
Console.WriteLine("");
Console.WriteLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
Console.WriteLine("The email message will be sent at: " + sendTime + ".");
// Submit the request to send the email message. 
message.SendAndSaveCopy();
```

## <a name="send-a-delayed-email-message-by-using-ews"></a>使用 EWS 发送延迟的电子邮件
<a name="bk_senddelayedews"> </a>

以下代码示例介绍如何使用 [MessageDisposition](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 值为 **SendAndSaveCopy** 的 **CreateItem** 操作创建电子邮件，如何使用 [ExtendedProperty](https://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) 元素为 [PidTagDeferredSendTime](https://msdn.microsoft.com/library/cc840017.aspx) (0x3FEF0040) 属性创建属性定义以设置发送邮件的时间，以及如何使用 [SavedItemFolderId](https://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) 元素将已发送的邮件保存在"已发送邮件"文件夹中。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Delayed email</t:Subject>
          <t:Body BodyType="HTML">
            The client submitted the SendAndSaveCopy request at: 1/2/2014 9:08:52 PM.
            The email message will be sent at: 1/2/2014 9:09:52 PM.
          </t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI PropertyTag="16367"
                                PropertyType="SystemTime" />
            <t:Value>2014-01-02T21:09:52.000</t:Value>
          </t:ExtendedProperty>
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

服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。 
  
## <a name="see-also"></a>另请参阅


- [Exchange 中的电子邮件和 EMS](email-and-ews-in-exchange.md)
    
- [在 Exchange 中使用 EWS 响应电子邮件](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    

