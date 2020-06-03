---
title: PostItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostItem
api_type:
- schema
ms.assetid: 7727ed84-9591-4a1c-bb04-12129926499b
description: PostItem 元素表示 Exchange 存储中的公告项。
ms.openlocfilehash: 5fba1a9a6a3abc95ea2ce65cafa2b62bc7423f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528865"
---
# <a name="postitem"></a><span data-ttu-id="fdd62-103">PostItem</span><span class="sxs-lookup"><span data-stu-id="fdd62-103">PostItem</span></span>

<span data-ttu-id="fdd62-104">**PostItem**元素表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="fdd62-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
```xml
<PostItem>
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
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <PostedTime/>
   <References/>
   <Sender/>
</PostItem>
```

 <span data-ttu-id="fdd62-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="fdd62-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fdd62-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fdd62-106">Attributes and elements</span></span>

<span data-ttu-id="fdd62-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fdd62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fdd62-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fdd62-108">Attributes</span></span>

<span data-ttu-id="fdd62-109">无。</span><span class="sxs-lookup"><span data-stu-id="fdd62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fdd62-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fdd62-110">Child elements</span></span>

|<span data-ttu-id="fdd62-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fdd62-111">**Element**</span></span>|<span data-ttu-id="fdd62-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fdd62-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdd62-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="fdd62-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="fdd62-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="fdd62-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="fdd62-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="fdd62-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="fdd62-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="fdd62-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="fdd62-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="fdd62-119">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="fdd62-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="fdd62-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="fdd62-122">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="fdd62-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-123">主题</span><span class="sxs-lookup"><span data-stu-id="fdd62-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="fdd62-124">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="fdd62-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="fdd62-125">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="fdd62-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="fdd62-127">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="fdd62-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-128">Body</span><span class="sxs-lookup"><span data-stu-id="fdd62-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="fdd62-129">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="fdd62-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-130">附件</span><span class="sxs-lookup"><span data-stu-id="fdd62-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fdd62-131">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="fdd62-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="fdd62-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="fdd62-133">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-134">大小</span><span class="sxs-lookup"><span data-stu-id="fdd62-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="fdd62-135">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="fdd62-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="fdd62-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-137">类别</span><span class="sxs-lookup"><span data-stu-id="fdd62-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="fdd62-138">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="fdd62-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-139">Importance</span><span class="sxs-lookup"><span data-stu-id="fdd62-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="fdd62-140">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="fdd62-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="fdd62-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="fdd62-142">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="fdd62-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="fdd62-144">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="fdd62-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="fdd62-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="fdd62-146">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="fdd62-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="fdd62-148">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="fdd62-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="fdd62-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="fdd62-150">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="fdd62-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="fdd62-152">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="fdd62-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-153">Message</span><span class="sxs-lookup"><span data-stu-id="fdd62-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="fdd62-154">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="fdd62-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="fdd62-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="fdd62-156">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="fdd62-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="fdd62-158">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="fdd62-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="fdd62-160">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="fdd62-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="fdd62-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="fdd62-162">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="fdd62-163">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="fdd62-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="fdd62-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="fdd62-165">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="fdd62-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="fdd62-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="fdd62-167">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="fdd62-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="fdd62-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="fdd62-169">表示用于 "抄送" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="fdd62-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="fdd62-170">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="fdd62-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="fdd62-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="fdd62-172">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="fdd62-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="fdd62-173">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="fdd62-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="fdd62-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="fdd62-175">表示一个在项至少有一个附件的情况设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="fdd62-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="fdd62-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="fdd62-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="fdd62-178">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="fdd62-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-179">Culture</span><span class="sxs-lookup"><span data-stu-id="fdd62-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="fdd62-180">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="fdd62-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="fdd62-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="fdd62-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="fdd62-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="fdd62-185">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="fdd62-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="fdd62-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="fdd62-187">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="fdd62-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="fdd62-189">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="fdd62-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fdd62-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="fdd62-191">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="fdd62-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="fdd62-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="fdd62-193">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="fdd62-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="fdd62-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="fdd62-195">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="fdd62-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="fdd62-197">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="fdd62-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="fdd62-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="fdd62-199">包含代表此邮件所属线程的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="fdd62-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="fdd62-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="fdd62-201">表示会话标识符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-202">From</span><span class="sxs-lookup"><span data-stu-id="fdd62-202">From</span></span>](from.md) <br/> |<span data-ttu-id="fdd62-203">表示发送公告项目的地址。</span><span class="sxs-lookup"><span data-stu-id="fdd62-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="fdd62-204">**From**元素只能在创建时设置。</span><span class="sxs-lookup"><span data-stu-id="fdd62-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="fdd62-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="fdd62-206">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="fdd62-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-207">IsRead</span><span class="sxs-lookup"><span data-stu-id="fdd62-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="fdd62-208">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="fdd62-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-209">PostedTime</span><span class="sxs-lookup"><span data-stu-id="fdd62-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="fdd62-210">表示[PostItem](postitem.md)的发布时间。</span><span class="sxs-lookup"><span data-stu-id="fdd62-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-211">References</span><span class="sxs-lookup"><span data-stu-id="fdd62-211">References</span></span>](references.md) <br/> |<span data-ttu-id="fdd62-212">表示用于将答复与原始邮件关联的 Usenet 标头。</span><span class="sxs-lookup"><span data-stu-id="fdd62-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-213">发件人</span><span class="sxs-lookup"><span data-stu-id="fdd62-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="fdd62-214">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="fdd62-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fdd62-215">父元素</span><span class="sxs-lookup"><span data-stu-id="fdd62-215">Parent elements</span></span>

|<span data-ttu-id="fdd62-216">**元素**</span><span class="sxs-lookup"><span data-stu-id="fdd62-216">**Element**</span></span>|<span data-ttu-id="fdd62-217">**说明**</span><span class="sxs-lookup"><span data-stu-id="fdd62-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fdd62-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="fdd62-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="fdd62-219">表示对 UpdateItem 操作中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="fdd62-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="fdd62-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="fdd62-221">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项或文件夹的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="fdd62-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="fdd62-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="fdd62-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="fdd62-223">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-224">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="fdd62-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="fdd62-225">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-226">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="fdd62-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="fdd62-227">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="fdd62-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="fdd62-229">在已读取项目时， [SyncFolderItems](syncfolderitems.md)响应中返回。</span><span class="sxs-lookup"><span data-stu-id="fdd62-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="fdd62-230">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="fdd62-230">This property is read-only.</span></span> <span data-ttu-id="fdd62-231">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fdd62-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-232">Items</span><span class="sxs-lookup"><span data-stu-id="fdd62-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="fdd62-233">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="fdd62-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="fdd62-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="fdd62-235">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="fdd62-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="fdd62-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="fdd62-237">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="fdd62-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fdd62-238">文本值</span><span class="sxs-lookup"><span data-stu-id="fdd62-238">Text value</span></span>

<span data-ttu-id="fdd62-239">无。</span><span class="sxs-lookup"><span data-stu-id="fdd62-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fdd62-240">说明</span><span class="sxs-lookup"><span data-stu-id="fdd62-240">Remarks</span></span>

<span data-ttu-id="fdd62-241">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fdd62-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fdd62-242">元素信息</span><span class="sxs-lookup"><span data-stu-id="fdd62-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fdd62-243">命名空间</span><span class="sxs-lookup"><span data-stu-id="fdd62-243">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fdd62-244">架构名称</span><span class="sxs-lookup"><span data-stu-id="fdd62-244">Schema Name</span></span>  <br/> |<span data-ttu-id="fdd62-245">类型架构</span><span class="sxs-lookup"><span data-stu-id="fdd62-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="fdd62-246">验证文件</span><span class="sxs-lookup"><span data-stu-id="fdd62-246">Validation File</span></span>  <br/> |<span data-ttu-id="fdd62-247">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fdd62-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fdd62-248">可以为空</span><span class="sxs-lookup"><span data-stu-id="fdd62-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="fdd62-249">False</span><span class="sxs-lookup"><span data-stu-id="fdd62-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fdd62-250">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fdd62-250">See also</span></span>



- [<span data-ttu-id="fdd62-251">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fdd62-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

