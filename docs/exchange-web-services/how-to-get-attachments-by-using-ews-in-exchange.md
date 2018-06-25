---
title: 使用 EWS 在 Exchange 服务器获取附件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 12ce3cc0-a201-42e4-93e1-1f57961ff711
description: 了解如何从 EWS 项目使用 EWS 托管 API 或 EWS 在 Exchange 服务器获取附件。
ms.openlocfilehash: 2e1b3cfb346abd068695f66b01f9e34f1f5ff03f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752781"
---
# <a name="get-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="46113-103">使用 EWS 在 Exchange 服务器获取附件</span><span class="sxs-lookup"><span data-stu-id="46113-103">Get attachments by using EWS in Exchange</span></span>

<span data-ttu-id="46113-104">了解如何从 EWS 项目使用 EWS 托管 API 或 EWS 在 Exchange 服务器获取附件。</span><span class="sxs-lookup"><span data-stu-id="46113-104">Learn how to get attachments from EWS items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="46113-105">您可以通过使用 EWS 托管 API 或 EWS 获取从项目的附件。</span><span class="sxs-lookup"><span data-stu-id="46113-105">You can get attachments from an item by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="46113-106">获取项的初始调用仅包含有关项目的附件集合的元数据，因为始终多检索附件是一个两步过程。</span><span class="sxs-lookup"><span data-stu-id="46113-106">Because the initial call to get an item only includes metadata about the attachment collection on the item, retrieving attachments is always a two-step process.</span></span> <span data-ttu-id="46113-107">首先，检索项目。</span><span class="sxs-lookup"><span data-stu-id="46113-107">First, retrieve the item.</span></span> <span data-ttu-id="46113-108">接下来，检索附件。</span><span class="sxs-lookup"><span data-stu-id="46113-108">Next, retrieve the attachment.</span></span>
  
<span data-ttu-id="46113-109">**表 1。EWS 托管 API 方法和添加附件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="46113-109">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="46113-110">**任务**</span><span class="sxs-lookup"><span data-stu-id="46113-110">**Task**</span></span>|<span data-ttu-id="46113-111">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="46113-111">**EWS Managed API method**</span></span>|<span data-ttu-id="46113-112">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="46113-112">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46113-113">获取项目附件</span><span class="sxs-lookup"><span data-stu-id="46113-113">Get item attachments</span></span>  <br/> |<span data-ttu-id="46113-114">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)跟[ItemAttachment.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemattachment.load%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46113-114">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) followed by [ItemAttachment.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemattachment.load%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="46113-115">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)跟[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46113-115">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) followed by [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="46113-116">获取文件附件</span><span class="sxs-lookup"><span data-stu-id="46113-116">Get file attachments</span></span>  <br/> |<span data-ttu-id="46113-117">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)跟[FileAttachment.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.fileattachment.load%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46113-117">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) followed by [FileAttachment.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.fileattachment.load%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="46113-118">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)跟[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46113-118">[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) followed by [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span></span> <br/> |
   
## <a name="get-attachments-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="46113-119">从电子邮件使用 EWS 托管 API 服务器获取附件</span><span class="sxs-lookup"><span data-stu-id="46113-119">Get attachments from an email by using the EWS Managed API</span></span>
<span data-ttu-id="46113-120"><a name="bk_getattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="46113-120"></span></span>

<span data-ttu-id="46113-121">下面的代码示例演示如何使用**绑定**方法，获取[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象然后循环访问附件集合并对每个调用**FileAttachment.Load**或**ItemAttachment.Load**方法根据附件。</span><span class="sxs-lookup"><span data-stu-id="46113-121">The following code example shows how to get an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object by using the **Bind** method, then iterate through the attachment collection and call the **FileAttachment.Load** or **ItemAttachment.Load** method on each attachment as appropriate.</span></span> <span data-ttu-id="46113-122">每个文件附件保存到 C:\temp\ 文件夹中，并加载到内存中每个项目附件。</span><span class="sxs-lookup"><span data-stu-id="46113-122">Each file attachment is saved to the C:\temp\ folder, and each item attachment is loaded into memory.</span></span> <span data-ttu-id="46113-123">有关如何保存项目附件的信息，请参阅[保存使用 EWS 托管 API 附加电子邮件](#bk_saveitemattach)。</span><span class="sxs-lookup"><span data-stu-id="46113-123">For information about how to save an item attachment, see [Save an attached email by using the EWS Managed API](#bk_saveitemattach).</span></span>
  
<span data-ttu-id="46113-124">此示例假定该**服务**是有效[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，该**itemId**为[ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)从中将检索附件，并且用户已经过身份验证到 Exchange 服务器的邮件。</span><span class="sxs-lookup"><span data-stu-id="46113-124">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, that **itemId** is the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which attachments will be retrieved, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void GetAttachmentsFromEmail(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message item and retrieve the attachments collection.
    // This method results in an GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and load each attachment.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment is FileAttachment)
        {
            FileAttachment fileAttachment = attachment as FileAttachment;
            // Load the attachment into a file.
            // This call results in a GetAttachment call to EWS.
            fileAttachment.Load("C:\\temp\\" + fileAttachment.Name);
           
            Console.WriteLine("File attachment name: " + fileAttachment.Name);
        }
        else // Attachment is an item attachment.
        {
            ItemAttachment itemAttachment = attachment as ItemAttachment;
            // Load attachment into memory and write out the subject.
            // This does not save the file like it does with a file attachment.
            // This call results in a GetAttachment call to EWS.
            itemAttachment.Load();
            Console.WriteLine("Item attachment name: " + itemAttachment.Name);
        }
    }
}
```

## <a name="get-an-attachment-from-an-email-by-using-ews"></a><span data-ttu-id="46113-125">从电子邮件的使用 EWS 获取附件</span><span class="sxs-lookup"><span data-stu-id="46113-125">Get an attachment from an email by using EWS</span></span>
<span data-ttu-id="46113-126"><a name="bk_getattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="46113-126"></span></span>

<span data-ttu-id="46113-127">若要使用 EWS 获取附件，首先需要检索邮件和附件集合获取附件[AttachmentId （GetAttachment 和 DeleteAttachment）](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx)检索。</span><span class="sxs-lookup"><span data-stu-id="46113-127">To get attachments by using EWS, you first need to retrieve the message and the attachment collection to get the [AttachmentId (GetAttachment and DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) of the attachment to retrieve.</span></span> <span data-ttu-id="46113-128">要检索的一个或多个**AttachmentId**值后，调用[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作加载附件的所有属性。</span><span class="sxs-lookup"><span data-stu-id="46113-128">After you have one or more **AttachmentId** values to retrieve, call the [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) operation to load all the properties for the attachment.</span></span> 
  
<span data-ttu-id="46113-129">下面的代码示例演示如何使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作获取邮件上的电子邮件和附件的集合。</span><span class="sxs-lookup"><span data-stu-id="46113-129">The following code example shows how to use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to get an email message and the collection of attachments on the message.</span></span> <span data-ttu-id="46113-130">这也是使用 EWS 托管 API[获取电子邮件中的所有附件](#bk_getattachewsma)时，将发送 EWS 托管 API 的第一个 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="46113-130">This is also the first XML request that the EWS Managed API sends when you use the EWS Managed API to [get all attachments from an email](#bk_getattachewsma).</span></span> <span data-ttu-id="46113-131">为便于阅读缩短某些属性的值。</span><span class="sxs-lookup"><span data-stu-id="46113-131">The values of some attributes are shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
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
        <t:ItemId Id="ERu/AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="46113-132">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功检索电子邮件， [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值和[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值现有的附件。</span><span class="sxs-lookup"><span data-stu-id="46113-132">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values of the existing attachments.</span></span> 
  
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
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="ERu/AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAYEMnd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="5zTzlqU=" />
                  <t:Name>FileAttachment.txt</t:Name>
                  <t:Size>212</t:Size>
                  <t:LastModifiedTime>2014-05-14T17:59:30</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
                  <t:IsContactPhoto>false</t:IsContactPhoto>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="Ktum21o=" />
                  <t:Name>Attached Message Item</t:Name>
                  <t:Size>3063</t:Size>
                  <t:LastModifiedTime>2014-05-14T17:59:30</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
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

<span data-ttu-id="46113-133">既然您已经[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值，调用[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)上要检索每个附件。</span><span class="sxs-lookup"><span data-stu-id="46113-133">Now that you have the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values, call [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) on each attachment you want to retrieve.</span></span> 
  
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
    <m:GetAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="5zTzlqU=" />
      </m:AttachmentIds>
    </m:GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="46113-134">检索项目附件时, 服务器响应[GetAttachmentResponse](http://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx)消息，其中包括**NoError**，这表明已检索附件[ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值的**GetAttachment**请求成功，并附加项目，在这种情况下是一封电子邮件的所有元素。</span><span class="sxs-lookup"><span data-stu-id="46113-134">When retrieving an item attachment, the server responds to the **GetAttachment** request with a [GetAttachmentResponse](http://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was retrieved successfully, and all the elements for the attached item, which in this case is an email message.</span></span>
  
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
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="Ktum21o=" />
              <t:Name>Attached Message Item</t:Name>
              <t:Message>
                <t:ItemClass>IPM.Note</t:ItemClass>
                <t:Subject>Message Item Subject</t:Subject>
                <t:Body BodyType="HTML">&amp;lt;meta http-equiv="Content-Type" 
                    content="text/html; charset=utf-8"&amp;gt;Message Item Body</t:Body>
                <t:Size>2859</t:Size>
                <t:IsSubmitted>false</t:IsSubmitted>
                <t:IsDraft>true</t:IsDraft>
                <t:IsFromMe>false</t:IsFromMe>
                <t:IsResend>false</t:IsResend>
                <t:IsUnmodified>false</t:IsUnmodified>
                <t:DateTimeCreated>2014-05-14T17:59:37Z</t:DateTimeCreated>
                <t:ResponseObjects>
                  <t:ForwardItem />
                </t:ResponseObjects>
                <t:DisplayCc />
                <t:DisplayTo>primary; emaildelegate</t:DisplayTo>
                <t:HasAttachments>false</t:HasAttachments>
                <t:Culture>en</t:Culture>
                <t:EffectiveRights>
                  <t:CreateAssociated>false</t:CreateAssociated>
                  <t:CreateContents>false</t:CreateContents>
                  <t:CreateHierarchy>false</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                </t:EffectiveRights>
                <t:LastModifiedName>primary</t:LastModifiedName>
                <t:LastModifiedTime>2014-05-14T17:59:30Z</t:LastModifiedTime>
                <t:IsAssociated>false</t:IsAssociated>
                <t:WebClientReadFormQueryString>?ItemID=AAMk3D&amp;amp;exvsurl=1&amp;amp;viewmodel=
                    ReadMessageItem</t:WebClientReadFormQueryString>
                <t:ConversationId Id="AAQkADIwM2ZlM2ZlLWMwYjctNDg2N/Rc+d0=" />
                <t:ToRecipients>
                  <t:Mailbox>
                    <t:Name>primary</t:Name>
                    <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                    <t:MailboxType>Mailbox</t:MailboxType>
                  </t:Mailbox>
                  <t:Mailbox>
                    <t:Name>emaildelegate</t:Name>
                    <t:EmailAddress>ronnie@contoso.com</t:EmailAddress>
                    <t:RoutingType>SMTP</t:RoutingType>
                    <t:MailboxType>Mailbox</t:MailboxType>
                  </t:Mailbox>
                </t:ToRecipients>
                <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                <t:ConversationIndex>AQHPb55BxR5Fm0Arx0yY4xbL9Fz53Q==</t:ConversationIndex>
                <t:ConversationTopic>Message Item Subject</t:ConversationTopic>
                <t:IsRead>true</t:IsRead>
              </t:Message>
            </t:ItemAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="46113-135">检索文件附件时, 服务器响应[GetAttachmentResponse](http://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx)消息，其中包括**NoError**，这表明已检索附件[ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值的**GetAttachment**请求成功的附件文件的所有元素。</span><span class="sxs-lookup"><span data-stu-id="46113-135">When retrieving a file attachment, the server responds to the **GetAttachment** request with a [GetAttachmentResponse](http://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was retrieved successfully, and all the elements of the file attachment.</span></span>
  
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
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="5zTzlqU=" />
              <t:Name>FileAttachment.txt</t:Name>
              <t:Content>VGhpcyBpcyBhIGZpbGUgYXR0YWNobWVudC4=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="save-an-attached-email-by-using-the-ews-managed-api"></a><span data-ttu-id="46113-136">通过使用 EWS 托管 API 来保存附加电子邮件</span><span class="sxs-lookup"><span data-stu-id="46113-136">Save an attached email by using the EWS Managed API</span></span>
<span data-ttu-id="46113-137"><a name="bk_saveitemattach"> </a></span><span class="sxs-lookup"><span data-stu-id="46113-137"></span></span>

<span data-ttu-id="46113-138">为了节省使用 EWS 托管 API 的电子邮件附件的内容，您需要将[MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)保存到文件。</span><span class="sxs-lookup"><span data-stu-id="46113-138">In order to save the contents of an email attachment using the EWS Managed API, you need to save the [MimeContent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) to a file.</span></span> <span data-ttu-id="46113-139">这样，则将丢失的项，如后续标志和类别设置的所有扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="46113-139">In doing so, you will lose any extended properties set on the item, such as follow-up flags and categories.</span></span> <span data-ttu-id="46113-140">本示例将保存到的电子邮件附件 C:\temp\ 文件夹。</span><span class="sxs-lookup"><span data-stu-id="46113-140">This example saves the email attachment to the to the C:\temp\ folder.</span></span> 
  
<span data-ttu-id="46113-141">请注意，您无法移动或复制到另一个文件夹的项目附件，因为项目附件的强类型的项，因此如果您正在尝试移动到另一个文件夹，附件使用下面的代码示例，然后[将文件导](how-to-import-items-by-using-ews-in-exchange.md)入不同的文件夹。</span><span class="sxs-lookup"><span data-stu-id="46113-141">Note that you cannot move or copy the item attachment to another folder because the item attachment is not a strongly-typed item, so if you're trying to move an attachment to a different folder, use the following code example and then [import the file](how-to-import-items-by-using-ews-in-exchange.md) into a different folder.</span></span> 
  
```cs
public static void SaveEmailAttachment(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message item and retrieve the attachments collection.
    // This method results in an GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment is ItemAttachment)
        {
            ItemAttachment itemAttachment = attachment as ItemAttachment;
            itemAttachment.Load(ItemSchema.MimeContent);
            string fileName = "C:\\Temp\\" + itemAttachment.Item.Subject + ".eml";
            // Write the bytes of the attachment into a file.
            File.WriteAllBytes(fileName, itemAttachment.Item.MimeContent.Content);
            Console.WriteLine("Email attachment name: "+ itemAttachment.Item.Subject + ".eml");
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="46113-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46113-142">See also</span></span>


- [<span data-ttu-id="46113-143">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="46113-143">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="46113-144">在 Exchange 使用 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="46113-144">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="46113-145">使用 EWS 在 Exchange 中删除附件</span><span class="sxs-lookup"><span data-stu-id="46113-145">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    

