---
title: 日历和 Exchange 中的 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: 了解日历、 日历文件夹和项目、 约会和 Exchange 中的会议。
ms.openlocfilehash: bb9702118ff1db66862a5788c2d8f58dd55c4d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752702"
---
# <a name="calendars-and-ews-in-exchange"></a><span data-ttu-id="94a54-103">日历和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="94a54-103">Calendars and EWS in Exchange</span></span>

<span data-ttu-id="94a54-104">了解日历、 日历文件夹和项目、 约会和 Exchange 中的会议。</span><span class="sxs-lookup"><span data-stu-id="94a54-104">Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.</span></span>
  
<span data-ttu-id="94a54-105">您可能已经熟悉许多像 Outlook 的电子邮件客户端使您能够跟踪约会、 安排会议、 检查用户的可用性、 邀请与会者，并更改或取消会议中的日历功能。</span><span class="sxs-lookup"><span data-stu-id="94a54-105">You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.</span></span>
  
<span data-ttu-id="94a54-106">Exchange 中的日历相关的功能是有点不同于如 Outlook 客户端中看到的内容。</span><span class="sxs-lookup"><span data-stu-id="94a54-106">Calendar-related features in Exchange are a little different than what you see in a client like Outlook.</span></span> <span data-ttu-id="94a54-107">而不是在 Exchange 中显示的信息，EWS 使您能够执行某些操作，如创建、 存储、 发送，或更改信息。</span><span class="sxs-lookup"><span data-stu-id="94a54-107">Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information.</span></span> <span data-ttu-id="94a54-108">若要使用 EWS 使用日历，您需要熟悉如信息存储、 时间、 定期，和邮件流的概念。</span><span class="sxs-lookup"><span data-stu-id="94a54-108">To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow.</span></span> <span data-ttu-id="94a54-109">更具体地说，您需要熟悉以下：</span><span class="sxs-lookup"><span data-stu-id="94a54-109">More specifically, you'll need to be familiar with the following:</span></span>
  
- <span data-ttu-id="94a54-110">日历文件夹、 日历项和日历视图</span><span class="sxs-lookup"><span data-stu-id="94a54-110">Calendar folders, calendar items, and calendar views</span></span>
    
- <span data-ttu-id="94a54-111">会议请求、 响应、 日程安排，与会者、 资源、 聊天室和可用性</span><span class="sxs-lookup"><span data-stu-id="94a54-111">Meeting requests, responses, scheduling, attendees, resources, rooms, and availability</span></span>
    
- <span data-ttu-id="94a54-112">持续时间、 时区和会议和约会的开始和结束时间</span><span class="sxs-lookup"><span data-stu-id="94a54-112">Time durations, time zones, and start and end times of meetings and appointments</span></span>
    
- <span data-ttu-id="94a54-113">定期系列、 定期模式、 例外和单实例约会和会议</span><span class="sxs-lookup"><span data-stu-id="94a54-113">Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings</span></span>
    
<span data-ttu-id="94a54-114">幸运的是，EWS 和 EWS 托管 API 提供了一组丰富的操作和方法，使您能够执行各种与日历相关的任务。</span><span class="sxs-lookup"><span data-stu-id="94a54-114">Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks.</span></span> <span data-ttu-id="94a54-115">例如，使用 EWS 托管 API，可以创建会议并发送邀请与会者几行代码，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="94a54-115">For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.</span></span>
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## <a name="calendar-folders-and-calendar-items"></a><span data-ttu-id="94a54-116">日历文件夹和日历项目</span><span class="sxs-lookup"><span data-stu-id="94a54-116">Calendar folders and calendar items</span></span>
<span data-ttu-id="94a54-117"><a name="bk_CalendarFolder"> </a></span><span class="sxs-lookup"><span data-stu-id="94a54-117"></span></span>

<span data-ttu-id="94a54-118">日历文件夹包含日历项。</span><span class="sxs-lookup"><span data-stu-id="94a54-118">Calendar folders contain calendar items.</span></span> <span data-ttu-id="94a54-119">日历文件夹具有**IPF[文件夹类](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)。约会**，并且可以包括仅由[ItemClass](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS 托管 API 属性，其相关联的[约会类](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或 EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素定义的项目。</span><span class="sxs-lookup"><span data-stu-id="94a54-119">Calendar folders have a [folder class](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="94a54-120">日历文件夹中的项目是有点不同于邮箱中的其他文件夹中的项目，因为定期系列和定期系列的例外发生次数不是实际的项目中邮箱，而不内部存储为定期附件主控形状。</span><span class="sxs-lookup"><span data-stu-id="94a54-120">Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="94a54-121">因此，为了检索给定的日期范围内的所有约会，您需要使用日历视图。</span><span class="sxs-lookup"><span data-stu-id="94a54-121">Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view.</span></span> <span data-ttu-id="94a54-122">若要了解有关检索约会和日历视图的详细信息，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="94a54-122">To learn more about retrieving appointments and calendar views, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="meetings-and-appointments"></a><span data-ttu-id="94a54-123">会议和约会</span><span class="sxs-lookup"><span data-stu-id="94a54-123">Meetings and appointments</span></span>
<span data-ttu-id="94a54-124"><a name="bk_meetings"> </a></span><span class="sxs-lookup"><span data-stu-id="94a54-124"></span></span>

<span data-ttu-id="94a54-125">会议和约会的基本区别是，会议具有与会者，并且不约会。</span><span class="sxs-lookup"><span data-stu-id="94a54-125">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="94a54-126">内部 Exchange 使用相同的对象的会议和约会。</span><span class="sxs-lookup"><span data-stu-id="94a54-126">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="94a54-127">使用 EWS 托管 API[约会类](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 EWS[日历项目](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素以使用会议和约会。</span><span class="sxs-lookup"><span data-stu-id="94a54-127">You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="94a54-128">约会和会议可以是单个实例或[定期系列](recurrence-patterns-and-ews.md)，一部分但约会不包括与会者、 聊天室或资源，因为它们不需要发送一条消息。</span><span class="sxs-lookup"><span data-stu-id="94a54-128">Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span>
  
<span data-ttu-id="94a54-129">会议包括发送和响应请求和更新，因为它们涉及多个只需访问日历文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="94a54-129">Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder.</span></span> <span data-ttu-id="94a54-130">它们还具有关联的工作流。</span><span class="sxs-lookup"><span data-stu-id="94a54-130">They also have an associated workflow.</span></span> <span data-ttu-id="94a54-131">当与会者可用，并且还会涉及预留会议室，或资源如投影仪或其他设备必须安排会议。</span><span class="sxs-lookup"><span data-stu-id="94a54-131">Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.</span></span>
  
<span data-ttu-id="94a54-132">会议工作流通常包括以下步骤：</span><span class="sxs-lookup"><span data-stu-id="94a54-132">The meeting workflow typically involves the following steps:</span></span>
  
1. <span data-ttu-id="94a54-133">创建会议并将其填充开始和结束时间、 位置和邮件正文等信息。</span><span class="sxs-lookup"><span data-stu-id="94a54-133">A meeting is created and populated with information such as start and end time, location, and a message body.</span></span>
    
2. <span data-ttu-id="94a54-134">创建的潜在与会者、 资源和会议室列表。</span><span class="sxs-lookup"><span data-stu-id="94a54-134">A list of prospective attendees, resources, and rooms is created.</span></span>
    
3. <span data-ttu-id="94a54-135">检查与会者的可用性状态。</span><span class="sxs-lookup"><span data-stu-id="94a54-135">The availability status of attendees is checked.</span></span> 
    
4. <span data-ttu-id="94a54-136">会议请求发送给与会者。</span><span class="sxs-lookup"><span data-stu-id="94a54-136">A meeting request is sent to attendees.</span></span>
    
5. <span data-ttu-id="94a54-137">与会者的答复其目的参加会议的会议。</span><span class="sxs-lookup"><span data-stu-id="94a54-137">Attendees reply to the meeting with their intention to attend or not.</span></span> <span data-ttu-id="94a54-138">与会者可能还建议会议的新时间。</span><span class="sxs-lookup"><span data-stu-id="94a54-138">Attendees may also propose a new time for the meeting.</span></span>
    
6. <span data-ttu-id="94a54-139">会议可以取消此事件或更新，这通常会触发新邮件发送给与会者。</span><span class="sxs-lookup"><span data-stu-id="94a54-139">Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.</span></span>
    
## <a name="calendars-and-time"></a><span data-ttu-id="94a54-140">日历和时间</span><span class="sxs-lookup"><span data-stu-id="94a54-140">Calendars and time</span></span>
<span data-ttu-id="94a54-141"><a name="bk_Time"> </a></span><span class="sxs-lookup"><span data-stu-id="94a54-141"></span></span>

<span data-ttu-id="94a54-142">或缺日历时间相关功能。</span><span class="sxs-lookup"><span data-stu-id="94a54-142">Time-related functionality is integral to calendaring.</span></span> <span data-ttu-id="94a54-143">约会和会议已开始和结束时间、 持续时间，以及其他与时间有关的属性，如频率一条消息是创建、 发送和接收的时间。</span><span class="sxs-lookup"><span data-stu-id="94a54-143">Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received.</span></span> <span data-ttu-id="94a54-144">可以从基于开始和结束时间的日历文件夹中检索现有约会和会议。</span><span class="sxs-lookup"><span data-stu-id="94a54-144">Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time.</span></span> <span data-ttu-id="94a54-145">定期系列有起始和结束。</span><span class="sxs-lookup"><span data-stu-id="94a54-145">Recurring series have beginnings and ends.</span></span> <span data-ttu-id="94a54-146">会议中给定时区，即在全球经济越来越重要发生。</span><span class="sxs-lookup"><span data-stu-id="94a54-146">And meetings occur within a given time zone, which is increasingly important in a global economy.</span></span>
  
<span data-ttu-id="94a54-147">时间内部存储在 Exchange 服务器以协调世界时 (UTC) 上。</span><span class="sxs-lookup"><span data-stu-id="94a54-147">Times are stored internally on an Exchange server in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="94a54-148">Exchange 将其转换为基于客户端设置本地时区。</span><span class="sxs-lookup"><span data-stu-id="94a54-148">Exchange converts them to local time zone based on client settings.</span></span> <span data-ttu-id="94a54-149">[DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)属性范围限定到计算机的本地时区。</span><span class="sxs-lookup"><span data-stu-id="94a54-149">[DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone.</span></span> 
  
## <a name="recurring-series"></a><span data-ttu-id="94a54-150">定期系列</span><span class="sxs-lookup"><span data-stu-id="94a54-150">Recurring series</span></span>
<span data-ttu-id="94a54-151"><a name="bk_recurrence"> </a></span><span class="sxs-lookup"><span data-stu-id="94a54-151"></span></span>

<span data-ttu-id="94a54-152">一系列定期约会或会议组成定期主控形状、 匹配项，一套和 （可选） 的一组例外项。</span><span class="sxs-lookup"><span data-stu-id="94a54-152">A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items.</span></span> <span data-ttu-id="94a54-153">重复信息存储在定期主项目。</span><span class="sxs-lookup"><span data-stu-id="94a54-153">Recurrence information is stored on the recurring master item.</span></span> <span data-ttu-id="94a54-154">[RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS 元素是与出现系列的例外关联，或者您可以使用[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/zh-cn/library/dd635978%28v=EXCHG.80%29.aspx) EWS 托管 API 方法以获取定期主控形状。</span><span class="sxs-lookup"><span data-stu-id="94a54-154">The [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/zh-cn/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master.</span></span> <span data-ttu-id="94a54-155">使用的一系列实例，您可以找到的元素和系列相关联的信息。</span><span class="sxs-lookup"><span data-stu-id="94a54-155">Using an instance of a series, you can find all the elements and information associated with the series.</span></span> 
  
<span data-ttu-id="94a54-156">请注意，定期属性存在于上的所有日历项目，但他们会仅在定期主项目上填充。</span><span class="sxs-lookup"><span data-stu-id="94a54-156">Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items.</span></span> <span data-ttu-id="94a54-157">除了系列中所有匹配项的索引，定期主具有修改和删除匹配项和一系列定期模式参考 （例如、 每日、 每周、 每月或年）。</span><span class="sxs-lookup"><span data-stu-id="94a54-157">In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="94a54-158">本节内容</span><span class="sxs-lookup"><span data-stu-id="94a54-158">In this section</span></span>
<span data-ttu-id="94a54-159"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="94a54-159"></span></span>

- [<span data-ttu-id="94a54-160">使用 Exchange 2013 中的 EWS 中创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="94a54-160">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="94a54-161">使用 EWS 在 Exchange 中创建全天事件</span><span class="sxs-lookup"><span data-stu-id="94a54-161">Create all-day events by using EWS in Exchange</span></span>](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-162">在 Exchange 使用 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="94a54-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-163">在 Exchange 使用 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="94a54-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-164">删除约会，并在 Exchange 使用 EWS 取消会议</span><span class="sxs-lookup"><span data-stu-id="94a54-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-165">要在 Exchange 使用 EWS 获取会议室列表</span><span class="sxs-lookup"><span data-stu-id="94a54-165">Get room lists by using EWS in Exchange</span></span>](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-166">要在 Exchange 使用 EWS 获取忙/闲信息</span><span class="sxs-lookup"><span data-stu-id="94a54-166">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-167">建议在 Exchange 使用 EWS 的新的会议时间</span><span class="sxs-lookup"><span data-stu-id="94a54-167">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="94a54-168">在 Exchange 处理批次中的日历项目</span><span class="sxs-lookup"><span data-stu-id="94a54-168">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [<span data-ttu-id="94a54-169">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="94a54-169">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="94a54-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94a54-170">See also</span></span>


- [<span data-ttu-id="94a54-171">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="94a54-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="94a54-172">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="94a54-172">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="94a54-173">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="94a54-173">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

