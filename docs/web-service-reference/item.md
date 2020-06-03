---
title: 项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Item
api_type:
- schema
ms.assetid: 4dfe8f48-e7b4-444d-bdf9-a34e180f598b
description: Item 元素表示 Exchange 存储中的一般项目。
ms.openlocfilehash: 72d8b1344bea3bcd105a0e293365b17f37193ac3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460314"
---
# <a name="item"></a><span data-ttu-id="4ec42-103">项目</span><span class="sxs-lookup"><span data-stu-id="4ec42-103">Item</span></span>

<span data-ttu-id="4ec42-104">**Item**元素表示 Exchange 存储中的一般项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
```xml
<Item>
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
</Item>
```

 <span data-ttu-id="4ec42-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="4ec42-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ec42-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4ec42-106">Attributes and elements</span></span>

<span data-ttu-id="4ec42-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4ec42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ec42-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4ec42-108">Attributes</span></span>

<span data-ttu-id="4ec42-109">无。</span><span class="sxs-lookup"><span data-stu-id="4ec42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ec42-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4ec42-110">Child elements</span></span>

|<span data-ttu-id="4ec42-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ec42-111">**Element**</span></span>|<span data-ttu-id="4ec42-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ec42-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec42-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="4ec42-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="4ec42-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="4ec42-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="4ec42-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="4ec42-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="4ec42-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="4ec42-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="4ec42-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="4ec42-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="4ec42-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="4ec42-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="4ec42-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="4ec42-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="4ec42-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="4ec42-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="4ec42-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-123">主题</span><span class="sxs-lookup"><span data-stu-id="4ec42-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="4ec42-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="4ec42-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="4ec42-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="4ec42-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="4ec42-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="4ec42-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="4ec42-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-128">Body</span><span class="sxs-lookup"><span data-stu-id="4ec42-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="4ec42-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="4ec42-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-130">附件</span><span class="sxs-lookup"><span data-stu-id="4ec42-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4ec42-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="4ec42-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="4ec42-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="4ec42-133">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="4ec42-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-134">大小</span><span class="sxs-lookup"><span data-stu-id="4ec42-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="4ec42-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="4ec42-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="4ec42-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="4ec42-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-137">类别</span><span class="sxs-lookup"><span data-stu-id="4ec42-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4ec42-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="4ec42-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-139">Importance</span><span class="sxs-lookup"><span data-stu-id="4ec42-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="4ec42-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="4ec42-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="4ec42-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="4ec42-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="4ec42-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="4ec42-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="4ec42-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="4ec42-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="4ec42-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="4ec42-146">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="4ec42-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="4ec42-148">指示用户是否向其自身发送了项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="4ec42-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="4ec42-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="4ec42-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="4ec42-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="4ec42-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-153">Message</span><span class="sxs-lookup"><span data-stu-id="4ec42-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="4ec42-154">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="4ec42-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="4ec42-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="4ec42-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="4ec42-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="4ec42-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="4ec42-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="4ec42-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="4ec42-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="4ec42-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="4ec42-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="4ec42-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="4ec42-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="4ec42-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="4ec42-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="4ec42-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="4ec42-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="4ec42-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="4ec42-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="4ec42-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="4ec42-167">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="4ec42-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="4ec42-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="4ec42-169">表示用于 "抄送" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="4ec42-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="4ec42-170">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="4ec42-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="4ec42-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="4ec42-172">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="4ec42-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="4ec42-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="4ec42-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="4ec42-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="4ec42-175">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="4ec42-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="4ec42-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="4ec42-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4ec42-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="4ec42-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="4ec42-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-179">Culture</span><span class="sxs-lookup"><span data-stu-id="4ec42-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="4ec42-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="4ec42-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="4ec42-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="4ec42-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="4ec42-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="4ec42-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="4ec42-185">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4ec42-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="4ec42-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="4ec42-187">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="4ec42-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="4ec42-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="4ec42-189">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="4ec42-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="4ec42-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="4ec42-191">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="4ec42-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="4ec42-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="4ec42-193">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="4ec42-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="4ec42-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="4ec42-195">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="4ec42-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="4ec42-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="4ec42-197">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="4ec42-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ec42-198">父元素</span><span class="sxs-lookup"><span data-stu-id="4ec42-198">Parent elements</span></span>

|<span data-ttu-id="4ec42-199">**元素**</span><span class="sxs-lookup"><span data-stu-id="4ec42-199">**Element**</span></span>|<span data-ttu-id="4ec42-200">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ec42-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ec42-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="4ec42-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="4ec42-202">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="4ec42-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="4ec42-204">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项目/文件夹的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="4ec42-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4ec42-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="4ec42-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="4ec42-206">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-207">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="4ec42-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="4ec42-208">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="4ec42-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="4ec42-210">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-211">Items</span><span class="sxs-lookup"><span data-stu-id="4ec42-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="4ec42-212">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="4ec42-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-213">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="4ec42-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="4ec42-214">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="4ec42-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="4ec42-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="4ec42-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="4ec42-216">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="4ec42-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="4ec42-217">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="4ec42-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="4ec42-218">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ec42-219">文本值</span><span class="sxs-lookup"><span data-stu-id="4ec42-219">Text value</span></span>

<span data-ttu-id="4ec42-220">无。</span><span class="sxs-lookup"><span data-stu-id="4ec42-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ec42-221">说明</span><span class="sxs-lookup"><span data-stu-id="4ec42-221">Remarks</span></span>

<span data-ttu-id="4ec42-222">请务必注意， **ItemType**是[Task](task.md)、 [CalendarItem](calendaritem.md)、 [Contact](contact.md)、 [DistributionList](distributionlist.md)和[Message](message-ex15websvcsotherref.md)的基本类型。</span><span class="sxs-lookup"><span data-stu-id="4ec42-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="4ec42-223">[Message](message-ex15websvcsotherref.md)元素表示电子邮件以及 Exchange Web 服务（EWS）架构未强类型化的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="4ec42-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="4ec42-224">项目，如 IPM。共享和 IPM. InfoPath 以**邮件**元素的形式返回。</span><span class="sxs-lookup"><span data-stu-id="4ec42-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="4ec42-225">Microsoft Exchange Server 2010 不会在响应中返回基本**项目**元素。</span><span class="sxs-lookup"><span data-stu-id="4ec42-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="4ec42-226">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4ec42-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ec42-227">元素信息</span><span class="sxs-lookup"><span data-stu-id="4ec42-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ec42-228">命名空间</span><span class="sxs-lookup"><span data-stu-id="4ec42-228">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ec42-229">架构名称</span><span class="sxs-lookup"><span data-stu-id="4ec42-229">Schema Name</span></span>  <br/> |<span data-ttu-id="4ec42-230">类型架构</span><span class="sxs-lookup"><span data-stu-id="4ec42-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ec42-231">验证文件</span><span class="sxs-lookup"><span data-stu-id="4ec42-231">Validation File</span></span>  <br/> |<span data-ttu-id="4ec42-232">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ec42-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ec42-233">可以为空</span><span class="sxs-lookup"><span data-stu-id="4ec42-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ec42-234">False</span><span class="sxs-lookup"><span data-stu-id="4ec42-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ec42-235">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4ec42-235">See also</span></span>



- [<span data-ttu-id="4ec42-236">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4ec42-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="4ec42-237">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="4ec42-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

