---
title: 使用 Exchange 中的 EWS 获取附件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 12ce3cc0-a201-42e4-93e1-1f57961ff711
description: 了解如何通过在 Exchange 中使用 EWS 托管 API 或 EWS 从 EWS 项目中获取附件。
localization_priority: Priority
ms.openlocfilehash: de3e3ebfbcb16935130203dfed50f255bd59be7b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528081"
---
# <a name="get-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="b97e1-103">使用 Exchange 中的 EWS 获取附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-103">Get attachments by using EWS in Exchange</span></span>

<span data-ttu-id="b97e1-104">了解如何通过在 Exchange 中使用 EWS 托管 API 或 EWS 从 EWS 项目中获取附件。</span><span class="sxs-lookup"><span data-stu-id="b97e1-104">Learn how to get attachments from EWS items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="b97e1-105">您可以使用 EWS 托管 API 或 EWS 从项目中获取附件。</span><span class="sxs-lookup"><span data-stu-id="b97e1-105">You can get attachments from an item by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="b97e1-106">由于最初对获取项目的调用包含有关项目上的附件集合的元数据，因此检索附件的过程始终为两个步骤。</span><span class="sxs-lookup"><span data-stu-id="b97e1-106">Because the initial call to get an item only includes metadata about the attachment collection on the item, retrieving attachments is always a two-step process.</span></span> <span data-ttu-id="b97e1-107">首先，检索项目。</span><span class="sxs-lookup"><span data-stu-id="b97e1-107">First, retrieve the item.</span></span> <span data-ttu-id="b97e1-108">接下来，检索附件。</span><span class="sxs-lookup"><span data-stu-id="b97e1-108">Next, retrieve the attachment.</span></span>
  
<span data-ttu-id="b97e1-109">**表1。用于添加附件的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="b97e1-109">**Table 1. EWS Managed API methods and EWS operations for adding attachments**</span></span>

|<span data-ttu-id="b97e1-110">**任务**</span><span class="sxs-lookup"><span data-stu-id="b97e1-110">**Task**</span></span>|<span data-ttu-id="b97e1-111">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="b97e1-111">**EWS Managed API method**</span></span>|<span data-ttu-id="b97e1-112">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="b97e1-112">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b97e1-113">获取项目附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-113">Get item attachments</span></span>  <br/> |<span data-ttu-id="b97e1-114">先绑定后接[ItemAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment.load%28v=exchg.80%29.aspx)的[项](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b97e1-114">[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) followed by [ItemAttachment.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment.load%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="b97e1-115">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)后接[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b97e1-115">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) followed by [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="b97e1-116">获取文件附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-116">Get file attachments</span></span>  <br/> |<span data-ttu-id="b97e1-117">先绑定后接[FileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment.load%28v=exchg.80%29.aspx)的[项](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b97e1-117">[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) followed by [FileAttachment.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment.load%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="b97e1-118">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)后接[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b97e1-118">[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) followed by [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)</span></span> <br/> |
   
## <a name="get-attachments-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="b97e1-119">使用 EWS 托管 API 从电子邮件获取附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-119">Get attachments from an email by using the EWS Managed API</span></span>
<span data-ttu-id="b97e1-120"><a name="bk_getattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b97e1-120"><a name="bk_getattachewsma"> </a></span></span>

<span data-ttu-id="b97e1-121">下面的代码示例演示如何使用**Bind**方法获取[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象，然后循环访问附件集合，并根据需要对每个附件调用**FileAttachment**或**ItemAttachment**方法。</span><span class="sxs-lookup"><span data-stu-id="b97e1-121">The following code example shows how to get an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object by using the **Bind** method, then iterate through the attachment collection and call the **FileAttachment.Load** or **ItemAttachment.Load** method on each attachment as appropriate.</span></span> <span data-ttu-id="b97e1-122">每个文件附件都保存到 C:\temp\ 文件夹，每个项目附件都会加载到内存中。</span><span class="sxs-lookup"><span data-stu-id="b97e1-122">Each file attachment is saved to the C:\temp\ folder, and each item attachment is loaded into memory.</span></span> <span data-ttu-id="b97e1-123">有关如何保存项目附件的信息，请参阅[使用 EWS 托管 API 保存附加的电子邮件](#bk_saveitemattach)。</span><span class="sxs-lookup"><span data-stu-id="b97e1-123">For information about how to save an item attachment, see [Save an attached email by using the EWS Managed API](#bk_saveitemattach).</span></span>
  
<span data-ttu-id="b97e1-124">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，则**itemid**是将从中检索附件的邮件的[itemid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) ，并且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="b97e1-124">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, that **itemId** is the [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which attachments will be retrieved, and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-an-attachment-from-an-email-by-using-ews"></a><span data-ttu-id="b97e1-125">使用 EWS 从电子邮件获取附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-125">Get an attachment from an email by using EWS</span></span>
<span data-ttu-id="b97e1-126"><a name="bk_getattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="b97e1-126"><a name="bk_getattachewsma"> </a></span></span>

<span data-ttu-id="b97e1-127">若要使用 EWS 获取附件，首先需要检索邮件和附件集合，以获取要检索的附件的[AttachmentId （GetAttachment 和 DeleteAttachment）](https://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="b97e1-127">To get attachments by using EWS, you first need to retrieve the message and the attachment collection to get the [AttachmentId (GetAttachment and DeleteAttachment)](https://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) of the attachment to retrieve.</span></span> <span data-ttu-id="b97e1-128">在具有一个或多个要检索的**AttachmentId**值之后，调用[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作以加载附件的所有属性。</span><span class="sxs-lookup"><span data-stu-id="b97e1-128">After you have one or more **AttachmentId** values to retrieve, call the [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) operation to load all the properties for the attachment.</span></span> 
  
<span data-ttu-id="b97e1-129">下面的代码示例演示如何使用[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作来获取电子邮件和邮件附件的集合。</span><span class="sxs-lookup"><span data-stu-id="b97e1-129">The following code example shows how to use the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to get an email message and the collection of attachments on the message.</span></span> <span data-ttu-id="b97e1-130">这也是当您使用 EWS 托管 API[从电子邮件获取所有附件](#bk_getattachewsma)时，EWS 托管 api 发送的第一个 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="b97e1-130">This is also the first XML request that the EWS Managed API sends when you use the EWS Managed API to [get all attachments from an email](#bk_getattachewsma).</span></span> <span data-ttu-id="b97e1-131">为了提高可读性，某些属性的值会缩短。</span><span class="sxs-lookup"><span data-stu-id="b97e1-131">The values of some attributes are shortened for readability.</span></span>
  
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

<span data-ttu-id="b97e1-132">服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，该值指示电子邮件已成功检索，以及现有附件的[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="b97e1-132">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values of the existing attachments.</span></span> 
  
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

<span data-ttu-id="b97e1-133">现在您已拥有[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值，请在要检索的每个附件上调用[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="b97e1-133">Now that you have the [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values, call [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) on each attachment you want to retrieve.</span></span> 
  
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
    <m:GetAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="5zTzlqU=" />
      </m:AttachmentIds>
    </m:GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="b97e1-134">检索项目附件时，服务器会使用[GetAttachmentResponse](https://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx)邮件响应**GetAttachment**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示已成功检索附件，并且附加项目的所有元素（在此示例中为电子邮件）。</span><span class="sxs-lookup"><span data-stu-id="b97e1-134">When retrieving an item attachment, the server responds to the **GetAttachment** request with a [GetAttachmentResponse](https://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was retrieved successfully, and all the elements for the attached item, which in this case is an email message.</span></span>
  
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
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="b97e1-135">检索文件附件时，服务器会使用[GetAttachmentResponse](https://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx)邮件响应**GetAttachment**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，表示已成功检索附件，并且文件附件的所有元素。</span><span class="sxs-lookup"><span data-stu-id="b97e1-135">When retrieving a file attachment, the server responds to the **GetAttachment** request with a [GetAttachmentResponse](https://msdn.microsoft.com/library/cb65f449-309b-4b6e-8d22-d1967135490c%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the attachment was retrieved successfully, and all the elements of the file attachment.</span></span>
  
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
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="save-an-attached-email-by-using-the-ews-managed-api"></a><span data-ttu-id="b97e1-136">使用 EWS 托管 API 保存附加的电子邮件</span><span class="sxs-lookup"><span data-stu-id="b97e1-136">Save an attached email by using the EWS Managed API</span></span>
<span data-ttu-id="b97e1-137"><a name="bk_saveitemattach"> </a></span><span class="sxs-lookup"><span data-stu-id="b97e1-137"><a name="bk_saveitemattach"> </a></span></span>

<span data-ttu-id="b97e1-138">为了使用 EWS 托管 API 保存电子邮件附件的内容，您需要将[MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx)保存到文件中。</span><span class="sxs-lookup"><span data-stu-id="b97e1-138">In order to save the contents of an email attachment using the EWS Managed API, you need to save the [MimeContent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.mimecontent%28v=exchg.80%29.aspx) to a file.</span></span> <span data-ttu-id="b97e1-139">在执行此操作时，将丢失对项目设置的任何扩展属性，例如后续标志和类别。</span><span class="sxs-lookup"><span data-stu-id="b97e1-139">In doing so, you will lose any extended properties set on the item, such as follow-up flags and categories.</span></span> <span data-ttu-id="b97e1-140">此示例将电子邮件附件保存到 "C:\temp\" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b97e1-140">This example saves the email attachment to the to the C:\temp\ folder.</span></span> 
  
<span data-ttu-id="b97e1-141">请注意，不能将项目附件移动或复制到另一个文件夹，因为项目附件不是强类型项目，因此，如果您尝试将附件移动到其他文件夹，请使用以下代码示例，然后将[该文件导入](how-to-import-items-by-using-ews-in-exchange.md)到其他文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b97e1-141">Note that you cannot move or copy the item attachment to another folder because the item attachment is not a strongly-typed item, so if you're trying to move an attachment to a different folder, use the following code example and then [import the file](how-to-import-items-by-using-ews-in-exchange.md) into a different folder.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b97e1-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b97e1-142">See also</span></span>


- [<span data-ttu-id="b97e1-143">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="b97e1-143">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="b97e1-144">使用 Exchange 中的 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-144">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="b97e1-145">使用 Exchange 中的 EWS 删除附件</span><span class="sxs-lookup"><span data-stu-id="b97e1-145">Delete attachments by using EWS in Exchange</span></span>](how-to-delete-attachments-by-using-ews-in-exchange.md)
    

