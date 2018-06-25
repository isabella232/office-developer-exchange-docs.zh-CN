---
title: 使用 EWS 在 Exchange 中删除附件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 从项目中删除附件。
ms.openlocfilehash: 458331f81493283efc20d24c7e2bebe0e74bbdbd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752772"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a><span data-ttu-id="e1846-103">使用 EWS 在 Exchange 中删除附件</span><span class="sxs-lookup"><span data-stu-id="e1846-103">Delete attachments by using EWS in Exchange</span></span>

<span data-ttu-id="e1846-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 从项目中删除附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-104">Learn how to delete attachments from items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e1846-105">当谈到正在删除文件和项目附件从项目使用 EWS 托管 API，您具有多个选项。</span><span class="sxs-lookup"><span data-stu-id="e1846-105">You have a number of options when it comes to deleting file and item attachments from items by using the EWS Managed API.</span></span> <span data-ttu-id="e1846-106">可以从邮件中删除所有附件，都删除按文件名，或按位置集合中都删除。</span><span class="sxs-lookup"><span data-stu-id="e1846-106">You can delete all the attachments from the message, delete by a file name, or delete by position in the collection.</span></span> <span data-ttu-id="e1846-107">对于每个这些选项，没有[AttachmentCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="e1846-107">For each of these options, there is an [AttachmentCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="e1846-108">相反，EWS，无论是否从项或只是一个删除所有附件操作的顺序是相同。</span><span class="sxs-lookup"><span data-stu-id="e1846-108">Conversely, with EWS, no matter whether you're deleting all attachments from an item or just one, the sequence of operations is same.</span></span> <span data-ttu-id="e1846-109">与 EWS 托管 API 不同 EWS 不包括单独操作删除基于名称或附件数组中的位置。</span><span class="sxs-lookup"><span data-stu-id="e1846-109">Unlike the EWS Managed API, EWS does not include separate operations to delete based on name or position in the attachments array.</span></span>
  
<span data-ttu-id="e1846-110">**表 1。EWS 托管 API 方法和删除附件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="e1846-110">**Table 1. EWS Managed API methods and EWS operations for deleting attachments**</span></span>

|<span data-ttu-id="e1846-111">**任务**</span><span class="sxs-lookup"><span data-stu-id="e1846-111">**Task**</span></span>|<span data-ttu-id="e1846-112">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="e1846-112">**EWS Managed API method**</span></span>|<span data-ttu-id="e1846-113">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="e1846-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1846-114">从项目中删除所有附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-114">Delete all attachments from an item.</span></span>  <br/> |<span data-ttu-id="e1846-115">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)后, 跟[AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx)后, 跟[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-115">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e1846-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)跟[DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-116">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="e1846-117">按名称从项目中删除附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-117">Delete an attachment from an item by name.</span></span>  <br/> |<span data-ttu-id="e1846-118">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)后, 跟[AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx)后, 跟[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-118">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e1846-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)跟[DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-119">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="e1846-120">从集合中的位置的项目中删除附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-120">Delete an attachment from an item by position in the collection.</span></span>  <br/> |<span data-ttu-id="e1846-121">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)后, 跟[AttachmentCollection.RemoveAt](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx)后, 跟[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-121">[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), followed by [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e1846-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)跟[DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1846-122">[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) followed by [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx)</span></span> <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="e1846-123">从电子邮件中删除所有附件，通过使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="e1846-123">Delete all attachments from an email by using the EWS Managed API</span></span>
<span data-ttu-id="e1846-124"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e1846-124"></span></span>

<span data-ttu-id="e1846-125">下面的代码示例演示如何通过电子邮件中删除所有附件：</span><span class="sxs-lookup"><span data-stu-id="e1846-125">The following code example shows how to delete all attachments from an email by:</span></span>
  
1. <span data-ttu-id="e1846-126">使用[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法将绑定到现有电子邮件和检索的[附件](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)集合。</span><span class="sxs-lookup"><span data-stu-id="e1846-126">Using the [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="e1846-127">使用[AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx)方法从电子邮件中删除所有附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-127">Using the [AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) method to delete all the attachments from the email.</span></span> 
    
3. <span data-ttu-id="e1846-128">使用[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e1846-128">Using the [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="e1846-129">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、 **itemId**是从中将删除附件，邮件[ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="e1846-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which attachments will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="e1846-130">按名称从电子邮件中删除附件，通过使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="e1846-130">Delete an attachment by name from an email by using the EWS Managed API</span></span>
<span data-ttu-id="e1846-131"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e1846-131"></span></span>

<span data-ttu-id="e1846-132">下面的代码示例演示如何按名称删除附件：</span><span class="sxs-lookup"><span data-stu-id="e1846-132">The following code example shows how delete an attachment by name by:</span></span>
  
1. <span data-ttu-id="e1846-133">使用[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法将绑定到现有电子邮件和检索的[附件](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)集合。</span><span class="sxs-lookup"><span data-stu-id="e1846-133">Using the [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).</span></span>
    
2. <span data-ttu-id="e1846-134">使用[AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx)方法删除名为 FileAttachment.txt 附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-134">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete an attachment named FileAttachment.txt.</span></span> 
    
3. <span data-ttu-id="e1846-135">使用[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e1846-135">Using the [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="e1846-136">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、 **itemId**是从中将删除附件，邮件[ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="e1846-136">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a><span data-ttu-id="e1846-137">使用 EWS 托管 API 删除附件按位置</span><span class="sxs-lookup"><span data-stu-id="e1846-137">Delete attachments by position by using the EWS Managed API</span></span>
<span data-ttu-id="e1846-138"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e1846-138"></span></span>

<span data-ttu-id="e1846-139">下面的代码示例演示如何删除按位置通过附件：</span><span class="sxs-lookup"><span data-stu-id="e1846-139">The following code example shows how to delete an attachment by position by:</span></span>
  
1. <span data-ttu-id="e1846-140">使用[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)方法将绑定到现有电子邮件和检索的[附件](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)和[EmailMessage.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx)属性集合。</span><span class="sxs-lookup"><span data-stu-id="e1846-140">Using the [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to bind to an existing email message and retrieve the collection of [Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) and the [EmailMessage.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) property.</span></span> 
    
2. <span data-ttu-id="e1846-141">使用[AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx)方法删除集合中的第一个附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-141">Using the [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) method to delete the first attachment in the collection.</span></span> 
    
3. <span data-ttu-id="e1846-142">使用[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)方法保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e1846-142">Using the [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
    
<span data-ttu-id="e1846-143">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象、 **itemId**是从中将删除附件，邮件[ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="e1846-143">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, **itemId** is the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) of the message from which the attachment will be deleted, and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a><span data-ttu-id="e1846-144">使用 EWS 从项目中删除附件</span><span class="sxs-lookup"><span data-stu-id="e1846-144">Delete attachments from an item by using EWS</span></span>
<span data-ttu-id="e1846-145"><a name="bk_deleteattachewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e1846-145"></span></span>

<span data-ttu-id="e1846-146">使用 EWS 删除附件，首先需要检索邮件和附件集合来确定附件[AttachmentId （GetAttachment 和 DeleteAttachment）](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) ，删除。</span><span class="sxs-lookup"><span data-stu-id="e1846-146">To delete attachments by using EWS, you first need to retrieve the message and the attachment collection to determine the [AttachmentId (GetAttachment and DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) of the attachment to delete.</span></span> <span data-ttu-id="e1846-147">要删除的一个或多个**AttachmentId**值后，调用[DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx)操作从邮件中删除指定的附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-147">After you have one or more **AttachmentId** values to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation to remove the specified attachments from the message.</span></span> 
  
<span data-ttu-id="e1846-148">下面的代码示例演示如何使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作获取邮件上的电子邮件和附件的集合。</span><span class="sxs-lookup"><span data-stu-id="e1846-148">The following code example shows how to use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to get an email message and the collection of attachments on the message.</span></span> <span data-ttu-id="e1846-149">这也是使用 EWS 托管 API 到[删除电子邮件中的所有附件](#bk_deleteattachewsma)时，将发送 EWS 托管 API 的第一个 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e1846-149">This is also the first XML request that the EWS Managed API sends when you use the EWS Managed API to [delete all attachments from an email](#bk_deleteattachewsma).</span></span> <span data-ttu-id="e1846-150">为便于阅读缩短某些属性的值。</span><span class="sxs-lookup"><span data-stu-id="e1846-150">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e1846-151">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功检索电子邮件， [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值和[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)值现有的附件。</span><span class="sxs-lookup"><span data-stu-id="e1846-151">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was retrieved successfully, and the [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) values of the existing attachments.</span></span> 
  
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
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
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

<span data-ttu-id="e1846-152">后确定哪些附件删除、 呼叫[DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx)操作，并包含要删除的附件的**AttachmentId**值。</span><span class="sxs-lookup"><span data-stu-id="e1846-152">After you determine which attachment to delete, call the [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) operation and include the **AttachmentId** values of the attachments to delete.</span></span> 
  
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
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

服务器响应**DeleteAttachment**请求[DeleteAttachmentResponse](http://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx)消息的每个[DeleteAttachmentResponseMessage](http://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx)，这表示包含**NoError** [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)值已成功删除每个附件。 <span data-ttu-id="e1846-154">为便于阅读缩短某些属性的值。</span><span class="sxs-lookup"><span data-stu-id="e1846-154">The values of some attributes are shortened for readability.</span></span>
  
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
    <m:DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="e1846-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e1846-155">See also</span></span>


- [<span data-ttu-id="e1846-156">附件和 EWS Exchange 中</span><span class="sxs-lookup"><span data-stu-id="e1846-156">Attachments and EWS in Exchange</span></span>](attachments-and-ews-in-exchange.md)
    
- [<span data-ttu-id="e1846-157">在 Exchange 使用 EWS 添加附件</span><span class="sxs-lookup"><span data-stu-id="e1846-157">Add attachments by using EWS in Exchange</span></span>](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e1846-158">使用 EWS 在 Exchange 服务器获取附件</span><span class="sxs-lookup"><span data-stu-id="e1846-158">Get attachments by using EWS in Exchange</span></span>](how-to-get-attachments-by-using-ews-in-exchange.md)
    

