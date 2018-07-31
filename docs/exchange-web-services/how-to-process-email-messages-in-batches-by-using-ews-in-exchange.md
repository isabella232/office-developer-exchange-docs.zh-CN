---
title: 在 Exchange 中使用 EWS 的批次中的过程电子邮件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: 了解如何创建、 获取、 更新和删除在 Exchange 使用 EWS 托管 API 或 EWS 批次的单个调用中的电子邮件。
ms.openlocfilehash: b7dcc8f0961a34061b0476e2136193bf21731d99
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354041"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="4d48a-103">在 Exchange 中使用 EWS 的批次中的过程电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-103">Process email messages in batches by using EWS in Exchange</span></span>

<span data-ttu-id="4d48a-104">了解如何创建、 获取、 更新和删除在 Exchange 使用 EWS 托管 API 或 EWS 批次的单个调用中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-104">Learn how to create, get, update, and delete batches of email messages in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4d48a-105">您可以使用 EWS 托管 API 或 EWS 客户端使用的电子邮件以减少的呼叫数的批次向 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="4d48a-105">You can use the EWS Managed API or EWS to work with batches of email messages to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="4d48a-106">使用 EWS 托管 API 创建、 获取、 更新、 删除和批处理中发送消息，您会使用[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象方法，而当您处理单个电子邮件，则使用[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象方法。</span><span class="sxs-lookup"><span data-stu-id="4d48a-106">When you use the EWS Managed API to create, get, update, delete, and send messages in batches, you use [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single email messages, you use [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="4d48a-107">如果您使用 EWS，您使用的相同操作来处理简单和批量电子邮件消息。</span><span class="sxs-lookup"><span data-stu-id="4d48a-107">If you are using EWS, you use the same operations to work with both single and batches of email messages.</span></span> 
  
<span data-ttu-id="4d48a-108">**表 1。EWS 托管 API 方法和用于处理电子邮件的批次的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4d48a-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of email messages**</span></span>

|<span data-ttu-id="4d48a-109">**若要...**</span><span class="sxs-lookup"><span data-stu-id="4d48a-109">**In order to…**</span></span>|<span data-ttu-id="4d48a-110">**使用此 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="4d48a-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="4d48a-111">**使用此 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4d48a-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d48a-112">在批处理中创建电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-112">Create email messages in batches</span></span>  <br/> |[<span data-ttu-id="4d48a-113">ExchangeService.CreateItems</span><span class="sxs-lookup"><span data-stu-id="4d48a-113">ExchangeService.CreateItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4d48a-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="4d48a-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4d48a-115">获取批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-115">Get email messages in batches</span></span>  <br/> |[<span data-ttu-id="4d48a-116">ExchangeService.BindToItems</span><span class="sxs-lookup"><span data-stu-id="4d48a-116">ExchangeService.BindToItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4d48a-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="4d48a-117">GetItem</span></span>](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4d48a-118">更新批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-118">Update email messages in batches</span></span>  <br/> |[<span data-ttu-id="4d48a-119">ExchangeService.UpdateItems</span><span class="sxs-lookup"><span data-stu-id="4d48a-119">ExchangeService.UpdateItems</span></span>](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4d48a-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="4d48a-120">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4d48a-121">删除批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-121">Delete email messages in batches</span></span>  <br/> |[<span data-ttu-id="4d48a-122">ExchangeService.DeleteItems</span><span class="sxs-lookup"><span data-stu-id="4d48a-122">ExchangeService.DeleteItems</span></span>](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4d48a-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="4d48a-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="4d48a-124">在本文中，您将了解如何通过使用 EWS 托管 API 或 EWS 完成的批量电子邮件的基本任务。</span><span class="sxs-lookup"><span data-stu-id="4d48a-124">In this article, you'll learn how to complete basic tasks for batches of email messages by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4d48a-125">通过使用 EWS 托管 API 批次中创建电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-125">Create email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4d48a-126"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-126"></span></span>

<span data-ttu-id="4d48a-127">下面的示例中所示，可以创建批次中使用 EWS 托管 API **CreateItems**方法的邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-127">You can create messages in batches by using the EWS Managed API **CreateItems** method, as shown in the following example.</span></span> <span data-ttu-id="4d48a-128">本示例创建本地的三个[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象，将每条消息添加到集合中，然后调用**CreateItems**方法集合的邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-128">This example creates three [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects locally, adds each message to a collection, then calls the **CreateItems** method on the collection of messages.</span></span> 
  
<span data-ttu-id="4d48a-129">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d48a-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<ItemId> CreateDraftEmailInBatch(ExchangeService service)
{
    // These are unsaved local instances of an EmailMessage object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    EmailMessage message1 = new EmailMessage(service);
    EmailMessage message2 = new EmailMessage(service);
    EmailMessage message3 = new EmailMessage(service);
    // Set the properties on the first message.
    message1.Subject = "Project priorities";
    message1.Body = "(1) Buy pizza, (2) Eat pizza";
    message1.ToRecipients.Add("sadie@contoso.com");
    // Set the properties on the second message.
    message2.Subject = "Company Soccer Team";
    message2.Body = "Are you interested in joining?";
    message2.ToRecipients.Add("magdalena@contoso.com");
    // Set the properties on the third message.
    message3.Subject = "Code Blast";
    message3.Body = "Are you interested in getting together to finish the methods for the ContosoLive project?";
    message3.ToRecipients.Add("mack@contoso.com");
    // Add the EmailMessage objects to a collection.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>() { message1, message2, message3 };
    // Create the batch of email messages on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.Drafts, MessageDisposition.SaveOnly, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created email messages.
    foreach (EmailMessage message in messageItems)
    {
        try
        {
            itemIds.Add(message.Id);
            Console.WriteLine("Email message '{0}' created successfully.", message.Subject);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating message {0}: {1}", message.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Check for success of the CreateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created messages were successfully saved to the Drafts folder.");
            Console.WriteLine("\r\n");
    }
   
    // If the method did not return success, print the result message for each email.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (message {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

<span data-ttu-id="4d48a-130">请注意该示例在草稿文件夹中; 仅保存邮件它不会发送邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-130">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="4d48a-131">有关如何发送该邮件的详细信息，请参阅[使用 EWS 托管 API 的批处理中发送电子邮件](#bk_sendewsma)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-131">For more about how to send the messages, see [Send email messages in batches by using the EWS Managed API](#bk_sendewsma).</span></span>
  
## <a name="create-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="4d48a-132">通过使用 EWS 批次中创建电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-132">Create email messages in batches by using EWS</span></span>
<span data-ttu-id="4d48a-133"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-133"></span></span>

<span data-ttu-id="4d48a-134">您可以使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS 操作的批次中创建电子邮件中下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="4d48a-134">You can create email messages in batches by using the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="4d48a-135">这也是 EWS 托管 API 时您使用 EWS 托管 API 创建[在批次中的电子邮件](#bk_createewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-135">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create email messages in batches](#bk_createewsma).</span></span> 
  
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
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>magdalena@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Code Blast</t:Subject>
          <t:Body BodyType="HTML">Are you interested in getting together to finish the methods for the ContosoLive project?</t:Body>
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

<span data-ttu-id="4d48a-136">服务器响应**CreateItem**请求[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的新消息，指示每个电子邮件已创建并成功保存的每个包含**NoError** [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值.</span><span class="sxs-lookup"><span data-stu-id="4d48a-136">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and saved successfully.</span></span> 
  
<span data-ttu-id="4d48a-137">请注意该示例在草稿文件夹中; 仅保存邮件它不会发送邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-137">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="4d48a-138">有关如何发送该邮件的详细信息，请参阅[使用 EWS 批处理中的发送电子邮件](#bk_sendews)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-138">For more about how to send the messages, see [Send email messages in batches by using EWS](#bk_sendews).</span></span>
  
## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4d48a-139">使用 EWS 托管 API 批处理中发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-139">Send email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4d48a-140"><a name="bk_sendewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-140"></span></span>

<span data-ttu-id="4d48a-141">使用相同的代码中的用于批处理中创建电子邮件之处在于[CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)方法参数的一些更改批发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-141">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method parameters change.</span></span> <span data-ttu-id="4d48a-142">因此，使用 EWS 托管 API 发送电子邮件，使用您使用来[创建批次中的电子邮件](#bk_createewsma)，代码，并对**CreateItems**方法的调用替换下面的示例中的调用。</span><span class="sxs-lookup"><span data-stu-id="4d48a-142">So, to send email messages by using the EWS Managed API, use the code you use to [create email messages in batches](#bk_createewsma), and replace the call to the **CreateItems** method with the call in the following example.</span></span> <span data-ttu-id="4d48a-143">本示例中，在已发送邮件文件夹中创建邮件和消息处置更改为[MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx)，以便发送，并且不只是保存在本地邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-143">In this example, the messages are created in the Sent Items folder, and the message disposition is changed to [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so that the message is sent, and not just saved locally.</span></span>
  
```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="4d48a-144">使用 EWS 批处理中发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-144">Send email messages in batches by using EWS</span></span>
<span data-ttu-id="4d48a-145"><a name="bk_sendews"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-145"></span></span>

<span data-ttu-id="4d48a-146">使用相同的代码，您使用电子邮件中创建批次，只不过几个属性值更改为**CreateItem** operation 批处理中发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-146">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the attribute values change for the **CreateItem** operation.</span></span> <span data-ttu-id="4d48a-147">因此，若要使用 EWS 发送电子邮件，请使用的代码使用[创建批次中的电子邮件](#bk_createews)，并将**MessageDisposition**值更改为"SendAndSaveCopy"，并将[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)更改为"已发送邮件"，如中所示下面的代码示例。</span><span class="sxs-lookup"><span data-stu-id="4d48a-147">So, to send email messages by using EWS, use the code you use to [create email message in batches](#bk_createews), and change the **MessageDisposition** value to "SendAndSaveCopy", and change the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) to "sentitems", as shown in the following code example.</span></span> 
  
```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

<span data-ttu-id="4d48a-148">服务器响应[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息**NoError** [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值包含每个新消息，指示每个电子邮件已创建并成功发送**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-148">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and sent successfully.</span></span> 
  
## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4d48a-149">通过使用 EWS 托管 API 获取批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-149">Get email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4d48a-150"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-150"></span></span>

<span data-ttu-id="4d48a-151">您可以通过使用 EWS 托管 API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)方法的批次中获取电子邮件中下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="4d48a-151">You can get email messages in batches by using the EWS Managed API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="4d48a-152">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d48a-152">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<EmailMessage> BatchGetEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Create a property set that limits the properties returned by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
    // Get the items from the server.
    // This method call results in a GetItem call to EWS.
    ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);
           
    // Instantiate a collection of EmailMessage objects to populate from the values that are returned by the Exchange server.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>();
    foreach (GetItemResponse getItemResponse in response)
    {
        try
        {
            Item item = getItemResponse.Item;
            EmailMessage message = (EmailMessage)item;
            messageItems.Add(message);
            // Print out confirmation and the last eight characters of the item ID.
            Console.WriteLine("Found item {0}.", message.Id.ToString().Substring(144));
        }
        catch (Exception ex)
        {
           Console.WriteLine("Exception while getting a message: {0}", ex.Message);
        }
    }
    // Check for success of the BindToItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages retrieved successfully.");
        Console.WriteLine("\r\n");
    }
        return messageItems;
}
```

## <a name="get-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="4d48a-153">通过使用 EWS 获取批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-153">Get email messages in batches by using EWS</span></span>
<span data-ttu-id="4d48a-154"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-154"></span></span>

<span data-ttu-id="4d48a-155">您可以通过在下面的示例使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作和代码批次中获取电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-155">You can get email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="4d48a-156">这也是 EWS 托管 API 时您使用 EWS 托管 API[获取批次中的电子邮件](#bk_getewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-156">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get email messages in batches](#bk_getewsma).</span></span> 
  
<span data-ttu-id="4d48a-157">为便于阅读变短了**ItemId**和**更改密钥**属性。</span><span class="sxs-lookup"><span data-stu-id="4d48a-157">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="m4NxAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB0" />
        <t:ItemId Id="m4NyAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB1" />
        <t:ItemId Id="m4NzAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB2" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="4d48a-158">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)消息的每个请求的消息中包括[第一类的属性](email-properties-and-elements-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-158">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the [first class properties](email-properties-and-elements-in-ews-in-exchange.md) for each of the requested messages.</span></span> 
  
## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4d48a-159">使用 EWS 托管 API 更新批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-159">Update email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4d48a-160"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-160"></span></span>

<span data-ttu-id="4d48a-161">您可以通过使用 EWS 托管 API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx)方法的批次中获取电子邮件中下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="4d48a-161">You can get email messages in batches by using the EWS Managed API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="4d48a-162">可写的电子邮件属性的列表，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-162">For a list of writable email message properties, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="4d48a-163">有关如何发送邮件草稿已更新后的详细信息，请参阅[使用 EWS 托管 API 发送电子邮件](#bk_sendewsma)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-163">For details about how to send a draft message after it's been updated, see [Sending email messages by using the EWS Managed API](#bk_sendewsma).</span></span>
  
<span data-ttu-id="4d48a-164">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d48a-164">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static Collection<EmailMessage> BatchUpdateEmailItems(ExchangeService service, Collection<EmailMessage> messageItems)
{
    // Update the subject of each message locally.
    foreach (EmailMessage message in messageItems)
    {
        // Update the Subject of the email.
        message.Subject = "Updated subject at " + DateTime.Now;
        // Print out confirmation with the last eight characters of the item ID and the email subject.
        Console.WriteLine("Updated local email message {0} with the subject '{1}'.", message.Id.ToString().Substring(144), message.Subject);
    }
    // Send the item updates to the server.
    // This method call results in an UpdateItem call to EWS.
    ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(messageItems, WellKnownFolderName.Drafts, ConflictResolutionMode.AutoResolve, MessageDisposition.SaveOnly, null);
    // Check for success of the UpdateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages updated successfully.\r\n");
    }
    // If the method did not return success, print the result message for each email.
    else
    {
        Console.WriteLine("All emails were not successfully saved on the server.\r\n");
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            Console.WriteLine("Result for (message {0}): {1}", counter, resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            counter++;
        }
    }
    return messageItems;
}    
```

## <a name="update-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="4d48a-165">使用 EWS 更新批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-165">Update email messages in batches by using EWS</span></span>
<span data-ttu-id="4d48a-166"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-166"></span></span>

<span data-ttu-id="4d48a-167">下面的代码示例中所示，您可以通过使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作，更新批次中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-167">You can update email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="4d48a-168">这也是 EWS 托管 API 时您使用 EWS 托管 API 更新[批次中的电子邮件](#bk_updateewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-168">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update email messages in batches](#bk_updateewsma).</span></span>
  
<span data-ttu-id="4d48a-169">一个可写的电子邮件消息元素的列表，请参阅[在 Exchange 电子邮件属性和 EWS 中的元素](email-properties-and-elements-in-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-169">For a list of writable email message elements, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="4d48a-170">有关如何发送邮件草稿已更新后的详细信息，请参阅[发送使用 EWS 草稿电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-170">For details about how to send a draft message after it's been updated, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>
  
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
    <m:UpdateItem MessageDisposition="SaveOnly"
                  ConflictResolution="AutoResolve">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="m4OVAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCy" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OWAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCz" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OXAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKC0" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="4d48a-171">服务器响应**UpdateItem**请求使用[UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**，这表明，每个更新已成功保存在服务器上的值。</span><span class="sxs-lookup"><span data-stu-id="4d48a-171">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="4d48a-172">[ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx)元素中报告的所有冲突。</span><span class="sxs-lookup"><span data-stu-id="4d48a-172">Any conflicts are reported in the [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4d48a-173">使用 EWS 托管 API 删除批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-173">Delete email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4d48a-174"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-174"></span></span>

<span data-ttu-id="4d48a-175">下面的示例中所示，您可以通过使用 EWS 托管 API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx)方法中，删除批次中的邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-175">You can delete messages in batches by using the EWS Managed API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="4d48a-176">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4d48a-176">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void BatchDeleteEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Delete the batch of email message objects.
    // This method call results in an DeleteItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);
    
    // Check for success of the DeleteItems method call.
    // DeleteItems returns success even if it does not find all the item IDs.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("Email messages deleted successfully.\r\n");
    }
    // If the method did not return success, print a message.
    else
    {
        Console.WriteLine("Not all email messages deleted successfully.\r\n");
    }
}
```

## <a name="delete-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="4d48a-177">使用 EWS 删除批次中的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-177">Delete email messages in batches by using EWS</span></span>
<span data-ttu-id="4d48a-178"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-178"></span></span>

<span data-ttu-id="4d48a-179">下面的代码示例中所示，您可以使用[删除项](../web-service-reference/deleteitem-operation.md)EWS 操作中，删除批次中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4d48a-179">You can delete email messages in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="4d48a-180">这也是 EWS 托管 API 时您使用 EWS 托管 API 到[删除批次中的电子邮件](#bk_deleteewsma)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete email messages in batches](#bk_deleteewsma).</span></span>
  
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
    <m:DeleteItem DeleteType="SoftDelete"
                  AffectedTaskOccurrences="AllOccurrences">
      <m:ItemIds>
        <t:ItemId Id="m4OkAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDE" />
        <t:ItemId Id="m4OlAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDF" />
        <t:ItemId Id="m4OmAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDG" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="4d48a-181">服务器响应[DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)邮件包含已删除的每个项目**NoError** [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**删除项**要求。</span><span class="sxs-lookup"><span data-stu-id="4d48a-181">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="4d48a-182">请注意，此操作还返回成功是否找不到的项 ID。</span><span class="sxs-lookup"><span data-stu-id="4d48a-182">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="4d48a-183">验证批处理已成功完成</span><span class="sxs-lookup"><span data-stu-id="4d48a-183">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="4d48a-184"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="4d48a-184"></span></span>

<span data-ttu-id="4d48a-185">无法处理批处理请求中的一个或多个电子邮件，如请求时失败，每个电子邮件将返回错误和预期处理的批次中的电子邮件的其余部分。</span><span class="sxs-lookup"><span data-stu-id="4d48a-185">When one or more email messages in a batched request can't be processed as requested, an error is returned for each email message that failed, and the rest of the emails in the batch are processed as expected.</span></span> <span data-ttu-id="4d48a-186">在批处理中可能会出现故障如果项目已删除，因此无法发送、 检索，或更新，或者如果项目移动到另一个文件夹，并因此具有新的项目 ID，并且不能使用发送的项目 ID 修改。</span><span class="sxs-lookup"><span data-stu-id="4d48a-186">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="4d48a-187">本节中的信息显示如何获取有关失败的错误详细信息中的电子邮件的批处理。</span><span class="sxs-lookup"><span data-stu-id="4d48a-187">The information in this section shows how to get error details about failures in batch processing of email message.</span></span>
  
<span data-ttu-id="4d48a-188">使用 EWS 托管 API 验证成功的批处理过程，您可以检查[ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx)的[OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx)属性等于[ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4d48a-188">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="4d48a-189">如果是这样，所有电子邮件都已成功处理。</span><span class="sxs-lookup"><span data-stu-id="4d48a-189">If so, all the emails were processed successfully.</span></span> <span data-ttu-id="4d48a-190">如果**OverallResult**不等于**ServiceResult.Success**，一个或多个电子邮件未成功处理。</span><span class="sxs-lookup"><span data-stu-id="4d48a-190">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the emails were not processed successfully.</span></span> <span data-ttu-id="4d48a-191">每个**ServiceResponseCollection**中返回的对象包含以下属性：</span><span class="sxs-lookup"><span data-stu-id="4d48a-191">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="4d48a-192">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="4d48a-192">ErrorCode</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4d48a-193">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="4d48a-193">ErrorDetails</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4d48a-194">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="4d48a-194">ErrorMessage</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4d48a-195">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="4d48a-195">ErrorProperties</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4d48a-196">结果</span><span class="sxs-lookup"><span data-stu-id="4d48a-196">Result</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="4d48a-197">这些属性包含有关为什么电子邮件无法处理所要求的信息。</span><span class="sxs-lookup"><span data-stu-id="4d48a-197">These properties contain information about why the email messages could not be processed as requested.</span></span> <span data-ttu-id="4d48a-198">本文中的示例输出的**结果**，**错误代码**和**ErrorMessage**为每个失败的消息。</span><span class="sxs-lookup"><span data-stu-id="4d48a-198">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed message.</span></span> <span data-ttu-id="4d48a-199">您可以使用这些结果调查问题。</span><span class="sxs-lookup"><span data-stu-id="4d48a-199">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="4d48a-200">Ews，若要验证成功批处理过程，检查正在处理每个项目的[ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="4d48a-200">For EWS, to verify the success of a batched process, check the [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="4d48a-201">下面是**ResponseMessageType**，派生的所有响应消息的基类型的基本结构。</span><span class="sxs-lookup"><span data-stu-id="4d48a-201">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="4d48a-202">如果未成功处理电子邮件的**ResponseClass**属性设置为**成功**如果电子邮件已成功处理或**错误**。</span><span class="sxs-lookup"><span data-stu-id="4d48a-202">The **ResponseClass** attribute is set to **Success** if the email was processed successfully, or **Error** if the email was not processed successfully.</span></span> <span data-ttu-id="4d48a-203">电子邮件，不会批处理过程中遇到**警告**。</span><span class="sxs-lookup"><span data-stu-id="4d48a-203">For email messages, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="4d48a-204">如果**ResponseClass**为**成功**，后面的[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素也始终设置为**NoError**。</span><span class="sxs-lookup"><span data-stu-id="4d48a-204">If the **ResponseClass** is **Success**, the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="4d48a-205">如果**ResponseClass** **错误**，您需要检查[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)、 **ResponseCode**和[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx)元素以确定问题的原因的值。</span><span class="sxs-lookup"><span data-stu-id="4d48a-205">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="4d48a-206">当前未使用[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4d48a-206">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d48a-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d48a-207">See also</span></span>


- [<span data-ttu-id="4d48a-208">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="4d48a-208">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="4d48a-209">在 Exchange 使用 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-209">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4d48a-210">在 Exchange 使用 EWS 响应电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-210">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4d48a-211">移动和复制在 Exchange 使用 EWS 的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4d48a-211">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4d48a-212">限制的 EWS 批处理请求的影响</span><span class="sxs-lookup"><span data-stu-id="4d48a-212">Throttling implications for EWS batch requests</span></span>](ews-throttling-in-exchange.md#bk_ThrottlingBatch)
    

