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
description: PostReplyItem 元素包含一个公告项目答复。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 70a0d6a7c670d0f16a55e66e7ef329331a04a5f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826868"
---
# <a name="postreplyitem"></a><span data-ttu-id="16118-104">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="16118-104">PostReplyItem</span></span>

<span data-ttu-id="16118-105">**PostReplyItem**元素包含一个公告项目答复。</span><span class="sxs-lookup"><span data-stu-id="16118-105">The **PostReplyItem** element contains a reply to a post item.</span></span> <span data-ttu-id="16118-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16118-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

 <span data-ttu-id="16118-107">**PostReplyItemType**</span><span class="sxs-lookup"><span data-stu-id="16118-107">**PostReplyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16118-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="16118-108">Attributes and elements</span></span>

<span data-ttu-id="16118-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="16118-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16118-110">属性</span><span class="sxs-lookup"><span data-stu-id="16118-110">Attributes</span></span>

<span data-ttu-id="16118-111">无。</span><span class="sxs-lookup"><span data-stu-id="16118-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16118-112">子元素</span><span class="sxs-lookup"><span data-stu-id="16118-112">Child elements</span></span>

|<span data-ttu-id="16118-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="16118-113">**Element**</span></span>|<span data-ttu-id="16118-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="16118-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16118-115">MimeContent</span><span class="sxs-lookup"><span data-stu-id="16118-115">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="16118-116">包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="16118-116">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="16118-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="16118-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="16118-118">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="16118-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="16118-119">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="16118-119">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="16118-120">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="16118-120">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="16118-121">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="16118-121">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="16118-122">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="16118-122">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="16118-123">ItemClass</span><span class="sxs-lookup"><span data-stu-id="16118-123">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="16118-124">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="16118-124">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="16118-125">Subject</span><span class="sxs-lookup"><span data-stu-id="16118-125">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="16118-126">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="16118-126">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="16118-127">主题被限制为 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="16118-127">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="16118-128">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="16118-128">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="16118-129">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="16118-129">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="16118-130">Body</span><span class="sxs-lookup"><span data-stu-id="16118-130">Body</span></span>](body.md) <br/> |<span data-ttu-id="16118-131">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="16118-131">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="16118-132">附件</span><span class="sxs-lookup"><span data-stu-id="16118-132">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="16118-133">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="16118-133">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16118-134">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="16118-134">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="16118-135">表示的日期和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="16118-135">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="16118-136">Size</span><span class="sxs-lookup"><span data-stu-id="16118-136">Size</span></span>](size.md) <br/> |<span data-ttu-id="16118-137">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="16118-137">Represents the size in bytes of an item.</span></span> <span data-ttu-id="16118-138">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="16118-138">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="16118-139">类别</span><span class="sxs-lookup"><span data-stu-id="16118-139">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="16118-140">表示字符串标识的邮箱中项目所属的类别的集合。</span><span class="sxs-lookup"><span data-stu-id="16118-140">Represents a collection of strings that identify categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="16118-141">Importance</span><span class="sxs-lookup"><span data-stu-id="16118-141">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="16118-142">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="16118-142">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="16118-143">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="16118-143">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="16118-144">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="16118-144">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="16118-145">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="16118-145">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="16118-146">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="16118-146">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="16118-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="16118-147">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="16118-148">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="16118-148">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="16118-149">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="16118-149">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="16118-150">指示用户是否发送到他或她自己的项目。</span><span class="sxs-lookup"><span data-stu-id="16118-150">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="16118-151">IsResend</span><span class="sxs-lookup"><span data-stu-id="16118-151">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="16118-152">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="16118-152">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="16118-153">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="16118-153">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="16118-154">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="16118-154">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="16118-155">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="16118-155">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="16118-156">代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="16118-156">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="16118-157">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="16118-157">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="16118-158">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="16118-158">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="16118-159">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="16118-159">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="16118-160">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="16118-160">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="16118-161">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="16118-161">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="16118-162">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="16118-162">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16118-163">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="16118-163">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="16118-164">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="16118-164">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="16118-165">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="16118-165">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="16118-166">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="16118-166">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="16118-167">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="16118-167">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16118-168">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="16118-168">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="16118-169">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="16118-169">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="16118-170">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="16118-170">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="16118-171">表示用于 Cc 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="16118-171">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="16118-172">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="16118-172">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="16118-173">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="16118-173">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="16118-174">表示用于收件人框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="16118-174">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="16118-175">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="16118-175">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="16118-176">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="16118-176">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="16118-177">表示项目包含附件如果设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="16118-177">Represents a property that is set to **true** if an item has an attachment.</span></span> <span data-ttu-id="16118-178">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="16118-178">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="16118-179">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="16118-179">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="16118-180">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="16118-180">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="16118-181">区域性</span><span class="sxs-lookup"><span data-stu-id="16118-181">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="16118-182">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="16118-182">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="16118-183">发件人</span><span class="sxs-lookup"><span data-stu-id="16118-183">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="16118-184">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="16118-184">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="16118-185">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="16118-185">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="16118-186">包含邮件收件人的一组。</span><span class="sxs-lookup"><span data-stu-id="16118-186">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="16118-187">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="16118-187">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="16118-188">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="16118-188">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="16118-189">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="16118-189">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="16118-190">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="16118-190">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="16118-191">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="16118-191">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="16118-192">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="16118-192">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="16118-193">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="16118-193">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="16118-194">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="16118-194">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="16118-195">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="16118-195">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="16118-196">包含表示此消息所属的主题的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="16118-196">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="16118-197">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="16118-197">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="16118-198">表示对话标识符。</span><span class="sxs-lookup"><span data-stu-id="16118-198">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="16118-199">发件人</span><span class="sxs-lookup"><span data-stu-id="16118-199">From</span></span>](from.md) <br/> |<span data-ttu-id="16118-200">代表从中发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="16118-200">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="16118-201">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="16118-201">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="16118-202">表示项目的 Internet 消息标识符。</span><span class="sxs-lookup"><span data-stu-id="16118-202">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="16118-203">IsRead</span><span class="sxs-lookup"><span data-stu-id="16118-203">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="16118-204">指示是否已读取一条消息。</span><span class="sxs-lookup"><span data-stu-id="16118-204">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="16118-205">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="16118-205">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="16118-206">指示是否对电子邮件的响应请求。</span><span class="sxs-lookup"><span data-stu-id="16118-206">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="16118-207">引用</span><span class="sxs-lookup"><span data-stu-id="16118-207">References</span></span>](references.md) <br/> |<span data-ttu-id="16118-208">代表用于将答复其原始消息相关联的新闻标头。</span><span class="sxs-lookup"><span data-stu-id="16118-208">Represents the Usenet header that is used to associate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="16118-209">回复</span><span class="sxs-lookup"><span data-stu-id="16118-209">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="16118-210">标识一组地址应向其发送答复。</span><span class="sxs-lookup"><span data-stu-id="16118-210">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="16118-211">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="16118-211">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="16118-p111">包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16118-p111">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="16118-215">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="16118-215">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="16118-216">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="16118-216">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="16118-217">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16118-217">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="16118-218">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="16118-218">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="16118-219">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="16118-219">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="16118-220">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16118-220">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="16118-221">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="16118-221">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="16118-222">代表新公告项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="16118-222">Represents the new body content of a post item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="16118-223">父元素</span><span class="sxs-lookup"><span data-stu-id="16118-223">Parent elements</span></span>

|<span data-ttu-id="16118-224">**元素**</span><span class="sxs-lookup"><span data-stu-id="16118-224">**Element**</span></span>|<span data-ttu-id="16118-225">**说明**</span><span class="sxs-lookup"><span data-stu-id="16118-225">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16118-226">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="16118-226">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="16118-227">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="16118-227">Describes all items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="16118-228">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="16118-228">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="16118-229">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="16118-229">Describes all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="16118-230">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="16118-230">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="16118-231">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="16118-231">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="16118-232">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="16118-232">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="16118-233">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="16118-233">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16118-234">备注</span><span class="sxs-lookup"><span data-stu-id="16118-234">Remarks</span></span>

<span data-ttu-id="16118-235">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="16118-235">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16118-236">元素信息</span><span class="sxs-lookup"><span data-stu-id="16118-236">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16118-237">命名空间</span><span class="sxs-lookup"><span data-stu-id="16118-237">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16118-238">架构名称</span><span class="sxs-lookup"><span data-stu-id="16118-238">Schema Name</span></span>  <br/> |<span data-ttu-id="16118-239">类型架构</span><span class="sxs-lookup"><span data-stu-id="16118-239">Types schema</span></span>  <br/> |
|<span data-ttu-id="16118-240">验证文件</span><span class="sxs-lookup"><span data-stu-id="16118-240">Validation File</span></span>  <br/> |<span data-ttu-id="16118-241">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="16118-241">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="16118-242">可以为空</span><span class="sxs-lookup"><span data-stu-id="16118-242">Can be Empty</span></span>  <br/> |<span data-ttu-id="16118-243">False</span><span class="sxs-lookup"><span data-stu-id="16118-243">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16118-244">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16118-244">See also</span></span>



- [<span data-ttu-id="16118-245">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="16118-245">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

