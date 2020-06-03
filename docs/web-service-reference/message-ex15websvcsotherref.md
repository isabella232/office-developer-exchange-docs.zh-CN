---
title: 消息
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 2400b33c-43b2-4fc2-b6fb-275a99e0e810
description: Message 元素表示 Microsoft Exchange 电子邮件。
ms.openlocfilehash: 510e97572e54f0ea0cb65fc7c75910e69cc0651f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467779"
---
# <a name="message"></a><span data-ttu-id="fa6db-103">消息</span><span class="sxs-lookup"><span data-stu-id="fa6db-103">Message</span></span>

<span data-ttu-id="fa6db-104">**Message**元素表示 Microsoft Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="fa6db-104">The **Message** element represents a Microsoft Exchange e-mail message.</span></span> 
  
```xml
<Message>
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
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <ReminderMessageData/>
</Message>
```

 <span data-ttu-id="fa6db-105">**MessageType**</span><span class="sxs-lookup"><span data-stu-id="fa6db-105">**MessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa6db-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa6db-106">Attributes and elements</span></span>

<span data-ttu-id="fa6db-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa6db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa6db-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fa6db-108">Attributes</span></span>

<span data-ttu-id="fa6db-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa6db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa6db-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa6db-110">Child elements</span></span>

|<span data-ttu-id="fa6db-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa6db-111">**Element**</span></span>|<span data-ttu-id="fa6db-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa6db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6db-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="fa6db-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="fa6db-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="fa6db-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="fa6db-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fa6db-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="fa6db-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="fa6db-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fa6db-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="fa6db-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="fa6db-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="fa6db-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fa6db-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="fa6db-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="fa6db-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="fa6db-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-123">主题</span><span class="sxs-lookup"><span data-stu-id="fa6db-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="fa6db-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="fa6db-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="fa6db-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="fa6db-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="fa6db-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="fa6db-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-128">Body</span><span class="sxs-lookup"><span data-stu-id="fa6db-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="fa6db-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="fa6db-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-130">附件</span><span class="sxs-lookup"><span data-stu-id="fa6db-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fa6db-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="fa6db-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="fa6db-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="fa6db-133">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fa6db-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-134">大小</span><span class="sxs-lookup"><span data-stu-id="fa6db-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="fa6db-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="fa6db-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="fa6db-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fa6db-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-137">类别</span><span class="sxs-lookup"><span data-stu-id="fa6db-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fa6db-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="fa6db-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-139">Importance</span><span class="sxs-lookup"><span data-stu-id="fa6db-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="fa6db-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="fa6db-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="fa6db-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="fa6db-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fa6db-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="fa6db-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa6db-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="fa6db-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="fa6db-146">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="fa6db-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="fa6db-148">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="fa6db-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="fa6db-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="fa6db-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="fa6db-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="fa6db-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="fa6db-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-153">Message</span><span class="sxs-lookup"><span data-stu-id="fa6db-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="fa6db-154">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="fa6db-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="fa6db-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="fa6db-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fa6db-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="fa6db-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="fa6db-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fa6db-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="fa6db-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="fa6db-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="fa6db-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="fa6db-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="fa6db-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fa6db-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="fa6db-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="fa6db-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="fa6db-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="fa6db-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="fa6db-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="fa6db-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="fa6db-167">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="fa6db-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="fa6db-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="fa6db-169">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="fa6db-169">Represents the display string that is used for the contents of the CC line.</span></span> <span data-ttu-id="fa6db-170">这是所有 CC 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="fa6db-170">This is the concatenated string of all CC recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="fa6db-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="fa6db-172">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="fa6db-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="fa6db-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="fa6db-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="fa6db-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="fa6db-175">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="fa6db-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="fa6db-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fa6db-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="fa6db-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="fa6db-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="fa6db-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-179">Culture</span><span class="sxs-lookup"><span data-stu-id="fa6db-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="fa6db-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="fa6db-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-181">发件人</span><span class="sxs-lookup"><span data-stu-id="fa6db-181">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="fa6db-182">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="fa6db-182">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-183">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="fa6db-183">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="fa6db-184">包含一组邮件的收件人。</span><span class="sxs-lookup"><span data-stu-id="fa6db-184">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-185">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="fa6db-185">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="fa6db-186">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="fa6db-186">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-187">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="fa6db-187">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="fa6db-188">表示接收电子邮件的密件抄送（Bcc）的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="fa6db-188">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-189">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="fa6db-189">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="fa6db-190">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="fa6db-190">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-191">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="fa6db-191">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="fa6db-192">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="fa6db-192">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-193">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="fa6db-193">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="fa6db-194">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="fa6db-194">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-195">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="fa6db-195">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="fa6db-196">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-196">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-197">发件人</span><span class="sxs-lookup"><span data-stu-id="fa6db-197">From</span></span>](from.md) <br/> |<span data-ttu-id="fa6db-198">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="fa6db-198">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-199">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="fa6db-199">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="fa6db-200">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-200">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-201">IsRead</span><span class="sxs-lookup"><span data-stu-id="fa6db-201">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="fa6db-202">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="fa6db-202">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-203">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="fa6db-203">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="fa6db-204">指示是否请求对电子邮件的响应。</span><span class="sxs-lookup"><span data-stu-id="fa6db-204">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-205">References</span><span class="sxs-lookup"><span data-stu-id="fa6db-205">References</span></span>](references.md) <br/> |<span data-ttu-id="fa6db-206">表示用于将答复与其原始邮件关联起来的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="fa6db-206">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-207">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="fa6db-207">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="fa6db-208">标识应将答复发送到的一组地址。</span><span class="sxs-lookup"><span data-stu-id="fa6db-208">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-209">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="fa6db-209">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="fa6db-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="fa6db-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-212">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="fa6db-212">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="fa6db-213">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="fa6db-213">Identifies the delegate in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-214">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="fa6db-214">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="fa6db-215">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="fa6db-215">Identifies the principal in a delegate access scenario.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-216">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="fa6db-216">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="fa6db-217">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="fa6db-217">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-218">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="fa6db-218">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="fa6db-219">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="fa6db-219">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-220">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="fa6db-220">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="fa6db-221">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="fa6db-221">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-222">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fa6db-222">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="fa6db-223">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="fa6db-223">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-224">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fa6db-224">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="fa6db-225">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="fa6db-225">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-226">ConversationId</span><span class="sxs-lookup"><span data-stu-id="fa6db-226">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="fa6db-227">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="fa6db-227">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-228">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="fa6db-228">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="fa6db-229">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="fa6db-229">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-230">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="fa6db-230">ReminderMessageData</span></span>](remindermessagedata.md) <br/> |<span data-ttu-id="fa6db-231">包含提醒邮件的数据。</span><span class="sxs-lookup"><span data-stu-id="fa6db-231">Contains the data for a reminder message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa6db-232">父元素</span><span class="sxs-lookup"><span data-stu-id="fa6db-232">Parent elements</span></span>

|<span data-ttu-id="fa6db-233">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa6db-233">**Element**</span></span>|<span data-ttu-id="fa6db-234">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa6db-234">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6db-235">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="fa6db-235">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="fa6db-236">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-236">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-237">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="fa6db-237">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="fa6db-238">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="fa6db-238">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fa6db-239">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="fa6db-239">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="fa6db-240">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-240">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-241">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="fa6db-241">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="fa6db-242">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-242">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-243">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="fa6db-243">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="fa6db-244">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-244">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-245">Items</span><span class="sxs-lookup"><span data-stu-id="fa6db-245">Items</span></span>](items.md) <br/> |<span data-ttu-id="fa6db-246">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="fa6db-246">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-247">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="fa6db-247">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="fa6db-248">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="fa6db-248">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="fa6db-249">SetItemField</span><span class="sxs-lookup"><span data-stu-id="fa6db-249">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="fa6db-250">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="fa6db-250">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fa6db-251">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="fa6db-251">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="fa6db-252">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-252">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa6db-253">文本值</span><span class="sxs-lookup"><span data-stu-id="fa6db-253">Text value</span></span>

<span data-ttu-id="fa6db-254">无。</span><span class="sxs-lookup"><span data-stu-id="fa6db-254">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa6db-255">说明</span><span class="sxs-lookup"><span data-stu-id="fa6db-255">Remarks</span></span>

<span data-ttu-id="fa6db-256">另一个**message**元素时，可用性操作使用[消息（可用性）](message-availability.md)返回 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="fa6db-256">Another **Message** element, [Message (Availability)](message-availability.md) is used by the Availability operations to return OOF messages.</span></span> 
  
<span data-ttu-id="fa6db-257">[Message](message-ex15websvcsotherref.md)元素表示电子邮件以及 Exchange Web 服务（EWS）架构未强类型化的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="fa6db-257">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="fa6db-258">项目，如 IPM。共享和 IPM. InfoPath 以**邮件**元素的形式返回。</span><span class="sxs-lookup"><span data-stu-id="fa6db-258">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="fa6db-259">Exchange 2010 不会在响应中返回基本**项**元素。</span><span class="sxs-lookup"><span data-stu-id="fa6db-259">Exchange 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="fa6db-260">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa6db-260">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa6db-261">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa6db-261">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa6db-262">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa6db-262">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa6db-263">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa6db-263">Schema Name</span></span>  <br/> |<span data-ttu-id="fa6db-264">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa6db-264">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa6db-265">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa6db-265">Validation File</span></span>  <br/> |<span data-ttu-id="fa6db-266">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa6db-266">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa6db-267">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa6db-267">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa6db-268">False</span><span class="sxs-lookup"><span data-stu-id="fa6db-268">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa6db-269">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa6db-269">See also</span></span>



- [<span data-ttu-id="fa6db-270">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa6db-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

