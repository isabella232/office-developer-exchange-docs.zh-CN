---
title: 在 Exchange 中使用 EWS 以代理的形式访问电子邮件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，将电子邮件作为代理访问。
ms.openlocfilehash: 0c26f69042c568fe7d877778c7d8f1e689e5b372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528284"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="02f00-103">在 Exchange 中使用 EWS 以代理的形式访问电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-103">Access email as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="02f00-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，将电子邮件作为代理访问。</span><span class="sxs-lookup"><span data-stu-id="02f00-104">Learn how to access email as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="02f00-105">您可以使用 EWS 托管 API 或 EWS 为用户委派对邮箱所有者的 "收件箱" 文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="02f00-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Inbox folder.</span></span> <span data-ttu-id="02f00-106">然后，代理可以代表邮箱所有者创建会议请求、搜索电子邮件、检索、更新和删除邮箱所有者的 "收件箱" 文件夹中的电子邮件，具体取决于他们的权限。</span><span class="sxs-lookup"><span data-stu-id="02f00-106">The delegate can then create meeting requests on behalf of the mailbox owner, search for email, and retrieve, update, and delete email from the mailbox owner's Inbox folder, depending on their permissions.</span></span>
  
<span data-ttu-id="02f00-107">作为代理，您可以使用相同的方法和操作访问邮箱所有者的 "收件箱" 文件夹，而无需委派访问权限即可访问该文件夹。</span><span class="sxs-lookup"><span data-stu-id="02f00-107">As a delegate, you use the same methods and operations to access a mailbox owner's Inbox folder that you use to access an Inbox folder without delegate access.</span></span> <span data-ttu-id="02f00-108">主要区别在于，必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)来查找或创建电子邮件项目，然后在确定项目 ID 之后，可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="02f00-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create an email item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="02f00-109">**表1。用于将电子邮件作为代理访问的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="02f00-109">**Table 1. EWS Managed API methods and EWS operations for accessing email as a delegate**</span></span>

|<span data-ttu-id="02f00-110">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="02f00-110">**If you want to…**</span></span>|<span data-ttu-id="02f00-111">**使用此 EWS 托管 API 方法 .。。**</span><span class="sxs-lookup"><span data-stu-id="02f00-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="02f00-112">**使用此 EWS 操作 .。。**</span><span class="sxs-lookup"><span data-stu-id="02f00-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02f00-113">创建电子邮件并将其作为代理发送</span><span class="sxs-lookup"><span data-stu-id="02f00-113">Create and send an email as a delegate</span></span>  <br/> |<span data-ttu-id="02f00-114">[EmailMessage](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) ， [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "草稿" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)</span><span class="sxs-lookup"><span data-stu-id="02f00-114">[EmailMessage.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder</span></span>  <br/> <span data-ttu-id="02f00-115">[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "已发送邮件" 文件夹的[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[SendAndSaveCopy EmailMessage](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-115">[EmailMessage.SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Sent Items folder</span></span>  <br/> |<span data-ttu-id="02f00-116">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-116">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> <span data-ttu-id="02f00-117">[SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-117">[SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="02f00-118">创建多封电子邮件作为代理</span><span class="sxs-lookup"><span data-stu-id="02f00-118">Create multiple email messages as a delegate</span></span>  <br/> |<span data-ttu-id="02f00-119">**FolderId**参数提供对邮箱所有者的 "收件箱" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[CreateItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-119">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="02f00-120">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-120">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="02f00-121">搜索电子邮件或查找作为代理的电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-121">Search for or find an email as a delegate</span></span>  <br/> |<span data-ttu-id="02f00-122">**FolderId**参数提供对邮箱所有者的 "收件箱" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[FindItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-122">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="02f00-123">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-123">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="02f00-124">将电子邮件作为代理获取</span><span class="sxs-lookup"><span data-stu-id="02f00-124">Get an email as a delegate</span></span>  <br/> |[<span data-ttu-id="02f00-125">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="02f00-125">EmailMessage.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="02f00-126">GetItem</span><span class="sxs-lookup"><span data-stu-id="02f00-126">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="02f00-127">将电子邮件更新为代理</span><span class="sxs-lookup"><span data-stu-id="02f00-127">Update an email as a delegate</span></span>  <br/> |<span data-ttu-id="02f00-128">[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-128">[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="02f00-129">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-129">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="02f00-130">删除作为代理的电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-130">Delete an email as a delegate</span></span>  <br/> |<span data-ttu-id="02f00-131">[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-131">[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="02f00-132">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="02f00-132">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
<span data-ttu-id="02f00-133">在将电子邮件作为代理人处理时，请记住以下事项：</span><span class="sxs-lookup"><span data-stu-id="02f00-133">Keep the following things in mind when working with emails as a delegate:</span></span>
  
- <span data-ttu-id="02f00-134">如果代理只需要处理会议请求和响应，则代理不需要对 "收件箱" 文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="02f00-134">If a delegate only needs to work with meeting requests and responses, the delegate does not need access to the Inbox folder.</span></span> <span data-ttu-id="02f00-135">有关详细信息，请参阅以[委派方式访问日历的先决条件任务](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)。</span><span class="sxs-lookup"><span data-stu-id="02f00-135">For more information, see [prerequisite tasks for accessing calendars as a delegate](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span></span>
    
- <span data-ttu-id="02f00-136">当收件人收到代表邮箱所有者发送的邮件时，发件人将显示为 "代表*邮箱所有者\*\*委派*"。</span><span class="sxs-lookup"><span data-stu-id="02f00-136">When a recipient receives a message that was sent on behalf of a mailbox owner, the sender appears as " *Delegate*  on behalf of  *mailbox owner*  ."</span></span> 
    
> [!NOTE]
> <span data-ttu-id="02f00-137">在本文的代码示例中，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="02f00-137">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="02f00-138">先决条件任务</span><span class="sxs-lookup"><span data-stu-id="02f00-138">Prerequisite tasks</span></span>
<span data-ttu-id="02f00-139"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-139"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="02f00-140">在用户将邮箱所有者的 "收件箱" 文件夹作为代理进行访问之前，必须将该用户[添加为具有](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的 "收件箱" 文件夹权限的代理。</span><span class="sxs-lookup"><span data-stu-id="02f00-140">Before a user can access the mailbox owner's Inbox folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="02f00-141">使用 EWS 托管 API 创建电子邮件并将其作为代理发送</span><span class="sxs-lookup"><span data-stu-id="02f00-141">Create and send an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="02f00-142"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-142"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="02f00-143">使用 EWS 托管 API，您可以使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-143">The EWS Managed API enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="02f00-144">本示例演示如何使用[save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx)方法将邮件保存到邮箱所有者的 "草稿" 文件夹中，然后使用[SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx)方法将邮件保存到邮箱所有者的 "已发送邮件" 文件夹中，并将其保存到邮箱所有者的 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="02f00-144">This example shows how to use the [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) method to save the message in the mailbox owner's Drafts folder, and then the [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) method to send the mail and save the message in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="02f00-145">本示例假定**服务**是代理的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且已为委派授予对[邮箱所有者的 "收件箱"、"草稿" 和 "已发送邮件" 文件夹的适当权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="02f00-145">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the [appropriate permissions for the mailbox owner's Inbox, Drafts, and Sent Items folder](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="02f00-146">使用 EWS 创建电子邮件并将其作为代理发送</span><span class="sxs-lookup"><span data-stu-id="02f00-146">Create and send an email as a delegate by using EWS</span></span>
<span data-ttu-id="02f00-147"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-147"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="02f00-148">EWS 使您可以使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-148">EWS enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="02f00-149">本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建电子邮件和[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作，以发送时间并将其保存在邮箱所有者的 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="02f00-149">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an email and the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the time and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="02f00-150">这也是在使用**Save**方法[创建和发送电子邮件](#bk_createewsma)时，EWS 托管 API 发送的第一个 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="02f00-150">This is also the first XML request that the EWS Managed API sends when you use the **Save** method to [create and send an email](#bk_createewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
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

<span data-ttu-id="02f00-151">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功创建并保存了该电子邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-151">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was created and saved successfully.</span></span> <span data-ttu-id="02f00-152">该响应还包含新创建的电子邮件的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="02f00-152">The response also contains the item ID of the newly created email.</span></span>
  
<span data-ttu-id="02f00-153">为了提高可读性， **ItemId**值已缩短。</span><span class="sxs-lookup"><span data-stu-id="02f00-153">The **ItemId** value has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="02f00-154">接下来，使用**SendItem**操作代表邮箱所有者发送邮件，并将其保存在邮箱所有者的 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="02f00-154">Next, use the **SendItem** operation to send the message on behalf of the mailbox owner and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="02f00-155">为了提高可读性， **ItemId**值已缩短。</span><span class="sxs-lookup"><span data-stu-id="02f00-155">The **ItemId** value has been shortened for readability.</span></span> 
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="02f00-156">服务器使用[SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)邮件响应**SendItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示电子邮件已成功发送并保存到邮箱所有者的 "已发送邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="02f00-156">The server responds to the **SendItem** request with a [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was sent and saved to the mailbox owner's Sent Items folder successfully.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="02f00-157">使用 EWS 托管 API 搜索作为代理的电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-157">Search for an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="02f00-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-158"><a name="bk_searchewsma"> </a></span></span>

<span data-ttu-id="02f00-159">若要搜索电子邮件，您必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的 FindItems 方法之一，以便您可以指定邮箱所有者的 "收件箱" 文件夹[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="02f00-159">To search for an email, you must use one of the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Inbox folder.</span></span> 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="02f00-160">在**FindItems**调用返回带有 ID 的响应后，您可以使用 id 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该电子邮件，而无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="02f00-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that email by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="02f00-161">使用 EWS 搜索作为代理的电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-161">Search for an email as a delegate by using EWS</span></span>
<span data-ttu-id="02f00-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-162"><a name="bk_searchews"> </a></span></span>

<span data-ttu-id="02f00-163">通过 EWS，您可以使用代理用户的服务对象搜索符合一组搜索条件的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-163">EWS enables you to use the service object for the delegate user to search for emails that meet a set of search criteria.</span></span> <span data-ttu-id="02f00-164">本示例演示如何使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作查找所有者的 "收件箱" 文件夹中包含主题中包含 "足球" 一词的邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-164">This example shows how to use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find messages in the owner's Inbox folder that contain the word "soccer" in the subject.</span></span> 
  
<span data-ttu-id="02f00-165">这也是在[搜索电子邮件](#bk_searchewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="02f00-165">This is also the XML request that the EWS Managed API sends when you [search for an email](#bk_searchewsma).</span></span>
  
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
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="02f00-166">服务器使用[FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)邮件响应**FindItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功完成搜索。</span><span class="sxs-lookup"><span data-stu-id="02f00-166">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="02f00-167">响应包含符合搜索条件的任何电子邮件的[Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="02f00-167">The response contains a [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element for any emails that met the search criteria.</span></span> <span data-ttu-id="02f00-168">在这种情况下，仅找到一个电子邮件。</span><span class="sxs-lookup"><span data-stu-id="02f00-168">In this case, only one email is found.</span></span> 
  
<span data-ttu-id="02f00-169">为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="02f00-169">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="02f00-170">现在您已拥有满足条件的电子邮件的**ItemId** ，您可以通过使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该电子邮件，而无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="02f00-170">Now that you have the **ItemId** for the email that meets your criteria, you can get, update, or delete that email by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="02f00-171">使用 EWS 托管 API 获取、更新或删除作为委派的电子邮件项目</span><span class="sxs-lookup"><span data-stu-id="02f00-171">Get, update, or delete email items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="02f00-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-172"><a name="bk_geteswma"> </a></span></span>

<span data-ttu-id="02f00-173">您可以使用 EWS 托管 API 来获取、更新或删除电子邮件，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="02f00-173">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="02f00-174">唯一的区别是**ExchangeService**对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="02f00-174">The only difference is that the **ExchangeService** object is for the delegate user.</span></span> <span data-ttu-id="02f00-175">**Bind**方法调用中包含的项目 ID 在邮箱所有者的 "收件箱" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="02f00-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="02f00-176">**表2。将电子邮件作为代理使用的 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="02f00-176">**Table 2. EWS Managed API methods working with email as a delegate**</span></span>

|<span data-ttu-id="02f00-177">**任务**</span><span class="sxs-lookup"><span data-stu-id="02f00-177">**Task**</span></span>|<span data-ttu-id="02f00-178">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="02f00-178">**EWS Managed API method**</span></span>|<span data-ttu-id="02f00-179">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="02f00-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02f00-180">获取电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-180">Get an email</span></span>  <br/> |[<span data-ttu-id="02f00-181">绑定</span><span class="sxs-lookup"><span data-stu-id="02f00-181">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="02f00-182">使用 EWS 托管 API 获取项</span><span class="sxs-lookup"><span data-stu-id="02f00-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="02f00-183">更新电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-183">Update an email</span></span>  <br/> |<span data-ttu-id="02f00-184">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="02f00-185">使用 EWS 托管 API 更新项</span><span class="sxs-lookup"><span data-stu-id="02f00-185">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="02f00-186">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-186">Delete an email</span></span>  <br/> |<span data-ttu-id="02f00-187">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="02f00-188">使用 EWS 托管 API 删除项</span><span class="sxs-lookup"><span data-stu-id="02f00-188">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="02f00-189">使用 EWS 获取、更新或删除作为代理的电子邮件项目</span><span class="sxs-lookup"><span data-stu-id="02f00-189">Get, update, or delete email items as a delegate by using EWS</span></span>
<span data-ttu-id="02f00-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="02f00-190"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="02f00-191">您可以使用 EWS 托管 API 来获取、更新或删除电子邮件，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="02f00-191">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="02f00-192">唯一的区别是，服务对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="02f00-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="02f00-193">**GetItem**请求中包含的项目 ID 在邮箱所有者的 "收件箱" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="02f00-193">The item ID included in the **GetItem** request uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="02f00-194">**表3。将电子邮件作为代理使用的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="02f00-194">**Table 3. EWS operations for working with email as a delegate**</span></span>

|<span data-ttu-id="02f00-195">**任务**</span><span class="sxs-lookup"><span data-stu-id="02f00-195">**Task**</span></span>|<span data-ttu-id="02f00-196">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="02f00-196">**EWS operation**</span></span>|<span data-ttu-id="02f00-197">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="02f00-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02f00-198">获取电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-198">Get an email</span></span>  <br/> |[<span data-ttu-id="02f00-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="02f00-199">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="02f00-200">使用 EWS 获取项</span><span class="sxs-lookup"><span data-stu-id="02f00-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="02f00-201">更新电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-201">Update an email</span></span>  <br/> |<span data-ttu-id="02f00-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02f00-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="02f00-203">使用 EWS 更新项</span><span class="sxs-lookup"><span data-stu-id="02f00-203">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="02f00-204">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="02f00-204">Delete an email</span></span>  <br/> |<span data-ttu-id="02f00-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="02f00-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[<span data-ttu-id="02f00-206">使用 EWS 删除项</span><span class="sxs-lookup"><span data-stu-id="02f00-206">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02f00-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="02f00-207">See also</span></span>

- [<span data-ttu-id="02f00-208">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="02f00-208">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)    
- [<span data-ttu-id="02f00-209">使用 Exchange 中的 EWS 添加和删除委派</span><span class="sxs-lookup"><span data-stu-id="02f00-209">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="02f00-210">使用 Exchange 中的 EWS 为另一个用户设置文件夹权限</span><span class="sxs-lookup"><span data-stu-id="02f00-210">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="02f00-211">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="02f00-211">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

