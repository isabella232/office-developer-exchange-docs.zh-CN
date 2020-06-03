---
title: PostReplyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostReplyItem
api_type:
- schema
ms.assetid: e5d93d63-0a3b-470f-9a94-2d57284c6745
description: PostReplyItem 元素包含对公告项的答复。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 4104e79449acc6e358b729cf2de769d28dac52bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461679"
---
# <a name="postreplyitem"></a><span data-ttu-id="762e0-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="762e0-104">PostReplyItem</span></span>

<span data-ttu-id="762e0-105">**PostReplyItem**元素包含对公告项的答复。</span><span class="sxs-lookup"><span data-stu-id="762e0-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="762e0-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="762e0-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostReplyItem>
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
   <NewBodyContent/>
</PostReplyItem>
```

 <span data-ttu-id="762e0-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="762e0-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="762e0-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="762e0-108">Attributes and elements</span></span>

<span data-ttu-id="762e0-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="762e0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="762e0-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="762e0-110">Attributes</span></span>

<span data-ttu-id="762e0-111">无。</span><span class="sxs-lookup"><span data-stu-id="762e0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="762e0-112">子元素</span><span class="sxs-lookup"><span data-stu-id="762e0-112">Child elements</span></span>

|<span data-ttu-id="762e0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="762e0-113">**Element**</span></span>|<span data-ttu-id="762e0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="762e0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="762e0-115">MimeContent</span><span class="sxs-lookup"><span data-stu-id="762e0-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="762e0-116">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="762e0-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="762e0-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="762e0-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="762e0-118">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="762e0-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="762e0-119">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="762e0-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="762e0-120">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="762e0-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="762e0-121">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="762e0-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="762e0-122">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="762e0-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="762e0-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="762e0-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="762e0-124">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="762e0-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="762e0-125">主题</span><span class="sxs-lookup"><span data-stu-id="762e0-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="762e0-126">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="762e0-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="762e0-127">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="762e0-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="762e0-128">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="762e0-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="762e0-129">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="762e0-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="762e0-130">Body</span><span class="sxs-lookup"><span data-stu-id="762e0-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="762e0-131">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="762e0-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="762e0-132">附件</span><span class="sxs-lookup"><span data-stu-id="762e0-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="762e0-133">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="762e0-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="762e0-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="762e0-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="762e0-135">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="762e0-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="762e0-136">大小</span><span class="sxs-lookup"><span data-stu-id="762e0-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="762e0-137">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="762e0-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="762e0-138">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="762e0-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="762e0-139">类别</span><span class="sxs-lookup"><span data-stu-id="762e0-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="762e0-140">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="762e0-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="762e0-141">Importance</span><span class="sxs-lookup"><span data-stu-id="762e0-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="762e0-142">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="762e0-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="762e0-143">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="762e0-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="762e0-144">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="762e0-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="762e0-145">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="762e0-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="762e0-146">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="762e0-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="762e0-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="762e0-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="762e0-148">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="762e0-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="762e0-149">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="762e0-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="762e0-150">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="762e0-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="762e0-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="762e0-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="762e0-152">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="762e0-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="762e0-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="762e0-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="762e0-154">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="762e0-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="762e0-155">Message</span><span class="sxs-lookup"><span data-stu-id="762e0-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="762e0-156">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="762e0-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="762e0-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="762e0-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="762e0-158">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="762e0-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="762e0-159">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="762e0-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="762e0-160">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="762e0-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="762e0-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="762e0-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="762e0-162">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="762e0-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="762e0-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="762e0-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="762e0-164">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="762e0-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="762e0-165">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="762e0-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="762e0-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="762e0-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="762e0-167">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="762e0-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="762e0-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="762e0-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="762e0-169">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="762e0-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="762e0-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="762e0-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="762e0-171">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="762e0-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="762e0-172">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="762e0-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="762e0-173">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="762e0-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="762e0-174">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="762e0-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="762e0-175">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="762e0-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="762e0-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="762e0-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="762e0-177">表示一个在项目有附件的情况设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="762e0-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="762e0-178">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="762e0-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="762e0-179">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="762e0-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="762e0-180">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="762e0-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="762e0-181">Culture</span><span class="sxs-lookup"><span data-stu-id="762e0-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="762e0-182">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="762e0-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="762e0-183">发件人</span><span class="sxs-lookup"><span data-stu-id="762e0-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="762e0-184">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="762e0-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="762e0-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="762e0-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="762e0-186">包含一组邮件的收件人。</span><span class="sxs-lookup"><span data-stu-id="762e0-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="762e0-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="762e0-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="762e0-188">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="762e0-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="762e0-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="762e0-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="762e0-190">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="762e0-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="762e0-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="762e0-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="762e0-192">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="762e0-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="762e0-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="762e0-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="762e0-194">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="762e0-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="762e0-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="762e0-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="762e0-196">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="762e0-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="762e0-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="762e0-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="762e0-198">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="762e0-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="762e0-199">From</span><span class="sxs-lookup"><span data-stu-id="762e0-199">From</span></span>](from.md) <br/> |<span data-ttu-id="762e0-200">表示发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="762e0-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="762e0-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="762e0-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="762e0-202">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="762e0-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="762e0-203">IsRead</span><span class="sxs-lookup"><span data-stu-id="762e0-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="762e0-204">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="762e0-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="762e0-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="762e0-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="762e0-206">指示是否请求对电子邮件的响应。</span><span class="sxs-lookup"><span data-stu-id="762e0-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="762e0-207">References</span><span class="sxs-lookup"><span data-stu-id="762e0-207">References</span></span>](references.md) <br/> |<span data-ttu-id="762e0-208">表示用于将答复与原始邮件关联的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="762e0-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="762e0-209">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="762e0-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="762e0-210">标识应将答复发送到的一组地址。</span><span class="sxs-lookup"><span data-stu-id="762e0-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="762e0-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="762e0-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="762e0-p111">包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="762e0-p111">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="762e0-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="762e0-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="762e0-216">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="762e0-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="762e0-217">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="762e0-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="762e0-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="762e0-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="762e0-219">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="762e0-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="762e0-220">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="762e0-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="762e0-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="762e0-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="762e0-222">表示公告项的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="762e0-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="762e0-223">父元素</span><span class="sxs-lookup"><span data-stu-id="762e0-223">Parent elements</span></span>

|<span data-ttu-id="762e0-224">**元素**</span><span class="sxs-lookup"><span data-stu-id="762e0-224">**Element**</span></span>|<span data-ttu-id="762e0-225">**说明**</span><span class="sxs-lookup"><span data-stu-id="762e0-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="762e0-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="762e0-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="762e0-227">描述与会议时间相邻的所有项目。</span><span class="sxs-lookup"><span data-stu-id="762e0-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="762e0-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="762e0-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="762e0-229">描述与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="762e0-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="762e0-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="762e0-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="762e0-231">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="762e0-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="762e0-232">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="762e0-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="762e0-233">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="762e0-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="762e0-234">说明</span><span class="sxs-lookup"><span data-stu-id="762e0-234">Remarks</span></span>

<span data-ttu-id="762e0-235">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="762e0-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="762e0-236">元素信息</span><span class="sxs-lookup"><span data-stu-id="762e0-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="762e0-237">命名空间</span><span class="sxs-lookup"><span data-stu-id="762e0-237">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="762e0-238">架构名称</span><span class="sxs-lookup"><span data-stu-id="762e0-238">Schema Name</span></span>  <br/> |<span data-ttu-id="762e0-239">类型架构</span><span class="sxs-lookup"><span data-stu-id="762e0-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="762e0-240">验证文件</span><span class="sxs-lookup"><span data-stu-id="762e0-240">Validation File</span></span>  <br/> |<span data-ttu-id="762e0-241">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="762e0-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="762e0-242">可以为空</span><span class="sxs-lookup"><span data-stu-id="762e0-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="762e0-243">False</span><span class="sxs-lookup"><span data-stu-id="762e0-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="762e0-244">另请参阅</span><span class="sxs-lookup"><span data-stu-id="762e0-244">See also</span></span>



- [<span data-ttu-id="762e0-245">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="762e0-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

