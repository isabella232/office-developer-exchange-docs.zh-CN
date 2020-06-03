---
title: 在 Exchange 中使用 EWS 作为代理访问日历
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来以委派方式访问日历。
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528291"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="dc2b6-103">在 Exchange 中使用 EWS 作为代理访问日历</span><span class="sxs-lookup"><span data-stu-id="dc2b6-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="dc2b6-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来以委派方式访问日历。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="dc2b6-105">您可以使用 EWS 托管 API 或 EWS 为用户委派对邮箱所有者的日历文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="dc2b6-106">然后，代理可以代表邮箱所有者创建会议请求、创建约会、响应会议请求以及检索、更新和删除邮箱所有者的 "日历" 文件夹中的会议，具体取决于他们的权限。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="dc2b6-107">作为代理，您可以使用相同的方法和操作来访问邮箱所有者的 "日历" 文件夹，以便访问自己的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="dc2b6-108">主要区别在于，必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)来查找或创建日历项目或日历子文件夹，然后在确定项目 id 或文件夹 id 之后，可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="dc2b6-109">**表1。用于将日历作为代理访问的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="dc2b6-110">**如果您想要 .。。**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-110">**If you want to…**</span></span>|<span data-ttu-id="dc2b6-111">**使用此 EWS 托管 API 方法 .。。**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="dc2b6-112">**使用此 EWS 操作 .。。**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc2b6-113">以代理人的形式创建会议或约会</span><span class="sxs-lookup"><span data-stu-id="dc2b6-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="dc2b6-114">在[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的情况下[保存。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-114">[Appointment.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="dc2b6-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="dc2b6-116">将多个会议或约会创建为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="dc2b6-117">**FolderId**参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[CreateItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="dc2b6-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="dc2b6-119">搜索或查找作为代理的约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="dc2b6-120">**FolderId**参数提供对邮箱所有者的 "日历" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[FindItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-120">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="dc2b6-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="dc2b6-122">将约会或会议作为代理获取</span><span class="sxs-lookup"><span data-stu-id="dc2b6-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="dc2b6-123">约会. 绑定</span><span class="sxs-lookup"><span data-stu-id="dc2b6-123">Appointment.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="dc2b6-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="dc2b6-124">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="dc2b6-125">将约会或会议更新为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="dc2b6-126">接[下来是约会](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) [。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-126">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="dc2b6-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="dc2b6-128">将约会或会议作为代理删除</span><span class="sxs-lookup"><span data-stu-id="dc2b6-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="dc2b6-129">接下来为 "约会" 的 "先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)"。[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-129">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="dc2b6-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="dc2b6-131">在本文的代码示例中，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="dc2b6-132">先决条件任务</span><span class="sxs-lookup"><span data-stu-id="dc2b6-132">Prerequisite tasks</span></span>
<span data-ttu-id="dc2b6-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-133"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="dc2b6-134">在用户可以将邮箱所有者的日历文件夹作为代理访问之前，必须将该用户[添加为具有](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的 "日历" 文件夹权限的代理。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="dc2b6-135">代理必须将邮箱附加到其帐户，才能更新邮箱所有者的日历。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="dc2b6-136">如果代理只需要处理会议请求和响应，则可以将该代理添加到 "日历" 文件夹中，并使用默认的[MeetingRequestsDeliveryScope "DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS 托管 API 枚举值" 或 " [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) ews 元素值**DelegatesAndSendInformationToMe** " 将请求发送给邮箱所有者，并将信息消息发送给邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="dc2b6-137">然后，无需授予代理对邮箱所有者的收件箱文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="dc2b6-138">使用 EWS 托管 API 将会议或约会创建为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="dc2b6-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-139"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="dc2b6-140">使用 EWS 托管 API，您可以使用代理用户的服务对象为邮箱所有者创建日历项目。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="dc2b6-141">本示例演示如何使用[Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="dc2b6-142">本示例假定**服务**是代理的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且已为委派授予对邮箱所有者的 "日历" 文件夹的适当权限。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

<span data-ttu-id="dc2b6-143">请注意，保存项目时， [save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法调用必须标识邮箱所有者的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="dc2b6-144">如果未指定邮箱所有者的 "日历" 文件夹，则会将会议请求保存到代理的日历中，而不是邮箱所有者的 "日历" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="dc2b6-145">您可以通过两种方式将邮箱所有者的 "日历" 文件夹包含在**Save**方法调用中。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="dc2b6-146">建议使用[WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)和邮箱所有者的 SMTP 地址实例化[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="dc2b6-147">不过，您还可以先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)到 "日历" 文件夹，然后在**Save**方法调用中使用该文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="dc2b6-148">但请注意，这会导致额外的 EWS 调用。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="dc2b6-149">使用 EWS 创建会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="dc2b6-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-150"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="dc2b6-151">EWS 使您可以使用委派用户的服务对象为邮箱所有者创建日历项目。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="dc2b6-152">本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="dc2b6-153">这也是当您使用**Save**方法以[代理的形式创建会议或约会](#bk_createewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="dc2b6-154">为简洁起见，已从以下示例中删除了 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="dc2b6-155">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功创建会议。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-155">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="dc2b6-156">该响应还包含新创建的会议的项目 ID。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="dc2b6-157">使用 EWS 托管 API 将会议或约会搜索为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="dc2b6-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-158"><a name="bk_searchewsma"> </a></span></span>

<span data-ttu-id="dc2b6-159">若要搜索会议，必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法之一，以便您可以指定邮箱所有者的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="dc2b6-160">在**FindItems**调用返回带有 ID 的响应之后，您可以使用 id 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该会议，而无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="dc2b6-161">使用 EWS 作为代理人搜索会议或约会</span><span class="sxs-lookup"><span data-stu-id="dc2b6-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="dc2b6-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-162"><a name="bk_searchews"> </a></span></span>

<span data-ttu-id="dc2b6-163">通过 EWS，您可以使用代理用户的服务对象来搜索符合一组搜索条件的约会和会议。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="dc2b6-164">本示例演示如何使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作在邮箱所有者的 "日历" 文件夹中查找包含主题中包含 "建筑物" 一词的会议。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-164">This example shows how to use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="dc2b6-165">这也是当您使用**FindItem**方法将[会议或约会作为代理搜索](#bk_searchewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
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
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="dc2b6-166">服务器使用[FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)邮件响应**FindItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功完成搜索。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-166">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="dc2b6-167">响应包含符合搜索条件的任何约会或会议的[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-167">The response contains a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="dc2b6-168">在这种情况下，仅找到一个会议。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="dc2b6-169">为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-169">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
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
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="dc2b6-170">现在，您已拥有满足**条件的符合**条件，您可以使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该会议，而无需指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="dc2b6-171">使用 EWS 托管 API 获取、更新或删除日历项目为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="dc2b6-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-172"><a name="bk_geteswma"> </a></span></span>

<span data-ttu-id="dc2b6-173">您可以使用 EWS 托管 API 来获取、更新或删除会议或约会，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="dc2b6-174">唯一的区别是，服务对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="dc2b6-175">**Bind**方法调用中包含的项目 ID 在邮箱所有者的 "日历" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="dc2b6-176">**表2。用于将约会和会议作为代理使用的 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="dc2b6-177">**任务**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-177">**Task**</span></span>|<span data-ttu-id="dc2b6-178">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-178">**EWS Managed API method**</span></span>|<span data-ttu-id="dc2b6-179">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc2b6-180">获取约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="dc2b6-181">绑定</span><span class="sxs-lookup"><span data-stu-id="dc2b6-181">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="dc2b6-182">使用 EWS 托管 API 获取项</span><span class="sxs-lookup"><span data-stu-id="dc2b6-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="dc2b6-183">更新约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="dc2b6-184">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="dc2b6-185">使用 EWS 托管 API 更新会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="dc2b6-186">删除约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="dc2b6-187">先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)后接[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="dc2b6-188">使用 EWS 托管 API 删除会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="dc2b6-189">使用 EWS 获取、更新或删除日历项目作为代理人</span><span class="sxs-lookup"><span data-stu-id="dc2b6-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="dc2b6-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="dc2b6-190"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="dc2b6-191">您可以使用 EWS 获取、更新或删除会议或约会，方式与您在不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="dc2b6-192">唯一的区别是，服务对象是代表委派用户的。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="dc2b6-193">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)方法调用中包含的项目 ID 在邮箱所有者的 "日历" 文件夹中唯一标识邮箱存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="dc2b6-193">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="dc2b6-194">**表3。将约会和会议作为代理使用的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="dc2b6-195">**任务**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-195">**Task**</span></span>|<span data-ttu-id="dc2b6-196">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-196">**EWS operation**</span></span>|<span data-ttu-id="dc2b6-197">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="dc2b6-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc2b6-198">获取约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="dc2b6-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="dc2b6-199">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="dc2b6-200">使用 EWS 获取项</span><span class="sxs-lookup"><span data-stu-id="dc2b6-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="dc2b6-201">更新约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="dc2b6-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="dc2b6-203">使用 EWS 更新会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="dc2b6-204">删除约会或会议</span><span class="sxs-lookup"><span data-stu-id="dc2b6-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="dc2b6-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="dc2b6-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc2b6-206">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc2b6-206">See also</span></span>

- [<span data-ttu-id="dc2b6-207">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="dc2b6-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="dc2b6-208">使用 Exchange 中的 EWS 添加和删除委派</span><span class="sxs-lookup"><span data-stu-id="dc2b6-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="dc2b6-209">使用 Exchange 中的 EWS 为另一个用户设置文件夹权限</span><span class="sxs-lookup"><span data-stu-id="dc2b6-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="dc2b6-210">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc2b6-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

