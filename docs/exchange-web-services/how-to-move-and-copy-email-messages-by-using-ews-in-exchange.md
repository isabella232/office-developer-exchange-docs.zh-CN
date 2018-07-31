---
title: 移动和复制在 Exchange 使用 EWS 的电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: 了解如何移动和复制在 Exchange 使用 EWS 托管 API 或 EWS 的电子邮件。
ms.openlocfilehash: 44d5834176b55ad041befbad2230b8b507a12ecc
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353467"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="09bd2-103">移动和复制在 Exchange 使用 EWS 的电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-103">Move and copy email messages by using EWS in Exchange</span></span>

<span data-ttu-id="09bd2-104">了解如何移动和复制在 Exchange 使用 EWS 托管 API 或 EWS 的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="09bd2-104">Learn how to move and copy email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="09bd2-105">您可以使用 EWS 托管 API 或 EWS 移动和复制电子邮件的邮箱中的邮件。</span><span class="sxs-lookup"><span data-stu-id="09bd2-105">You can use the EWS Managed API or EWS to move and copy email messages in a mailbox.</span></span>
  
<span data-ttu-id="09bd2-106">**表 1。EWS 托管 API 方法和移动和复制电子邮件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="09bd2-106">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="09bd2-107">**任务**</span><span class="sxs-lookup"><span data-stu-id="09bd2-107">**Task**</span></span>|<span data-ttu-id="09bd2-108">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="09bd2-108">**EWS Managed API method**</span></span>|<span data-ttu-id="09bd2-109">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="09bd2-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09bd2-110">移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-110">Move an email message</span></span>  <br/> |[<span data-ttu-id="09bd2-111">EmailMessage.Move</span><span class="sxs-lookup"><span data-stu-id="09bd2-111">EmailMessage.Move</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="09bd2-112">MoveItem</span><span class="sxs-lookup"><span data-stu-id="09bd2-112">MoveItem</span></span>](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="09bd2-113">复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-113">Copy an email message</span></span>  <br/> |[<span data-ttu-id="09bd2-114">EmailMessage.Copy</span><span class="sxs-lookup"><span data-stu-id="09bd2-114">EmailMessage.Copy</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="09bd2-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="09bd2-115">CopyItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="09bd2-116">请务必注意当移动或复制到一个不同的文件夹的电子邮件时，在新文件夹中具有唯一项目 ID，创建一个新项，而且原始邮件将被删除。</span><span class="sxs-lookup"><span data-stu-id="09bd2-116">It's important to note that when you move or copy an email message into a different folder, a new item is created in the new folder with a unique item ID, and the original message is deleted.</span></span> <span data-ttu-id="09bd2-117">如果您正在移动或复制电子邮件中的同一邮箱的两个文件夹之间，将新项返回响应，它可以访问新项目 id。</span><span class="sxs-lookup"><span data-stu-id="09bd2-117">If you're moving or copying an email message between two folders in the same mailbox, the new item is returned in the response, which gives you access to the new item ID.</span></span> <span data-ttu-id="09bd2-118">但是，如果您正在移动或复制或邮箱和公用文件夹之间的两个邮箱的电子邮件，在响应中不返回新项目。</span><span class="sxs-lookup"><span data-stu-id="09bd2-118">However, if you're moving or copying an email message between two mailboxes or between a mailbox and a public folder, the new item is not returned in the response.</span></span> <span data-ttu-id="09bd2-119">若要访问该方案中的移动的消息，使用 EWS 托管 API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法或 EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作，为[PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102) 属性中，[创建扩展的属性定义](properties-and-extended-properties-in-ews-in-exchange.md)或创建和设置自定义扩展属性，然后搜索新文件夹中的自定义扩展属性。</span><span class="sxs-lookup"><span data-stu-id="09bd2-119">To access the moved message in that scenario, use the EWS Managed API [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method or EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, [create an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the [PidTagSearchKey](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x300B0102) property, or create and set a custom extended property and then search for the custom extended property in the new folder.</span></span> 
  
<span data-ttu-id="09bd2-120">删除电子邮件是不同于项目移动到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="09bd2-120">Deleting an email message is different than moving an item to the Deleted Items folder.</span></span> <span data-ttu-id="09bd2-121">如果您使用 EWS 托管 API [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx)方法或 EWS[删除项](../web-service-reference/deleteitem-operation.md)操作，在请求中指定的项已从原始文件夹，并副本处于已删除邮件文件夹具有新的项 id。</span><span class="sxs-lookup"><span data-stu-id="09bd2-121">If you use the EWS Managed API [Item.Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method or the EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) operation, the item specified in the request is removed from the original folder, and a copy is placed in the Deleted Items folder with a new item ID.</span></span> <span data-ttu-id="09bd2-122">与移动或复制任何项，不同的新项目不会返回**Delete**方法或**删除项**操作响应中。</span><span class="sxs-lookup"><span data-stu-id="09bd2-122">Unlike when you move or copy any item, the new item is not returned in the **Delete** method or the **DeleteItem** operation response.</span></span> <span data-ttu-id="09bd2-123">[删除电子邮件使用 EWS 托管 API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma)涉及的步骤或[EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews)从 Exchange 存储中删除任何泛型项目相同。</span><span class="sxs-lookup"><span data-stu-id="09bd2-123">The steps involved in [deleting an email by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) or [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) are the same as those for deleting any generic item from the Exchange store.</span></span> 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="09bd2-124">使用 EWS 托管 API 移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-124">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="09bd2-125"><a name="bk_moveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="09bd2-125"></span></span>

<span data-ttu-id="09bd2-126">下面的代码示例演示如何[EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法用于移动到另一个文件夹中现有的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="09bd2-126">The following code example shows how to use the [EmailMessage.Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method to move an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="09bd2-127">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该**ItemId**是[Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)的电子邮件移动或复制。</span><span class="sxs-lookup"><span data-stu-id="09bd2-127">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage beforeMessage = EmailMessage.Bind(service, ItemId, propSet);
// Move the specified mail to the JunkEmail folder and store the returned item.
Item item = beforeMessage.Move(WellKnownFolderName.JunkEmail);
// Check that the item was moved by binding to the moved email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage movedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + beforeMessage.Subject + "' has been moved from the '" + beforeMessage.ParentFolderId + "' folder to the '" + movedMessage.ParentFolderId + "' folder.");
```

## <a name="move-an-email-message-by-using-ews"></a><span data-ttu-id="09bd2-128">使用 EWS 移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-128">Move an email message by using EWS</span></span>
<span data-ttu-id="09bd2-129"><a name="bk_moveews"> </a></span><span class="sxs-lookup"><span data-stu-id="09bd2-129"></span></span>

<span data-ttu-id="09bd2-130">下面的代码示例演示如何使用[MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作将电子邮件移动到垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="09bd2-130">The following code example shows how to use the [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation to move an email message to the Junk Email folder.</span></span> 
  
<span data-ttu-id="09bd2-131">这也是 XML 请求发送的 EWS 托管 API 调用[Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法时。</span><span class="sxs-lookup"><span data-stu-id="09bd2-131">This is also the XML request that is sent by the EWS Managed API when calling the [Move](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="09bd2-132">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="09bd2-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:MoveItem>
      <m:ToFolderId>
        <t:DistinguishedFolderId Id="junkemail" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="AfwDoAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF25sM1" />
      </m:ItemIds>
    </m:MoveItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="09bd2-133">服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，这表明已成功移动电子邮件的[MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx)消息的**MoveItem**请求。</span><span class="sxs-lookup"><span data-stu-id="09bd2-133">The server responds to the **MoveItem** request with a [MoveItemResponse](http://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was moved successfully.</span></span> <span data-ttu-id="09bd2-134">响应在新文件夹中，这是重要存储，因为**ItemId**位于不同的新文件夹还包括**ItemId**的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="09bd2-134">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="09bd2-135">使用 EWS 托管 API 复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-135">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="09bd2-136"><a name="bk_copyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="09bd2-136"></span></span>

<span data-ttu-id="09bd2-137">下面的代码示例演示如何使用[EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法可将现有电子邮件从一个文件夹复制到另一个。</span><span class="sxs-lookup"><span data-stu-id="09bd2-137">The following code example shows how to use the [EmailMessage.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method to copy an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="09bd2-138">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该**ItemId**是电子邮件将复制的[Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="09bd2-138">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to copy.</span></span> <span data-ttu-id="09bd2-139">为便于阅读变短了一些参数的值。</span><span class="sxs-lookup"><span data-stu-id="09bd2-139">The values of some parameters have been shortened for readability.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage originalMessage = EmailMessage.Bind(service, ItemId, propSet);
// Copy the orignal message into another folder in the mailbox and store the returned item.
Item item = originalMessage.Copy("epQ/3AAA=");
// Check that the item was copied by binding to the copied email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage copiedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + originalMessage.Subject + "' has been copied from the '" + originalMessage.ParentFolderId + "' folder to the '" + copiedMessage.ParentFolderId + "' folder.");
```

## <a name="copy-an-email-message-by-using-ews"></a><span data-ttu-id="09bd2-140">使用 EWS 复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-140">Copy an email message by using EWS</span></span>
<span data-ttu-id="09bd2-141"><a name="bk_copyews"> </a></span><span class="sxs-lookup"><span data-stu-id="09bd2-141"></span></span>

<span data-ttu-id="09bd2-142">下面的代码示例演示如何使用[CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)操作将通过发送电子邮件移动， [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)和[ToFolderId 中指定的目标文件夹复制到不同的文件夹中的同一邮箱的电子邮件](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="09bd2-142">The following code example shows how to use the [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to copy an email message to different folder in the same mailbox by sending the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to move, and specifying the destination folder in the [ToFolderId](http://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="09bd2-143">这也是 XML 请求时调用[的复制](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法，EWS 托管 API 所发送的。</span><span class="sxs-lookup"><span data-stu-id="09bd2-143">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="09bd2-144">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="09bd2-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CopyItem>
      <m:ToFolderId>
        <t:FolderId Id="pQ/3AAA=" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="2TSeSAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF2d+3+" />
      </m:ItemIds>
    </m:CopyItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="09bd2-145">服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，这表明已成功复制电子邮件的[CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx)消息的**CopyItem**请求。</span><span class="sxs-lookup"><span data-stu-id="09bd2-145">The server responds to the **CopyItem** request with a [CopyItemResponse](http://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully.</span></span> <span data-ttu-id="09bd2-146">响应在新文件夹中，这是重要存储，因为**ItemId**位于不同的新文件夹还包括**ItemId**的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="09bd2-146">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="09bd2-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09bd2-147">See also</span></span>


- [<span data-ttu-id="09bd2-148">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="09bd2-148">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="09bd2-149">在 Exchange 使用 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="09bd2-149">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

