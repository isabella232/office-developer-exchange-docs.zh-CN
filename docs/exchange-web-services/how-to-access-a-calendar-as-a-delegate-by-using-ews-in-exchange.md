---
title: 在 Exchange 中使用 EWS 作为代理人访问日历
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: 了解如何通过在 Exchange 使用 EWS 托管 API 或 EWS 作为代理人访问日历。
ms.openlocfilehash: 24327c28f58e728807fc5581b480d3c01d3b7208
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752742"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="f98ca-103">在 Exchange 中使用 EWS 作为代理人访问日历</span><span class="sxs-lookup"><span data-stu-id="f98ca-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="f98ca-104">了解如何通过在 Exchange 使用 EWS 托管 API 或 EWS 作为代理人访问日历。</span><span class="sxs-lookup"><span data-stu-id="f98ca-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f98ca-105">您可以使用 EWS 托管 API 或 EWS 来使用户委派访问权限的邮箱所有者日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="f98ca-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f98ca-106">代理人可以然后创建会议请求代表邮箱所有者、 创建约会、 会议请求、 响应和检索、 更新和删除会议从邮箱所有者的日历文件夹中，根据其权限。</span><span class="sxs-lookup"><span data-stu-id="f98ca-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="f98ca-107">作为代理人，您使用相同的方法和操作访问邮箱所有者的日历文件夹的用于访问自己日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="f98ca-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="f98ca-108">主要区别是，您必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)查找或创建的日历项目或日历子文件夹，，然后确定项目 ID 或文件夹 ID 后，您可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)以获取、 更新或删除项目。</span><span class="sxs-lookup"><span data-stu-id="f98ca-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="f98ca-109">**表 1。EWS 托管 API 方法和用于访问日历作为代理人的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="f98ca-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="f98ca-110">**如果您希望...**</span><span class="sxs-lookup"><span data-stu-id="f98ca-110">**If you want to…**</span></span>|<span data-ttu-id="f98ca-111">**使用此 EWS 托管 API 方法...**</span><span class="sxs-lookup"><span data-stu-id="f98ca-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="f98ca-112">**使用此 EWS 操作...**</span><span class="sxs-lookup"><span data-stu-id="f98ca-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f98ca-113">创建会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="f98ca-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) [文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的日历文件夹的位置</span><span class="sxs-lookup"><span data-stu-id="f98ca-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f98ca-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f98ca-116">创建多个会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="f98ca-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) **文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的日历文件夹的位置</span><span class="sxs-lookup"><span data-stu-id="f98ca-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f98ca-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f98ca-119">搜索或查找约会或会议作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f98ca-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) **文件夹 Id**参数提供[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的日历文件夹的位置</span><span class="sxs-lookup"><span data-stu-id="f98ca-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="f98ca-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[电子邮件地址](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="f98ca-122">获取约会或会议作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="f98ca-123">Appointment.Bind</span><span class="sxs-lookup"><span data-stu-id="f98ca-123">Appointment.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f98ca-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="f98ca-124">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="f98ca-125">更新约会或会议作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f98ca-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)跟[Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f98ca-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="f98ca-128">删除约会或会议作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="f98ca-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)跟[Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="f98ca-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="f98ca-131">在本文中的代码示例，primary@contoso.com 是邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="f98ca-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="f98ca-132">必备组件的任务</span><span class="sxs-lookup"><span data-stu-id="f98ca-132">Prerequisite tasks</span></span>
<span data-ttu-id="f98ca-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-133"></span></span>

<span data-ttu-id="f98ca-134">用户可以访问邮箱所有者的日历文件夹作为代理人之前，用户必须对邮箱所有者的日历文件夹[添加为具有权限代理](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="f98ca-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f98ca-135">代理人必须具有附加到更新邮箱所有者的日历其帐户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="f98ca-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="f98ca-136">如果代理需要处理会议请求和响应，您可以将代理添加到日历文件夹中，并使用默认[MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS 托管 API 枚举值或[DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) **DelegatesAndSendInformationToMe**将请求发送到的代理人和信息性消息向邮箱所有者的 EWS 元素的值。</span><span class="sxs-lookup"><span data-stu-id="f98ca-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="f98ca-137">委托然后不必不授予对邮箱所有者的收件箱文件夹的访问。</span><span class="sxs-lookup"><span data-stu-id="f98ca-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f98ca-138">使用 EWS 托管 API 创建会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f98ca-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-139"></span></span>

<span data-ttu-id="f98ca-140">EWS 托管 API 可使用的代理用户的服务对象创建邮箱所有者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="f98ca-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="f98ca-141">本示例演示如何使用[Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="f98ca-141">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="f98ca-142">此示例假定该**服务**的代理是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和委托已被授予邮箱所有者的日历文件夹的相应权限。</span><span class="sxs-lookup"><span data-stu-id="f98ca-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="f98ca-143">注意当您保存项目时，[保存](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx)方法调用必须确定邮箱所有者的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="f98ca-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f98ca-144">如果未指定邮箱所有者的日历文件夹，则会议请求中获取保存到代理人的日历和不邮箱所有者的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="f98ca-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="f98ca-145">您可以通过两种方式中的**保存**方法调用中包含邮箱所有者的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="f98ca-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="f98ca-146">我们建议您通过使用[WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)和邮箱所有者的 SMTP 地址实例[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="f98ca-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="f98ca-147">但是，您还可以[将绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)到日历文件夹首先，然后使用**保存**方法调用中的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="f98ca-147">However, you can also [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="f98ca-148">请注意，但是，这将创建的额外的 EWS 调用。</span><span class="sxs-lookup"><span data-stu-id="f98ca-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
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

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="f98ca-149">使用 EWS 创建会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="f98ca-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-150"></span></span>

<span data-ttu-id="f98ca-151">EWS，可以使用的代理用户的服务对象创建邮箱所有者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="f98ca-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="f98ca-152">本示例演示如何使用[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建会议并向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="f98ca-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="f98ca-153">这也是 XML 请求 EWS 托管 API 发送时使用[创建会议或约会作为代理人](#bk_createewsma)**保存**方法。</span><span class="sxs-lookup"><span data-stu-id="f98ca-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="f98ca-154">从下面的示例为简便起见的 SOAP 标头已被删除。</span><span class="sxs-lookup"><span data-stu-id="f98ca-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="f98ca-155">服务器响应包含**NoError**，这表明已成功创建会议[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求。</span><span class="sxs-lookup"><span data-stu-id="f98ca-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="f98ca-156">响应还包含新创建的会议的项 ID。</span><span class="sxs-lookup"><span data-stu-id="f98ca-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f98ca-157">使用 EWS 托管 API 来搜索会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f98ca-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-158"></span></span>

<span data-ttu-id="f98ca-159">若要搜索的会议，您必须以便您可以指定邮箱所有者的日历文件夹使用[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法，其中包括[文件夹 Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数之一。</span><span class="sxs-lookup"><span data-stu-id="f98ca-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="f98ca-160">**FindItems**呼叫将返回一个响应 id 后，您可以获取、 更新或删除该会议使用 ID 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)— 并不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="f98ca-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="f98ca-161">使用 EWS 搜索会议或约会作为代理人</span><span class="sxs-lookup"><span data-stu-id="f98ca-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="f98ca-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-162"></span></span>

<span data-ttu-id="f98ca-163">EWS，可以使用的代理用户的服务对象搜索约会和会议符合搜索条件的一组。</span><span class="sxs-lookup"><span data-stu-id="f98ca-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="f98ca-164">本示例演示如何使用[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作包含单词"building"主题中的邮箱所有者的日历文件夹中找到的会议。</span><span class="sxs-lookup"><span data-stu-id="f98ca-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="f98ca-165">这也是 XML 请求 EWS 托管 API 发送时使用[的会议或约会作为代理人搜索](#bk_searchewsma) **FindItem**方法。</span><span class="sxs-lookup"><span data-stu-id="f98ca-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
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

<span data-ttu-id="f98ca-166">服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，指示已成功完成搜索的[FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)消息的**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="f98ca-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="f98ca-167">则响应中包含的任何约会或会议符合搜索条件的[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f98ca-167">The response contains a [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="f98ca-168">在这种情况下，找到只有一个会议。</span><span class="sxs-lookup"><span data-stu-id="f98ca-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="f98ca-169">为便于阅读缩短了[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="f98ca-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
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

<span data-ttu-id="f98ca-170">既然您已经**ItemId**会议符合以下条件，您可以获取、 更新或删除该会议使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)— 并不需要指定邮箱所有者的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="f98ca-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="f98ca-171">获取、 更新或删除的日历项目作为代理人使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="f98ca-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="f98ca-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-172"></span></span>

<span data-ttu-id="f98ca-173">EWS 托管 API 可用于获取、 更新或删除会议或约会中不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="f98ca-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f98ca-174">唯一的区别是服务对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="f98ca-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f98ca-175">唯一的**绑定**方法调用中包含的项 ID 标识邮箱所有者的日历文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="f98ca-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f98ca-176">**表 2。作为代理人处理约会和会议的 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="f98ca-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="f98ca-177">**任务**</span><span class="sxs-lookup"><span data-stu-id="f98ca-177">**Task**</span></span>|<span data-ttu-id="f98ca-178">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="f98ca-178">**EWS Managed API method**</span></span>|<span data-ttu-id="f98ca-179">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="f98ca-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f98ca-180">获取约会或会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="f98ca-181">绑定</span><span class="sxs-lookup"><span data-stu-id="f98ca-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="f98ca-182">使用 EWS 托管 API 中获取项</span><span class="sxs-lookup"><span data-stu-id="f98ca-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="f98ca-183">约会或会议的更新</span><span class="sxs-lookup"><span data-stu-id="f98ca-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f98ca-184">[更新](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f98ca-185">使用 EWS 托管 API 更新会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="f98ca-186">删除约会或会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f98ca-187">[删除](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)后跟[绑定](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="f98ca-188">使用 EWS 托管 API 删除会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="f98ca-189">获取、 更新或删除作为代理人使用 EWS 的日历项目</span><span class="sxs-lookup"><span data-stu-id="f98ca-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="f98ca-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="f98ca-190"></span></span>

<span data-ttu-id="f98ca-191">您可以使用 EWS 获取、 更新或删除会议或约会中不使用代理访问时执行这些操作的方式相同。</span><span class="sxs-lookup"><span data-stu-id="f98ca-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="f98ca-192">唯一的区别是服务对象为代理用户。</span><span class="sxs-lookup"><span data-stu-id="f98ca-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="f98ca-193">唯一的[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)方法调用中包含的项 ID 标识邮箱所有者的日历文件夹中的邮箱存储中的项。</span><span class="sxs-lookup"><span data-stu-id="f98ca-193">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="f98ca-194">**表 3。作为代理人处理约会和会议的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="f98ca-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="f98ca-195">**任务**</span><span class="sxs-lookup"><span data-stu-id="f98ca-195">**Task**</span></span>|<span data-ttu-id="f98ca-196">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="f98ca-196">**EWS operation**</span></span>|<span data-ttu-id="f98ca-197">**代码示例**</span><span class="sxs-lookup"><span data-stu-id="f98ca-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f98ca-198">获取约会或会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="f98ca-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="f98ca-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="f98ca-200">使用 EWS 获取项目</span><span class="sxs-lookup"><span data-stu-id="f98ca-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="f98ca-201">约会或会议的更新</span><span class="sxs-lookup"><span data-stu-id="f98ca-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f98ca-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="f98ca-203">使用 EWS 更新会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="f98ca-204">删除约会或会议</span><span class="sxs-lookup"><span data-stu-id="f98ca-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="f98ca-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)跟[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f98ca-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f98ca-206">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f98ca-206">See also</span></span>

- [<span data-ttu-id="f98ca-207">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="f98ca-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="f98ca-208">添加和删除代理人，在 Exchange 使用 EWS</span><span class="sxs-lookup"><span data-stu-id="f98ca-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="f98ca-209">在 Exchange 使用 EWS 设置另一个用户的文件夹权限</span><span class="sxs-lookup"><span data-stu-id="f98ca-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="f98ca-210">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="f98ca-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

