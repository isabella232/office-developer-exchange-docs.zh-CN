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
description: MeetingResponse 元素表示 Exchange 存储中的会议响应。
ms.openlocfilehash: ff999a671c0321586fbc2adae6cbb5c1ad117ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467695"
---
# <a name="meetingresponse"></a><span data-ttu-id="083ec-103">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="083ec-103">MeetingResponse</span></span>

<span data-ttu-id="083ec-104">**MeetingResponse**元素表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="083ec-104">The **MeetingResponse** element represents a meeting response in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="083ec-105">**MeetingResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="083ec-105">**MeetingResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="083ec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="083ec-106">Attributes and elements</span></span>

<span data-ttu-id="083ec-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="083ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="083ec-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="083ec-108">Attributes</span></span>

<span data-ttu-id="083ec-109">无。</span><span class="sxs-lookup"><span data-stu-id="083ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="083ec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="083ec-110">Child elements</span></span>

|<span data-ttu-id="083ec-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="083ec-111">**Element**</span></span>|<span data-ttu-id="083ec-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="083ec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="083ec-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="083ec-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="083ec-114">包含以 base64Binary 格式表示的对象的本机 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="083ec-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="083ec-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="083ec-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="083ec-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="083ec-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="083ec-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="083ec-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="083ec-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="083ec-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="083ec-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="083ec-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="083ec-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="083ec-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="083ec-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="083ec-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="083ec-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="083ec-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-123">主题</span><span class="sxs-lookup"><span data-stu-id="083ec-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="083ec-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="083ec-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="083ec-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="083ec-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="083ec-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="083ec-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="083ec-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="083ec-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-128">Body</span><span class="sxs-lookup"><span data-stu-id="083ec-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="083ec-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="083ec-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="083ec-130">附件</span><span class="sxs-lookup"><span data-stu-id="083ec-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="083ec-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="083ec-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="083ec-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="083ec-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="083ec-133">表示接收邮箱中的项目的数据和时间。</span><span class="sxs-lookup"><span data-stu-id="083ec-133">Represents the data and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="083ec-134">大小</span><span class="sxs-lookup"><span data-stu-id="083ec-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="083ec-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="083ec-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="083ec-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="083ec-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="083ec-137">类别</span><span class="sxs-lookup"><span data-stu-id="083ec-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="083ec-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="083ec-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="083ec-139">Importance</span><span class="sxs-lookup"><span data-stu-id="083ec-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="083ec-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="083ec-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="083ec-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="083ec-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="083ec-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="083ec-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="083ec-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="083ec-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="083ec-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="083ec-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="083ec-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="083ec-146">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="083ec-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="083ec-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="083ec-148">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="083ec-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="083ec-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="083ec-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="083ec-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="083ec-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="083ec-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="083ec-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="083ec-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="083ec-153">Message</span><span class="sxs-lookup"><span data-stu-id="083ec-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="083ec-154">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="083ec-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="083ec-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="083ec-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="083ec-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="083ec-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="083ec-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="083ec-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="083ec-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="083ec-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="083ec-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="083ec-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="083ec-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="083ec-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="083ec-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="083ec-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="083ec-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="083ec-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="083ec-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="083ec-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="083ec-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="083ec-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="083ec-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="083ec-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="083ec-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="083ec-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="083ec-167">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="083ec-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="083ec-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="083ec-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="083ec-169">表示用于 "抄送" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="083ec-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="083ec-170">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="083ec-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="083ec-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="083ec-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="083ec-172">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="083ec-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="083ec-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="083ec-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="083ec-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="083ec-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="083ec-175">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="083ec-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="083ec-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="083ec-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="083ec-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="083ec-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="083ec-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="083ec-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="083ec-179">Culture</span><span class="sxs-lookup"><span data-stu-id="083ec-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="083ec-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="083ec-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="083ec-181">发件人</span><span class="sxs-lookup"><span data-stu-id="083ec-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="083ec-182">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="083ec-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="083ec-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="083ec-184">包含一组邮件的收件人。</span><span class="sxs-lookup"><span data-stu-id="083ec-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="083ec-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="083ec-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="083ec-186">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="083ec-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="083ec-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="083ec-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="083ec-188">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="083ec-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="083ec-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="083ec-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="083ec-190">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="083ec-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="083ec-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="083ec-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="083ec-192">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="083ec-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="083ec-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="083ec-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="083ec-194">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="083ec-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="083ec-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="083ec-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="083ec-196">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="083ec-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="083ec-197">发件人</span><span class="sxs-lookup"><span data-stu-id="083ec-197">From</span></span>](from.md) <br/> |<span data-ttu-id="083ec-198">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="083ec-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="083ec-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="083ec-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="083ec-200">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="083ec-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="083ec-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="083ec-202">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="083ec-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="083ec-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="083ec-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="083ec-204">指示是否请求对电子邮件的响应。</span><span class="sxs-lookup"><span data-stu-id="083ec-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="083ec-205">References</span><span class="sxs-lookup"><span data-stu-id="083ec-205">References</span></span>](references.md) <br/> |<span data-ttu-id="083ec-206">表示用于将答复与其原始邮件关联起来的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="083ec-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="083ec-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="083ec-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="083ec-208">标识应将答复发送到的一组地址。</span><span class="sxs-lookup"><span data-stu-id="083ec-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="083ec-209">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="083ec-209">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="083ec-210">表示与[MeetingMessage](meetingmessage.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-210">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="083ec-211">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="083ec-211">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="083ec-212">指示是否由具有代理访问权限的帐户处理会议。</span><span class="sxs-lookup"><span data-stu-id="083ec-212">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="083ec-213">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="083ec-213">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="083ec-214">指示会议邮件是否已过期。</span><span class="sxs-lookup"><span data-stu-id="083ec-214">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="083ec-215">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="083ec-215">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="083ec-216">指示是否已处理会议邮件项。</span><span class="sxs-lookup"><span data-stu-id="083ec-216">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="083ec-217">ResponseType</span><span class="sxs-lookup"><span data-stu-id="083ec-217">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="083ec-218">表示接收会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="083ec-218">Represents the type of recipient response that is received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="083ec-219">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="083ec-219">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="083ec-220">包含客户端的权利基础的项或文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="083ec-220">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="083ec-221">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="083ec-221">This element is read-only.</span></span> <span data-ttu-id="083ec-222">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="083ec-222">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="083ec-223">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="083ec-223">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="083ec-224">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="083ec-224">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="083ec-225">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="083ec-225">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="083ec-226">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="083ec-226">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="083ec-227">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="083ec-227">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="083ec-228">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="083ec-228">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="083ec-229">UID</span><span class="sxs-lookup"><span data-stu-id="083ec-229">UID</span></span>](uid.md) <br/> |<span data-ttu-id="083ec-230">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-230">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-231">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="083ec-231">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="083ec-232">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="083ec-232">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-233">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="083ec-233">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="083ec-234">指示 iCalendar 对象的实例的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="083ec-234">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="083ec-235">父元素</span><span class="sxs-lookup"><span data-stu-id="083ec-235">Parent elements</span></span>

|<span data-ttu-id="083ec-236">**元素**</span><span class="sxs-lookup"><span data-stu-id="083ec-236">**Element**</span></span>|<span data-ttu-id="083ec-237">**说明**</span><span class="sxs-lookup"><span data-stu-id="083ec-237">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="083ec-238">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="083ec-238">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="083ec-239">标识与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-239">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="083ec-240">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="083ec-240">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="083ec-241">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="083ec-241">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="083ec-242">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="083ec-242">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="083ec-243">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-243">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="083ec-244">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="083ec-244">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="083ec-245">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-245">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="083ec-246">Items</span><span class="sxs-lookup"><span data-stu-id="083ec-246">Items</span></span>](items.md) <br/> |<span data-ttu-id="083ec-247">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="083ec-247">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="083ec-248">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="083ec-248">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="083ec-249">包含要创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="083ec-249">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="083ec-250">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="083ec-250">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="083ec-251">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-251">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="083ec-252">SetItemField</span><span class="sxs-lookup"><span data-stu-id="083ec-252">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="083ec-253">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="083ec-253">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="083ec-254">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="083ec-254">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="083ec-255">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="083ec-255">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="083ec-256">说明</span><span class="sxs-lookup"><span data-stu-id="083ec-256">Remarks</span></span>

<span data-ttu-id="083ec-257">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="083ec-257">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="083ec-258">元素信息</span><span class="sxs-lookup"><span data-stu-id="083ec-258">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="083ec-259">命名空间</span><span class="sxs-lookup"><span data-stu-id="083ec-259">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="083ec-260">架构名称</span><span class="sxs-lookup"><span data-stu-id="083ec-260">Schema Name</span></span>  <br/> |<span data-ttu-id="083ec-261">类型架构</span><span class="sxs-lookup"><span data-stu-id="083ec-261">Types schema</span></span>  <br/> |
|<span data-ttu-id="083ec-262">验证文件</span><span class="sxs-lookup"><span data-stu-id="083ec-262">Validation File</span></span>  <br/> |<span data-ttu-id="083ec-263">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="083ec-263">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="083ec-264">可以为空</span><span class="sxs-lookup"><span data-stu-id="083ec-264">Can be Empty</span></span>  <br/> |<span data-ttu-id="083ec-265">False</span><span class="sxs-lookup"><span data-stu-id="083ec-265">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="083ec-266">另请参阅</span><span class="sxs-lookup"><span data-stu-id="083ec-266">See also</span></span>



- [<span data-ttu-id="083ec-267">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="083ec-267">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

