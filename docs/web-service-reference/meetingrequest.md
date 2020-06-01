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
ms.openlocfilehash: 7b39ec52d2b4fe8b3cdd2b6fd5e7ba97cfa69c7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465826"
---
# <a name="meetingrequest"></a><span data-ttu-id="44586-103">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="44586-103">MeetingRequest</span></span>

<span data-ttu-id="44586-104">**MeetingRequest**元素表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="44586-104">The **MeetingRequest** element represents a meeting request in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="44586-105">**MeetingRequestMessageType**</span><span class="sxs-lookup"><span data-stu-id="44586-105">**MeetingRequestMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44586-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="44586-106">Attributes and elements</span></span>

<span data-ttu-id="44586-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="44586-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44586-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="44586-108">Attributes</span></span>

<span data-ttu-id="44586-109">无。</span><span class="sxs-lookup"><span data-stu-id="44586-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44586-110">子元素</span><span class="sxs-lookup"><span data-stu-id="44586-110">Child elements</span></span>

|<span data-ttu-id="44586-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="44586-111">**Element**</span></span>|<span data-ttu-id="44586-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="44586-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44586-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="44586-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="44586-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="44586-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="44586-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="44586-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="44586-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="44586-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="44586-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44586-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="44586-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="44586-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="44586-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="44586-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44586-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="44586-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="44586-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="44586-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-123">主题</span><span class="sxs-lookup"><span data-stu-id="44586-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="44586-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="44586-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="44586-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="44586-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="44586-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="44586-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="44586-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="44586-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-128">Body</span><span class="sxs-lookup"><span data-stu-id="44586-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="44586-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="44586-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="44586-130">附件</span><span class="sxs-lookup"><span data-stu-id="44586-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44586-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="44586-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44586-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="44586-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="44586-133">表示接收邮箱中的项目的数据和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="44586-134">大小</span><span class="sxs-lookup"><span data-stu-id="44586-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="44586-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="44586-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="44586-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44586-137">类别</span><span class="sxs-lookup"><span data-stu-id="44586-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44586-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="44586-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="44586-139">Importance</span><span class="sxs-lookup"><span data-stu-id="44586-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="44586-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="44586-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="44586-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="44586-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="44586-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="44586-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="44586-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="44586-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="44586-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="44586-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="44586-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="44586-146">指示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="44586-146">Indicates whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="44586-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="44586-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="44586-148">指示用户是否向其自身发送了项目。</span><span class="sxs-lookup"><span data-stu-id="44586-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="44586-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="44586-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="44586-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="44586-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="44586-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="44586-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="44586-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="44586-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="44586-153">Message</span><span class="sxs-lookup"><span data-stu-id="44586-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="44586-154">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="44586-154">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44586-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="44586-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="44586-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="44586-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="44586-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="44586-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="44586-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="44586-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="44586-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="44586-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44586-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="44586-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="44586-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="44586-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="44586-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="44586-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="44586-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="44586-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="44586-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44586-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="44586-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="44586-167">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="44586-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="44586-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="44586-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="44586-169">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="44586-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="44586-170">这是所有 CC 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="44586-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="44586-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="44586-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="44586-172">表示用于 "To" 行的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="44586-172">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="44586-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="44586-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="44586-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="44586-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="44586-175">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="44586-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="44586-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-176">This property is read only.</span></span>  <br/> |
|[<span data-ttu-id="44586-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="44586-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="44586-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="44586-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="44586-179">Culture</span><span class="sxs-lookup"><span data-stu-id="44586-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="44586-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="44586-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="44586-181">发件人</span><span class="sxs-lookup"><span data-stu-id="44586-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="44586-182">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="44586-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="44586-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="44586-184">包含一组邮件的收件人。</span><span class="sxs-lookup"><span data-stu-id="44586-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="44586-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="44586-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="44586-186">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="44586-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="44586-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="44586-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="44586-188">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="44586-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="44586-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="44586-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="44586-190">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="44586-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="44586-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="44586-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="44586-192">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="44586-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="44586-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="44586-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="44586-194">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="44586-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="44586-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="44586-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="44586-196">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="44586-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="44586-197">发件人</span><span class="sxs-lookup"><span data-stu-id="44586-197">From</span></span>](from.md) <br/> |<span data-ttu-id="44586-198">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="44586-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="44586-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="44586-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="44586-200">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="44586-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="44586-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="44586-202">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="44586-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="44586-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="44586-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="44586-204">指示是否请求对电子邮件的响应。</span><span class="sxs-lookup"><span data-stu-id="44586-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="44586-205">References</span><span class="sxs-lookup"><span data-stu-id="44586-205">References</span></span>](references.md) <br/> |<span data-ttu-id="44586-206">表示用于将答复与其原始邮件关联起来的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="44586-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="44586-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="44586-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="44586-208">标识应将答复发送到的一组地址。</span><span class="sxs-lookup"><span data-stu-id="44586-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="44586-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="44586-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="44586-210">表示与[MeetingMessage](meetingmessage.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="44586-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="44586-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="44586-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="44586-212">指示是否由具有代理访问权限的帐户处理会议。</span><span class="sxs-lookup"><span data-stu-id="44586-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="44586-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="44586-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="44586-214">指示会议邮件是否已过期。</span><span class="sxs-lookup"><span data-stu-id="44586-214">Indicates whether a meeting message is out of date.</span></span>  <br/> |
|[<span data-ttu-id="44586-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="44586-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="44586-216">指示是否已处理会议邮件项。</span><span class="sxs-lookup"><span data-stu-id="44586-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="44586-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="44586-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="44586-218">表示接收会议的收件人响应的种类。</span><span class="sxs-lookup"><span data-stu-id="44586-218">Represents the kind of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-219">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="44586-219">MeetingRequestType</span></span>](meetingrequesttype.md) <br/> |<span data-ttu-id="44586-220">描述会议请求的类型。</span><span class="sxs-lookup"><span data-stu-id="44586-220">Describes the type of the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44586-221">IntendedFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="44586-221">IntendedFreeBusyStatus</span></span>](intendedfreebusystatus.md) <br/> |<span data-ttu-id="44586-222">表示与会议请求相关联的日历项目的预期状态。</span><span class="sxs-lookup"><span data-stu-id="44586-222">Represents the intended status for the calendar item that is associated with the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44586-223">开始</span><span class="sxs-lookup"><span data-stu-id="44586-223">Start</span></span>](start.md) <br/> |<span data-ttu-id="44586-224">代表日历项目的开始。</span><span class="sxs-lookup"><span data-stu-id="44586-224">Represents the start of a calendar item.</span></span> <span data-ttu-id="44586-225">此元素仅适用于日历项目的一次事件。</span><span class="sxs-lookup"><span data-stu-id="44586-225">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-226">停止</span><span class="sxs-lookup"><span data-stu-id="44586-226">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="44586-227">表示持续时间的结束。</span><span class="sxs-lookup"><span data-stu-id="44586-227">Represents the end of a duration.</span></span> <span data-ttu-id="44586-228">此元素仅适用于日历项目的一次事件。</span><span class="sxs-lookup"><span data-stu-id="44586-228">This element only applies to a single occurrence of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-229">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="44586-229">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="44586-230">表示日历项目的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="44586-230">Represents the original start time of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-231">IsAllDayEvent</span><span class="sxs-lookup"><span data-stu-id="44586-231">IsAllDayEvent</span></span>](isalldayevent.md) <br/> |<span data-ttu-id="44586-232">指示日历项目或会议请求是否代表全天事件。</span><span class="sxs-lookup"><span data-stu-id="44586-232">Indicates whether a calendar item or meeting request represents an all-day event.</span></span>  <br/> |
|[<span data-ttu-id="44586-233">LegacyFreeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="44586-233">LegacyFreeBusyStatus</span></span>](legacyfreebusystatus.md) <br/> |<span data-ttu-id="44586-234">表示日历项目的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="44586-234">Represents the free/busy status of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-235">Location</span><span class="sxs-lookup"><span data-stu-id="44586-235">Location</span></span>](location.md) <br/> |<span data-ttu-id="44586-236">代表会议或约会的位置。</span><span class="sxs-lookup"><span data-stu-id="44586-236">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="44586-237">When</span><span class="sxs-lookup"><span data-stu-id="44586-237">When</span></span>](when.md) <br/> |<span data-ttu-id="44586-238">提供会议发生时间的说明。</span><span class="sxs-lookup"><span data-stu-id="44586-238">Provides a description of when a meeting occurs.</span></span>  <br/> |
|[<span data-ttu-id="44586-239">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="44586-239">IsMeeting</span></span>](ismeeting.md) <br/> |<span data-ttu-id="44586-240">指示日历项目是会议还是约会。</span><span class="sxs-lookup"><span data-stu-id="44586-240">Indicates whether the calendar item is either a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="44586-241">IsCancelled</span><span class="sxs-lookup"><span data-stu-id="44586-241">IsCancelled</span></span>](iscancelled.md) <br/> |<span data-ttu-id="44586-242">指示约会或会议是否已被取消。</span><span class="sxs-lookup"><span data-stu-id="44586-242">Indicates whether an appointment or meeting has been cancelled.</span></span>  <br/> |
|[<span data-ttu-id="44586-243">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="44586-243">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="44586-244">指示日历项目是否是定期项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="44586-244">Indicates whether a calendar item is part of a recurring item.</span></span> <span data-ttu-id="44586-245">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-245">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44586-246">MeetingRequestWasSent</span><span class="sxs-lookup"><span data-stu-id="44586-246">MeetingRequestWasSent</span></span>](meetingrequestwassent.md) <br/> |<span data-ttu-id="44586-247">指示是否已将会议请求发送到请求的与会者。</span><span class="sxs-lookup"><span data-stu-id="44586-247">Indicates whether a meeting request has been sent to requested attendees.</span></span>  <br/> |
|[<span data-ttu-id="44586-248">CalendarItemType</span><span class="sxs-lookup"><span data-stu-id="44586-248">CalendarItemType</span></span>](calendaritemtype.md) <br/> |<span data-ttu-id="44586-249">表示日历项的发生类型。</span><span class="sxs-lookup"><span data-stu-id="44586-249">Represents the occurrence type of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-250">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="44586-250">MyResponseType</span></span>](myresponsetype.md) <br/> |<span data-ttu-id="44586-251">包含日历项目的状态或响应。</span><span class="sxs-lookup"><span data-stu-id="44586-251">Contains the status of or response to a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-252">Organizer</span><span class="sxs-lookup"><span data-stu-id="44586-252">Organizer</span></span>](organizer.md) <br/> |<span data-ttu-id="44586-253">表示会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="44586-253">Represents the organizer of a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-254">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="44586-254">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="44586-255">表示参加会议所需的与会者。</span><span class="sxs-lookup"><span data-stu-id="44586-255">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-256">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="44586-256">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="44586-257">表示参加会议不需要的与会者。</span><span class="sxs-lookup"><span data-stu-id="44586-257">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-258">资源</span><span class="sxs-lookup"><span data-stu-id="44586-258">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="44586-259">表示会议的计划资源。</span><span class="sxs-lookup"><span data-stu-id="44586-259">Represents a scheduled resource for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-260">ConflictingMeetingCount</span><span class="sxs-lookup"><span data-stu-id="44586-260">ConflictingMeetingCount</span></span>](conflictingmeetingcount.md) <br/> |<span data-ttu-id="44586-261">表示与会议请求发生冲突的会议数。</span><span class="sxs-lookup"><span data-stu-id="44586-261">Represents the number of meetings that conflict with the meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44586-262">AdjacentMeetingCount</span><span class="sxs-lookup"><span data-stu-id="44586-262">AdjacentMeetingCount</span></span>](adjacentmeetingcount.md) <br/> |<span data-ttu-id="44586-263">表示与会议时间相邻的日历项目的总数。</span><span class="sxs-lookup"><span data-stu-id="44586-263">Represents the total number of calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="44586-264">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="44586-264">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="44586-265">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="44586-265">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="44586-266">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="44586-266">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="44586-267">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="44586-267">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="44586-268">持续时间（项目）</span><span class="sxs-lookup"><span data-stu-id="44586-268">Duration (Items)</span></span>](duration-items.md) <br/> |<span data-ttu-id="44586-269">表示日历项的持续时间。</span><span class="sxs-lookup"><span data-stu-id="44586-269">Represents the duration of a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-270">时区（项目）</span><span class="sxs-lookup"><span data-stu-id="44586-270">TimeZone (Item)</span></span>](timezone-item.md) <br/> |<span data-ttu-id="44586-271">提供时区的文本说明。</span><span class="sxs-lookup"><span data-stu-id="44586-271">Provides a text description of a time zone.</span></span>  <br/> |
|[<span data-ttu-id="44586-272">AppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="44586-272">AppointmentReplyTime</span></span>](appointmentreplytime.md) <br/> |<span data-ttu-id="44586-273">表示与会者答复会议请求的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-273">Represents the date and time when an attendee replied to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="44586-274">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="44586-274">AppointmentSequenceNumber</span></span>](appointmentsequencenumber.md) <br/> |<span data-ttu-id="44586-275">指定约会的一个版本的序列号。</span><span class="sxs-lookup"><span data-stu-id="44586-275">Specifies the sequence number of a version of an appointment.</span></span>  <br/> |
|[<span data-ttu-id="44586-276">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="44586-276">AppointmentState</span></span>](appointmentstate.md) <br/> |<span data-ttu-id="44586-277">指定约会的状态。</span><span class="sxs-lookup"><span data-stu-id="44586-277">Specifies the status of the appointment.</span></span>  <br/> |
|[<span data-ttu-id="44586-278">重复周期（RecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="44586-278">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="44586-279">包含日历项目和会议请求的定期模式。</span><span class="sxs-lookup"><span data-stu-id="44586-279">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="44586-280">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="44586-280">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="44586-281">表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="44586-281">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="44586-282">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="44586-282">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="44586-283">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="44586-283">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="44586-284">表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="44586-284">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="44586-285">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="44586-285">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="44586-286">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="44586-286">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="44586-287">包含已修改的定期日历项目匹配项的数组，以便它们不同于定期主项目。</span><span class="sxs-lookup"><span data-stu-id="44586-287">Contains an array of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> <span data-ttu-id="44586-288">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="44586-288">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="44586-289">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="44586-289">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="44586-290">包含定期日历项目的已删除事件数组。</span><span class="sxs-lookup"><span data-stu-id="44586-290">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> <span data-ttu-id="44586-291">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="44586-291">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span>  <br/> |
|[<span data-ttu-id="44586-292">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="44586-292">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="44586-293">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="44586-293">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
|[<span data-ttu-id="44586-294">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="44586-294">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="44586-295">表示日历项目的起始时区。</span><span class="sxs-lookup"><span data-stu-id="44586-295">Represents the start time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-296">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="44586-296">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="44586-297">表示日历项目的结束时区。</span><span class="sxs-lookup"><span data-stu-id="44586-297">Represents the end time zone of the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-298">ConferenceType</span><span class="sxs-lookup"><span data-stu-id="44586-298">ConferenceType</span></span>](conferencetype.md) <br/> |<span data-ttu-id="44586-299">介绍使用日历项目执行的会议的类型。</span><span class="sxs-lookup"><span data-stu-id="44586-299">Describes the type of conferencing that is performed with a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-300">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="44586-300">AllowNewTimeProposal</span></span>](allownewtimeproposal.md) <br/> |<span data-ttu-id="44586-301">表示是否可以为会议建议新的会议时间。</span><span class="sxs-lookup"><span data-stu-id="44586-301">Represents whether a new meeting time can be proposed for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-302">IsOnlineMeeting</span><span class="sxs-lookup"><span data-stu-id="44586-302">IsOnlineMeeting</span></span>](isonlinemeeting.md) <br/> |<span data-ttu-id="44586-303">指示会议是否处于联机状态。</span><span class="sxs-lookup"><span data-stu-id="44586-303">Indicates whether the meeting is online.</span></span>  <br/> |
|[<span data-ttu-id="44586-304">MeetingWorkspaceUrl</span><span class="sxs-lookup"><span data-stu-id="44586-304">MeetingWorkspaceUrl</span></span>](meetingworkspaceurl.md) <br/> |<span data-ttu-id="44586-305">包含由日历项目链接到的会议工作区的 URL。</span><span class="sxs-lookup"><span data-stu-id="44586-305">Contains the URL for the meeting workspace that is linked to by the calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-306">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="44586-306">NetShowUrl</span></span>](netshowurl.md) <br/> |<span data-ttu-id="44586-307">指定 Microsoft Netshow online 会议的 URL。</span><span class="sxs-lookup"><span data-stu-id="44586-307">Specifies the URL for a Microsoft Netshow online meeting.</span></span>  <br/> |
|[<span data-ttu-id="44586-308">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="44586-308">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="44586-309">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="44586-309">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="44586-310">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="44586-310">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="44586-311">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="44586-311">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="44586-312">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="44586-312">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="44586-313">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="44586-313">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="44586-314">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="44586-314">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="44586-315">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="44586-315">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="44586-316">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="44586-316">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="44586-317">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="44586-317">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="44586-318">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="44586-318">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="44586-319">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="44586-319">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="44586-320">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="44586-320">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="44586-321">ConversationId</span><span class="sxs-lookup"><span data-stu-id="44586-321">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="44586-322">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="44586-322">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="44586-323">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="44586-323">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="44586-324">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="44586-324">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="44586-325">UID</span><span class="sxs-lookup"><span data-stu-id="44586-325">UID</span></span>](uid.md) <br/> |<span data-ttu-id="44586-326">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="44586-326">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-327">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="44586-327">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="44586-328">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="44586-328">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44586-329">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="44586-329">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="44586-330">指示 iCalendar 对象的实例的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="44586-330">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44586-331">父元素</span><span class="sxs-lookup"><span data-stu-id="44586-331">Parent elements</span></span>

|<span data-ttu-id="44586-332">**元素**</span><span class="sxs-lookup"><span data-stu-id="44586-332">**Element**</span></span>|<span data-ttu-id="44586-333">**说明**</span><span class="sxs-lookup"><span data-stu-id="44586-333">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44586-334">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="44586-334">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="44586-335">标识与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="44586-335">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="44586-336">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="44586-336">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="44586-337">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="44586-337">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="44586-338">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="44586-338">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="44586-339">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="44586-339">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="44586-340">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="44586-340">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="44586-341">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="44586-341">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="44586-342">Items</span><span class="sxs-lookup"><span data-stu-id="44586-342">Items</span></span>](items.md) <br/> |<span data-ttu-id="44586-343">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="44586-343">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="44586-344">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="44586-344">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="44586-345">包含要创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="44586-345">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="44586-346">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="44586-346">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="44586-347">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="44586-347">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="44586-348">SetItemField</span><span class="sxs-lookup"><span data-stu-id="44586-348">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="44586-349">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="44586-349">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="44586-350">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="44586-350">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="44586-351">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="44586-351">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44586-352">文本值</span><span class="sxs-lookup"><span data-stu-id="44586-352">Text value</span></span>

<span data-ttu-id="44586-353">无。</span><span class="sxs-lookup"><span data-stu-id="44586-353">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44586-354">说明</span><span class="sxs-lookup"><span data-stu-id="44586-354">Remarks</span></span>

<span data-ttu-id="44586-355">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="44586-355">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44586-356">元素信息</span><span class="sxs-lookup"><span data-stu-id="44586-356">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44586-357">命名空间</span><span class="sxs-lookup"><span data-stu-id="44586-357">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44586-358">架构名称</span><span class="sxs-lookup"><span data-stu-id="44586-358">Schema Name</span></span>  <br/> |<span data-ttu-id="44586-359">类型架构</span><span class="sxs-lookup"><span data-stu-id="44586-359">Types schema</span></span>  <br/> |
|<span data-ttu-id="44586-360">验证文件</span><span class="sxs-lookup"><span data-stu-id="44586-360">Validation File</span></span>  <br/> |<span data-ttu-id="44586-361">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44586-361">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44586-362">可以为空</span><span class="sxs-lookup"><span data-stu-id="44586-362">Can be Empty</span></span>  <br/> |<span data-ttu-id="44586-363">False</span><span class="sxs-lookup"><span data-stu-id="44586-363">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44586-364">另请参阅</span><span class="sxs-lookup"><span data-stu-id="44586-364">See also</span></span>



- [<span data-ttu-id="44586-365">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="44586-365">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

