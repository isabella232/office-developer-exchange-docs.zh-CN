---
title: 使用 Exchange 中的 EWS 响应电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 对电子邮件进行响应。
ms.openlocfilehash: 81599051f603654cdf8a50b789b37d7e76664a53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455707"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="d2df2-103">使用 Exchange 中的 EWS 响应电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-103">Respond to email messages by using EWS in Exchange</span></span>

<span data-ttu-id="d2df2-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 对电子邮件进行响应。</span><span class="sxs-lookup"><span data-stu-id="d2df2-104">Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d2df2-105">您可以使用 EWS 托管 API 或 EWS 回复邮件，或将其转发给收件人。</span><span class="sxs-lookup"><span data-stu-id="d2df2-105">You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.</span></span>
  
<span data-ttu-id="d2df2-106">**表1。用于响应电子邮件的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="d2df2-106">**Table 1. EWS Managed API methods and EWS operations for responding to email messages**</span></span>

|<span data-ttu-id="d2df2-107">**任务**</span><span class="sxs-lookup"><span data-stu-id="d2df2-107">**Task**</span></span>|<span data-ttu-id="d2df2-108">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="d2df2-108">**EWS Managed API method**</span></span>|<span data-ttu-id="d2df2-109">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="d2df2-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2df2-110">答复电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-110">Reply to an email message</span></span>  <br/> |[<span data-ttu-id="d2df2-111">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="d2df2-111">EmailMessage.Reply</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="d2df2-112">EmailMessage。 CreateReply</span><span class="sxs-lookup"><span data-stu-id="d2df2-112">EmailMessage.CreateReply</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="d2df2-113">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)，其中[Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素的子元素为[ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx)或[ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d2df2-113">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="d2df2-114">转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-114">Forward an email message</span></span>  <br/> |[<span data-ttu-id="d2df2-115">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="d2df2-115">EmailMessage.Forward</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="d2df2-116">EmailMessage。 CreateForward</span><span class="sxs-lookup"><span data-stu-id="d2df2-116">EmailMessage.CreateForward</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="d2df2-117">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)，其中[Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素具有[ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)的子元素。</span><span class="sxs-lookup"><span data-stu-id="d2df2-117">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).</span></span>  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="d2df2-118">使用 EWS 托管 API 答复电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-118">Reply to an email message by using the EWS Managed API</span></span>
<span data-ttu-id="d2df2-119"><a name="bk_replyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d2df2-119"><a name="bk_replyewsma"> </a></span></span>

<span data-ttu-id="d2df2-120">EWS 托管 API 提供了两种方法，可用于响应邮件： [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)和[CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d2df2-120">The EWS Managed API provides two methods that you can use to respond to messages: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="d2df2-121">**Reply**方法仅采用两个参数：要在现有正文前面追加的响应消息，以及一个**布尔**值，指示响应是应转到所有收件人（true）还是仅发件人（false）。</span><span class="sxs-lookup"><span data-stu-id="d2df2-121">The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false).</span></span> <span data-ttu-id="d2df2-122">如果需要向邮件中添加其他收件人、设置响应的其他属性或添加附件，请使用**CreateReply**方法，该方法使您能够设置[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象上可用的所有[第一类属性](email-properties-and-elements-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d2df2-122">If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="d2df2-123">下面的代码示例演示如何使用**Reply**方法响应电子邮件。</span><span class="sxs-lookup"><span data-stu-id="d2df2-123">The following code example shows how to use the **Reply** method to respond to an email message.</span></span> 
  
<span data-ttu-id="d2df2-124">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d2df2-124">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="d2df2-125">本地变量*ItemId*是要响应的项的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d2df2-125">The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to.</span></span> <span data-ttu-id="d2df2-126">该示例调用[FindRecentlySent 方法](#bk_findlast)来验证是否已将邮件标记为 "已答复"。</span><span class="sxs-lookup"><span data-stu-id="d2df2-126">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.LastModifiedTime);
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
string myReply = "This is the message body of the email reply.";
bool replyToAll = false;
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Reply(myReply, replyToAll);
// Verify that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="d2df2-127">下面的代码示例演示如何使用**CreateReply**方法来响应电子邮件。</span><span class="sxs-lookup"><span data-stu-id="d2df2-127">The following code example shows how to use the **CreateReply** method to respond to an email message.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
bool replyToAll = true;
ResponseMessage responseMessage = message.CreateReply(replyToAll);
// Prepend the reply to the message body. 
string myReply = "This is the message body of the email reply.";
responseMessage.BodyPrefix = myReply;
// Send the response message.
// This method call results in a CreateItem call to EWS.
responseMessage.SendAndSaveCopy();
// Check that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="d2df2-128">如果需要将附件添加到响应消息，请将对**SendAndSaveCopy**方法的调用替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="d2df2-128">If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a><span data-ttu-id="d2df2-129">使用 EWS 答复电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-129">Reply to an email message by using EWS</span></span>
<span data-ttu-id="d2df2-130"><a name="bk_replyews"> </a></span><span class="sxs-lookup"><span data-stu-id="d2df2-130"><a name="bk_replyews"> </a></span></span>

<span data-ttu-id="d2df2-131">下面的代码示例演示如何使用 EWS 回复邮件。</span><span class="sxs-lookup"><span data-stu-id="d2df2-131">The following code example shows how to reply to a message by using EWS.</span></span> <span data-ttu-id="d2df2-132">使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作，将**MessageDisposition**属性设置为**SendAndSaveCopy** ，以发送邮件并将响应保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d2df2-132">Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="d2df2-133">包含[ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)元素作为[Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素的子元素，以答复邮件线程中的每个人，或包含[ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx)元素以仅答复发件人。</span><span class="sxs-lookup"><span data-stu-id="d2df2-133">Include either the [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender.</span></span> 
  
<span data-ttu-id="d2df2-134">这也是在调用[Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)或[CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx)方法时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d2df2-134">This is also the XML request that the EWS Managed API sends when calling either the [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ReplyAllToItem>
          <t:ReferenceItemId Id="AAMkADE4="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the email reply.</t:NewBodyContent>
        </t:ReplyAllToItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d2df2-135">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功创建并发送了答复。</span><span class="sxs-lookup"><span data-stu-id="d2df2-135">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.</span></span>
  
<span data-ttu-id="d2df2-136">如果需要将附件添加到响应邮件中，请按照上面的规定调用**CreateItem**操作，但将**MessageDisposition**更改为**SaveOnly**。</span><span class="sxs-lookup"><span data-stu-id="d2df2-136">If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="d2df2-137">然后，调用[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作，后跟[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="d2df2-137">Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="d2df2-138">使用 EWS 托管 API 转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-138">Forward an email message by using the EWS Managed API</span></span>
<span data-ttu-id="d2df2-139"><a name="bk_forwardewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d2df2-139"><a name="bk_forwardewsma"> </a></span></span>

<span data-ttu-id="d2df2-140">EWS 托管 API 提供了两种可用于转发邮件的方法： [forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx)和[CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d2df2-140">The EWS Managed API provides two methods that you can use to forward messages: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="d2df2-141">**Forward**方法仅采用两个参数：要追加到现有正文的邮件，以及一个或一组收件人，具体取决于您选择使用的重载。</span><span class="sxs-lookup"><span data-stu-id="d2df2-141">The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use.</span></span> <span data-ttu-id="d2df2-142">如果需要将附件添加到要转发的邮件中，或在新邮件上设置其他属性，请使用**CreateForward**方法，该方法使您能够设置[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象上可用的所有属性。</span><span class="sxs-lookup"><span data-stu-id="d2df2-142">If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="d2df2-143">下面的代码示例演示如何使用**forward**方法将电子邮件转发给一个收件人。</span><span class="sxs-lookup"><span data-stu-id="d2df2-143">The following code example shows how to use the **Forward** method to forward an email message to one recipient.</span></span> 
  
<span data-ttu-id="d2df2-144">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d2df2-144">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="d2df2-145">本地变量*ItemId*是要转发的项的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d2df2-145">The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward.</span></span> <span data-ttu-id="d2df2-146">该示例调用[FindRecentlySent 方法](#bk_findlast)来验证是否已将邮件标记为 "已转发"。</span><span class="sxs-lookup"><span data-stu-id="d2df2-146">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
string myForward = "This is the message body of the forwarded email.";
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Forward(myForward, "sadie@contoso.com");
// Verify that the forwarded response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="d2df2-147">下面的代码示例演示如何使用**CreateForward**方法将电子邮件转发给一个收件人。</span><span class="sxs-lookup"><span data-stu-id="d2df2-147">The following code example shows how to use the **CreateForward** method to forward an email message to one recipient.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
ResponseMessage forwardMessage = message.CreateForward();
// Set properties on the email message.
forwardMessage.ToRecipients.Add("sadie@contoso.com");
forwardMessage.Body = "Sadie,<br><br>I thought you'd be interested in this thread.<br><br>-Mack";
// Send and save a copy of the replied email message in the default Sent Items folder. 
forwardMessage.SendAndSaveCopy();
// Verify that the forwarded message was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="d2df2-148">如果需要向转发的邮件中添加附件，请将对**SendAndSaveCopy**方法的调用替换为以下代码。</span><span class="sxs-lookup"><span data-stu-id="d2df2-148">If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a><span data-ttu-id="d2df2-149">使用 EWS 转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-149">Forward an email message by using EWS</span></span>
<span data-ttu-id="d2df2-150"><a name="bk_forwardews"> </a></span><span class="sxs-lookup"><span data-stu-id="d2df2-150"><a name="bk_forwardews"> </a></span></span>

<span data-ttu-id="d2df2-151">下面的代码示例演示如何使用 EWS 转发邮件。</span><span class="sxs-lookup"><span data-stu-id="d2df2-151">The following code example shows how to forward a message by using EWS.</span></span> <span data-ttu-id="d2df2-152">使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作，将**MessageDisposition**属性设置为**SendAndSaveCopy** ，以发送邮件并将响应保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d2df2-152">Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="d2df2-153">[ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)元素指示项目是转发的邮件。</span><span class="sxs-lookup"><span data-stu-id="d2df2-153">The [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message.</span></span> 
  
<span data-ttu-id="d2df2-154">这也是在调用[Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx)或[CREATEFORWARD](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx)方法时 EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d2df2-154">This is also the XML request that the EWS Managed API sends when calling either the [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method.</span></span> 
  
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
      <m:Items>
        <t:ForwardItem>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:ReferenceItemId Id="AAAMkADE="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the forwarded email.</t:NewBodyContent>
        </t:ForwardItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d2df2-155">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，这表示已转发的邮件已成功创建和发送。</span><span class="sxs-lookup"><span data-stu-id="d2df2-155">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.</span></span>
  
<span data-ttu-id="d2df2-156">如果需要将附件添加到响应消息中，请调用**CreateItem**操作，但将**MessageDisposition**更改为**SaveOnly**。</span><span class="sxs-lookup"><span data-stu-id="d2df2-156">If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="d2df2-157">然后，调用[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作，后跟[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="d2df2-157">Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a><span data-ttu-id="d2df2-158">查找上次使用 EWS 托管 API 答复或转发的邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-158">Find the message last replied to or forwarded by using the EWS Managed API</span></span>
<span data-ttu-id="d2df2-159"><a name="bk_findlast"> </a></span><span class="sxs-lookup"><span data-stu-id="d2df2-159"><a name="bk_findlast"> </a></span></span>

<span data-ttu-id="d2df2-160">下面的代码示例演示如何查找上次执行的动作以及在指定项目上执行最后一个动作的时间。</span><span class="sxs-lookup"><span data-stu-id="d2df2-160">The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified.</span></span> <span data-ttu-id="d2df2-161">此方法从本主题中的其他 EWS 托管 API 代码示例中调用，以验证您答复或转发的项目是否已在您的收件箱中标记为已答复或已转发。</span><span class="sxs-lookup"><span data-stu-id="d2df2-161">This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox.</span></span> 
  
<span data-ttu-id="d2df2-162">该示例使用[PidTagLastVerbExecuted](https://msdn.microsoft.com/library/cc841968.aspx) （0x10820003）扩展属性来确定邮件是答复、全部答复还是转发，以及[PidTagLastVerbExecutionTime](https://msdn.microsoft.com/library/cc839918.aspx) （0x10820040）扩展属性，以确定答复或转发何时发送。</span><span class="sxs-lookup"><span data-stu-id="d2df2-162">The example uses the [PidTagLastVerbExecuted](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent.</span></span> 
  
```cs
public static void FindRecentlySent(EmailMessage messageToCheck)
{
    // Create extended property definitions for PidTagLastVerbExecuted and PidTagLastVerbExecutionTime.
    ExtendedPropertyDefinition PidTagLastVerbExecuted = new ExtendedPropertyDefinition(0x1081, MapiPropertyType.Integer);
    ExtendedPropertyDefinition PidTagLastVerbExecutionTime = new ExtendedPropertyDefinition(0x1082, MapiPropertyType.SystemTime);
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, PidTagLastVerbExecutionTime, PidTagLastVerbExecuted);
    messageToCheck = EmailMessage.Bind(service, messageToCheck.Id, propSet);
    // Determine the last verb executed on the message and display output.
    object responseType;
    if (messageToCheck.TryGetProperty(PidTagLastVerbExecuted, out responseType))
    {
        object ReplyTime = null;
        switch (((Int32)responseType))
        {
            case 102: Console.WriteLine("A reply was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 103: Console.WriteLine("A reply all was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 104: Console.WriteLine("The '" + messageToCheck.Subject.ToString() + "' email message was forwarded at");
                break;
        }
        if (messageToCheck.TryGetProperty(PidTagLastVerbExecutionTime, out ReplyTime))
        {
            Console.WriteLine(((DateTime)ReplyTime).ToString() + ".");
        }
    }
    else
    {
        Console.WriteLine("No changes were made to  '" + messageToCheck.Subject.ToString() + "'.");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="d2df2-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2df2-163">See also</span></span>


- [<span data-ttu-id="d2df2-164">Exchange 中的电子邮件和 EMS</span><span class="sxs-lookup"><span data-stu-id="d2df2-164">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d2df2-165">使用 Exchange 中的 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="d2df2-165">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

