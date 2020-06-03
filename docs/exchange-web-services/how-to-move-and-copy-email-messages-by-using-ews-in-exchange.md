---
title: 使用 Exchange 中的 EWS 移动和复制电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: 了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 移动和复制电子邮件。
localization_priority: Priority
ms.openlocfilehash: d13e84648f194dd4f431cf128396daf016addb22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527934"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="e75e9-103">使用 Exchange 中的 EWS 移动和复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-103">Move and copy email messages by using EWS in Exchange</span></span>

<span data-ttu-id="e75e9-104">了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 移动和复制电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e75e9-104">Learn how to move and copy email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e75e9-105">您可以使用 EWS 托管 API 或 EWS 在邮箱中移动和复制电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e75e9-105">You can use the EWS Managed API or EWS to move and copy email messages in a mailbox.</span></span>
  
<span data-ttu-id="e75e9-106">**表1。用于移动和复制电子邮件的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="e75e9-106">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="e75e9-107">**任务**</span><span class="sxs-lookup"><span data-stu-id="e75e9-107">**Task**</span></span>|<span data-ttu-id="e75e9-108">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="e75e9-108">**EWS Managed API method**</span></span>|<span data-ttu-id="e75e9-109">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="e75e9-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e75e9-110">移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-110">Move an email message</span></span>  <br/> |[<span data-ttu-id="e75e9-111">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="e75e9-111">EmailMessage.Move</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e75e9-112">MoveItem</span><span class="sxs-lookup"><span data-stu-id="e75e9-112">MoveItem</span></span>](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="e75e9-113">复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-113">Copy an email message</span></span>  <br/> |[<span data-ttu-id="e75e9-114">EmailMessage</span><span class="sxs-lookup"><span data-stu-id="e75e9-114">EmailMessage.Copy</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e75e9-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="e75e9-115">CopyItem</span></span>](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="e75e9-116">请务必注意，当您将电子邮件移动或复制到另一个文件夹中时，将会在具有唯一项目 ID 的新文件夹中创建一个新项目，并删除原始邮件。</span><span class="sxs-lookup"><span data-stu-id="e75e9-116">It's important to note that when you move or copy an email message into a different folder, a new item is created in the new folder with a unique item ID, and the original message is deleted.</span></span> <span data-ttu-id="e75e9-117">如果要在同一邮箱中的两个文件夹之间移动或复制电子邮件，则会在响应中返回新项目，从而使您可以访问新的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="e75e9-117">If you're moving or copying an email message between two folders in the same mailbox, the new item is returned in the response, which gives you access to the new item ID.</span></span> <span data-ttu-id="e75e9-118">但是，如果要在两个邮箱之间或邮箱与公用文件夹之间移动或复制电子邮件，响应中不会返回新项目。</span><span class="sxs-lookup"><span data-stu-id="e75e9-118">However, if you're moving or copying an email message between two mailboxes or between a mailbox and a public folder, the new item is not returned in the response.</span></span> <span data-ttu-id="e75e9-119">若要在该方案中访问移动的邮件，请使用 EWS 托管 API [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法或 EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作，为[PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) （0x300B0102）属性[创建扩展属性定义](properties-and-extended-properties-in-ews-in-exchange.md)，或者创建和设置自定义扩展属性，然后在新文件夹中搜索自定义扩展属性。</span><span class="sxs-lookup"><span data-stu-id="e75e9-119">To access the moved message in that scenario, use the EWS Managed API [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) method or EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation, [create an extended property definition](properties-and-extended-properties-in-ews-in-exchange.md) for the [PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) (0x300B0102) property, or create and set a custom extended property and then search for the custom extended property in the new folder.</span></span> 
  
<span data-ttu-id="e75e9-120">删除电子邮件与将项目移动到 "已删除邮件" 文件夹中的邮件不同。</span><span class="sxs-lookup"><span data-stu-id="e75e9-120">Deleting an email message is different than moving an item to the Deleted Items folder.</span></span> <span data-ttu-id="e75e9-121">如果使用 EWS 托管 API[项。 Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx)方法或 EWS [DeleteItem](../web-service-reference/deleteitem-operation.md)操作，将从原始文件夹中删除在请求中指定的项目，并将副本放在 "已删除邮件" 文件夹中，同时包含一个新的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="e75e9-121">If you use the EWS Managed API [Item.Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx) method or the EWS [DeleteItem](../web-service-reference/deleteitem-operation.md) operation, the item specified in the request is removed from the original folder, and a copy is placed in the Deleted Items folder with a new item ID.</span></span> <span data-ttu-id="e75e9-122">与移动或复制任何项不同时， **Delete**方法或**DeleteItem**操作响应中不会返回新项。</span><span class="sxs-lookup"><span data-stu-id="e75e9-122">Unlike when you move or copy any item, the new item is not returned in the **Delete** method or the **DeleteItem** operation response.</span></span> <span data-ttu-id="e75e9-123">[使用 EWS 托管 API 或 EWS 删除电子邮件](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma)所涉及的步骤与[EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews)从 Exchange 存储中删除任何通用项的步骤相同。</span><span class="sxs-lookup"><span data-stu-id="e75e9-123">The steps involved in [deleting an email by using the EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) or [EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) are the same as those for deleting any generic item from the Exchange store.</span></span> 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="e75e9-124">使用 EWS 托管 API 移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-124">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="e75e9-125"><a name="bk_moveewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e75e9-125"><a name="bk_moveewsma"> </a></span></span>

<span data-ttu-id="e75e9-126">下面的代码示例演示如何使用[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法将现有电子邮件从一个文件夹移动到另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e75e9-126">The following code example shows how to use the [EmailMessage.Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method to move an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="e75e9-127">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且**ItemId**是要移动或复制的电子邮件的[Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e75e9-127">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
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

## <a name="move-an-email-message-by-using-ews"></a><span data-ttu-id="e75e9-128">使用 EWS 移动电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-128">Move an email message by using EWS</span></span>
<span data-ttu-id="e75e9-129"><a name="bk_moveews"> </a></span><span class="sxs-lookup"><span data-stu-id="e75e9-129"><a name="bk_moveews"> </a></span></span>

<span data-ttu-id="e75e9-130">下面的代码示例演示如何使用[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作将电子邮件移动到 "垃圾邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="e75e9-130">The following code example shows how to use the [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation to move an email message to the Junk Email folder.</span></span> 
  
<span data-ttu-id="e75e9-131">这也是在调用[Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法时由 EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e75e9-131">This is also the XML request that is sent by the EWS Managed API when calling the [Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="e75e9-132">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="e75e9-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e75e9-133">服务器使用[MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx)邮件响应**MoveItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，表示电子邮件已成功移动。</span><span class="sxs-lookup"><span data-stu-id="e75e9-133">The server responds to the **MoveItem** request with a [MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was moved successfully.</span></span> <span data-ttu-id="e75e9-134">该响应还包括新文件夹中电子邮件的**ItemId** ，这一点对于存储很重要，因为新文件夹中的**ItemId**是不同的。</span><span class="sxs-lookup"><span data-stu-id="e75e9-134">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="e75e9-135">使用 EWS 托管 API 复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-135">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="e75e9-136"><a name="bk_copyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e75e9-136"><a name="bk_copyewsma"> </a></span></span>

<span data-ttu-id="e75e9-137">下面的代码示例演示如何使用[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法将现有电子邮件从一个文件夹复制到另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e75e9-137">The following code example shows how to use the [EmailMessage.Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method to copy an existing email message from one folder to another.</span></span> 
  
<span data-ttu-id="e75e9-138">此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且**ItemId**是要复制的电子邮件的[Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="e75e9-138">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to copy.</span></span> <span data-ttu-id="e75e9-139">为了提高可读性，某些参数的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="e75e9-139">The values of some parameters have been shortened for readability.</span></span> 
  
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

## <a name="copy-an-email-message-by-using-ews"></a><span data-ttu-id="e75e9-140">使用 EWS 复制电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-140">Copy an email message by using EWS</span></span>
<span data-ttu-id="e75e9-141"><a name="bk_copyews"> </a></span><span class="sxs-lookup"><span data-stu-id="e75e9-141"><a name="bk_copyews"> </a></span></span>

<span data-ttu-id="e75e9-142">下面的代码示例演示如何使用[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)操作将电子邮件复制到同一邮箱中的不同文件夹中，方法是发送要移动的电子邮件的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ，并在[ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)元素中指定目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="e75e9-142">The following code example shows how to use the [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to copy an email message to different folder in the same mailbox by sending the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to move, and specifying the destination folder in the [ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="e75e9-143">这也是在调用[Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法时由 EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e75e9-143">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="e75e9-144">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="e75e9-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="e75e9-145">服务器使用[CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx)邮件响应**CopyItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，表示电子邮件已成功复制。</span><span class="sxs-lookup"><span data-stu-id="e75e9-145">The server responds to the **CopyItem** request with a [CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully.</span></span> <span data-ttu-id="e75e9-146">该响应还包括新文件夹中电子邮件的**ItemId** ，这一点对于存储很重要，因为新文件夹中的**ItemId**是不同的。</span><span class="sxs-lookup"><span data-stu-id="e75e9-146">The response also includes the **ItemId** for the email message in the new folder, which is important to store because the **ItemId** is different in the new folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e75e9-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e75e9-147">See also</span></span>


- [<span data-ttu-id="e75e9-148">Exchange 中的电子邮件和 EMS</span><span class="sxs-lookup"><span data-stu-id="e75e9-148">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="e75e9-149">使用 Exchange 中的 EWS 发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="e75e9-149">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

