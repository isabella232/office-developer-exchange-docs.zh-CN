---
title: MeetingCancellation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingCancellation
api_type:
- schema
ms.assetid: a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea
description: MeetingCancellation 元素表示 Exchange 存储中的会议取消。
ms.openlocfilehash: b0fca0a2dcbdf8685f7b9fb2197db1c3123d54b1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467527"
---
# <a name="meetingcancellation"></a><span data-ttu-id="b3722-103">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="b3722-103">MeetingCancellation</span></span>

<span data-ttu-id="b3722-104">**MeetingCancellation**元素表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="b3722-104">The **MeetingCancellation** element represents a meeting cancellation in the Exchange store.</span></span> 
  
```xml
<MeetingCancellation>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
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
</MeetingCancellation>
```

 <span data-ttu-id="b3722-105">**MeetingCancellationMessageType**</span><span class="sxs-lookup"><span data-stu-id="b3722-105">**MeetingCancellationMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3722-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b3722-106">Attributes and elements</span></span>

<span data-ttu-id="b3722-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b3722-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3722-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b3722-108">Attributes</span></span>

<span data-ttu-id="b3722-109">无。</span><span class="sxs-lookup"><span data-stu-id="b3722-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3722-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b3722-110">Child elements</span></span>

|<span data-ttu-id="b3722-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3722-111">**Element**</span></span>|<span data-ttu-id="b3722-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3722-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3722-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="b3722-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="b3722-114">包含以 base64Binary 格式表示的对象的本机 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="b3722-114">Contains the native MIME stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="b3722-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="b3722-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b3722-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="b3722-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="b3722-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b3722-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b3722-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="b3722-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="b3722-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="b3722-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b3722-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b3722-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="b3722-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="b3722-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-123">主题</span><span class="sxs-lookup"><span data-stu-id="b3722-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="b3722-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="b3722-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="b3722-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="b3722-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="b3722-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b3722-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="b3722-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="b3722-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-128">Body</span><span class="sxs-lookup"><span data-stu-id="b3722-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="b3722-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="b3722-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="b3722-130">附件</span><span class="sxs-lookup"><span data-stu-id="b3722-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b3722-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="b3722-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b3722-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="b3722-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="b3722-133">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="b3722-134">大小</span><span class="sxs-lookup"><span data-stu-id="b3722-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="b3722-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="b3722-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="b3722-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b3722-137">类别</span><span class="sxs-lookup"><span data-stu-id="b3722-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b3722-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="b3722-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="b3722-139">Importance</span><span class="sxs-lookup"><span data-stu-id="b3722-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="b3722-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="b3722-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="b3722-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="b3722-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="b3722-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="b3722-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b3722-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="b3722-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="b3722-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="b3722-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="b3722-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="b3722-146">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="b3722-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="b3722-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="b3722-148">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="b3722-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="b3722-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="b3722-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="b3722-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="b3722-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="b3722-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="b3722-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="b3722-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="b3722-153">Message</span><span class="sxs-lookup"><span data-stu-id="b3722-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b3722-154">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="b3722-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b3722-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="b3722-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="b3722-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="b3722-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="b3722-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="b3722-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="b3722-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="b3722-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="b3722-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="b3722-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b3722-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="b3722-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="b3722-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="b3722-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="b3722-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b3722-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="b3722-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="b3722-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="b3722-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b3722-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="b3722-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="b3722-167">表示显示提醒的事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="b3722-167">Represents the number of minutes before an event that a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b3722-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="b3722-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="b3722-169">表示用于 "抄送" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b3722-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="b3722-170">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="b3722-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b3722-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="b3722-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="b3722-172">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b3722-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="b3722-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="b3722-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b3722-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="b3722-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="b3722-175">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="b3722-175">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="b3722-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b3722-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="b3722-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b3722-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="b3722-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="b3722-179">Culture</span><span class="sxs-lookup"><span data-stu-id="b3722-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="b3722-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="b3722-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b3722-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b3722-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b3722-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b3722-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="b3722-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="b3722-185">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b3722-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="b3722-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="b3722-187">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="b3722-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="b3722-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="b3722-189">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="b3722-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="b3722-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b3722-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="b3722-191">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="b3722-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b3722-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b3722-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="b3722-193">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="b3722-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b3722-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="b3722-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="b3722-195">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="b3722-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="b3722-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="b3722-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="b3722-197">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="b3722-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="b3722-198">发件人</span><span class="sxs-lookup"><span data-stu-id="b3722-198">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="b3722-199">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="b3722-199">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-200">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="b3722-200">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="b3722-201">包含一组邮件的收件人。</span><span class="sxs-lookup"><span data-stu-id="b3722-201">Contains a set of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="b3722-202">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="b3722-202">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="b3722-203">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="b3722-203">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="b3722-204">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="b3722-204">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="b3722-205">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="b3722-205">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="b3722-206">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b3722-206">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="b3722-207">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="b3722-207">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="b3722-208">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b3722-208">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="b3722-209">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="b3722-209">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="b3722-210">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="b3722-210">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="b3722-211">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="b3722-211">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="b3722-212">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="b3722-212">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="b3722-213">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="b3722-213">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="b3722-214">发件人</span><span class="sxs-lookup"><span data-stu-id="b3722-214">From</span></span>](from.md) <br/> |<span data-ttu-id="b3722-215">表示邮件发件人的地址。</span><span class="sxs-lookup"><span data-stu-id="b3722-215">Represents the addressee from whom the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="b3722-216">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="b3722-216">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="b3722-217">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="b3722-217">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-218">IsRead</span><span class="sxs-lookup"><span data-stu-id="b3722-218">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="b3722-219">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="b3722-219">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="b3722-220">IsResponseRequested</span><span class="sxs-lookup"><span data-stu-id="b3722-220">IsResponseRequested</span></span>](isresponserequested.md) <br/> |<span data-ttu-id="b3722-221">指示是否请求对电子邮件的响应。</span><span class="sxs-lookup"><span data-stu-id="b3722-221">Indicates whether a response to an e-mail message is requested.</span></span>  <br/> |
|[<span data-ttu-id="b3722-222">References</span><span class="sxs-lookup"><span data-stu-id="b3722-222">References</span></span>](references.md) <br/> |<span data-ttu-id="b3722-223">表示用于将答复与其原始邮件关联起来的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="b3722-223">Represents the Usenet header that is used to correlate replies with their original messages.</span></span>  <br/> |
|[<span data-ttu-id="b3722-224">ReplyTo</span><span class="sxs-lookup"><span data-stu-id="b3722-224">ReplyTo</span></span>](replyto.md) <br/> |<span data-ttu-id="b3722-225">标识应将答复发送到的一组地址。</span><span class="sxs-lookup"><span data-stu-id="b3722-225">Identifies a set of addresses to which replies should be sent.</span></span>  <br/> |
|[<span data-ttu-id="b3722-226">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="b3722-226">AssociatedCalendarItemId</span></span>](associatedcalendaritemid.md) <br/> |<span data-ttu-id="b3722-227">表示与[MeetingMessage](meetingmessage.md)相关联的日历项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-227">Represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md).</span></span>  <br/> |
|[<span data-ttu-id="b3722-228">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="b3722-228">IsDelegated</span></span>](isdelegated.md) <br/> |<span data-ttu-id="b3722-229">指示是否由具有代理访问权限的帐户处理会议。</span><span class="sxs-lookup"><span data-stu-id="b3722-229">Indicates whether a meeting was handled by an account with delegate access.</span></span>  <br/> |
|[<span data-ttu-id="b3722-230">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="b3722-230">IsOutOfDate</span></span>](isoutofdate.md) <br/> |<span data-ttu-id="b3722-231">指示会议邮件是否已过期。</span><span class="sxs-lookup"><span data-stu-id="b3722-231">Indicates whether a meeting message is out-of-date.</span></span>  <br/> |
|[<span data-ttu-id="b3722-232">HasBeenProcessed</span><span class="sxs-lookup"><span data-stu-id="b3722-232">HasBeenProcessed</span></span>](hasbeenprocessed.md) <br/> |<span data-ttu-id="b3722-233">指示是否已处理会议邮件项。</span><span class="sxs-lookup"><span data-stu-id="b3722-233">Indicates whether a meeting message item has been processed.</span></span>  <br/> |
|[<span data-ttu-id="b3722-234">ResponseType</span><span class="sxs-lookup"><span data-stu-id="b3722-234">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="b3722-235">表示收到的针对会议的收件人响应的类型。</span><span class="sxs-lookup"><span data-stu-id="b3722-235">Represents the type of recipient response received for a meeting.</span></span>  <br/> |
|[<span data-ttu-id="b3722-236">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b3722-236">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b3722-237">包含客户端的权利基础的项或文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="b3722-237">Contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="b3722-238">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="b3722-238">This element is read-only.</span></span> <span data-ttu-id="b3722-239">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b3722-239">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="b3722-240">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="b3722-240">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="b3722-241">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="b3722-241">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="b3722-242">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b3722-242">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b3722-243">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="b3722-243">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="b3722-244">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="b3722-244">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="b3722-245">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b3722-245">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b3722-246">UID</span><span class="sxs-lookup"><span data-stu-id="b3722-246">UID</span></span>](uid.md) <br/> |<span data-ttu-id="b3722-247">标识日历项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-247">Identifies a calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-248">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="b3722-248">RecurrenceId</span></span>](recurrenceid.md) <br/> |<span data-ttu-id="b3722-249">用于标识定期日历项目的特定实例。</span><span class="sxs-lookup"><span data-stu-id="b3722-249">Used to identify a specific instance of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-250">DateTimeStamp</span><span class="sxs-lookup"><span data-stu-id="b3722-250">DateTimeStamp</span></span>](datetimestamp.md) <br/> |<span data-ttu-id="b3722-251">指示 iCalendar 对象的实例的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="b3722-251">Indicates the date and time that an instance of an iCalendar object was created.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3722-252">父元素</span><span class="sxs-lookup"><span data-stu-id="b3722-252">Parent elements</span></span>

|<span data-ttu-id="b3722-253">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3722-253">**Element**</span></span>|<span data-ttu-id="b3722-254">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3722-254">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3722-255">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="b3722-255">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="b3722-256">标识与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-256">Identifies all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="b3722-257">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="b3722-257">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="b3722-258">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="b3722-258">Identifies data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b3722-259">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="b3722-259">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="b3722-260">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-260">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="b3722-261">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="b3722-261">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="b3722-262">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-262">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b3722-263">Items</span><span class="sxs-lookup"><span data-stu-id="b3722-263">Items</span></span>](items.md) <br/> |<span data-ttu-id="b3722-264">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="b3722-264">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="b3722-265">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="b3722-265">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="b3722-266">包含要创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="b3722-266">Contains an array of items to create.</span></span>  <br/> |
|[<span data-ttu-id="b3722-267">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b3722-267">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="b3722-268">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-268">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="b3722-269">SetItemField</span><span class="sxs-lookup"><span data-stu-id="b3722-269">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="b3722-270">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="b3722-270">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b3722-271">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="b3722-271">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="b3722-272">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="b3722-272">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b3722-273">文本值</span><span class="sxs-lookup"><span data-stu-id="b3722-273">Text value</span></span>

<span data-ttu-id="b3722-274">无。</span><span class="sxs-lookup"><span data-stu-id="b3722-274">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3722-275">说明</span><span class="sxs-lookup"><span data-stu-id="b3722-275">Remarks</span></span>

<span data-ttu-id="b3722-276">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b3722-276">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3722-277">元素信息</span><span class="sxs-lookup"><span data-stu-id="b3722-277">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3722-278">命名空间</span><span class="sxs-lookup"><span data-stu-id="b3722-278">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b3722-279">架构名称</span><span class="sxs-lookup"><span data-stu-id="b3722-279">Schema Name</span></span>  <br/> |<span data-ttu-id="b3722-280">类型架构</span><span class="sxs-lookup"><span data-stu-id="b3722-280">Types schema</span></span>  <br/> |
|<span data-ttu-id="b3722-281">验证文件</span><span class="sxs-lookup"><span data-stu-id="b3722-281">Validation File</span></span>  <br/> |<span data-ttu-id="b3722-282">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b3722-282">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b3722-283">可以为空</span><span class="sxs-lookup"><span data-stu-id="b3722-283">Can be Empty</span></span>  <br/> |<span data-ttu-id="b3722-284">False</span><span class="sxs-lookup"><span data-stu-id="b3722-284">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3722-285">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3722-285">See also</span></span>



- [<span data-ttu-id="b3722-286">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b3722-286">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

