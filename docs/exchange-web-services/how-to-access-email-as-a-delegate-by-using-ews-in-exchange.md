---
title: 作为 Exchange 中使用 EWS 代理人的访问电子邮件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: 了解如何在 Exchange 使用 EWS 托管 API 或 EWS 作为代理人访问电子邮件。
ms.openlocfilehash: 8331f337136426913347cf6941d64b4611922d74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752740"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="80047-103">作为 Exchange 中使用 EWS 代理人的访问电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-103">Access email as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="80047-104">了解如何在 Exchange 使用 EWS 托管 API 或 EWS 作为代理人访问电子邮件。</span><span class="sxs-lookup"><span data-stu-id="80047-104">Learn how to access email as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="80047-105">您可以使用 EWS 托管 API 或 EWS 来使用户委派访问邮箱所有者的收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="80047-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Inbox folder.</span></span> <span data-ttu-id="80047-106">代理人可以然后创建会议请求代表邮箱所有者、 电子邮件、 搜索和检索、 更新和删除电子邮件从邮箱所有者的收件箱文件夹中，根据其权限。</span><span class="sxs-lookup"><span data-stu-id="80047-106">The delegate can then create meeting requests on behalf of the mailbox owner, search for email, and retrieve, update, and delete email from the mailbox owner's Inbox folder, depending on their permissions.</span></span>
  
<span data-ttu-id="80047-107">作为代理人，您使用相同的方法和操作访问邮箱所有者的收件箱文件夹用于访问没有委派访问权限收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="80047-107">As a delegate, you use the same methods and operations to access a mailbox owner's Inbox folder that you use to access an Inbox folder without delegate access.</span></span> <span data-ttu-id="80047-108">主要区别是，您必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)查找或创建电子邮件项目，，然后确定项目 ID 后，您可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)以获取、 更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="80047-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create an email item, and then after you identify the item ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="80047-109">**表 1。EWS 托管 API 方法和用于访问作为代理人的电子邮件的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="80047-109">**Table 1. EWS Managed API methods and EWS operations for accessing email as a delegate**</span></span>

|<span data-ttu-id="80047-110">**如果您希望...**</span><span class="sxs-lookup"><span data-stu-id="80047-110">**If you want to…**</span></span>|<span data-ttu-id="80047-111">**使用此 EWS 托管 API 方法...**</span><span class="sxs-lookup"><span data-stu-id="80047-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="80047-112">**使用此 EWS 操作...**</span><span class="sxs-lookup"><span data-stu-id="80047-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80047-113">创建和发送电子邮件作为代理人</span><span class="sxs-lookup"><span data-stu-id="80047-113">Create and send an email as a delegate</span></span>  <br/> |<span data-ttu-id="80047-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx)其中的[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的草稿文件夹</span><span class="sxs-lookup"><span data-stu-id="80047-114">[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder</span></span>  <br/> <span data-ttu-id="80047-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx)其中的[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的已发送邮件文件夹</span><span class="sxs-lookup"><span data-stu-id="80047-115">[EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Sent Items folder</span></span>  <br/> |<span data-ttu-id="80047-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-116">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> <span data-ttu-id="80047-117">[SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-117">[SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="80047-118">作为代理人创建多个电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-118">Create multiple email messages as a delegate</span></span>  <br/> |<span data-ttu-id="80047-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)其中的**文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的收件箱文件夹</span><span class="sxs-lookup"><span data-stu-id="80047-119">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="80047-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-120">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="80047-121">搜索或查找作为代理人电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-121">Search for or find an email as a delegate</span></span>  <br/> |<span data-ttu-id="80047-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)其中的**文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的收件箱文件夹</span><span class="sxs-lookup"><span data-stu-id="80047-122">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Inbox folder</span></span>  <br/> |<span data-ttu-id="80047-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-123">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="80047-124">作为代理人获取电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-124">Get an email as a delegate</span></span>  <br/> |[<span data-ttu-id="80047-125">EmailMessage.Bind</span><span class="sxs-lookup"><span data-stu-id="80047-125">EmailMessage.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="80047-126">GetItem</span><span class="sxs-lookup"><span data-stu-id="80047-126">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="80047-127">作为代理人更新电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-127">Update an email as a delegate</span></span>  <br/> |<span data-ttu-id="80047-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)跟[EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-128">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="80047-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-129">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="80047-130">删除作为代理人的电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-130">Delete an email as a delegate</span></span>  <br/> |<span data-ttu-id="80047-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)跟[EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-131">[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="80047-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-132">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
<span data-ttu-id="80047-133">作为代理人使用电子邮件时，请注意以下几点：</span><span class="sxs-lookup"><span data-stu-id="80047-133">Keep the following things in mind when working with emails as a delegate:</span></span>
  
- <span data-ttu-id="80047-134">如果代理人只需要处理会议请求和响应，该委托不需要对收件箱文件夹的访问。</span><span class="sxs-lookup"><span data-stu-id="80047-134">If a delegate only needs to work with meeting requests and responses, the delegate does not need access to the Inbox folder.</span></span> <span data-ttu-id="80047-135">有关详细信息，请参阅[用于访问日历作为代理人的必备组件 tasks](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)。</span><span class="sxs-lookup"><span data-stu-id="80047-135">For more information, see [prerequisite tasks for accessing calendars as a delegate](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).</span></span>
    
- <span data-ttu-id="80047-136">当收件人收到一条消息，代表邮箱所有者发送时，发件人显示为"*委托*代表*邮箱所有者*。"</span><span class="sxs-lookup"><span data-stu-id="80047-136">When a recipient receives a message that was sent on behalf of a mailbox owner, the sender appears as " *Delegate*  on behalf of  *mailbox owner*  ."</span></span> 
    
> [!NOTE]
> <span data-ttu-id="80047-137">在本文中的代码示例，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="80047-137">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="80047-138">必备组件的任务</span><span class="sxs-lookup"><span data-stu-id="80047-138">Prerequisite tasks</span></span>
<span data-ttu-id="80047-139"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-139"></span></span>

<span data-ttu-id="80047-140">用户可以访问邮箱所有者的收件箱文件夹作为代理人之前，用户必须对邮箱所有者的收件箱文件夹[添加为具有权限代理](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="80047-140">Before a user can access the mailbox owner's Inbox folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="80047-141">创建和发送电子邮件作为代理人使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="80047-141">Create and send an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="80047-142"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-142"></span></span>

<span data-ttu-id="80047-143">EWS 托管 API 可使用的代理用户的服务对象创建并发送代表邮箱所有者的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="80047-143">The EWS Managed API enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="80047-144">本示例演示如何使用[Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx)方法可以将邮件保存在邮箱所有者的草稿文件夹，然后将邮件发送和邮箱所有者的已发送邮件文件夹中保存邮件的[SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="80047-144">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) method to save the message in the mailbox owner's Drafts folder, and then the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) method to send the mail and save the message in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="80047-145">此示例假定该**服务**的代理是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和委托已被授予[对邮箱所有者的收件箱、 草稿和已发送邮件文件夹的相应权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="80047-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the [appropriate permissions for the mailbox owner's Inbox, Drafts, and Sent Items folder](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).</span></span>
  
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

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="80047-146">创建和使用 EWS 作为代理人发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-146">Create and send an email as a delegate by using EWS</span></span>
<span data-ttu-id="80047-147"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-147"></span></span>

<span data-ttu-id="80047-148">EWS 使您可以使用的代理用户的服务对象来创建并发送代表邮箱所有者的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="80047-148">EWS enables you to use the service object for the delegate user to create and send email on behalf of the mailbox owner.</span></span> <span data-ttu-id="80047-149">本示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建电子邮件和[SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作发送时间，并将其保存邮箱所有者的已发送邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="80047-149">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create an email and the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the time and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="80047-150">这也是使用**Save**方法[创建](#bk_createewsma)和发送电子邮件时，将发送 EWS 托管 API 的第一个 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="80047-150">This is also the first XML request that the EWS Managed API sends when you use the **Save** method to [create and send an email](#bk_createewsma).</span></span>
  
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

<span data-ttu-id="80047-151">服务器响应包含**NoError**，这表明已创建电子邮件，并已将其成功保存[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="80047-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was created and saved successfully.</span></span> <span data-ttu-id="80047-152">响应还包含新创建的电子邮件的项 ID。</span><span class="sxs-lookup"><span data-stu-id="80047-152">The response also contains the item ID of the newly created email.</span></span>
  
<span data-ttu-id="80047-153">为便于阅读缩短了**ItemId**值。</span><span class="sxs-lookup"><span data-stu-id="80047-153">The **ItemId** value has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="80047-154">接下来，使用**SendItem**操作发送代表邮箱所有者消息，并将其保存邮箱所有者的已发送邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="80047-154">Next, use the **SendItem** operation to send the message on behalf of the mailbox owner and save it in the mailbox owner's Sent Items folder.</span></span> 
  
<span data-ttu-id="80047-155">为便于阅读缩短了**ItemId**值。</span><span class="sxs-lookup"><span data-stu-id="80047-155">The **ItemId** value has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="80047-156">服务器响应[SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)消息，其中包括**NoError**，这表明该电子邮件已发送和保存到邮箱所有者的已发送邮件文件夹[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值与**SendItem**请求成功。</span><span class="sxs-lookup"><span data-stu-id="80047-156">The server responds to the **SendItem** request with a [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the email was sent and saved to the mailbox owner's Sent Items folder successfully.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="80047-157">使用 EWS 托管 API 作为代理人搜索的电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-157">Search for an email as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="80047-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-158"></span></span>

<span data-ttu-id="80047-159">若要搜索电子邮件，您必须以便您可以指定邮箱所有者的收件箱文件夹使用[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法，其中包括[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数之一。</span><span class="sxs-lookup"><span data-stu-id="80047-159">To search for an email, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Inbox folder.</span></span> 
  
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

<span data-ttu-id="80047-160">**FindItems**呼叫将返回一个响应 id 后，您可以获取更新或删除的电子邮件使用 ID 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)-和您不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="80047-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that email by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a><span data-ttu-id="80047-161">使用 EWS 作为代理人搜索的电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-161">Search for an email as a delegate by using EWS</span></span>
<span data-ttu-id="80047-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-162"></span></span>

<span data-ttu-id="80047-163">EWS，可以使用的代理用户的服务对象的电子邮件符合搜索条件的一组搜索。</span><span class="sxs-lookup"><span data-stu-id="80047-163">EWS enables you to use the service object for the delegate user to search for emails that meet a set of search criteria.</span></span> <span data-ttu-id="80047-164">本示例演示如何使用[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作包含单词"足球"主题中的所有者的收件箱文件夹中找到邮件。</span><span class="sxs-lookup"><span data-stu-id="80047-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find messages in the owner's Inbox folder that contain the word "soccer" in the subject.</span></span> 
  
<span data-ttu-id="80047-165">这也是 XML 请求 EWS 托管 API 发送时[搜索电子邮件](#bk_searchewsma)。</span><span class="sxs-lookup"><span data-stu-id="80047-165">This is also the XML request that the EWS Managed API sends when you [search for an email](#bk_searchewsma).</span></span>
  
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

<span data-ttu-id="80047-166">服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，指示已成功完成搜索的[FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)消息的**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="80047-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="80047-167">则响应中包含的任何电子邮件符合搜索条件的[消息](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="80047-167">The response contains a [Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) element for any emails that met the search criteria.</span></span> <span data-ttu-id="80047-168">在这种情况下，找到只有一个电子邮件。</span><span class="sxs-lookup"><span data-stu-id="80047-168">In this case, only one email is found.</span></span> 
  
<span data-ttu-id="80047-169">为便于阅读缩短了[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="80047-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="80047-170">既然您已经**ItemId**电子邮件符合您的条件，您可以获取更新或使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)-和您的电子邮件的删除不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="80047-170">Now that you have the **ItemId** for the email that meets your criteria, you can get, update, or delete that email by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) - and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="80047-171">获取、 更新或删除电子邮件项作为代理人使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="80047-171">Get, update, or delete email items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="80047-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-172"></span></span>

<span data-ttu-id="80047-173">EWS 托管 API 可用于获取、 更新或删除电子邮件中时您不使用代理访问执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="80047-173">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="80047-174">唯一的区别是**ExchangeService**对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="80047-174">The only difference is that the **ExchangeService** object is for the delegate user.</span></span> <span data-ttu-id="80047-175">唯一的**绑定**方法调用中包含的项 ID 标识邮箱所有者的收件箱文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="80047-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="80047-176">**表 2。EWS 托管 API 方法处理作为代理人的电子邮件**</span><span class="sxs-lookup"><span data-stu-id="80047-176">**Table 2. EWS Managed API methods working with email as a delegate**</span></span>

|<span data-ttu-id="80047-177">**任务**</span><span class="sxs-lookup"><span data-stu-id="80047-177">**Task**</span></span>|<span data-ttu-id="80047-178">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="80047-178">**EWS Managed API method**</span></span>|<span data-ttu-id="80047-179">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="80047-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80047-180">获取电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-180">Get an email</span></span>  <br/> |[<span data-ttu-id="80047-181">绑定</span><span class="sxs-lookup"><span data-stu-id="80047-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="80047-182">使用 EWS 托管 API 中获取项</span><span class="sxs-lookup"><span data-stu-id="80047-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="80047-183">更新电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-183">Update an email</span></span>  <br/> |<span data-ttu-id="80047-184">[更新](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="80047-185">使用 EWS 托管 API 更新的项</span><span class="sxs-lookup"><span data-stu-id="80047-185">Update an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|<span data-ttu-id="80047-186">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-186">Delete an email</span></span>  <br/> |<span data-ttu-id="80047-187">[删除](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="80047-188">通过使用 EWS 托管 API 中删除项目</span><span class="sxs-lookup"><span data-stu-id="80047-188">Delete an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="80047-189">获取、 更新或删除作为代理人使用 EWS 的电子邮件项目</span><span class="sxs-lookup"><span data-stu-id="80047-189">Get, update, or delete email items as a delegate by using EWS</span></span>
<span data-ttu-id="80047-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="80047-190"></span></span>

<span data-ttu-id="80047-191">EWS 托管 API 可用于获取、 更新或删除电子邮件中时您不使用代理访问执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="80047-191">You can use the EWS Managed API to get, update, or delete an email in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="80047-192">唯一的区别是服务对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="80047-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="80047-193">唯一**GetItem**请求中包含的项 ID 标识邮箱所有者的收件箱文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="80047-193">The item ID included in the **GetItem** request uniquely identifies the item in the mailbox store, in the mailbox owner's Inbox folder.</span></span> 
  
<span data-ttu-id="80047-194">**表 3。作为代理人的电子邮件使用 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="80047-194">**Table 3. EWS operations for working with email as a delegate**</span></span>

|<span data-ttu-id="80047-195">**任务**</span><span class="sxs-lookup"><span data-stu-id="80047-195">**Task**</span></span>|<span data-ttu-id="80047-196">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="80047-196">**EWS operation**</span></span>|<span data-ttu-id="80047-197">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="80047-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80047-198">获取电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-198">Get an email</span></span>  <br/> |[<span data-ttu-id="80047-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="80047-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="80047-200">使用 EWS 获取项目</span><span class="sxs-lookup"><span data-stu-id="80047-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="80047-201">更新电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-201">Update an email</span></span>  <br/> |<span data-ttu-id="80047-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="80047-203">使用 EWS 更新的项</span><span class="sxs-lookup"><span data-stu-id="80047-203">Update an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|<span data-ttu-id="80047-204">删除电子邮件</span><span class="sxs-lookup"><span data-stu-id="80047-204">Delete an email</span></span>  <br/> |<span data-ttu-id="80047-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="80047-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="80047-206">通过使用 EWS 中删除项目</span><span class="sxs-lookup"><span data-stu-id="80047-206">Delete an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80047-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80047-207">See also</span></span>

- [<span data-ttu-id="80047-208">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="80047-208">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)    
- [<span data-ttu-id="80047-209">添加和删除代理人，在 Exchange 使用 EWS</span><span class="sxs-lookup"><span data-stu-id="80047-209">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="80047-210">在 Exchange 使用 EWS 设置另一个用户的文件夹权限</span><span class="sxs-lookup"><span data-stu-id="80047-210">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="80047-211">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="80047-211">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

