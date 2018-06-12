---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: MeetingRequest 元素表示 Exchange 存储中的会议请求。
ms.openlocfilehash: 3e290613293cb6ad1563912e5015742ffc503d08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826450"
---
# <a name="meetingrequest"></a><span data-ttu-id="3ab56-103">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3ab56-103">MeetingRequest</span></span>

<span data-ttu-id="3ab56-104">**MeetingRequest**元素表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="3ab56-104">The **MeetingRequest** element represents a meeting request in the Exchange store.</span></span> 
  
```xml
<MeetingRequest>
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
   <Importance/>
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
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <MeetingRequestType/>
   <IntendedFreeBusyStatus/>
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
</MeetingRequest>
```

 <span data-ttu-id="3ab56-105">**MeetingRequestMessageType**</span><span class="sxs-lookup"><span data-stu-id="3ab56-105">**MeetingRequestMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ab56-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3ab56-106">Attributes and elements</span></span>

<span data-ttu-id="3ab56-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3ab56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ab56-108">属性</span><span class="sxs-lookup"><span data-stu-id="3ab56-108">Attributes</span></span>

<span data-ttu-id="3ab56-109">无。</span><span class="sxs-lookup"><span data-stu-id="3ab56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ab56-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3ab56-110">Child elements</span></span>

|<span data-ttu-id="3ab56-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3ab56-111">**Element**</span></span>|<span data-ttu-id="3ab56-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3ab56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ab56-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="3ab56-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="3ab56-114">包含 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="3ab56-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="3ab56-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3ab56-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="3ab56-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="3ab56-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="3ab56-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="3ab56-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="3ab56-119">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="3ab56-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="3ab56-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="3ab56-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="3ab56-122">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="3ab56-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-123">Subject</span><span class="sxs-lookup"><span data-stu-id="3ab56-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="3ab56-124">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="3ab56-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="3ab56-125">主题被限制为 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3ab56-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="3ab56-127">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="3ab56-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-128">Body</span><span class="sxs-lookup"><span data-stu-id="3ab56-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="3ab56-129">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="3ab56-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-130">附件</span><span class="sxs-lookup"><span data-stu-id="3ab56-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3ab56-131">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="3ab56-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="3ab56-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="3ab56-133">代表的数据和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="3ab56-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-134">Size</span><span class="sxs-lookup"><span data-stu-id="3ab56-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="3ab56-135">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="3ab56-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="3ab56-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="3ab56-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-137">类别</span><span class="sxs-lookup"><span data-stu-id="3ab56-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3ab56-138">表示标识的邮箱中项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="3ab56-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-139">Importance</span><span class="sxs-lookup"><span data-stu-id="3ab56-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="3ab56-140">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="3ab56-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="3ab56-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="3ab56-142">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="3ab56-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="3ab56-144">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="3ab56-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="3ab56-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="3ab56-146">指示是否项目尚未发送。</span><span class="sxs-lookup"><span data-stu-id="3ab56-146">Indicates whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="3ab56-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="3ab56-148">指示用户是否发送到其自身的项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="3ab56-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="3ab56-150">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="3ab56-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="3ab56-152">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="3ab56-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="3ab56-154">代表邮箱中的一个项内包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="3ab56-154">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="3ab56-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="3ab56-156">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="3ab56-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="3ab56-158">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="3ab56-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="3ab56-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="3ab56-160">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="3ab56-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="3ab56-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="3ab56-162">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="3ab56-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="3ab56-163">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="3ab56-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="3ab56-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="3ab56-165">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="3ab56-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="3ab56-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="3ab56-167">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="3ab56-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="3ab56-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="3ab56-169">表示用于 CC 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="3ab56-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="3ab56-170">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="3ab56-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="3ab56-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="3ab56-172">表示用于 To 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="3ab56-172">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="3ab56-173">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="3ab56-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="3ab56-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="3ab56-175">表示如果项目具有至少一个可见的附件设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="3ab56-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="3ab56-176">此属性为只读。</span><span class="sxs-lookup"><span data-stu-id="3ab56-176">This property is read only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="3ab56-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="3ab56-178">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="3ab56-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-179">区域性</span><span class="sxs-lookup"><span data-stu-id="3ab56-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="3ab56-180">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="3ab56-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-181">发件人</span><span class="sxs-lookup"><span data-stu-id="3ab56-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="3ab56-182">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="3ab56-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="3ab56-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="3ab56-184">包含邮件收件人的一组。</span><span class="sxs-lookup"><span data-stu-id="3ab56-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="3ab56-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="3ab56-186">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="3ab56-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="3ab56-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="3ab56-188">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="3ab56-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3ab56-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="3ab56-190">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="3ab56-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3ab56-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="3ab56-192">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="3ab56-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="3ab56-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="3ab56-194">包含表示此消息所属的主题的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="3ab56-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="3ab56-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="3ab56-196">表示对话标识符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-197">发件人</span><span class="sxs-lookup"><span data-stu-id="3ab56-197">From</span></span>](from.md) <br/> |<span data-ttu-id="3ab56-198">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="3ab56-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="3ab56-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="3ab56-200">表示项目的 Internet 消息标识符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="3ab56-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="3ab56-202">指示是否已读取一条消息。</span><span class="sxs-lookup"><span data-stu-id="3ab56-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="3ab56-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="3ab56-204">指示是否对电子邮件的响应请求。</span><span class="sxs-lookup"><span data-stu-id="3ab56-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-205">引用</span><span class="sxs-lookup"><span data-stu-id="3ab56-205">References</span></span>](references.md) <br/> |<span data-ttu-id="3ab56-206">代表用于将答复其原始消息关联起来新闻标头。</span><span class="sxs-lookup"><span data-stu-id="3ab56-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-207">回复</span><span class="sxs-lookup"><span data-stu-id="3ab56-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="3ab56-208">标识一组地址应向其发送答复。</span><span class="sxs-lookup"><span data-stu-id="3ab56-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="3ab56-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="3ab56-210">代表与[MeetingMessage](meetingmessage.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="3ab56-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="3ab56-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="3ab56-212">指示是否具有代理访问的帐户已处理的会议。</span><span class="sxs-lookup"><span data-stu-id="3ab56-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="3ab56-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="3ab56-214">指示会议邮件是否过期。</span><span class="sxs-lookup"><span data-stu-id="3ab56-214">Indicates whether a meeting message is out of date.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="3ab56-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="3ab56-216">指示是否会议邮件项已处理。</span><span class="sxs-lookup"><span data-stu-id="3ab56-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="3ab56-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="3ab56-218">代表收到会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="3ab56-218">Represents the kind of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-219">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="3ab56-219">MeetingRequestType</span></span>](meetingrequesttype.md) <br/> |<span data-ttu-id="3ab56-220">描述将会议请求的类型。</span><span class="sxs-lookup"><span data-stu-id="3ab56-220">Describes the type of the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-221">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="3ab56-221">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md) <br/> |<span data-ttu-id="3ab56-222">代表与会议请求相关联的日历项目的预期的状态。</span><span class="sxs-lookup"><span data-stu-id="3ab56-222">Represents the intended status for the calendar item that is associated with the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-223">Start</span><span class="sxs-lookup"><span data-stu-id="3ab56-223">Start</span></span>](start.md) <br/> |<span data-ttu-id="3ab56-224">表示日历项目的开始。</span><span class="sxs-lookup"><span data-stu-id="3ab56-224">Represents the start of a calendar item.</span></span> <span data-ttu-id="3ab56-225">此元素仅适用于日历项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-225">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-226">结束</span><span class="sxs-lookup"><span data-stu-id="3ab56-226">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3ab56-227">代表工期的结束。</span><span class="sxs-lookup"><span data-stu-id="3ab56-227">Represents the end of a duration.</span></span> <span data-ttu-id="3ab56-228">此元素仅适用于日历项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-228">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-229">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="3ab56-229">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="3ab56-230">代表日历项目的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="3ab56-230">Represents the original start time of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-231">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="3ab56-231">IsAllDayEvent</span></span>](isalldayevent.md) <br/> |<span data-ttu-id="3ab56-232">指示日历项目或会议请求是否表示全天事件。</span><span class="sxs-lookup"><span data-stu-id="3ab56-232">Indicates whether a calendar item or meeting request represents an all-day event.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-233">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="3ab56-233">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md) <br/> |<span data-ttu-id="3ab56-234">代表日历项目的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="3ab56-234">Represents the free/busy status of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-235">位置</span><span class="sxs-lookup"><span data-stu-id="3ab56-235">Location</span></span>](location.md) <br/> |<span data-ttu-id="3ab56-236">表示会议或约会的位置。</span><span class="sxs-lookup"><span data-stu-id="3ab56-236">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-237">When</span><span class="sxs-lookup"><span data-stu-id="3ab56-237">When</span></span>](when.md) <br/> |<span data-ttu-id="3ab56-238">提供会议发生的说明。</span><span class="sxs-lookup"><span data-stu-id="3ab56-238">Provides a description of when a meeting occurs.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-239">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="3ab56-239">IsMeeting</span></span>](ismeeting.md) <br/> |<span data-ttu-id="3ab56-240">指示日历项目是否会议或约会。</span><span class="sxs-lookup"><span data-stu-id="3ab56-240">Indicates whether the calendar item is either a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-241">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="3ab56-241">IsCancelled</span></span>](iscancelled.md) <br/> |<span data-ttu-id="3ab56-242">指示是否已取消约会或会议。</span><span class="sxs-lookup"><span data-stu-id="3ab56-242">Indicates whether an appointment or meeting has been cancelled.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-243">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="3ab56-243">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="3ab56-244">指示日历项目是否定期项的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ab56-244">Indicates whether a calendar item is part of a recurring item.</span></span> <span data-ttu-id="3ab56-245">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="3ab56-245">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-246">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="3ab56-246">MeetingRequestWasSent</span></span>](meetingrequestwassent.md) <br/> |<span data-ttu-id="3ab56-247">指示是否已向请求与会者发送会议请求。</span><span class="sxs-lookup"><span data-stu-id="3ab56-247">Indicates whether a meeting request has been sent to requested attendees.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-248">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="3ab56-248">CalendarItemType</span></span>](calendaritemtype.md) <br/> |<span data-ttu-id="3ab56-249">表示日历项目的匹配项的类型。</span><span class="sxs-lookup"><span data-stu-id="3ab56-249">Represents the occurrence type of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-250">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="3ab56-250">MyResponseType</span></span>](myresponsetype.md) <br/> |<span data-ttu-id="3ab56-251">包含的状态或日历项目的响应。</span><span class="sxs-lookup"><span data-stu-id="3ab56-251">Contains the status of or response to a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-252">Organizer</span><span class="sxs-lookup"><span data-stu-id="3ab56-252">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="3ab56-253">表示会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="3ab56-253">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-254">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="3ab56-254">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="3ab56-255">代表需要参加会议的与会者。</span><span class="sxs-lookup"><span data-stu-id="3ab56-255">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-256">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="3ab56-256">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="3ab56-257">表示无需参加会议的与会者。</span><span class="sxs-lookup"><span data-stu-id="3ab56-257">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-258">资源</span><span class="sxs-lookup"><span data-stu-id="3ab56-258">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="3ab56-259">表示会议的计划的资源。</span><span class="sxs-lookup"><span data-stu-id="3ab56-259">Represents a scheduled resource for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-260">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="3ab56-260">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md) <br/> |<span data-ttu-id="3ab56-261">代表与会议请求冲突的会议数。</span><span class="sxs-lookup"><span data-stu-id="3ab56-261">Represents the number of meetings that conflict with the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-262">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="3ab56-262">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md) <br/> |<span data-ttu-id="3ab56-263">表示相邻的会议时间的日历项目的总数。</span><span class="sxs-lookup"><span data-stu-id="3ab56-263">Represents the total number of calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-264">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="3ab56-264">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="3ab56-265">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-265">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-266">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="3ab56-266">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="3ab56-267">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-267">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-268">持续时间 （项）</span><span class="sxs-lookup"><span data-stu-id="3ab56-268">Duration (Items)</span></span>](duration-items.md) <br/> |<span data-ttu-id="3ab56-269">表示日历项目的持续时间。</span><span class="sxs-lookup"><span data-stu-id="3ab56-269">Represents the duration of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-270">TimeZone （项）</span><span class="sxs-lookup"><span data-stu-id="3ab56-270">TimeZone (Item)</span></span>](timezone-item.md) <br/> |<span data-ttu-id="3ab56-271">提供时区的文本的说明。</span><span class="sxs-lookup"><span data-stu-id="3ab56-271">Provides a text description of a time zone.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-272">AppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="3ab56-272">AppointmentReplyTime</span></span>](appointmentreplytime.md) <br/> |<span data-ttu-id="3ab56-273">表示对会议请求的日期和时间与会者的答复。</span><span class="sxs-lookup"><span data-stu-id="3ab56-273">Represents the date and time when an attendee replied to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-274">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="3ab56-274">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md) <br/> |<span data-ttu-id="3ab56-275">指定约会的版本的序列号。</span><span class="sxs-lookup"><span data-stu-id="3ab56-275">Specifies the sequence number of a version of an appointment.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-276">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="3ab56-276">AppointmentState</span></span>](appointmentstate.md) <br/> |<span data-ttu-id="3ab56-277">指定约会的状态。</span><span class="sxs-lookup"><span data-stu-id="3ab56-277">Specifies the status of the appointment.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-278">定期 (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="3ab56-278">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="3ab56-279">包含日历项和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="3ab56-279">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-280">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="3ab56-280">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="3ab56-281">代表定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-281">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="3ab56-282">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="3ab56-282">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-283">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="3ab56-283">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="3ab56-284">代表定期日历项目的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="3ab56-284">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="3ab56-285">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="3ab56-285">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-286">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="3ab56-286">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="3ab56-287">包含一个数组，以便它们是不同的定期主项目已修改的定期日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="3ab56-287">Contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> <span data-ttu-id="3ab56-288">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="3ab56-288">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-289">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="3ab56-289">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="3ab56-290">包含数组的定期日历项目的已删除匹配项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-290">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="3ab56-291">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="3ab56-291">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-292">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="3ab56-292">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="3ab56-293">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="3ab56-293">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-294">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="3ab56-294">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="3ab56-295">代表日历项目开始所在的时区。</span><span class="sxs-lookup"><span data-stu-id="3ab56-295">Represents the start time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-296">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="3ab56-296">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="3ab56-297">代表最终所在的时区的日历项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-297">Represents the end time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-298">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="3ab56-298">ConferenceType</span></span>](conferencetype.md) <br/> |<span data-ttu-id="3ab56-299">描述使用日历项目执行的会议类型。</span><span class="sxs-lookup"><span data-stu-id="3ab56-299">Describes the type of conferencing that is performed with a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-300">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="3ab56-300">AllowNewTimeProposal</span></span>](allownewtimeproposal.md) <br/> |<span data-ttu-id="3ab56-301">表示是否可以为会议建议的新的会议时间。</span><span class="sxs-lookup"><span data-stu-id="3ab56-301">Represents whether a new meeting time can be proposed for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-302">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="3ab56-302">IsOnlineMeeting</span></span>](isonlinemeeting.md) <br/> |<span data-ttu-id="3ab56-303">指示是否联机会议。</span><span class="sxs-lookup"><span data-stu-id="3ab56-303">Indicates whether the meeting is online.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-304">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="3ab56-304">MeetingWorkspaceUrl</span></span>](meetingworkspaceurl.md) <br/> |<span data-ttu-id="3ab56-305">包含会议工作区链接到的日历项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ab56-305">Contains the URL for the meeting workspace that is linked to by the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-306">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="3ab56-306">NetShowUrl</span></span>](netshowurl.md) <br/> |<span data-ttu-id="3ab56-307">指定 Microsoft Netshow 联机会议的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ab56-307">Specifies the URL for a Microsoft Netshow online meeting.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-308">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="3ab56-308">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="3ab56-309">包含客户端基于的项目或文件夹的权限设置的权限。</span><span class="sxs-lookup"><span data-stu-id="3ab56-309">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="3ab56-310">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="3ab56-310">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-311">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="3ab56-311">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="3ab56-312">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="3ab56-312">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-313">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="3ab56-313">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="3ab56-314">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-314">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-315">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="3ab56-315">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="3ab56-316">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="3ab56-316">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-317">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="3ab56-317">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="3ab56-318">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ab56-318">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-319">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="3ab56-319">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="3ab56-320">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="3ab56-320">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-321">ConversationId</span><span class="sxs-lookup"><span data-stu-id="3ab56-321">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="3ab56-322">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="3ab56-322">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-323">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="3ab56-323">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="3ab56-324">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="3ab56-324">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-325">UID</span><span class="sxs-lookup"><span data-stu-id="3ab56-325">UID</span></span>](uid.md) <br/> |<span data-ttu-id="3ab56-326">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-326">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-327">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="3ab56-327">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="3ab56-328">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="3ab56-328">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-329">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="3ab56-329">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="3ab56-330">指示的日期和时间创建 iCalendar 对象的实例。</span><span class="sxs-lookup"><span data-stu-id="3ab56-330">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ab56-331">父元素</span><span class="sxs-lookup"><span data-stu-id="3ab56-331">Parent elements</span></span>

|<span data-ttu-id="3ab56-332">**元素**</span><span class="sxs-lookup"><span data-stu-id="3ab56-332">**Element**</span></span>|<span data-ttu-id="3ab56-333">**说明**</span><span class="sxs-lookup"><span data-stu-id="3ab56-333">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ab56-334">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="3ab56-334">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="3ab56-335">标识所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-335">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-336">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="3ab56-336">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="3ab56-337">标识要追加到的项目的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。</span><span class="sxs-lookup"><span data-stu-id="3ab56-337">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3ab56-338">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="3ab56-338">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="3ab56-339">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-339">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-340">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="3ab56-340">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="3ab56-341">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-341">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-342">Items</span><span class="sxs-lookup"><span data-stu-id="3ab56-342">Items</span></span>](items.md) <br/> |<span data-ttu-id="3ab56-343">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="3ab56-343">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-344">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="3ab56-344">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="3ab56-345">包含项创建的数组。</span><span class="sxs-lookup"><span data-stu-id="3ab56-345">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-346">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="3ab56-346">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="3ab56-347">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="3ab56-347">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="3ab56-348">SetItemField</span><span class="sxs-lookup"><span data-stu-id="3ab56-348">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="3ab56-349">表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="3ab56-349">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="3ab56-350">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="3ab56-350">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="3ab56-351">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="3ab56-351">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ab56-352">文本值</span><span class="sxs-lookup"><span data-stu-id="3ab56-352">Text value</span></span>

<span data-ttu-id="3ab56-353">无。</span><span class="sxs-lookup"><span data-stu-id="3ab56-353">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ab56-354">备注</span><span class="sxs-lookup"><span data-stu-id="3ab56-354">Remarks</span></span>

<span data-ttu-id="3ab56-355">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3ab56-355">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ab56-356">元素信息</span><span class="sxs-lookup"><span data-stu-id="3ab56-356">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ab56-357">命名空间</span><span class="sxs-lookup"><span data-stu-id="3ab56-357">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ab56-358">架构名称</span><span class="sxs-lookup"><span data-stu-id="3ab56-358">Schema Name</span></span>  <br/> |<span data-ttu-id="3ab56-359">类型架构</span><span class="sxs-lookup"><span data-stu-id="3ab56-359">Types schema</span></span>  <br/> |
|<span data-ttu-id="3ab56-360">验证文件</span><span class="sxs-lookup"><span data-stu-id="3ab56-360">Validation File</span></span>  <br/> |<span data-ttu-id="3ab56-361">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3ab56-361">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ab56-362">可以为空</span><span class="sxs-lookup"><span data-stu-id="3ab56-362">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ab56-363">False</span><span class="sxs-lookup"><span data-stu-id="3ab56-363">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ab56-364">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3ab56-364">See also</span></span>



- [<span data-ttu-id="3ab56-365">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3ab56-365">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

