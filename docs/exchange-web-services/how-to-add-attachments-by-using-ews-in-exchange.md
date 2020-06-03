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
# <a name="add-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="4bf61-103">使用 Exchange 中的 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="4bf61-103">Add attachments by using EWS in Exchange</span></span>

<span data-ttu-id="4bf61-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，创建包含附件的新项目，或向现有项目添加附件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-104">Learn how to create new items with attachments, or add attachments to existing items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4bf61-105">您可以使用 EWS 托管 API 或 EWS 将文件附件或项目附件添加到新项目或现有项目中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-105">You can add file attachments or item attachments to new or existing items by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="4bf61-106">如果使用 EWS 托管 API，则可以使用相同的方法将附件添加到新项目或现有项目中;但是，如果您使用的是文件或项目附件，则此方法会更改。</span><span class="sxs-lookup"><span data-stu-id="4bf61-106">If you are using the EWS Managed API, you use the same method to add attachments to new or existing items; however, the method changes if you're using a file or item attachment.</span></span> <span data-ttu-id="4bf61-107">相反，如果使用 EWS，则可以使用相同的操作将文件或项目附件添加到项目中，但如果要将附件添加到新项目或现有项目中，则该操作会更改。</span><span class="sxs-lookup"><span data-stu-id="4bf61-107">Conversely, if you are using EWS, you use the same operation to add either a file or item attachment to an item, but the operation changes if you're adding the attachment to a new or existing item.</span></span>
  
<span data-ttu-id="4bf61-108">**表1。用于添加附件的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4bf61-108">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="4bf61-109">**任务**</span><span class="sxs-lookup"><span data-stu-id="4bf61-109">**Task**</span></span>|<span data-ttu-id="4bf61-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="4bf61-110">**EWS Managed API method**</span></span>|<span data-ttu-id="4bf61-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4bf61-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bf61-112">将文件附件添加到新的或现有的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-112">Add a file attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="4bf61-113">AttachmentCollection.AddFileAttachment</span><span class="sxs-lookup"><span data-stu-id="4bf61-113">AttachmentCollection.AddFileAttachment</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="4bf61-114">新电子邮件的[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-114">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="4bf61-115">要添加到现有电子邮件中的[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-115">[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
|<span data-ttu-id="4bf61-116">将项目附件添加到新的或现有的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-116">Add an item attachment to a new or existing email</span></span>  <br/> |[<span data-ttu-id="4bf61-117">AttachmentCollection.AddItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4bf61-117">AttachmentCollection.AddItemAttachment</span></span>](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="4bf61-118">新电子邮件的[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-118">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) for a new email</span></span>  <br/> <span data-ttu-id="4bf61-119">要添加到现有电子邮件中的[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-119">[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) to add to an existing email</span></span>  <br/> |
   
## <a name="create-an-email-with-file-and-item-attachments-by-using-the-ews-managed-api"></a><span data-ttu-id="4bf61-120">使用 EWS 托管 API 创建包含文件和项目附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-120">Create an email with file and item attachments by using the EWS Managed API</span></span>
<span data-ttu-id="4bf61-121"><a name="bk_createattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-121"><a name="bk_createattachewsma"> </a></span></span>

<span data-ttu-id="4bf61-122">下面的代码示例演示如何通过以下方式创建包含多个文件附件和项目附件的电子邮件：</span><span class="sxs-lookup"><span data-stu-id="4bf61-122">The following code example shows how to create an email with multiple file attachments and an item attachment by:</span></span> 
  
1. <span data-ttu-id="4bf61-123">使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-123">Using the [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="4bf61-124">使用 AddFileAttachment 和[AttachmentCollection](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx)方法将附件添加到邮件中。 [AttachmentCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-124">Using the [AttachmentCollection.AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) and [AttachmentCollection.AddItemAttachment](https://msdn.microsoft.com/library/dd634986%28v=exchg.80%29.aspx) methods to add attachments to the message.</span></span> 
    
3. <span data-ttu-id="4bf61-125">使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法将邮件发送给收件人，并将邮件保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-125">Using the [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipients and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="4bf61-126">此代码示例演示使用 EWS 托管 API 将文件附件添加到项目的四种方式：</span><span class="sxs-lookup"><span data-stu-id="4bf61-126">This code example shows the four ways in which a file attachment can be added to an item by using the EWS Managed API:</span></span>
  
- <span data-ttu-id="4bf61-127">通过使用完全限定的文件位置。</span><span class="sxs-lookup"><span data-stu-id="4bf61-127">By using a fully qualified file location.</span></span>
    
- <span data-ttu-id="4bf61-128">通过使用完全限定的文件位置和新的附件名称。</span><span class="sxs-lookup"><span data-stu-id="4bf61-128">By using a fully qualified file location and a new attachment name.</span></span>
    
- <span data-ttu-id="4bf61-129">通过使用字节数组。</span><span class="sxs-lookup"><span data-stu-id="4bf61-129">By using a byte array.</span></span>
    
- <span data-ttu-id="4bf61-130">使用流。</span><span class="sxs-lookup"><span data-stu-id="4bf61-130">By using a stream.</span></span>
    
<span data-ttu-id="4bf61-131">请注意，此示例中的项目附件是在电子邮件的同一时间创建的。</span><span class="sxs-lookup"><span data-stu-id="4bf61-131">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="4bf61-132">若要将现有电子邮件添加为项目附件，请参阅[使用 MimeContent 和 EWS 托管 API 将现有项目添加到新电子邮件](#bk_addexistingemailewsma)。</span><span class="sxs-lookup"><span data-stu-id="4bf61-132">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
<span data-ttu-id="4bf61-133">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="4bf61-133">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="create-an-email-with-file-and-item-attachments-by-using-ews"></a><span data-ttu-id="4bf61-134">使用 EWS 创建包含文件和项目附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-134">Create an email with file and item attachments by using EWS</span></span>
<span data-ttu-id="4bf61-135"><a name="bk_createattachews"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-135"><a name="bk_createattachews"> </a></span></span>

<span data-ttu-id="4bf61-136">下面的代码示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作创建包含四个文件附件和一个项目附件的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-136">The following code example shows how to use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with four file attachments and one item attachment.</span></span> <span data-ttu-id="4bf61-137">这也是在您[创建包含文件和项目附件的电子邮件](#bk_createattachewsma)时，EWS 托管 API 发送的 XML 请求之一。</span><span class="sxs-lookup"><span data-stu-id="4bf61-137">This is also one of the XML requests that the EWS Managed API sends when you [create an email with file and item attachments](#bk_createattachewsma).</span></span>
  
<span data-ttu-id="4bf61-138">请注意，此示例中的项目附件是在电子邮件的同一时间创建的。</span><span class="sxs-lookup"><span data-stu-id="4bf61-138">Note that the item attachment in this example is created at the same time as the email message.</span></span> <span data-ttu-id="4bf61-139">若要将现有电子邮件添加为项目附件，请参阅[使用 MimeContent 和 EWS 托管 API 将现有项目添加到新电子邮件](#bk_addexistingemailewsma)。</span><span class="sxs-lookup"><span data-stu-id="4bf61-139">To add an existing email message as an item attachment, see [Add an existing item to a new email by using the MimeContent and the EWS Managed API](#bk_addexistingemailewsma).</span></span>
  
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

<span data-ttu-id="4bf61-140">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值为**NoError**，表示已成功创建电子邮件和附件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-140">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email and the attachments were created successfully.</span></span> <span data-ttu-id="4bf61-141">新创建的邮件的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)和每个附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值也包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-141">The [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message and the [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values for each of the attachments is also included in the response.</span></span> <span data-ttu-id="4bf61-142">为了提高可读性，某些属性的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="4bf61-142">The values of some attributes have been shortened for readability.</span></span> 
  
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

<span data-ttu-id="4bf61-143">若要[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)，请调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="4bf61-143">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-the-ews-managed-api"></a><span data-ttu-id="4bf61-144">使用 MimeContent 和 EWS 托管 API 将现有项添加到新电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-144">Add an existing item to a new email by using the MimeContent and the EWS Managed API</span></span>
<span data-ttu-id="4bf61-145"><a name="bk_addexistingemailewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-145"><a name="bk_addexistingemailewsma"> </a></span></span>

<span data-ttu-id="4bf61-146">若要将现有项目作为项目附件添加到另一个项目，您需要创建新的项目附件并将现有项目的内容复制到新项目中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-146">To add an existing item as an item attachment to another item, you need to create a new item attachment and copy the content of the existing item to the new item.</span></span> <span data-ttu-id="4bf61-147">可通过 2 种方法执行此操作：</span><span class="sxs-lookup"><span data-stu-id="4bf61-147">There are two ways to do this:</span></span> 
  
1. <span data-ttu-id="4bf61-148">如果您使用的是电子邮件，则可以将[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)属性的值从电子邮件复制到新创建的项目附件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-148">If you're working with email messages specifically, you can copy the value of the [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) property from the email into the newly created item attachment.</span></span> <span data-ttu-id="4bf61-149">在此过程中，您将丢失一些属性，如后续标志和类别，但它对标准电子邮件非常有用。</span><span class="sxs-lookup"><span data-stu-id="4bf61-149">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="4bf61-150">如果您需要所有项目类型的完全保真，则可以绑定到现有项目并将所有属性和扩展属性复制到新的附件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-150">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="4bf61-151">下面的代码示例演示了第一种方法，即将**MimeContent**复制到新项附件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-151">The following code example shows the first approach, copying the **MimeContent** into the new item attachment.</span></span> <span data-ttu-id="4bf61-152">下面的示例展示了如何修改代码以使用第二种方法的过程。</span><span class="sxs-lookup"><span data-stu-id="4bf61-152">Following this example is a procedure that shows how you can modify the code to use the second approach.</span></span> 
  
<span data-ttu-id="4bf61-153">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过 Exchange 服务器的身份验证，并且**itemid**是要附加的项的[itemid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4bf61-153">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server, and that the **itemId** is the [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the item to attach.</span></span> 
  
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

<span data-ttu-id="4bf61-154">若要修改此示例以将现有项的每个属性复制到新项附件中，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="4bf61-154">To modify this example to copy each of the properties on the existing item into the new item attachment, do the following:</span></span> 
  
1. <span data-ttu-id="4bf61-155">将属性集更改为包含**PropertySet**以及所需的任何其他属性或扩展属性。</span><span class="sxs-lookup"><span data-stu-id="4bf61-155">Change the property set to include **PropertySet.FirstClassProperties** and any additional properties or extended properties you need.</span></span> 
    
  ```cs
  // Add additional properties to the PropertySet.
  EmailMessage msgToAttach = EmailMessage.Bind(service, itemId, new PropertySet(PropertySet.FirstClassProperties));
  ```

2. <span data-ttu-id="4bf61-156">删除以下行，因为您不需要**MimeContent**属性。</span><span class="sxs-lookup"><span data-stu-id="4bf61-156">Remove the following line, because you do not need the **MimeContent** property.</span></span> 
    
  ```cs
  itemAttachment.Item.MimeContent = msgToAttach.MimeContent;
  ```

3. <span data-ttu-id="4bf61-157">对每个要从现有项目复制到新附件的属性重复此代码行。</span><span class="sxs-lookup"><span data-stu-id="4bf61-157">Repeat this line for each property to copy from the existing item to the new attachment.</span></span> <span data-ttu-id="4bf61-158">请勿将**ItemId**复制到新项目附件中，因为这是只读属性。</span><span class="sxs-lookup"><span data-stu-id="4bf61-158">Do not copy the **ItemId** into the new item attachment because that's a read-only property.</span></span> 
    
  ```cs
  itemAttachment.Item.Subject = msgToAttach.Subject;
  ```

4. <span data-ttu-id="4bf61-159">将附件上的[PidTagMessageFlags](https://msdn.microsoft.com/library/cc839733.aspx) （0x0E070003）属性设置为 "**已发送**"。</span><span class="sxs-lookup"><span data-stu-id="4bf61-159">Set the [PidTagMessageFlags](https://msdn.microsoft.com/library/cc839733.aspx) (0x0E070003) property on the attachment to **Sent**.</span></span>
    
  ```cs
  ExtendedPropertyDefinition sent = new ExtendedPropertyDefinition(3591, MapiPropertyType.Integer);
  msgToAttach.Item.SetExtendedProperty(sent, "1");
  ```

## <a name="add-an-existing-item-to-a-new-email-by-using-the-mimecontent-and-ews"></a><span data-ttu-id="4bf61-160">使用 MimeContent 和 EWS 将现有项添加到新电子邮件中</span><span class="sxs-lookup"><span data-stu-id="4bf61-160">Add an existing item to a new email by using the MimeContent and EWS</span></span>
<span data-ttu-id="4bf61-161"><a name="bk_addexistingemailews"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-161"><a name="bk_addexistingemailews"> </a></span></span>

<span data-ttu-id="4bf61-162">有两种方法可将现有项添加到新项：</span><span class="sxs-lookup"><span data-stu-id="4bf61-162">There are two ways to add an existing item to a new item:</span></span> 
  
1. <span data-ttu-id="4bf61-163">如果您使用的是电子邮件，则可以将[MimeContent](https://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx)元素的值从电子邮件复制到新创建的项目附件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-163">If you're working with email messages specifically, you can copy the value of the [MimeContent](https://msdn.microsoft.com/library/4f472a08-5653-4c54-ba65-831dfe32f20f%28Office.15%29.aspx) element from the email into the newly created item attachment.</span></span> <span data-ttu-id="4bf61-164">在此过程中，您将丢失一些属性，如后续标志和类别，但它对标准电子邮件非常有用。</span><span class="sxs-lookup"><span data-stu-id="4bf61-164">You will lose some properties during this process, such as follow up flags and categories, but it works great for standard email messages.</span></span> 
    
2. <span data-ttu-id="4bf61-165">如果您需要所有项目类型的完全保真，则可以绑定到现有项目并将所有属性和扩展属性复制到新的附件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-165">If you need full fidelity for all item types, you can bind to an existing item and copy all the properties and extended properties into the new attachment.</span></span>
    
<span data-ttu-id="4bf61-166">下面的代码示例演示如何使用**MimeContent**元素将原始项的内容复制到新项附件的**MimeContent**值中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-166">The following code example shows how to use the **MimeContent** element to copy the content of the original item into the **MimeContent** value of the new item attachment.</span></span> <span data-ttu-id="4bf61-167">此示例使用以下操作：</span><span class="sxs-lookup"><span data-stu-id="4bf61-167">The example uses the following operations:</span></span> 
  
1. <span data-ttu-id="4bf61-168">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) —获取将成为新邮件的项目附件的邮件的**MimeContent**和[主题](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4bf61-168">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) — To get the **MimeContent** and [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of the message that will become the item attachment on the new message.</span></span> 
    
2. <span data-ttu-id="4bf61-169">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) —创建新的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-169">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) — To create the new email message.</span></span> 
    
3. <span data-ttu-id="4bf61-170">[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)—使用由**GetItem**操作检索到的**MimeContent**和**主题**来创建新附件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-170">[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)— To create the new attachment, using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> 
    
4. <span data-ttu-id="4bf61-171">[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) —发送和保存邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-171">[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) — To send and save the message.</span></span> 
    
<span data-ttu-id="4bf61-172">该示例首先检索现有项的**MimeContent**和**主题**。</span><span class="sxs-lookup"><span data-stu-id="4bf61-172">The example starts by retrieving the **MimeContent** and the **Subject** of the existing item.</span></span> 
  
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

<span data-ttu-id="4bf61-173">服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示电子邮件已成功检索，以及电子邮件的**MimeContent**和**主题**。</span><span class="sxs-lookup"><span data-stu-id="4bf61-173">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the **MimeContent** and **Subject** of the email.</span></span> 
  
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

<span data-ttu-id="4bf61-174">接下来，调用**CreateItem**操作以创建新的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-174">Next, call the **CreateItem** operation to create the new email.</span></span> 
  
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

<span data-ttu-id="4bf61-175">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示已成功创建电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-175">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully.</span></span>
  
<span data-ttu-id="4bf61-176">接下来，使用**MimeContent**和**GetItem**操作检索到的**主题**创建新的项目附件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-176">Next, create the new item attachment by using the **MimeContent** and **Subject** retrieved by the **GetItem** operation.</span></span> <span data-ttu-id="4bf61-177">使用**CreateItem**响应中返回的**ItemId**值填充[ParentItemId](https://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="4bf61-177">The value of the [ParentItemId](https://msdn.microsoft.com/library/72dc4391-72db-44d2-85d9-4718d59886a7%28Office.15%29.aspx) element is populated by using the **ItemId** value returned in the **CreateItem** response.</span></span> 
  
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

<span data-ttu-id="4bf61-178">服务器使用[CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件响应**CreateAttachment**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，这表示附件已成功创建，以及新创建的附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4bf61-178">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
<span data-ttu-id="4bf61-179">现在已创建新邮件，并且已附加项目，您可以通过调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf61-179">Now that the new message has been created, and the item was attached, you can [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md) by calling the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
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

<span data-ttu-id="4bf61-180">服务器使用 **SendItemResponse** 邮件响应 [SendItem](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 值 **NoError**，表示电子邮件已成功发送。</span><span class="sxs-lookup"><span data-stu-id="4bf61-180">The server responds to the **SendItem** request with a [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was sent successfully.</span></span>
  
## <a name="create-an-email-with-an-inline-attachment-by-using-the-ews-managed-api"></a><span data-ttu-id="4bf61-181">使用 EWS 托管 API 创建带有内嵌附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-181">Create an email with an inline attachment by using the EWS Managed API</span></span>
<span data-ttu-id="4bf61-182"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-182"><a name="bk_createinlineattachewsma"> </a></span></span>

<span data-ttu-id="4bf61-183">下面的代码示例演示如何通过以下方式创建包含内联附件的电子邮件：</span><span class="sxs-lookup"><span data-stu-id="4bf61-183">The following code example shows how to create an email with an inline attachment by:</span></span>
  
1. <span data-ttu-id="4bf61-184">使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象创建电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-184">Using the [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message.</span></span> 
    
2. <span data-ttu-id="4bf61-185">将[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)属性设置为包含内联附件的 HTML 正文。</span><span class="sxs-lookup"><span data-stu-id="4bf61-185">Setting the [EmailMessage.Body](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) property to an HTML body that includes an inline attachment.</span></span> 
    
3. <span data-ttu-id="4bf61-186">使用 AddFileAttachment 方法可将附件添加到邮件中。 [AttachmentCollection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4bf61-186">Using the [AttachmentCollection.AddFileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.addfileattachment%28v=exchg.80%29.aspx) method to add the attachment to the message.</span></span> 
    
4. <span data-ttu-id="4bf61-187">使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)方法将邮件发送给收件人，并将邮件保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-187">Using the [EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
    
<span data-ttu-id="4bf61-188">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="4bf61-188">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="create-an-email-with-an-inline-attachment-by-using-ews"></a><span data-ttu-id="4bf61-189">使用 EWS 创建带有内嵌附件的电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-189">Create an email with an inline attachment by using EWS</span></span>
<span data-ttu-id="4bf61-190"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-190"><a name="bk_createinlineattachewsma"> </a></span></span>

<span data-ttu-id="4bf61-191">下面的代码示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)操作创建包含内联文件附件的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-191">The following code example shows how to use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation to create an email message with an inline file attachment.</span></span> <span data-ttu-id="4bf61-192">[Body](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx)元素的**office.mailboxenums.bodytype**属性指示内容为 HTML 格式，并包含图像源。</span><span class="sxs-lookup"><span data-stu-id="4bf61-192">The **BodyType** attribute of the [Body](https://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx) element indicates that the content is in HTML format and includes the image source.</span></span> <span data-ttu-id="4bf61-193">这也是当您使用 EWS 托管 API[创建带有内嵌附件的电子邮件](#bk_createinlineattachewsma)时，EWS 托管 api 发送的 XML 请求之一。</span><span class="sxs-lookup"><span data-stu-id="4bf61-193">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [create an email with an inline attachment](#bk_createinlineattachewsma).</span></span>
  
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

<span data-ttu-id="4bf61-194">服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4bf61-194">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="4bf61-195">若要[发送此新创建的邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)，请调用[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="4bf61-195">To [send this newly created message](how-to-send-email-messages-by-using-ews-in-exchange.md), call the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="add-an-attachment-to-an-existing-email-by-using-the-ews-managed-api"></a><span data-ttu-id="4bf61-196">使用 EWS 托管 API 将附件添加到现有电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-196">Add an attachment to an existing email by using the EWS Managed API</span></span>
<span data-ttu-id="4bf61-197"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-197"><a name="bk_createinlineattachewsma"> </a></span></span>

<span data-ttu-id="4bf61-198">下面的代码示例演示如何通过以下方式向现有电子邮件添加附件：</span><span class="sxs-lookup"><span data-stu-id="4bf61-198">The following code example shows how to add an attachment to an existing email by:</span></span> 
  
1. <span data-ttu-id="4bf61-199">使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法可绑定到现有电子邮件。</span><span class="sxs-lookup"><span data-stu-id="4bf61-199">Using the [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message.</span></span> 
    
2. <span data-ttu-id="4bf61-200">使用**AddFileAttachment**方法将文件附件添加到邮件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-200">Adding a file attachment to the message by using the **AddFileAttachment** method.</span></span> 
    
3. <span data-ttu-id="4bf61-201">通过调用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存更新。</span><span class="sxs-lookup"><span data-stu-id="4bf61-201">Saving the updates by calling the [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="4bf61-202">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="4bf61-202">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="add-an-attachment-to-an-existing-email-by-using-ews"></a><span data-ttu-id="4bf61-203">使用 EWS 将附件添加到现有电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-203">Add an attachment to an existing email by using EWS</span></span>
<span data-ttu-id="4bf61-204"><a name="bk_createinlineattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="4bf61-204"><a name="bk_createinlineattachewsma"> </a></span></span>

<span data-ttu-id="4bf61-205">下面的代码示例演示如何使用[CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx)操作将文件附件添加到现有电子邮件中。</span><span class="sxs-lookup"><span data-stu-id="4bf61-205">The following code example shows how to use the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation to add a file attachment to an existing email message.</span></span> <span data-ttu-id="4bf61-206">这也是当您使用 EWS 托管 API[将附件添加到现有电子邮件](#bk_createinlineattachewsma)中时，EWS 托管 api 发送的 XML 请求之一。</span><span class="sxs-lookup"><span data-stu-id="4bf61-206">This is also one of the XML requests that the EWS Managed API sends when you use the EWS Managed API to [add an attachment to an existing email](#bk_createinlineattachewsma).</span></span>
  
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

<span data-ttu-id="4bf61-207">服务器使用[CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx)邮件响应**CreateAttachment**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，这表示附件已成功创建，以及新创建的附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4bf61-207">The server responds to the **CreateAttachment** request with a [CreateAttachmentResponse](https://msdn.microsoft.com/library/cf6bd8bb-5317-4a03-bd75-297dd359b5da%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was created successfully, and the [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) of the newly created attachment.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="4bf61-208">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4bf61-208">See also</span></span>


- [<span data-ttu-id="4bf61-209">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="4bf61-209">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="4bf61-210">使用 Exchange 中的 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="4bf61-210">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4bf61-211">使用 Exchange 中的 EWS 删除附件</span><span class="sxs-lookup"><span data-stu-id="4bf61-211">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4bf61-212">使用 Exchange 中的 EWS 获取附件</span><span class="sxs-lookup"><span data-stu-id="4bf61-212">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4bf61-213">使用 Exchange 中的 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="4bf61-213">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

