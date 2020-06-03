---
title: CalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItem
api_type:
- schema
ms.assetid: b0c1fd27-b6da-46e5-88b8-88f00c71ba80
description: CalendarItem 元素表示 Exchange 日历项目。
ms.openlocfilehash: b29141470d157ef5bd67be06a1e1fa1c9536b042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529481"
---
# <a name="calendaritem"></a><span data-ttu-id="e37f1-103">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e37f1-103">CalendarItem</span></span>

<span data-ttu-id="e37f1-104">**CalendarItem**元素表示 Exchange 日历项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-104">The **CalendarItem** element represents an Exchange calendar item.</span></span> 
  
```XML
<CalendarItem>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Start/>
   <End/>
   <OriginalStart/>
   <IsAllDayEvent/>
   <LegacyFreeBusyStatus/>
   <Location/>
   <When/>
   <IsMeeting/>
   <IsCancelled/>
   <IsRecurring/>
   <MeetingRequestWasSent/>
   <IsResponseRequested/>
   <CalendarItemType/>
   <MyResponseType/>
   <Organizer/>
   <RequiredAttendees/>
   <OptionalAttendees/>
   <Resources/>
   <ConflictingMeetingCount/>
   <AdjacentMeetingCount/>
   <ConflictingMeetings/>
   <AdjacentMeetings/>
   <Duration/>
   <TimeZone/>
   <AppointmentReplyTime/>
   <AppointmentSequenceNumber/>
   <AppointmentState/>
   <Recurrence/>
   <FirstOccurrence/>
   <LastOccurrence/>
   <ModifiedOccurrences/>
   <DeletedOccurrences/>
   <MeetingTimeZone/>
   <StartTimeZone/>
   <EndTimeZone/>
   <ConferenceType/>
   <AllowNewTimeProposal/>
   <IsOnlineMeeting/>
   <MeetingWorkspaceUrl/>
   <NetShowUrl/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</CalendarItem>
```

 <span data-ttu-id="e37f1-105">**CalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="e37f1-105">**CalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e37f1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e37f1-106">Attributes and elements</span></span>

<span data-ttu-id="e37f1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e37f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e37f1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e37f1-108">Attributes</span></span>

<span data-ttu-id="e37f1-109">无。</span><span class="sxs-lookup"><span data-stu-id="e37f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e37f1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e37f1-110">Child elements</span></span>

|<span data-ttu-id="e37f1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e37f1-111">**Element**</span></span>|<span data-ttu-id="e37f1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e37f1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e37f1-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="e37f1-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="e37f1-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="e37f1-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="e37f1-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e37f1-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="e37f1-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="e37f1-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="e37f1-118">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="e37f1-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="e37f1-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="e37f1-120">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="e37f1-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-121">主题</span><span class="sxs-lookup"><span data-stu-id="e37f1-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="e37f1-122">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="e37f1-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="e37f1-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="e37f1-124">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="e37f1-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-125">Body</span><span class="sxs-lookup"><span data-stu-id="e37f1-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="e37f1-126">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="e37f1-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-127">附件</span><span class="sxs-lookup"><span data-stu-id="e37f1-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e37f1-128">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="e37f1-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="e37f1-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="e37f1-130">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-131">大小</span><span class="sxs-lookup"><span data-stu-id="e37f1-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="e37f1-132">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e37f1-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="e37f1-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="e37f1-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-134">类别</span><span class="sxs-lookup"><span data-stu-id="e37f1-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e37f1-135">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="e37f1-135">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-136">Importance</span><span class="sxs-lookup"><span data-stu-id="e37f1-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="e37f1-137">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="e37f1-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="e37f1-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="e37f1-139">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="e37f1-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="e37f1-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="e37f1-141">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="e37f1-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="e37f1-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="e37f1-143">指示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-143">Indicates whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="e37f1-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="e37f1-145">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="e37f1-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="e37f1-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="e37f1-147">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="e37f1-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="e37f1-149">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="e37f1-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-150">Message</span><span class="sxs-lookup"><span data-stu-id="e37f1-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="e37f1-151">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="e37f1-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="e37f1-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="e37f1-153">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="e37f1-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="e37f1-155">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="e37f1-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="e37f1-157">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="e37f1-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="e37f1-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="e37f1-159">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="e37f1-160">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="e37f1-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="e37f1-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="e37f1-162">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="e37f1-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="e37f1-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="e37f1-164">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="e37f1-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="e37f1-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="e37f1-166">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="e37f1-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="e37f1-167">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="e37f1-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="e37f1-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="e37f1-169">表示用于 "To" 行的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="e37f1-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="e37f1-170">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="e37f1-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="e37f1-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="e37f1-172">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="e37f1-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="e37f1-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="e37f1-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="e37f1-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="e37f1-175">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="e37f1-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-176">Culture</span><span class="sxs-lookup"><span data-stu-id="e37f1-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="e37f1-177">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="e37f1-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-178">UID</span><span class="sxs-lookup"><span data-stu-id="e37f1-178">UID</span></span>](uid.md) <br/> |<span data-ttu-id="e37f1-179">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-179">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-180">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="e37f1-180">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="e37f1-181">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="e37f1-181">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-182">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="e37f1-182">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="e37f1-183">指示 iCalendar 对象的实例的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-183">Indicates the date and time that an instance of a iCalendar object was created.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-184">开始</span><span class="sxs-lookup"><span data-stu-id="e37f1-184">Start</span></span>](start.md) <br/> |<span data-ttu-id="e37f1-185">代表日历项目的开始。</span><span class="sxs-lookup"><span data-stu-id="e37f1-185">Represents the start of a calendar item.</span></span> <span data-ttu-id="e37f1-186">此元素仅适用于日历项目的一次事件。</span><span class="sxs-lookup"><span data-stu-id="e37f1-186">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-187">停止</span><span class="sxs-lookup"><span data-stu-id="e37f1-187">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e37f1-188">表示持续时间的结束。</span><span class="sxs-lookup"><span data-stu-id="e37f1-188">Represents the end of a duration.</span></span> <span data-ttu-id="e37f1-189">此元素仅适用于日历项目的一次事件。</span><span class="sxs-lookup"><span data-stu-id="e37f1-189">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-190">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="e37f1-190">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="e37f1-191">表示日历项目的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-191">Represents the original start time of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-192">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="e37f1-192">IsAllDayEvent</span></span>](isalldayevent.md) <br/> |<span data-ttu-id="e37f1-193">指示日历项目或会议请求是否代表全天事件。</span><span class="sxs-lookup"><span data-stu-id="e37f1-193">Indicates whether a calendar item or meeting request represents an all-day event.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-194">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="e37f1-194">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md) <br/> |<span data-ttu-id="e37f1-195">表示日历项目的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="e37f1-195">Represents the free/busy status of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-196">Location</span><span class="sxs-lookup"><span data-stu-id="e37f1-196">Location</span></span>](location.md) <br/> |<span data-ttu-id="e37f1-197">代表会议或约会的位置。</span><span class="sxs-lookup"><span data-stu-id="e37f1-197">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-198">When</span><span class="sxs-lookup"><span data-stu-id="e37f1-198">When</span></span>](when.md) <br/> |<span data-ttu-id="e37f1-199">提供有关何时发生日历项的信息。</span><span class="sxs-lookup"><span data-stu-id="e37f1-199">Provides information about when a calendar item occurs.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-200">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="e37f1-200">IsMeeting</span></span>](ismeeting.md) <br/> |<span data-ttu-id="e37f1-201">指示日历项目是否为会议或约会。</span><span class="sxs-lookup"><span data-stu-id="e37f1-201">Indicates whether the calendar item is a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-202">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="e37f1-202">IsCancelled</span></span>](iscancelled.md) <br/> |<span data-ttu-id="e37f1-203">指示约会或会议是否已被取消。</span><span class="sxs-lookup"><span data-stu-id="e37f1-203">Indicates whether an appointment or meeting has been canceled.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-204">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="e37f1-204">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="e37f1-205">指示日历项目是否是定期项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="e37f1-205">Indicates whether a calendar item is part of a recurring item.</span></span> <span data-ttu-id="e37f1-206">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="e37f1-206">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-207">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="e37f1-207">MeetingRequestWasSent</span></span>](meetingrequestwassent.md) <br/> |<span data-ttu-id="e37f1-208">指示是否已将会议请求发送到请求的与会者。</span><span class="sxs-lookup"><span data-stu-id="e37f1-208">Indicates whether a meeting request has been sent to requested attendees.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-209">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="e37f1-209">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="e37f1-210">指示是否需要对项目的响应。</span><span class="sxs-lookup"><span data-stu-id="e37f1-210">Indicates whether a response to an item is required.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-211">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="e37f1-211">CalendarItemType</span></span>](calendaritemtype.md) <br/> |<span data-ttu-id="e37f1-212">表示日历项的发生类型。</span><span class="sxs-lookup"><span data-stu-id="e37f1-212">Represents the occurrence type of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-213">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="e37f1-213">MyResponseType</span></span>](myresponsetype.md) <br/> |<span data-ttu-id="e37f1-214">包含日历项目的状态或响应。</span><span class="sxs-lookup"><span data-stu-id="e37f1-214">Contains the status of or response to a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-215">Organizer</span><span class="sxs-lookup"><span data-stu-id="e37f1-215">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="e37f1-216">表示会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="e37f1-216">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-217">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="e37f1-217">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="e37f1-218">表示参加会议所需的与会者。</span><span class="sxs-lookup"><span data-stu-id="e37f1-218">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-219">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="e37f1-219">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="e37f1-220">表示参加会议不需要的与会者。</span><span class="sxs-lookup"><span data-stu-id="e37f1-220">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-221">资源</span><span class="sxs-lookup"><span data-stu-id="e37f1-221">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="e37f1-222">表示会议的计划资源。</span><span class="sxs-lookup"><span data-stu-id="e37f1-222">Represents a scheduled resource for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-223">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="e37f1-223">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md) <br/> |<span data-ttu-id="e37f1-224">表示与日历项目相冲突的会议数。</span><span class="sxs-lookup"><span data-stu-id="e37f1-224">Represents the number of meetings that conflict with the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-225">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="e37f1-225">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md) <br/> |<span data-ttu-id="e37f1-226">表示与会议时间相邻的日历项目的总数。</span><span class="sxs-lookup"><span data-stu-id="e37f1-226">Represents the total number of calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-227">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e37f1-227">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="e37f1-228">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-228">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-229">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="e37f1-229">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="e37f1-230">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-230">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-231">持续时间（项目）</span><span class="sxs-lookup"><span data-stu-id="e37f1-231">Duration (Items)</span></span>](duration-items.md) <br/> |<span data-ttu-id="e37f1-232">表示日历项的持续时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-232">Represents the duration of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-233">时区（项目）</span><span class="sxs-lookup"><span data-stu-id="e37f1-233">TimeZone (Item)</span></span>](timezone-item.md) <br/> |<span data-ttu-id="e37f1-234">提供时区的文本说明。</span><span class="sxs-lookup"><span data-stu-id="e37f1-234">Provides a text description of a time zone.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-235">AppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="e37f1-235">AppointmentReplyTime</span></span>](appointmentreplytime.md) <br/> |<span data-ttu-id="e37f1-236">表示与会者答复会议请求的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-236">Represents the date and time when an attendee replied to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-237">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="e37f1-237">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md) <br/> |<span data-ttu-id="e37f1-238">指定约会的一个版本的序列号。</span><span class="sxs-lookup"><span data-stu-id="e37f1-238">Specifies the sequence number of a version of an appointment.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-239">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="e37f1-239">AppointmentState</span></span>](appointmentstate.md) <br/> |<span data-ttu-id="e37f1-240">指定约会的状态。</span><span class="sxs-lookup"><span data-stu-id="e37f1-240">Specifies the status of the appointment.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-241">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="e37f1-241">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="e37f1-242">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="e37f1-242">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> <span data-ttu-id="e37f1-243">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="e37f1-243">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-244">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="e37f1-244">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="e37f1-245">表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="e37f1-245">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="e37f1-246">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="e37f1-246">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-247">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="e37f1-247">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="e37f1-248">表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="e37f1-248">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="e37f1-249">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="e37f1-249">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-250">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="e37f1-250">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="e37f1-251">包含已修改的定期日历项目匹配项的数组，以便它们不同于定期主项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-251">Contains an array of recurring calendar item occurrences that have been modified so that they differ from the recurrence master item.</span></span>  <br/> <span data-ttu-id="e37f1-252">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="e37f1-252">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-253">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="e37f1-253">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="e37f1-254">包含定期日历项目的已删除事件数组。</span><span class="sxs-lookup"><span data-stu-id="e37f1-254">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="e37f1-255">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="e37f1-255">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-256">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="e37f1-256">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="e37f1-257">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="e37f1-257">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-258">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="e37f1-258">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="e37f1-259">表示日历项目的起始时区。</span><span class="sxs-lookup"><span data-stu-id="e37f1-259">Represents the start time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-260">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="e37f1-260">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="e37f1-261">表示日历项目的结束时区。</span><span class="sxs-lookup"><span data-stu-id="e37f1-261">Represents the end time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-262">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="e37f1-262">ConferenceType</span></span>](conferencetype.md) <br/> |<span data-ttu-id="e37f1-263">介绍使用日历项目执行的会议的类型。</span><span class="sxs-lookup"><span data-stu-id="e37f1-263">Describes the type of conferencing that is performed with a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-264">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="e37f1-264">AllowNewTimeProposal</span></span>](allownewtimeproposal.md) <br/> |<span data-ttu-id="e37f1-265">指示与会者是否可以为会议建议新的会议时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-265">Indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-266">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="e37f1-266">IsOnlineMeeting</span></span>](isonlinemeeting.md) <br/> |<span data-ttu-id="e37f1-267">指示会议是否处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="e37f1-267">Indicates whether the meeting is online.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-268">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="e37f1-268">MeetingWorkspaceUrl</span></span>](meetingworkspaceurl.md) <br/> |<span data-ttu-id="e37f1-269">包含由日历项目链接到的会议工作区的 URL。</span><span class="sxs-lookup"><span data-stu-id="e37f1-269">Contains the URL for the meeting workspace that is linked to by the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-270">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="e37f1-270">NetShowUrl</span></span>](netshowurl.md) <br/> |<span data-ttu-id="e37f1-271">指定 Microsoft NetShow online 会议的 URL。</span><span class="sxs-lookup"><span data-stu-id="e37f1-271">Specifies the URL for a Microsoft NetShow online meeting.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-272">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="e37f1-272">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="e37f1-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="e37f1-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-275">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="e37f1-275">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="e37f1-276">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="e37f1-276">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-277">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="e37f1-277">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="e37f1-278">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="e37f1-278">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-279">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="e37f1-279">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="e37f1-280">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="e37f1-280">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-281">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="e37f1-281">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="e37f1-282">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="e37f1-282">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-283">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="e37f1-283">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="e37f1-284">表示一个用于连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="e37f1-284">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-285">ConversationId</span><span class="sxs-lookup"><span data-stu-id="e37f1-285">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="e37f1-286">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="e37f1-286">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-287">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="e37f1-287">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="e37f1-288">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="e37f1-288">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e37f1-289">父元素</span><span class="sxs-lookup"><span data-stu-id="e37f1-289">Parent elements</span></span>

|<span data-ttu-id="e37f1-290">**元素**</span><span class="sxs-lookup"><span data-stu-id="e37f1-290">**Element**</span></span>|<span data-ttu-id="e37f1-291">**说明**</span><span class="sxs-lookup"><span data-stu-id="e37f1-291">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e37f1-292">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="e37f1-292">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="e37f1-293">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-293">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-294">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="e37f1-294">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="e37f1-295">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项或文件夹的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="e37f1-295">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e37f1-296">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e37f1-296">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="e37f1-297">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-297">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-298">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="e37f1-298">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="e37f1-299">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e37f1-299">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-300">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="e37f1-300">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="e37f1-301">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-301">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-302">Items</span><span class="sxs-lookup"><span data-stu-id="e37f1-302">Items</span></span>](items.md) <br/> |<span data-ttu-id="e37f1-303">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="e37f1-303">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-304">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="e37f1-304">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="e37f1-305">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="e37f1-305">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="e37f1-306">SetItemField</span><span class="sxs-lookup"><span data-stu-id="e37f1-306">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="e37f1-307">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="e37f1-307">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e37f1-308">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="e37f1-308">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="e37f1-309">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="e37f1-309">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e37f1-310">文本值</span><span class="sxs-lookup"><span data-stu-id="e37f1-310">Text value</span></span>

<span data-ttu-id="e37f1-311">无。</span><span class="sxs-lookup"><span data-stu-id="e37f1-311">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e37f1-312">说明</span><span class="sxs-lookup"><span data-stu-id="e37f1-312">Remarks</span></span>

<span data-ttu-id="e37f1-313">更新单个日历项目以使其成为定期主日历项目时，必须指定[MeetingTimeZone](meetingtimezone.md)元素，以便保留日历项目的原始时区。</span><span class="sxs-lookup"><span data-stu-id="e37f1-313">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) element must be specified in order to preserve the calendar item's original time zone.</span></span> 
  
<span data-ttu-id="e37f1-314">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e37f1-314">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e37f1-315">元素信息</span><span class="sxs-lookup"><span data-stu-id="e37f1-315">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e37f1-316">命名空间</span><span class="sxs-lookup"><span data-stu-id="e37f1-316">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e37f1-317">架构名称</span><span class="sxs-lookup"><span data-stu-id="e37f1-317">Schema name</span></span>  <br/> |<span data-ttu-id="e37f1-318">类型架构</span><span class="sxs-lookup"><span data-stu-id="e37f1-318">Types schema</span></span>  <br/> |
|<span data-ttu-id="e37f1-319">验证文件</span><span class="sxs-lookup"><span data-stu-id="e37f1-319">Validation file</span></span>  <br/> |<span data-ttu-id="e37f1-320">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e37f1-320">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e37f1-321">可以为空</span><span class="sxs-lookup"><span data-stu-id="e37f1-321">Can be empty</span></span>  <br/> |<span data-ttu-id="e37f1-322">False</span><span class="sxs-lookup"><span data-stu-id="e37f1-322">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e37f1-323">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e37f1-323">See also</span></span>



- [<span data-ttu-id="e37f1-324">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e37f1-324">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="e37f1-325">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="e37f1-325">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

