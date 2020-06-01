---
title: 电子邮件和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4d7bdb37-f7f1-409f-9749-f8bcde7dc52a
description: 了解如何处理电子邮件，包括在 Exchange 中如何创建电子邮件以及如何通过使用 EWS 托管的 API 或 EWS 执行其他电子邮件相关任务。
localization_priority: Priority
ms.openlocfilehash: 323d9d2cc40aa86044a439ad53e53a4808916783
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455441"
---
# <a name="email-and-ews-in-exchange"></a><span data-ttu-id="bac19-103">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="bac19-103">Email and EWS in Exchange</span></span>

<span data-ttu-id="bac19-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何处理电子邮件，包括在 Exchange 中如何创建电子邮件以及如何通过使用 EWS 托管的 API 或 EWS 执行其他电子邮件相关任务。</span><span class="sxs-lookup"><span data-stu-id="bac19-104">Find out how to work with email messages, including how to create an email and how to perform other email-related tasks by using the EWS Managed API or EWS in Exchange.</span></span>
  

  
<span data-ttu-id="bac19-p101">其核心是，Exchange 与电子邮件有关。但是，电子邮件是怎么形成的呢？电子邮件是 Exchange 中的一种[强类型的邮件](folders-and-items-in-ews-in-exchange.md#bk_item)，这意味着它们包含一组特定[属性](email-properties-and-elements-in-ews-in-exchange.md)，甚至在发送之前也是如此。电子邮件可由 EWS 托管的 API 中的 [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 类以及由 EWS 中的 [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) 元素及其子元素进行表示。</span><span class="sxs-lookup"><span data-stu-id="bac19-p101">At its core, Exchange is about email. But what makes an email an email? Well, email messages are one of the [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item) in Exchange, which means that they contain a particular [set of properties](email-properties-and-elements-in-ews-in-exchange.md), even before they're sent. Email messages are represented by the [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) class in the EWS Managed API and by the [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element and its child elements in EWS.</span></span> 
  
<span data-ttu-id="bac19-p102">在 EWS 托管的 API 中， **EmailMessage** 对象由 [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象派生而来。 **EmailMessage** 类通过提供其他属性（如在几乎所有邮件方案中常见的 **EmailMessage.Sender** 和 [EmailMessage.IsRead](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx)）扩展 [Item](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx) 类。当您获取、更新或删除电子邮件时，在大多数情况下您可以通过使用 **EmailMessage** 对象或基 **Item** 对象来实现，具体取决于您正在使用的属性是在 [EmailMessageSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) 中还是在 [ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) 类中。项目的创建会由于 **Item** 类没有构造函数而有所不同，因此当您要创建一封电子邮件时，您将使用 [EmailMessage 构造函数](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx)进行创建以及使用 [EmailMessage.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) 或 [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法来保存它，或发送并保存它。</span><span class="sxs-lookup"><span data-stu-id="bac19-p102">In the EWS Managed API, the **EmailMessage** object derives from the [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object. The **EmailMessage** class extends the **Item** class by providing additional properties like [EmailMessage.Sender](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sender%28v=exchg.80%29.aspx) and [EmailMessage.IsRead](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.isread%28v=exchg.80%29.aspx), which are now common to nearly all messaging scenarios. When you get, update, or delete an email message, in most cases you can do that by using the **EmailMessage** object or the base **Item** object, depending on whether the properties you're working with are in the [EmailMessageSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessageschema%28v=exchg.80%29.aspx) or the [ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx) class. Item creation is different because the **Item** class does not have a constructor, so when you're creating an email, you'll use the [EmailMessage constructor](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create it and the [EmailMessage.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) or [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) methods to save it, or send it and save it.</span></span> 
  
<span data-ttu-id="bac19-p103">同样，在 EWS 中使用 [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 操作和 [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) 元素来创建一封电子邮件。若要通过使用 EWS 获取、更新或删除电子邮件，那么除了其他属性可用于电子邮件这一事实之外，正在进行修改的邮件是一封电子邮件的事实就显得不重要了。用于其他强类型邮件的相同操作还可用于电子邮件。</span><span class="sxs-lookup"><span data-stu-id="bac19-p103">Similarly, in EWS, use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element to create an email message. To get, update, or delete emails by using EWS, the fact that the item being modified is an email message is not important, aside from the fact that additional properties are available on email messages. The same operations that are used for other strongly typed items are also used for email messages.</span></span> 
  
|<span data-ttu-id="bac19-116">**任务**</span><span class="sxs-lookup"><span data-stu-id="bac19-116">**Task**</span></span>|<span data-ttu-id="bac19-117">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="bac19-117">**EWS Managed API method**</span></span>|<span data-ttu-id="bac19-118">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="bac19-118">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bac19-119">创建</span><span class="sxs-lookup"><span data-stu-id="bac19-119">Create</span></span>  <br/> |[<span data-ttu-id="bac19-120">EmailMessage.Save</span><span class="sxs-lookup"><span data-stu-id="bac19-120">EmailMessage.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bac19-121">CreateItem</span><span class="sxs-lookup"><span data-stu-id="bac19-121">CreateItem</span></span>](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="bac19-122">获取</span><span class="sxs-lookup"><span data-stu-id="bac19-122">Get</span></span>  <br/> |[<span data-ttu-id="bac19-123">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="bac19-123">EmailMessage.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bac19-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="bac19-124">GetItem</span></span>](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="bac19-125">更新</span><span class="sxs-lookup"><span data-stu-id="bac19-125">Update</span></span>  <br/> |[<span data-ttu-id="bac19-126">Item.Update</span><span class="sxs-lookup"><span data-stu-id="bac19-126">Item.Update</span></span>](https://msdn.microsoft.com/library/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bac19-127">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="bac19-127">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="bac19-128">Delete</span><span class="sxs-lookup"><span data-stu-id="bac19-128">Delete</span></span>  <br/> |[<span data-ttu-id="bac19-129">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="bac19-129">Item.Delete</span></span>](https://msdn.microsoft.com/library/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="bac19-130">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="bac19-130">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="bac19-131">因为电子邮件只是[强类型的邮件](folders-and-items-in-ews-in-exchange.md#bk_item)，所以在某些情况下您操作它们的方式与您[操作常规邮件](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)的方式是相同的。</span><span class="sxs-lookup"><span data-stu-id="bac19-131">Because email messages are simply [strongly typed items](folders-and-items-in-ews-in-exchange.md#bk_item), in some cases you work with them in the same way that you [work with generic items](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span> 
  
## <a name="create-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="bac19-132">使用 EWS 托管的 API 创建一封电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-132">Create an email message by using the EWS Managed API</span></span>
<span data-ttu-id="bac19-133"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bac19-133"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="bac19-134">您可以通过使用 EWS 托管的 API [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) 方法创建一封电子邮件，如以下示例的代码所示。</span><span class="sxs-lookup"><span data-stu-id="bac19-134">You can create an email message by using the EWS Managed API [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.save%28v=exchg.80%29.aspx) method, as shown in the code in the following example.</span></span> <span data-ttu-id="bac19-135">请注意，该示例仅将邮件保存在“草稿”文件夹中，不会发送此邮件。</span><span class="sxs-lookup"><span data-stu-id="bac19-135">Note that the example only saves the message in the Drafts folder, it does not send the message.</span></span> <span data-ttu-id="bac19-136">有关如何发送邮件或一键创建并发送邮件的信息，请参阅[使用 Exchange 中的 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bac19-136">For information about how to send the message or create and send the message in one step, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="bac19-137">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="bac19-137">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="create-an-email-message-by-using-ews"></a><span data-ttu-id="bac19-138">使用 EWS 创建一封电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-138">Create an email message by using EWS</span></span>
<span data-ttu-id="bac19-139"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="bac19-139"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="bac19-140">您可以通过使用 EWS [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) 操作创建一封电子邮件，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="bac19-140">You can create an email message by using the EWS [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation, as shown in the following example.</span></span> <span data-ttu-id="bac19-141">这也是当您 [创建电子邮件](#bk_createewsma)时，EWS 托管的 API 将发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="bac19-141">This is also the XML request that the EWS Managed API sends when you [create an email message](#bk_createewsma).</span></span> <span data-ttu-id="bac19-142">请注意，以下示例仅将邮件保存在“草稿”文件夹中，不会发送此邮件。</span><span class="sxs-lookup"><span data-stu-id="bac19-142">Note that the following example only saves the message in the Drafts folder, it does not send the message.</span></span> <span data-ttu-id="bac19-143">有关如何发送邮件或一键创建并发送邮件的信息，请参阅[使用 Exchange 中的 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bac19-143">For information about how to send the message or create and send the message in one ste, see [Send email messages by using EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="bac19-144">服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="bac19-144">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="get-update-and-delete-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="bac19-145">通过使用 EWS 托管的 API 获取、更新和删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-145">Get, update, and delete an email message by using the EWS Managed API</span></span>
<span data-ttu-id="bac19-146"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="bac19-146"><a name="bk_getewsma"> </a></span></span>

<span data-ttu-id="bac19-147">EWS 托管的 API 可以用于获取、更新或删除电子邮件，其操作方法与对 Exchange 存储中的任何常规项目执行这些操作的方法相同。</span><span class="sxs-lookup"><span data-stu-id="bac19-147">You can use the EWS Managed API to get, update, or delete an email message in the same way that you perform these actions on any generic item from the Exchange store.</span></span> <span data-ttu-id="bac19-148">有关详细信息，请参阅[使用 Exchange 中的 EWS 处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bac19-148">For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="bac19-p107">如果您要更新电子邮件，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)，了解可写的电子邮件属性的列表。若要在更新后发送草稿邮件，请参阅[通过使用 EWS 托管的 API 发送草稿电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma)。</span><span class="sxs-lookup"><span data-stu-id="bac19-p107">If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties. To send a draft message after you've updated it, see [Send a draft email message by using the EWS Managed API](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftewsma).</span></span>
  
## <a name="get-update-and-delete-an-email-message-by-using-ews"></a><span data-ttu-id="bac19-151">通过使用 EWS 获取、更新和删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-151">Get, update, and delete an email message by using EWS</span></span>
<span data-ttu-id="bac19-152"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="bac19-152"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="bac19-153">EWS 可以用于获取、更新和删除电子邮件，其操作方法与对 Exchange 存储中的任何常规项目执行这些操作的方法相同。</span><span class="sxs-lookup"><span data-stu-id="bac19-153">You can use EWS to get, update, and delete an email message in the same way that you perform these actions on any generic item from the Exchange store.</span></span> <span data-ttu-id="bac19-154">有关详细信息，请参阅[使用 Exchange 中的 EWS 处理 Exchange 邮箱项目](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bac19-154">For more information, see [Work with Exchange mailbox items by using EWS in Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="bac19-p109">如果您要更新电子邮件，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)，了解可写的电子邮件属性的列表。若要在更新后发送草稿邮件，请参阅[通过使用 EWS 发送草稿电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews)。</span><span class="sxs-lookup"><span data-stu-id="bac19-p109">If you're updating an email message, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md) for a list of writable email message properties. To send a draft message after you've updated it, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bac19-157">本节内容</span><span class="sxs-lookup"><span data-stu-id="bac19-157">In this section</span></span>
<span data-ttu-id="bac19-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="bac19-158"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="bac19-159">Exchange 中的 EWS 的电子邮件属性和元素</span><span class="sxs-lookup"><span data-stu-id="bac19-159">Email properties and elements in EWS in Exchange</span></span>](email-properties-and-elements-in-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-160">使用 Exchange 中的 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-160">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-161">使用 Exchange 中的 EWS 响应电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-161">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-162">使用 Exchange 中的 EWS 移动和复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-162">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-163">使用 Exchange 中的 EWS 处理对话</span><span class="sxs-lookup"><span data-stu-id="bac19-163">Work with conversations by using EWS in Exchange</span></span>](how-to-work-with-conversations-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-164">使用 Exchange 中的 EWS 从电子邮件中提取实体</span><span class="sxs-lookup"><span data-stu-id="bac19-164">Extract an entity from an email message by using EWS in Exchange</span></span>](how-to-extract-an-entity-from-an-email-message-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bac19-165">使用 Exchange 中的 EWS 批量处理电子邮件</span><span class="sxs-lookup"><span data-stu-id="bac19-165">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="bac19-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bac19-166">See also</span></span>


- [<span data-ttu-id="bac19-167">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="bac19-167">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="bac19-168">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="bac19-168">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

