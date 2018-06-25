---
title: MeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingResponse
api_type:
- schema
ms.assetid: 9f798e79-dafd-4d4d-9967-95fd8e5c0502
description: MeetingResponse 元素均表示 Exchange 存储中的会议响应。
ms.openlocfilehash: c5f9f3ac2fcd12e9c95f663311c33cdd36783251
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826446"
---
# <a name="meetingresponse"></a><span data-ttu-id="c87a5-103">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="c87a5-103">MeetingResponse</span></span>

<span data-ttu-id="c87a5-104">**MeetingResponse**元素均表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="c87a5-104">The **MeetingResponse** element represents a meeting response in the Exchange store.</span></span> 
  
```xml
<MeetingResponse>
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
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</MeetingResponse>
```

 <span data-ttu-id="c87a5-105">**MeetingResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c87a5-105">**MeetingResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c87a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c87a5-106">Attributes and elements</span></span>

<span data-ttu-id="c87a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c87a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c87a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="c87a5-108">Attributes</span></span>

<span data-ttu-id="c87a5-109">无。</span><span class="sxs-lookup"><span data-stu-id="c87a5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c87a5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c87a5-110">Child elements</span></span>

|<span data-ttu-id="c87a5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c87a5-111">**Element**</span></span>|<span data-ttu-id="c87a5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c87a5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c87a5-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="c87a5-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="c87a5-114">包含一个对象，表示 base64Binary 格式的本机 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="c87a5-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="c87a5-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="c87a5-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="c87a5-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="c87a5-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="c87a5-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="c87a5-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="c87a5-119">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="c87a5-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="c87a5-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="c87a5-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="c87a5-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="c87a5-122">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="c87a5-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-123">Subject</span><span class="sxs-lookup"><span data-stu-id="c87a5-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="c87a5-124">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="c87a5-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="c87a5-125">主题被限制为 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="c87a5-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="c87a5-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="c87a5-127">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="c87a5-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-128">Body</span><span class="sxs-lookup"><span data-stu-id="c87a5-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="c87a5-129">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="c87a5-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-130">附件</span><span class="sxs-lookup"><span data-stu-id="c87a5-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c87a5-131">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="c87a5-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="c87a5-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="c87a5-133">代表的数据和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="c87a5-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-134">Size</span><span class="sxs-lookup"><span data-stu-id="c87a5-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="c87a5-135">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="c87a5-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="c87a5-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="c87a5-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-137">类别</span><span class="sxs-lookup"><span data-stu-id="c87a5-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="c87a5-138">表示标识的邮箱中项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="c87a5-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-139">Importance</span><span class="sxs-lookup"><span data-stu-id="c87a5-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="c87a5-140">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="c87a5-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="c87a5-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="c87a5-142">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="c87a5-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="c87a5-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="c87a5-144">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="c87a5-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="c87a5-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="c87a5-146">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="c87a5-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="c87a5-148">指示用户是否发送到他或她自己的项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="c87a5-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="c87a5-150">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="c87a5-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="c87a5-152">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="c87a5-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="c87a5-154">代表包含在邮箱中项目的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="c87a5-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="c87a5-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="c87a5-156">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="c87a5-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="c87a5-158">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="c87a5-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="c87a5-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="c87a5-160">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="c87a5-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="c87a5-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="c87a5-162">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="c87a5-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="c87a5-163">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="c87a5-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="c87a5-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="c87a5-165">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="c87a5-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="c87a5-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="c87a5-167">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="c87a5-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="c87a5-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="c87a5-169">表示用于抄送框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="c87a5-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="c87a5-170">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="c87a5-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="c87a5-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="c87a5-172">表示用于收件人框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="c87a5-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="c87a5-173">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="c87a5-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="c87a5-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="c87a5-175">表示如果项目具有至少一个可见的附件设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="c87a5-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="c87a5-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="c87a5-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="c87a5-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="c87a5-178">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="c87a5-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-179">区域性</span><span class="sxs-lookup"><span data-stu-id="c87a5-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="c87a5-180">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="c87a5-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-181">发件人</span><span class="sxs-lookup"><span data-stu-id="c87a5-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="c87a5-182">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="c87a5-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="c87a5-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="c87a5-184">包含邮件收件人的一组。</span><span class="sxs-lookup"><span data-stu-id="c87a5-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="c87a5-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="c87a5-186">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="c87a5-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="c87a5-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="c87a5-188">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="c87a5-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c87a5-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="c87a5-190">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="c87a5-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c87a5-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="c87a5-192">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="c87a5-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="c87a5-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="c87a5-194">包含表示此消息所属的主题的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="c87a5-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="c87a5-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="c87a5-196">表示对话标识符。</span><span class="sxs-lookup"><span data-stu-id="c87a5-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-197">发件人</span><span class="sxs-lookup"><span data-stu-id="c87a5-197">From</span></span>](from.md) <br/> |<span data-ttu-id="c87a5-198">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="c87a5-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="c87a5-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="c87a5-200">表示项目的 Internet 消息标识符。</span><span class="sxs-lookup"><span data-stu-id="c87a5-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="c87a5-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="c87a5-202">指示是否已读取一条消息。</span><span class="sxs-lookup"><span data-stu-id="c87a5-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="c87a5-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="c87a5-204">指示是否对电子邮件的响应请求。</span><span class="sxs-lookup"><span data-stu-id="c87a5-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-205">引用</span><span class="sxs-lookup"><span data-stu-id="c87a5-205">References</span></span>](references.md) <br/> |<span data-ttu-id="c87a5-206">代表用于将答复其原始消息关联起来新闻标头。</span><span class="sxs-lookup"><span data-stu-id="c87a5-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-207">回复</span><span class="sxs-lookup"><span data-stu-id="c87a5-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="c87a5-208">标识一组地址应向其发送答复。</span><span class="sxs-lookup"><span data-stu-id="c87a5-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="c87a5-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="c87a5-210">代表与[MeetingMessage](meetingmessage.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="c87a5-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="c87a5-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="c87a5-212">指示是否具有代理访问的帐户已处理的会议。</span><span class="sxs-lookup"><span data-stu-id="c87a5-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="c87a5-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="c87a5-214">指示会议邮件是否过期。</span><span class="sxs-lookup"><span data-stu-id="c87a5-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="c87a5-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="c87a5-216">指示是否会议邮件项已处理。</span><span class="sxs-lookup"><span data-stu-id="c87a5-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="c87a5-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="c87a5-218">代表收到会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="c87a5-218">Represents the type of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="c87a5-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="c87a5-220">包含客户端的权利基础的项或文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="c87a5-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="c87a5-221">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="c87a5-221">This element is read-only.</span></span> <span data-ttu-id="c87a5-222">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c87a5-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="c87a5-223">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="c87a5-223">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="c87a5-224">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="c87a5-224">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="c87a5-225">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c87a5-225">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-226">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="c87a5-226">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="c87a5-227">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="c87a5-227">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="c87a5-228">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c87a5-228">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-229">UID</span><span class="sxs-lookup"><span data-stu-id="c87a5-229">UID</span></span>](uid.md) <br/> |<span data-ttu-id="c87a5-230">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-230">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-231">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c87a5-231">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="c87a5-232">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="c87a5-232">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-233">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="c87a5-233">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="c87a5-234">指示的日期和时间创建 iCalendar 对象的实例。</span><span class="sxs-lookup"><span data-stu-id="c87a5-234">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c87a5-235">父元素</span><span class="sxs-lookup"><span data-stu-id="c87a5-235">Parent elements</span></span>

|<span data-ttu-id="c87a5-236">**元素**</span><span class="sxs-lookup"><span data-stu-id="c87a5-236">**Element**</span></span>|<span data-ttu-id="c87a5-237">**说明**</span><span class="sxs-lookup"><span data-stu-id="c87a5-237">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c87a5-238">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="c87a5-238">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="c87a5-239">标识所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-239">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-240">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c87a5-240">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="c87a5-241">标识要追加到的项目的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。</span><span class="sxs-lookup"><span data-stu-id="c87a5-241">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c87a5-242">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="c87a5-242">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="c87a5-243">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-243">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-244">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c87a5-244">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="c87a5-245">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="c87a5-245">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-246">Items</span><span class="sxs-lookup"><span data-stu-id="c87a5-246">Items</span></span>](items.md) <br/> |<span data-ttu-id="c87a5-247">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="c87a5-247">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-248">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c87a5-248">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="c87a5-249">包含项创建的数组。</span><span class="sxs-lookup"><span data-stu-id="c87a5-249">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-250">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="c87a5-250">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="c87a5-251">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="c87a5-251">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="c87a5-252">SetItemField</span><span class="sxs-lookup"><span data-stu-id="c87a5-252">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="c87a5-253">表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c87a5-253">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="c87a5-254">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="c87a5-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="c87a5-255">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="c87a5-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c87a5-256">备注</span><span class="sxs-lookup"><span data-stu-id="c87a5-256">Remarks</span></span>

<span data-ttu-id="c87a5-257">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c87a5-257">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c87a5-258">元素信息</span><span class="sxs-lookup"><span data-stu-id="c87a5-258">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c87a5-259">命名空间</span><span class="sxs-lookup"><span data-stu-id="c87a5-259">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c87a5-260">架构名称</span><span class="sxs-lookup"><span data-stu-id="c87a5-260">Schema Name</span></span>  <br/> |<span data-ttu-id="c87a5-261">类型架构</span><span class="sxs-lookup"><span data-stu-id="c87a5-261">Types schema</span></span>  <br/> |
|<span data-ttu-id="c87a5-262">验证文件</span><span class="sxs-lookup"><span data-stu-id="c87a5-262">Validation File</span></span>  <br/> |<span data-ttu-id="c87a5-263">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c87a5-263">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c87a5-264">可以为空</span><span class="sxs-lookup"><span data-stu-id="c87a5-264">Can be Empty</span></span>  <br/> |<span data-ttu-id="c87a5-265">False</span><span class="sxs-lookup"><span data-stu-id="c87a5-265">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c87a5-266">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c87a5-266">See also</span></span>



- [<span data-ttu-id="c87a5-267">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c87a5-267">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

