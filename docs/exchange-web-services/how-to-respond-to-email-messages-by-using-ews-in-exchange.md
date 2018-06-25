---
title: 在 Exchange 使用 EWS 响应电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 响应电子邮件。
ms.openlocfilehash: 2f1428251084a7f2bf8d589a788c143f34b64d5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752878"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="10959-103">在 Exchange 使用 EWS 响应电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-103">Respond to email messages by using EWS in Exchange</span></span>

<span data-ttu-id="10959-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 响应电子邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-104">Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="10959-105">您可以使用 EWS 托管 API 或 EWS 回复邮件答复这些或将它们转发给收件人。</span><span class="sxs-lookup"><span data-stu-id="10959-105">You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.</span></span>
  
<span data-ttu-id="10959-106">**表 1。EWS 托管 API 方法和响应对电子邮件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="10959-106">**Table 1. EWS Managed API methods and EWS operations for responding to email messages**</span></span>

|<span data-ttu-id="10959-107">**任务**</span><span class="sxs-lookup"><span data-stu-id="10959-107">**Task**</span></span>|<span data-ttu-id="10959-108">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="10959-108">**EWS Managed API method**</span></span>|<span data-ttu-id="10959-109">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="10959-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10959-110">答复电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-110">Reply to an email message</span></span>  <br/> |[<span data-ttu-id="10959-111">EmailMessage.Reply</span><span class="sxs-lookup"><span data-stu-id="10959-111">EmailMessage.Reply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="10959-112">EmailMessage.CreateReply</span><span class="sxs-lookup"><span data-stu-id="10959-112">EmailMessage.CreateReply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="10959-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)，其中的[项目](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素具有[ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx)或[ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)的子元素。</span><span class="sxs-lookup"><span data-stu-id="10959-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="10959-114">转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-114">Forward an email message</span></span>  <br/> |[<span data-ttu-id="10959-115">EmailMessage.Forward</span><span class="sxs-lookup"><span data-stu-id="10959-115">EmailMessage.Forward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="10959-116">EmailMessage.CreateForward</span><span class="sxs-lookup"><span data-stu-id="10959-116">EmailMessage.CreateForward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="10959-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)，其中的[项目](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素具有[ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)的子元素。</span><span class="sxs-lookup"><span data-stu-id="10959-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).</span></span>  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="10959-118">使用 EWS 托管 API 对电子邮件答复</span><span class="sxs-lookup"><span data-stu-id="10959-118">Reply to an email message by using the EWS Managed API</span></span>
<span data-ttu-id="10959-119"><a name="bk_replyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="10959-119"></span></span>

<span data-ttu-id="10959-120">EWS 托管 API 提供了两种方法可用来响应消息:[答复](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)和[CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="10959-120">The EWS Managed API provides two methods that you can use to respond to messages: [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="10959-121">**Reply**方法只需两个参数： 要附加到现有的 body、 和一个**布尔**值，该值指示是否响应应转到所有收件人 (true) 或刚刚发件人 (false) 的响应消息。</span><span class="sxs-lookup"><span data-stu-id="10959-121">The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false).</span></span> <span data-ttu-id="10959-122">如果您需要将其他收件人添加到一条消息上一个响应，, 设置其他属性或添加附件，使用**CreateReply**方法，以便您可以设置所有[一类属性](email-properties-and-elements-in-ews-in-exchange.md) [EmailMessage 上可用](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="10959-122">If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="10959-123">下面的代码示例演示如何使用**Reply**方法来响应电子邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-123">The following code example shows how to use the **Reply** method to respond to an email message.</span></span> 
  
<span data-ttu-id="10959-124">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="10959-124">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="10959-125">局部变量*ItemId*是项目的[Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)的响应。</span><span class="sxs-lookup"><span data-stu-id="10959-125">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to.</span></span> <span data-ttu-id="10959-126">该示例调用[FindRecentlySent 方法](#bk_findlast)以验证邮件被标记为答复。</span><span class="sxs-lookup"><span data-stu-id="10959-126">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to.</span></span> 
  
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

<span data-ttu-id="10959-127">下面的代码示例演示如何使用**CreateReply**方法来响应电子邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-127">The following code example shows how to use the **CreateReply** method to respond to an email message.</span></span> 
  
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

<span data-ttu-id="10959-128">如果您需要将附件添加到响应消息，请替换为以下代码替换对**SendAndSaveCopy**方法的调用。</span><span class="sxs-lookup"><span data-stu-id="10959-128">If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a><span data-ttu-id="10959-129">通过 EWS 答复电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-129">Reply to an email message by using EWS</span></span>
<span data-ttu-id="10959-130"><a name="bk_replyews"> </a></span><span class="sxs-lookup"><span data-stu-id="10959-130"></span></span>

<span data-ttu-id="10959-131">下面的代码示例演示如何使用 EWS 答复邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-131">The following code example shows how to reply to a message by using EWS.</span></span> <span data-ttu-id="10959-132">使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation， **MessageDisposition**属性设置为**SendAndSaveCopy**发送消息，并在已发送邮件文件夹中保存的响应。</span><span class="sxs-lookup"><span data-stu-id="10959-132">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="10959-133">作为[项目](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx)元素的子元素来答复邮件线程上的所有人都包括[ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)元素或包含[ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx)元素以仅答复发件人。</span><span class="sxs-lookup"><span data-stu-id="10959-133">Include either the [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender.</span></span> 
  
<span data-ttu-id="10959-134">这也是调用[答复](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)或[CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx)方法时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="10959-134">This is also the XML request that the EWS Managed API sends when calling either the [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="10959-135">服务器响应[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明答复已创建并成功发送**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="10959-135">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.</span></span>
  
<span data-ttu-id="10959-136">如果您需要将附件添加到响应消息，请调用**CreateItem** operation，指定上方，但需要更改**MessageDisposition**为**SaveOnly**。</span><span class="sxs-lookup"><span data-stu-id="10959-136">If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="10959-137">然后调用[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作后, 跟[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="10959-137">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="10959-138">使用 EWS 托管 API 转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-138">Forward an email message by using the EWS Managed API</span></span>
<span data-ttu-id="10959-139"><a name="bk_forwardewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="10959-139"></span></span>

<span data-ttu-id="10959-140">EWS 托管 API 提供了可用于将邮件转发的两种方法：[向前](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx)和[CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="10959-140">The EWS Managed API provides two methods that you can use to forward messages: [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="10959-141">**转接**方法只需两个参数： 要附加到现有的 body、 数组或集合的收件人，具体取决于您选择要使用的重载的消息。</span><span class="sxs-lookup"><span data-stu-id="10959-141">The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use.</span></span> <span data-ttu-id="10959-142">如果您需要添加到您转接，或设置其他属性，对新邮件的邮件的附件，请使用**CreateForward**方法，以便您可以设置[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象可用的所有属性。</span><span class="sxs-lookup"><span data-stu-id="10959-142">If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="10959-143">下面的代码示例演示如何使用**转接**方法可将一封电子邮件转发给一个收件人。</span><span class="sxs-lookup"><span data-stu-id="10959-143">The following code example shows how to use the **Forward** method to forward an email message to one recipient.</span></span> 
  
<span data-ttu-id="10959-144">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="10959-144">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="10959-145">局部变量*ItemId*是项目的[Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)的转发。</span><span class="sxs-lookup"><span data-stu-id="10959-145">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward.</span></span> <span data-ttu-id="10959-146">该示例调用[FindRecentlySent 方法](#bk_findlast)以验证邮件被标记为转发。</span><span class="sxs-lookup"><span data-stu-id="10959-146">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded.</span></span> 
  
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

<span data-ttu-id="10959-147">下面的代码示例演示如何使用**CreateForward**方法可将一封电子邮件转发给一个收件人。</span><span class="sxs-lookup"><span data-stu-id="10959-147">The following code example shows how to use the **CreateForward** method to forward an email message to one recipient.</span></span> 
  
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

<span data-ttu-id="10959-148">如果您需要添加到转发邮件的附件，替换为以下代码替换对**SendAndSaveCopy**方法的调用。</span><span class="sxs-lookup"><span data-stu-id="10959-148">If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a><span data-ttu-id="10959-149">使用 EWS 转发电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-149">Forward an email message by using EWS</span></span>
<span data-ttu-id="10959-150"><a name="bk_forwardews"> </a></span><span class="sxs-lookup"><span data-stu-id="10959-150"></span></span>

<span data-ttu-id="10959-151">下面的代码示例演示如何使用 EWS 转发的邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-151">The following code example shows how to forward a message by using EWS.</span></span> <span data-ttu-id="10959-152">使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation， **MessageDisposition**属性设置为**SendAndSaveCopy**发送消息，并在已发送邮件文件夹中保存的响应。</span><span class="sxs-lookup"><span data-stu-id="10959-152">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="10959-153">[ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)元素表示项目转发的邮件。</span><span class="sxs-lookup"><span data-stu-id="10959-153">The [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message.</span></span> 
  
<span data-ttu-id="10959-154">这也是 EWS 托管 API 将呼叫[转接](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx)或[CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx)方法时发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="10959-154">This is also the XML request that the EWS Managed API sends when calling either the [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="10959-155">服务器响应[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明转发的邮件已创建并成功发送**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="10959-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.</span></span>
  
<span data-ttu-id="10959-156">如果您需要将附件添加到响应消息，请调用**CreateItem** operation，但将**MessageDisposition**更改为**SaveOnly**。</span><span class="sxs-lookup"><span data-stu-id="10959-156">If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="10959-157">然后调用[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作后, 跟[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="10959-157">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a><span data-ttu-id="10959-158">查找上次答复或转发使用 EWS 托管 API 的邮件</span><span class="sxs-lookup"><span data-stu-id="10959-158">Find the message last replied to or forwarded by using the EWS Managed API</span></span>
<span data-ttu-id="10959-159"><a name="bk_findlast"> </a></span><span class="sxs-lookup"><span data-stu-id="10959-159"></span></span>

<span data-ttu-id="10959-160">下面的代码示例演示如何查找执行的最后一个谓词和时间的最后一个动作上执行指定的项。</span><span class="sxs-lookup"><span data-stu-id="10959-160">The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified.</span></span> <span data-ttu-id="10959-161">从其他验证已标记为已答复或转发收件箱中的项目答复或转发本主题中的 EWS 托管 API 代码示例调用此方法。</span><span class="sxs-lookup"><span data-stu-id="10959-161">This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox.</span></span> 
  
<span data-ttu-id="10959-162">该示例使用[PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) 扩展属性来确定是否邮件已答复、 全部答复或正向和[PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) 扩展属性来确定何时发送答复或转发。</span><span class="sxs-lookup"><span data-stu-id="10959-162">The example uses the [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="10959-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10959-163">See also</span></span>


- [<span data-ttu-id="10959-164">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="10959-164">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="10959-165">在 Exchange 使用 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="10959-165">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

