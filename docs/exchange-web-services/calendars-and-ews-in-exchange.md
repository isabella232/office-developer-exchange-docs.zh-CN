---
title: Calendars and EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: 了解 Exchange 中的日历、日历文件夹和项目、约会和会议。
localization_priority: Priority
ms.openlocfilehash: 3312ebb4deeb6645ccd7048564d61c3db5ea4b94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456197"
---
# <a name="calendars-and-ews-in-exchange"></a><span data-ttu-id="bcb31-103">Calendars and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="bcb31-103">Calendars and EWS in Exchange</span></span>

<span data-ttu-id="bcb31-104">了解 Exchange 中的日历、日历文件夹和项目、约会和会议。</span><span class="sxs-lookup"><span data-stu-id="bcb31-104">Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.</span></span>
  
<span data-ttu-id="bcb31-105">您可能已经熟悉电子邮件客户端（如 Outlook）中的许多日历功能，这使您能够跟踪约会、安排会议、检查人员的可用性、邀请与会者以及更改或取消会议。</span><span class="sxs-lookup"><span data-stu-id="bcb31-105">You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.</span></span>
  
<span data-ttu-id="bcb31-106">Exchange 中日历相关的功能与在客户端（如 Outlook）中看到的功能稍有不同。</span><span class="sxs-lookup"><span data-stu-id="bcb31-106">Calendar-related features in Exchange are a little different than what you see in a client like Outlook.</span></span> <span data-ttu-id="bcb31-107">通过 Exchange 中的 EWS，可以执行创建、存储、发送或更改信息等操作，而不是显示信息。</span><span class="sxs-lookup"><span data-stu-id="bcb31-107">Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information.</span></span> <span data-ttu-id="bcb31-108">若要使用 EWS 处理日历，您需要熟悉诸如信息存储、时间、定期和邮件流等概念。</span><span class="sxs-lookup"><span data-stu-id="bcb31-108">To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow.</span></span> <span data-ttu-id="bcb31-109">更具体地说，您需要熟悉以下内容：</span><span class="sxs-lookup"><span data-stu-id="bcb31-109">More specifically, you'll need to be familiar with the following:</span></span>
  
- <span data-ttu-id="bcb31-110">日历文件夹、日历项目和日历视图</span><span class="sxs-lookup"><span data-stu-id="bcb31-110">Calendar folders, calendar items, and calendar views</span></span>
    
- <span data-ttu-id="bcb31-111">会议请求、响应、日程安排、与会者、资源、会议室和可用性</span><span class="sxs-lookup"><span data-stu-id="bcb31-111">Meeting requests, responses, scheduling, attendees, resources, rooms, and availability</span></span>
    
- <span data-ttu-id="bcb31-112">会议和约会的持续时间、时区以及开始和结束时间</span><span class="sxs-lookup"><span data-stu-id="bcb31-112">Time durations, time zones, and start and end times of meetings and appointments</span></span>
    
- <span data-ttu-id="bcb31-113">定期系列、定期模式、异常和单个实例约会和会议</span><span class="sxs-lookup"><span data-stu-id="bcb31-113">Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings</span></span>
    
<span data-ttu-id="bcb31-114">幸运的是，EWS 和 EWS 托管 API 提供了一组丰富的操作和方法，使您能够执行大量与日历相关的任务。</span><span class="sxs-lookup"><span data-stu-id="bcb31-114">Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks.</span></span> <span data-ttu-id="bcb31-115">例如，使用 EWS 托管 API，您可以创建会议并只向与会者发送邀请，只需几行代码，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="bcb31-115">For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.</span></span>
  
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

## <a name="calendar-folders-and-calendar-items"></a><span data-ttu-id="bcb31-116">日历文件夹和日历项目</span><span class="sxs-lookup"><span data-stu-id="bcb31-116">Calendar folders and calendar items</span></span>
<span data-ttu-id="bcb31-117"><a name="bk_CalendarFolder"> </a></span><span class="sxs-lookup"><span data-stu-id="bcb31-117"><a name="bk_CalendarFolder"> </a></span></span>

<span data-ttu-id="bcb31-118">"日历" 文件夹包含日历项目。</span><span class="sxs-lookup"><span data-stu-id="bcb31-118">Calendar folders contain calendar items.</span></span> <span data-ttu-id="bcb31-119">"日历" 文件夹的[folder 类](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)为**IPF。约会**，并且可以仅包括由[ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS 托管 API 属性（与[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)对象或 EWS [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)元素相关联）定义的项目。</span><span class="sxs-lookup"><span data-stu-id="bcb31-119">Calendar folders have a [folder class](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="bcb31-120">"日历" 文件夹中的项目与邮箱中的其他文件夹中的项目略有不同，因为定期系列中的事件和定期系列的例外不是邮箱中的实际项目，而是作为定期母版的附件在内部存储。</span><span class="sxs-lookup"><span data-stu-id="bcb31-120">Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="bcb31-121">因此，为了检索给定日期范围内的所有约会，您需要使用日历视图。</span><span class="sxs-lookup"><span data-stu-id="bcb31-121">Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view.</span></span> <span data-ttu-id="bcb31-122">若要了解有关检索约会和日历视图的详细信息，请参阅[使用 Exchange 中的 EWS 获取约会和会议](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bcb31-122">To learn more about retrieving appointments and calendar views, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="meetings-and-appointments"></a><span data-ttu-id="bcb31-123">会议和约会</span><span class="sxs-lookup"><span data-stu-id="bcb31-123">Meetings and appointments</span></span>
<span data-ttu-id="bcb31-124"><a name="bk_meetings"> </a></span><span class="sxs-lookup"><span data-stu-id="bcb31-124"><a name="bk_meetings"> </a></span></span>

<span data-ttu-id="bcb31-125">会议和约会之间的基本区别在于会议具有与会者，而约会则不是。</span><span class="sxs-lookup"><span data-stu-id="bcb31-125">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't.</span></span> <span data-ttu-id="bcb31-126">在内部，Exchange 对会议和约会使用相同的对象。</span><span class="sxs-lookup"><span data-stu-id="bcb31-126">Internally, Exchange uses the same object for both meetings and appointments.</span></span> <span data-ttu-id="bcb31-127">您可以使用 EWS 托管 API[约会类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)或 ews [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)元素来处理会议和约会。</span><span class="sxs-lookup"><span data-stu-id="bcb31-127">You use the EWS Managed API [Appointment class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="bcb31-128">约会和会议既可以是单个实例，也可以是[定期系列](recurrence-patterns-and-ews.md)的一部分，但由于约会不包括与会者、会议室或资源，因此它们不需要发送邮件。</span><span class="sxs-lookup"><span data-stu-id="bcb31-128">Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span>
  
<span data-ttu-id="bcb31-129">由于会议包括发送和响应请求和更新，因此他们不仅仅涉及访问 "日历" 文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="bcb31-129">Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder.</span></span> <span data-ttu-id="bcb31-130">它们还具有关联的工作流。</span><span class="sxs-lookup"><span data-stu-id="bcb31-130">They also have an associated workflow.</span></span> <span data-ttu-id="bcb31-131">会议必须在与会者可用时安排日程，还可以涉及保留会议室或诸如投影仪或其他设备等资源。</span><span class="sxs-lookup"><span data-stu-id="bcb31-131">Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.</span></span>
  
<span data-ttu-id="bcb31-132">会议工作流通常涉及以下步骤：</span><span class="sxs-lookup"><span data-stu-id="bcb31-132">The meeting workflow typically involves the following steps:</span></span>
  
1. <span data-ttu-id="bcb31-133">创建一个会议并使用诸如开始和结束时间、位置和邮件正文的信息填充。</span><span class="sxs-lookup"><span data-stu-id="bcb31-133">A meeting is created and populated with information such as start and end time, location, and a message body.</span></span>
    
2. <span data-ttu-id="bcb31-134">将创建一个预期的与会者、资源和聊天室的列表。</span><span class="sxs-lookup"><span data-stu-id="bcb31-134">A list of prospective attendees, resources, and rooms is created.</span></span>
    
3. <span data-ttu-id="bcb31-135">检查与会者的可用性状态。</span><span class="sxs-lookup"><span data-stu-id="bcb31-135">The availability status of attendees is checked.</span></span> 
    
4. <span data-ttu-id="bcb31-136">向与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="bcb31-136">A meeting request is sent to attendees.</span></span>
    
5. <span data-ttu-id="bcb31-137">与会者回复会议时，他们想要参加会议。</span><span class="sxs-lookup"><span data-stu-id="bcb31-137">Attendees reply to the meeting with their intention to attend or not.</span></span> <span data-ttu-id="bcb31-138">与会者还可能为会议建议新时间。</span><span class="sxs-lookup"><span data-stu-id="bcb31-138">Attendees may also propose a new time for the meeting.</span></span>
    
6. <span data-ttu-id="bcb31-139">可以取消或更新会议，这通常会触发要发送给与会者的新邮件。</span><span class="sxs-lookup"><span data-stu-id="bcb31-139">Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.</span></span>
    
## <a name="calendars-and-time"></a><span data-ttu-id="bcb31-140">日历和时间</span><span class="sxs-lookup"><span data-stu-id="bcb31-140">Calendars and time</span></span>
<span data-ttu-id="bcb31-141"><a name="bk_Time"> </a></span><span class="sxs-lookup"><span data-stu-id="bcb31-141"><a name="bk_Time"> </a></span></span>

<span data-ttu-id="bcb31-142">与时间相关的功能是日历不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="bcb31-142">Time-related functionality is integral to calendaring.</span></span> <span data-ttu-id="bcb31-143">约会和会议具有开始和结束时间、持续时间和其他与时间相关的属性，例如创建、发送和接收邮件的时间。</span><span class="sxs-lookup"><span data-stu-id="bcb31-143">Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received.</span></span> <span data-ttu-id="bcb31-144">可以基于开始时间和结束时间从 "日历" 文件夹中检索现有约会和会议。</span><span class="sxs-lookup"><span data-stu-id="bcb31-144">Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time.</span></span> <span data-ttu-id="bcb31-145">定期系列具有开头和结尾。</span><span class="sxs-lookup"><span data-stu-id="bcb31-145">Recurring series have beginnings and ends.</span></span> <span data-ttu-id="bcb31-146">和会议在给定时区内发生，这在全球经济中越来越重要。</span><span class="sxs-lookup"><span data-stu-id="bcb31-146">And meetings occur within a given time zone, which is increasingly important in a global economy.</span></span>
  
<span data-ttu-id="bcb31-147">时间以协调世界时（UTC）的形式存储在 Exchange 服务器内部。</span><span class="sxs-lookup"><span data-stu-id="bcb31-147">Times are stored internally on an Exchange server in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="bcb31-148">Exchange 将根据客户端设置将它们转换为本地时区。</span><span class="sxs-lookup"><span data-stu-id="bcb31-148">Exchange converts them to local time zone based on client settings.</span></span> <span data-ttu-id="bcb31-149">[DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)属性的作用范围限定为计算机的本地时区。</span><span class="sxs-lookup"><span data-stu-id="bcb31-149">[DateTime](https://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone.</span></span> 
  
## <a name="recurring-series"></a><span data-ttu-id="bcb31-150">定期系列</span><span class="sxs-lookup"><span data-stu-id="bcb31-150">Recurring series</span></span>
<span data-ttu-id="bcb31-151"><a name="bk_recurrence"> </a></span><span class="sxs-lookup"><span data-stu-id="bcb31-151"><a name="bk_recurrence"> </a></span></span>

<span data-ttu-id="bcb31-152">定期的约会或会议系列由一个定期的主控形状、一组发生项以及一组异常项组成。</span><span class="sxs-lookup"><span data-stu-id="bcb31-152">A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items.</span></span> <span data-ttu-id="bcb31-153">定期信息存储在定期主项目上。</span><span class="sxs-lookup"><span data-stu-id="bcb31-153">Recurrence information is stored on the recurring master item.</span></span> <span data-ttu-id="bcb31-154">[RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) ews 元素与系列中的匹配项和异常相关联，也可以使用[BINDTORECURRINGMASTER](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) EWS 托管 API 方法来获取定期母版。</span><span class="sxs-lookup"><span data-stu-id="bcb31-154">The [RecurringMasterItemId](https://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master.</span></span> <span data-ttu-id="bcb31-155">使用系列的实例，可以查找与系列关联的所有元素和信息。</span><span class="sxs-lookup"><span data-stu-id="bcb31-155">Using an instance of a series, you can find all the elements and information associated with the series.</span></span> 
  
<span data-ttu-id="bcb31-156">请注意，所有日历项目上都存在定期属性，但它们只是在定期的主项目上进行填充。</span><span class="sxs-lookup"><span data-stu-id="bcb31-156">Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items.</span></span> <span data-ttu-id="bcb31-157">除了一个系列中的所有匹配项的索引，该定期主控形状具有对修改和删除的匹配项以及系列的定期模式（例如，每天、每周、每月或每年）的引用。</span><span class="sxs-lookup"><span data-stu-id="bcb31-157">In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bcb31-158">本节内容</span><span class="sxs-lookup"><span data-stu-id="bcb31-158">In this section</span></span>
<span data-ttu-id="bcb31-159"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="bcb31-159"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="bcb31-160">使用 Exchange 2013 中的 EWS 创建约会和会议</span><span class="sxs-lookup"><span data-stu-id="bcb31-160">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="bcb31-161">使用 Exchange 中的 EWS 创建全天事件</span><span class="sxs-lookup"><span data-stu-id="bcb31-161">Create all-day events by using EWS in Exchange</span></span>](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-162">使用 Exchange 中的 EWS 获取约会和会议</span><span class="sxs-lookup"><span data-stu-id="bcb31-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-163">使用 Exchange 中的 EWS 更新约会和会议</span><span class="sxs-lookup"><span data-stu-id="bcb31-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-164">使用 Exchange 中的 EWS 删除约会和取消会议</span><span class="sxs-lookup"><span data-stu-id="bcb31-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-165">使用 Exchange 中的 EWS 获取会议室列表</span><span class="sxs-lookup"><span data-stu-id="bcb31-165">Get room lists by using EWS in Exchange</span></span>](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-166">使用 Exchange 中的 EWS 获取忙/闲信息</span><span class="sxs-lookup"><span data-stu-id="bcb31-166">Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-167">使用 Exchange 中的 EWS 建议新的会议时间</span><span class="sxs-lookup"><span data-stu-id="bcb31-167">Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="bcb31-168">在 Exchange 中批量处理日历项目</span><span class="sxs-lookup"><span data-stu-id="bcb31-168">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [<span data-ttu-id="bcb31-169">定期模式和 EWS</span><span class="sxs-lookup"><span data-stu-id="bcb31-169">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="bcb31-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bcb31-170">See also</span></span>


- [<span data-ttu-id="bcb31-171">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="bcb31-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="bcb31-172">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="bcb31-172">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="bcb31-173">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="bcb31-173">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

