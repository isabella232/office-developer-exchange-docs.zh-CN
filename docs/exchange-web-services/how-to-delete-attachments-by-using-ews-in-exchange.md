---
title: 使用 EWS 删除附件Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 从项目中删除Exchange。
ms.openlocfilehash: bc9b8bbf5833cfdb44f9ca4e8387681473fad3c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521149"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a>使用 EWS 删除附件Exchange

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 从项目中删除Exchange。
  
在使用 EWS 托管 API 从项目中删除文件和项目附件时，你具有许多选项。 可以从邮件中删除所有附件、按文件名删除或按集合中的位置删除。 对于其中每个选项，都有 [一个 AttachmentCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) 方法。 
  
相反，对于 EWS，无论您从某个项目中删除所有附件还是仅删除一个附件，操作序列都是相同的。 与 EWS 托管 API 不同，EWS 不包含要根据附件数组中的名称或位置删除的单独操作。
  
**表 1.用于删除附件的 EWS 托管 API 方法和 EWS 操作**

|**任务**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|删除项目的所有附件。  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)，后跟 [AttachmentCollection.Clear](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx)，后跟 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 后跟 [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|按名称从项目中删除附件。  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)，后跟 [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx)，后跟 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 后跟 [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|按集合中的位置从项中删除附件。  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)，后跟 [AttachmentCollection.RemoveAt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx)，后跟 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 后跟 [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除电子邮件的所有附件
<a name="bk_deleteattachewsma"> </a>

以下代码示例演示如何通过以下方法从电子邮件中删除所有附件：
  
1. 使用 [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 方法绑定到现有电子邮件并检索 [附件 的集合](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)。
    
2. 使用 [AttachmentCollection.Clear](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) 方法删除电子邮件的所有附件。 
    
3. 使用 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) 方法保存更改。 
    
本示例假定服务是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，itemId 是邮件的[ItemId，](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)附件将从中删除，并且用户已通过身份验证Exchange服务器。  
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 从电子邮件中按名称删除附件
<a name="bk_deleteattachewsma"> </a>

以下代码示例演示如何按名称删除附件：
  
1. 使用 [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 方法绑定到现有电子邮件并检索 [附件 的集合](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)。
    
2. 使用 [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) 方法删除名为 FileAttachment.txt。 
    
3. 使用 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) 方法保存更改。 
    
此示例假定服务是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，itemId 是将从中删除附件的邮件的 **ItemId，** 并且用户已通过 Exchange 服务器身份验证。 [](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 按位置删除附件
<a name="bk_deleteattachewsma"> </a>

以下代码示例演示如何按位置删除附件：
  
1. 使用 [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 方法绑定到现有电子邮件并检索 [Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) 和 [EmailMessage.HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) 属性的集合。 
    
2. 使用 [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) 方法删除集合中的第一个附件。 
    
3. 使用 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) 方法保存更改。 
    
此示例假定服务是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，itemId 是将从中删除附件的邮件的 **ItemId，** 并且用户已通过 Exchange 服务器身份验证。 [](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a>使用 EWS 从项目中删除附件
<a name="bk_deleteattachewsma"> </a>

若要使用 EWS 删除附件，首先需要检索邮件和附件集合以确定要删除的附件的 [AttachmentId (GetAttachment 和 DeleteAttachment ](https://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx)) 。 在删除一个或多个 **AttachmentId** 值后，调用 [DeleteAttachment](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) 操作以从邮件中删除指定的附件。 
  
以下代码示例演示如何使用 [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) 操作获取电子邮件和邮件上的附件集合。 这也是在使用 EWS 托管 API 从电子邮件中删除所有附件时，EWS 托管 API 发送的第一个 XML [请求](#bk_deleteattachewsma)。 为了可读性，已缩短某些属性的值。
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应 **GetItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值（指示电子邮件已成功检索）以及现有附件的 [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值。 
  
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
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

确定要删除的附件后，调用 [DeleteAttachment](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) 操作并包括要删除的附件的 **AttachmentId** 值。 
  
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
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [DeleteAttachmentResponse](https://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx)邮件响应 **DeleteAttachment** 请求，其中包含每个 [DeleteAttachmentResponseMessage](https://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx)的 [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值 **NoError，** 指示已成功删除每个附件。 为了可读性，已缩短某些属性的值。
  
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
    <m:DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅


- [附件和 EWS Exchange 中](attachments-and-ews-in-exchange.md)
    
- [使用 EWS 在 Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [使用 EWS 获取Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    

