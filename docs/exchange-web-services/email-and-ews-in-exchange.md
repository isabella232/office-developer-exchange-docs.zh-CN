---
title: 电子邮件和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: 了解如何处理电子邮件，包括在 Exchange 中如何创建电子邮件以及如何通过使用 EWS 托管的 API 或 EWS 执行其他电子邮件相关任务。
ms.openlocfilehash: d222be7409a3c3f4613a2be39b83b977fabb09e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752712"
---
# <a name="email-and-ews-in-exchange"></a>电子邮件和 Exchange 中的 EWS

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何处理电子邮件，包括在 Exchange 中如何创建电子邮件以及如何通过使用 EWS 托管的 API 或 EWS 执行其他电子邮件相关任务。
  

  
其核心是，Exchange 与电子邮件有关。但是，电子邮件是怎么形成的呢？电子邮件是 Exchange 中的一种[强类型的邮件](folders-and-items-in-ews-in-exchange.md#bk_item)，这意味着它们包含一组特定[属性](email-properties-and-elements-in-ews-in-exchange.md)，甚至在发送之前也是如此。电子邮件可由 EWS 托管的 API 中的 [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 类以及由 EWS 中的 [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) 元素及其子元素进行表示。 
  
在 EWS 托管的 API 中， **EmailMessage** 对象由 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象派生而来。 **EmailMessage** 类通过提供其他属性（如在几乎所有邮件方案中常见的 **EmailMessage.Sender** 和 [EmailMessage.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx)）扩展 [Item](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx) 类。当您获取、更新或删除电子邮件时，在大多数情况下您可以通过使用 **EmailMessage** 对象或基 **Item** 对象来实现，具体取决于您正在使用的属性是在 [EmailMessageSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) 中还是在 [ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) 类中。项目的创建会由于 **Item** 类没有构造函数而有所不同，因此当您要创建一封电子邮件时，您将使用 [EmailMessage 构造函数](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx)进行创建以及使用 [EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) 或 [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法来保存它，或发送并保存它。 
  
同样，在 EWS 中使用 [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 操作和 [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) 元素来创建一封电子邮件。若要通过使用 EWS 获取、更新或删除电子邮件，那么除了其他属性可用于电子邮件这一事实之外，正在进行修改的邮件是一封电子邮件的事实就显得不重要了。用于其他强类型邮件的相同操作还可用于电子邮件。 
  
|**任务**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|创建  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Get  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Update  <br/> |[Item.Update](http://msdn.microsoft.com/en-us/library/dd635915%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Delete  <br/> |[Item.Delete](http://msdn.microsoft.com/en-us/library/dd635072%28v=exchg.80%29.aspx) <br/> |[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
因为电子邮件只是[强类型的邮件](folders-and-items-in-ews-in-exchange.md#bk_item)，所以在某些情况下您操作它们的方式与您[操作常规邮件](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)的方式是相同的。 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管的 API 创建一封电子邮件
<a name="bk_createewsma"> </a>

您可以通过使用 EWS 托管的 API [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) 方法创建一封电子邮件，如以下示例的代码所示。 请注意该示例仅将邮件保存在草稿文件夹中，它不会发送该邮件。 有关如何发送消息或创建并发送一个步骤中的邮件的信息，请参阅[在 Exchange 使用 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。
  
此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// Create a new email message.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.ToRecipients.Add("mack@contoso.com");
message.Subject = "Project priorities";
message.Body = "(1) Buy pizza, (2) Eat pizza";
// Save the email message to the Drafts folder (where it can be retrieved, updated, and sent at a later time).
// This method call results in a CreateItem call to EWS.
message.Save(WellKnownFolderName.Drafts);
Console.WriteLine("A draft email message with the subject '" + message.Subject + "' has been saved to the Drafts folder.");
```

## <a name="create-an-email-message-by-using-ews"></a>使用 EWS 创建一封电子邮件
<a name="bk_createews"> </a>

您可以通过使用 EWS [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 操作创建一封电子邮件，如以下示例所示。 这也是当您 [创建电子邮件](#bk_createewsma)时，EWS 托管的 API 将发送的 XML 请求。 请注意，以下示例仅将邮件保存在草稿文件夹中，它不会发送该邮件。 有关如何发送消息或创建并发送一个站点中的邮件的信息，请参阅[在 Exchange 使用 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a>通过使用 EWS 托管的 API 获取、更新和删除电子邮件
<a name="bk_getewsma"> </a>

EWS 托管的 API 可以用于获取、更新或删除电子邮件，其操作方法与对 Exchange 存储中的任何常规项目执行这些操作的方法相同。 有关详细信息，请参阅[Work with Exchange 中使用 EWS 的 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)。
  
如果您要更新电子邮件，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)，了解可写的电子邮件属性的列表。若要在更新后发送草稿邮件，请参阅[通过使用 EWS 托管的 API 发送草稿电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma)。
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a>通过使用 EWS 获取、更新和删除电子邮件
<a name="bk_getews"> </a>

EWS 可以用于获取、更新和删除电子邮件，其操作方法与对 Exchange 存储中的任何常规项目执行这些操作的方法相同。 有关详细信息，请参阅[Work with Exchange 中使用 EWS 的 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)。
  
如果您要更新电子邮件，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)，了解可写的电子邮件属性的列表。若要在更新后发送草稿邮件，请参阅[通过使用 EWS 发送草稿电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews)。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 响应电子邮件](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [移动和复制在 Exchange 使用 EWS 的电子邮件](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [通过在 Exchange 使用 EWS 来处理对话](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [在 Exchange 使用 EWS 从电子邮件提取实体](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [在 Exchange 中使用 EWS 的批次中的过程电子邮件](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    

