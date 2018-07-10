---
title: 在 Exchange 使用 EWS 添加附件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0cbce436-2ae6-4fcc-bd8b-f517a0724e55
description: 了解如何创建新项目的附件，或通过使用 EWS 的 EWS 托管 API 在 Exchange 中添加现有项目的附件。
ms.openlocfilehash: dbfff879c92dafeec588d79cddd92e294b763c06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752773"
---
# <a name="add-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="b52e9-103">在 Exchange 使用 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-103">Add attachments by using EWS in Exchange</span></span>

<span data-ttu-id="b52e9-104">了解如何创建新项目的附件，或通过使用 EWS 的 EWS 托管 API 在 Exchange 中添加现有项目的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-104">Learn how to create new items with attachments, or add attachments to existing items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b52e9-105">您可以通过使用 EWS 托管 API 或 EWS 添加的文件附件或新的或现有项目的项目附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-105">You can add file attachments or item attachments to new or existing items by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="b52e9-106">如果您使用 EWS 托管 API，您可以使用相同的方法来将附件添加到新的或现有项目;但是，方法可更改如果您使用的文件或项目的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-106">If you are using the EWS Managed API, you use the same method to add attachments to new or existing items; however, the method changes if you're using a file or item attachment.</span></span> <span data-ttu-id="b52e9-107">相反，如果您使用 EWS，您使用相同的操作将文件或项目将附件添加到项目，但该操作将更改如果您要添加到新的或现有项目的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-107">Conversely, if you are using EWS, you use the same operation to add either a file or item attachment to an item, but the operation changes if you're adding the attachment to a new or existing item.</span></span>
  
<span data-ttu-id="b52e9-108">**表 1。EWS 托管 API 方法和添加附件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="b52e9-108">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="b52e9-109">**任务**</span><span class="sxs-lookup"><span data-stu-id="b52e9-109">**Task**</span></span>|<span data-ttu-id="b52e9-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="b52e9-110">**EWS Managed API method**</span></span>|<span data-ttu-id="b52e9-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="b52e9-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b52e9-112">添加新的或现有的电子邮件的文件附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-112">Add a file attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="b52e9-113">AttachmentCollection.AddFileAttachment</span><span class="sxs-lookup"><span data-stu-id="b52e9-113">AttachmentCollection.AddFileAttachment</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="b52e9-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)为新的电子邮件的</span><span class="sxs-lookup"><span data-stu-id="b52e9-114">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="b52e9-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)将添加到现有的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-115">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
|<span data-ttu-id="b52e9-116">添加到新的或现有的电子邮件项目附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-116">Add an item attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="b52e9-117">AttachmentCollection.AddItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b52e9-117">AttachmentCollection.AddItemAttachment</span></span>](http://msdn.microsoft.com/zh-cn/library/dd634986%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="b52e9-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)为新的电子邮件的</span><span class="sxs-lookup"><span data-stu-id="b52e9-118">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="b52e9-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)将添加到现有的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-119">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a><span data-ttu-id="b52e9-120">使用 EWS 托管 API 创建的文件和项目的附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-120">Create an email with file and item attachments by using the EWS Managed API</span></span>
<span data-ttu-id="b52e9-121"><a name="bk_createattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-121"></span></span>

<span data-ttu-id="b52e9-122">下面的代码示例演示如何创建包含多个文件附件和项目附件的电子邮件：</span><span class="sxs-lookup"><span data-stu-id="b52e9-122">The following code example shows how to create an email with multiple file attachments and an item attachment by:</span></span> 
  
1. <span data-ttu-id="b52e9-123">使用[EmailMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建一封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-123">Using the [EmailMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="b52e9-124">使用[AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx)和[AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/zh-cn/library/dd634986%28v=exchg.80%29.aspx)方法添加到邮件的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-124">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) and [AttachmentCollection.AddItemAttachment](http://msdn.microsoft.com/zh-cn/library/dd634986%28v=exchg.80%29.aspx) methods to add attachments to the message.</span></span> 
    
3. <span data-ttu-id="b52e9-125">使用[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法向收件人发送邮件并将邮件保存在已发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="b52e9-125">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipients and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="b52e9-126">此代码示例演示在其中的文件附件可以添加到项目使用 EWS 托管 API 的四个方法：</span><span class="sxs-lookup"><span data-stu-id="b52e9-126">This code example shows the four ways in which a file attachment can be added to an item by using the EWS Managed API:</span></span>
  
- <span data-ttu-id="b52e9-127">通过使用完全限定的文件位置。</span><span class="sxs-lookup"><span data-stu-id="b52e9-127">By using a fully qualified file location.</span></span>
    
- <span data-ttu-id="b52e9-128">使用完全限定的文件位置和新的附件名称。</span><span class="sxs-lookup"><span data-stu-id="b52e9-128">By using a fully qualified file location and a new attachment name.</span></span>
    
- <span data-ttu-id="b52e9-129">通过使用一个字节数组。</span><span class="sxs-lookup"><span data-stu-id="b52e9-129">By using a byte array.</span></span>
    
- <span data-ttu-id="b52e9-130">使用 stream。</span><span class="sxs-lookup"><span data-stu-id="b52e9-130">By using a stream.</span></span>
    
<span data-ttu-id="b52e9-131">请注意，在此示例中的项目附件创建电子邮件时。</span><span class="sxs-lookup"><span data-stu-id="b52e9-131">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="b52e9-132">若要添加为项目附件的现有电子邮件，请参阅[的现有项添加到使用 MimeContent 和 EWS 托管 API 的新电子邮件](#bk_addexistingemailewsma)。</span><span class="sxs-lookup"><span data-stu-id="b52e9-132">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
<span data-ttu-id="b52e9-133">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="b52e9-133">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a><span data-ttu-id="b52e9-134">使用 EWS 创建的文件和项目的附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-134">Create an email with file and item attachments by using EWS</span></span>
<span data-ttu-id="b52e9-135"><a name="bk_createattachews"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-135"></span></span>

<span data-ttu-id="b52e9-136">下面的代码示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation，以创建具有四个附件的文件和一个项目附件的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-136">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with four file attachments and one item attachment.</span></span> <span data-ttu-id="b52e9-137">这也是一个 XML 请求 EWS 托管 API 发送时您[创建的文件和项目的附件的电子邮件](#bk_createattachewsma)。</span><span class="sxs-lookup"><span data-stu-id="b52e9-137">This is also one of the XML requests that the EWS Managed API sends when you [create an email with file and item attachments](#bk_createattachewsma).</span></span>
  
<span data-ttu-id="b52e9-138">请注意，在此示例中的项目附件创建电子邮件时。</span><span class="sxs-lookup"><span data-stu-id="b52e9-138">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="b52e9-139">若要添加为项目附件的现有电子邮件，请参阅[的现有项添加到使用 MimeContent 和 EWS 托管 API 的新电子邮件](#bk_addexistingemailewsma)。</span><span class="sxs-lookup"><span data-stu-id="b52e9-139">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
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

<span data-ttu-id="b52e9-140">服务器响应包含**NoError**，这表明该电子邮件和附件已成功创建[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值的[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="b52e9-140">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email and the attachments were created successfully.</span></span> <span data-ttu-id="b52e9-141">[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)新创建的消息和附件的每个[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值，也包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="b52e9-141">The [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values for each of the attachments is also included in the response.</span></span> <span data-ttu-id="b52e9-142">为便于阅读变短了某些属性的值。</span><span class="sxs-lookup"><span data-stu-id="b52e9-142">The values of some attributes have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="b52e9-143">为[发送这个新创建的消息](how-to-send-email-messages-by-using-ews-in-exchange.md)，请在调用[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="b52e9-143">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a><span data-ttu-id="b52e9-144">将现有项添加到新的电子邮件，使用 MimeContent 和 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="b52e9-144">Add an existing item to a new email by using the MimeContent and the EWS Managed API</span></span>
<span data-ttu-id="b52e9-145"><a name="bk_addexistingemailewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-145"></span></span>

<span data-ttu-id="b52e9-146">若要作为项目附件转发到另一个项目中添加现有项，您需要创建一个新的项目附件，并将现有项目的内容复制到新项目。</span><span class="sxs-lookup"><span data-stu-id="b52e9-146">To add an existing item as an item attachment to another item, you need to create a new item attachment and copy the content of the existing item to the new item.</span></span> <span data-ttu-id="b52e9-147">有两种方法来执行此操作：</span><span class="sxs-lookup"><span data-stu-id="b52e9-147">There are two ways to do this:</span></span> 
  
1. <span data-ttu-id="b52e9-148">如果您正在专门使用电子邮件，可以将[MimeContent](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性的值从电子邮件复制到新创建的项附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-148">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property from the email into the newly created item attachment.</span></span> <span data-ttu-id="b52e9-149">在此过程，后续标志和类别，例如，您将会丢失一些属性，但它非常适用于标准电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-149">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="b52e9-150">如果您的所有项目类型需要全保真方式，可以将绑定到现有项目和复制到新附件的所有属性和扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-150">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="b52e9-151">下面的代码示例显示第一种方法，将**MimeContent**复制到新的项目附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-151">The following code example shows the first approach, copying the **MimeContent** into the new item attachment.</span></span> <span data-ttu-id="b52e9-152">此示例后面是说明如何修改代码以使用第二种方法的过程。</span><span class="sxs-lookup"><span data-stu-id="b52e9-152">Following this example is a procedure that shows how you can modify the code to use the second approach.</span></span> 
  
<span data-ttu-id="b52e9-153">此示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象的用户已经过身份验证到 Exchange 服务器，和[ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)项目的附加的**itemId** 。</span><span class="sxs-lookup"><span data-stu-id="b52e9-153">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server, and that the **itemId** is the [ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the item to attach.</span></span> 
  
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

<span data-ttu-id="b52e9-154">要修改此示例将每个对现有项目属性复制到新的项目附件，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="b52e9-154">To modify this example to copy each of the properties on the existing item into the new item attachment, do the following:</span></span> 
  
1. <span data-ttu-id="b52e9-155">更改属性设置为包括**PropertySet.FirstClassProperties**和任何其他属性或所需的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-155">Change the property set to include **PropertySet.FirstClassProperties** and any additional properties or extended properties you need.</span></span> 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. <span data-ttu-id="b52e9-156">删除下面一行，因为您无需**MimeContent**属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-156">Remove the following line, because you do not need the **MimeContent** property.</span></span> 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. <span data-ttu-id="b52e9-157">重复每个属性，将从现有的项目复制到新附件的以下的行。</span><span class="sxs-lookup"><span data-stu-id="b52e9-157">Repeat this line for each property to copy from the existing item to the new attachment.</span></span> <span data-ttu-id="b52e9-158">不要到新的项目附件复制**ItemId** ，因为这是只读属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-158">Do not copy the **ItemId** into the new item attachment because that's a read-only property.</span></span> 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. <span data-ttu-id="b52e9-159">设置为**已发送**附件[PidTagMessageFlags](http://msdn.microsoft.com/zh-cn/library/cc839733.aspx) (0x0E070003) 属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-159">Set the [PidTagMessageFlags](http://msdn.microsoft.com/zh-cn/library/cc839733.aspx) (0x0E070003) property on the attachment to **Sent**.</span></span>
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a><span data-ttu-id="b52e9-160">使用 MimeContent 和 EWS 现有项目添加到新的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-160">Add an existing item to a new email by using the MimeContent and EWS</span></span>
<span data-ttu-id="b52e9-161"><a name="bk_addexistingemailews"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-161"></span></span>

<span data-ttu-id="b52e9-162">有两种方法的新项目添加现有项：</span><span class="sxs-lookup"><span data-stu-id="b52e9-162">There are two ways to add an existing item to a new item:</span></span> 
  
1. <span data-ttu-id="b52e9-163">如果您正在专门使用电子邮件，可以将[MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx)元素的值从电子邮件复制到新创建的项附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-163">If you're working with email messages specifically, you can copy the value of the [MimeContent](http://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) element from the email into the newly created item attachment.</span></span> <span data-ttu-id="b52e9-164">在此过程，后续标志和类别，例如，您将会丢失一些属性，但它非常适用于标准电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-164">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="b52e9-165">如果您的所有项目类型需要全保真方式，可以将绑定到现有项目和复制到新附件的所有属性和扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b52e9-165">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="b52e9-166">下面的代码示例演示如何使用**MimeContent**元素将原始项目的内容复制到新的项目附件的**MimeContent**值。</span><span class="sxs-lookup"><span data-stu-id="b52e9-166">The following code example shows how to use the **MimeContent** element to copy the content of the original item into the **MimeContent** value of the new item attachment.</span></span> <span data-ttu-id="b52e9-167">该示例使用以下操作：</span><span class="sxs-lookup"><span data-stu-id="b52e9-167">The example uses the following operations:</span></span> 
  
1. <span data-ttu-id="b52e9-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) — 要获取的**MimeContent**和将成为新邮件项目附件的邮件的[主题](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b52e9-168">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) — To get the **MimeContent** and [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of the message that will become the item attachment on the new message.</span></span> 
    
2. <span data-ttu-id="b52e9-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) — 创建新的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-169">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) — To create the new email message.</span></span> 
    
3. <span data-ttu-id="b52e9-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)— 若要创建新附件，使用**MimeContent**和**主题**检索**GetItem**操作。</span><span class="sxs-lookup"><span data-stu-id="b52e9-170">[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)— To create the new attachment, using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> 
    
4. <span data-ttu-id="b52e9-171">[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) — 发送和保存邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-171">[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) — To send and save the message.</span></span> 
    
<span data-ttu-id="b52e9-172">此示例首先会检索**MimeContent**和现有项目的**主题**。</span><span class="sxs-lookup"><span data-stu-id="b52e9-172">The example starts by retrieving the **MimeContent** and the **Subject** of the existing item.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-173">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功检索电子邮件，以及**MimeContent**和**[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值主题**电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-173">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the **MimeContent** and **Subject** of the email.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="944"
                         MinorBuildNumber="11"
                         Version="V2_12"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="b52e9-174">接下来，调用**CreateItem** operation，创建新的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-174">Next, call the **CreateItem** operation to create the new email.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-175">服务器响应包含[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，这表明已成功创建电子邮件的[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="b52e9-175">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully.</span></span>
  
<span data-ttu-id="b52e9-176">接下来，创建新的项目附件使用**MimeContent**和**主题** **GetItem**操作检索的。</span><span class="sxs-lookup"><span data-stu-id="b52e9-176">Next, create the new item attachment by using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> <span data-ttu-id="b52e9-177">使用**CreateItem**响应中返回的**ItemId**值填充[ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="b52e9-177">The value of the [ParentItemId](http://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) element is populated by using the **ItemId** value returned in the **CreateItem** response.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-178">服务器响应**CreateAttachment**请求[CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功创建附件，并[[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)的新创建的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-178">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
<span data-ttu-id="b52e9-179">既然已经创建新邮件，并附加项目，您还可以[发送这个新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)通过调用[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="b52e9-179">Now that the new message has been created, and the item was attached, you can [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md) by calling the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-180">服务器使用 **SendItemResponse** 邮件响应 [SendItem](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**，表示电子邮件已成功发送。</span><span class="sxs-lookup"><span data-stu-id="b52e9-180">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was sent successfully.</span></span>
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a><span data-ttu-id="b52e9-181">使用 EWS 托管 API 创建与内嵌附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-181">Create an email with an inline attachment by using the EWS Managed API</span></span>
<span data-ttu-id="b52e9-182"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-182"></span></span>

<span data-ttu-id="b52e9-183">下面的代码示例演示如何创建与内嵌附件的电子邮件：</span><span class="sxs-lookup"><span data-stu-id="b52e9-183">The following code example shows how to create an email with an inline attachment by:</span></span>
  
1. <span data-ttu-id="b52e9-184">使用[EmailMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建一封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-184">Using the [EmailMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="b52e9-185">[EmailMessage.Body](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)属性设置为 HTML 正文包含内嵌附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-185">Setting the [EmailMessage.Body](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) property to an HTML body that includes an inline attachment.</span></span> 
    
3. <span data-ttu-id="b52e9-186">使用[AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx)方法添加到邮件的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-186">Using the [AttachmentCollection.AddFileAttachment](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) method to add the attachment to the message.</span></span> 
    
4. <span data-ttu-id="b52e9-187">使用[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法向收件人发送邮件并将邮件保存在已发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="b52e9-187">Using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="b52e9-188">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="b52e9-188">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a><span data-ttu-id="b52e9-189">使用 EWS 创建与内嵌附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-189">Create an email with an inline attachment by using EWS</span></span>
<span data-ttu-id="b52e9-190"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-190"></span></span>

<span data-ttu-id="b52e9-191">下面的代码示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作创建带有内嵌文件附件的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-191">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with an inline file attachment.</span></span> <span data-ttu-id="b52e9-192">[Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx)元素的**BodyType**属性指示内容采用 HTML 格式，并包括图像源。</span><span class="sxs-lookup"><span data-stu-id="b52e9-192">The **BodyType** attribute of the [Body](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) element indicates that the content is in HTML format and includes the image source.</span></span> <span data-ttu-id="b52e9-193">这也就是一个 EWS 托管 API 时您使用 EWS 托管 API[创建电子邮件与内嵌附件](#bk_createinlineattachewsma)发送的请求的 XML。</span><span class="sxs-lookup"><span data-stu-id="b52e9-193">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [create an email with an inline attachment](#bk_createinlineattachewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-194">服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b52e9-194">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="b52e9-195">为[发送这个新创建的消息](how-to-send-email-messages-by-using-ews-in-exchange.md)，请在调用[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="b52e9-195">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a><span data-ttu-id="b52e9-196">使用 EWS 托管 API 添加到现有的电子邮件附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-196">Add an attachment to an existing email by using the EWS Managed API</span></span>
<span data-ttu-id="b52e9-197"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-197"></span></span>

<span data-ttu-id="b52e9-198">下面的代码示例演示如何添加到现有的电子邮件的附件：</span><span class="sxs-lookup"><span data-stu-id="b52e9-198">The following code example shows how to add an attachment to an existing email by:</span></span> 
  
1. <span data-ttu-id="b52e9-199">使用[EmailMessage.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法将绑定到现有电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-199">Using the [EmailMessage.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message.</span></span> 
    
2. <span data-ttu-id="b52e9-200">使用**AddFileAttachment**方法添加到邮件的文件附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-200">Adding a file attachment to the message by using the **AddFileAttachment** method.</span></span> 
    
3. <span data-ttu-id="b52e9-201">通过调用[EmailMessage.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存更新。</span><span class="sxs-lookup"><span data-stu-id="b52e9-201">Saving the updates by calling the [EmailMessage.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="b52e9-202">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="b52e9-202">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a><span data-ttu-id="b52e9-203">使用 EWS 添加到现有的电子邮件附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-203">Add an attachment to an existing email by using EWS</span></span>
<span data-ttu-id="b52e9-204"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b52e9-204"></span></span>

<span data-ttu-id="b52e9-205">下面的代码示例演示如何使用[CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作添加到现有的电子邮件的文件附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-205">The following code example shows how to use the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation to add a file attachment to an existing email message.</span></span> <span data-ttu-id="b52e9-206">这也就是一个 EWS 托管 API 时您使用 EWS 托管 API[添加到现有的电子邮件附件](#bk_createinlineattachewsma)发送的请求的 XML。</span><span class="sxs-lookup"><span data-stu-id="b52e9-206">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [add an attachment to an existing email](#bk_createinlineattachewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="b52e9-207">服务器响应**CreateAttachment**请求[CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功创建附件，并[[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)的新创建的附件。</span><span class="sxs-lookup"><span data-stu-id="b52e9-207">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](http://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="b52e9-208">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b52e9-208">See also</span></span>


- [<span data-ttu-id="b52e9-209">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="b52e9-209">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="b52e9-210">在 Exchange 使用 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-210">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b52e9-211">使用 EWS 在 Exchange 中删除附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-211">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b52e9-212">使用 EWS 在 Exchange 服务器获取附件</span><span class="sxs-lookup"><span data-stu-id="b52e9-212">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b52e9-213">在 Exchange 使用 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="b52e9-213">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

