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
description: PostItem 元素均表示一个 Exchange 存储中的公告项目。
ms.openlocfilehash: 3fb6d6cfe334999c93ca0238547dd5aee8150a5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826866"
---
# <a name="postitem"></a><span data-ttu-id="b591e-103">PostItem</span><span class="sxs-lookup"><span data-stu-id="b591e-103">PostItem</span></span>

<span data-ttu-id="b591e-104">**PostItem**元素均表示一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-104">The **PostItem** element represents a post item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="b591e-105">**PostItemType**</span><span class="sxs-lookup"><span data-stu-id="b591e-105">**PostItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b591e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b591e-106">Attributes and elements</span></span>

<span data-ttu-id="b591e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b591e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b591e-108">属性</span><span class="sxs-lookup"><span data-stu-id="b591e-108">Attributes</span></span>

<span data-ttu-id="b591e-109">无。</span><span class="sxs-lookup"><span data-stu-id="b591e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b591e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b591e-110">Child elements</span></span>

|<span data-ttu-id="b591e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b591e-111">**Element**</span></span>|<span data-ttu-id="b591e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b591e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b591e-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="b591e-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="b591e-114">包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="b591e-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="b591e-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="b591e-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b591e-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="b591e-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="b591e-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b591e-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b591e-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="b591e-119">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="b591e-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="b591e-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b591e-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b591e-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="b591e-122">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="b591e-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-123">Subject</span><span class="sxs-lookup"><span data-stu-id="b591e-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="b591e-124">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="b591e-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="b591e-125">主题被限制为 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="b591e-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="b591e-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b591e-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="b591e-127">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="b591e-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-128">Body</span><span class="sxs-lookup"><span data-stu-id="b591e-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="b591e-129">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="b591e-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="b591e-130">附件</span><span class="sxs-lookup"><span data-stu-id="b591e-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b591e-131">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="b591e-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b591e-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="b591e-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="b591e-133">表示的日期和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="b591e-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="b591e-134">Size</span><span class="sxs-lookup"><span data-stu-id="b591e-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="b591e-135">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="b591e-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="b591e-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b591e-137">类别</span><span class="sxs-lookup"><span data-stu-id="b591e-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b591e-138">表示字符串标识的邮箱中项目所属的类别的集合。</span><span class="sxs-lookup"><span data-stu-id="b591e-138">Represents a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="b591e-139">Importance</span><span class="sxs-lookup"><span data-stu-id="b591e-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="b591e-140">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="b591e-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="b591e-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="b591e-142">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="b591e-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="b591e-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b591e-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="b591e-144">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="b591e-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="b591e-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="b591e-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="b591e-146">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="b591e-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="b591e-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="b591e-148">指示用户是否发送到他或她自己的项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-148">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="b591e-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="b591e-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="b591e-150">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="b591e-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="b591e-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="b591e-152">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="b591e-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b591e-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b591e-154">代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="b591e-154">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b591e-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="b591e-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="b591e-156">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="b591e-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="b591e-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="b591e-158">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="b591e-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="b591e-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="b591e-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="b591e-160">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="b591e-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b591e-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="b591e-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="b591e-162">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="b591e-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="b591e-163">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="b591e-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b591e-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="b591e-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="b591e-165">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="b591e-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b591e-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="b591e-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="b591e-167">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="b591e-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b591e-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="b591e-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="b591e-169">表示用于抄送框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b591e-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="b591e-170">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="b591e-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b591e-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="b591e-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="b591e-172">表示用于收件人框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b591e-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="b591e-173">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="b591e-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b591e-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="b591e-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="b591e-175">表示一项具有至少一个附件如果设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="b591e-175">Represents a property that is set to **true** if an item has at least one attachment.</span></span> <span data-ttu-id="b591e-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b591e-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="b591e-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b591e-178">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b591e-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="b591e-179">区域性</span><span class="sxs-lookup"><span data-stu-id="b591e-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="b591e-180">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="b591e-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b591e-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b591e-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b591e-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b591e-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="b591e-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="b591e-185">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b591e-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="b591e-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="b591e-187">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="b591e-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="b591e-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="b591e-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="b591e-189">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="b591e-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="b591e-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b591e-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="b591e-191">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="b591e-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b591e-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b591e-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="b591e-193">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="b591e-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b591e-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="b591e-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="b591e-195">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="b591e-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="b591e-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="b591e-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="b591e-197">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="b591e-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="b591e-198">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="b591e-198">ConversationIndex</span></span>](conversationindex.md) <br/> |<span data-ttu-id="b591e-199">包含表示此消息所属的主题的二进制 ID。</span><span class="sxs-lookup"><span data-stu-id="b591e-199">Contains a binary ID that represents the thread to which this message belongs.</span></span>  <br/> |
|[<span data-ttu-id="b591e-200">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="b591e-200">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="b591e-201">表示对话标识符。</span><span class="sxs-lookup"><span data-stu-id="b591e-201">Represents the conversation identifier.</span></span>  <br/> |
|[<span data-ttu-id="b591e-202">发件人</span><span class="sxs-lookup"><span data-stu-id="b591e-202">From</span></span>](from.md) <br/> |<span data-ttu-id="b591e-203">代表从中发送公告项的地址。</span><span class="sxs-lookup"><span data-stu-id="b591e-203">Represents the address from which the post item was sent.</span></span> <span data-ttu-id="b591e-204">**从**元素只能在创建时设置。</span><span class="sxs-lookup"><span data-stu-id="b591e-204">The **From** element can only be set at creation time.</span></span>  <br/> |
|[<span data-ttu-id="b591e-205">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="b591e-205">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="b591e-206">表示项目的 Internet 消息标识符。</span><span class="sxs-lookup"><span data-stu-id="b591e-206">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-207">IsRead</span><span class="sxs-lookup"><span data-stu-id="b591e-207">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="b591e-208">指示是否已读取一条消息。</span><span class="sxs-lookup"><span data-stu-id="b591e-208">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="b591e-209">PostedTime</span><span class="sxs-lookup"><span data-stu-id="b591e-209">PostedTime</span></span>](postedtime.md) <br/> |<span data-ttu-id="b591e-210">表示[PostItem](postitem.md)已发布的时间。</span><span class="sxs-lookup"><span data-stu-id="b591e-210">Represents the time that a [PostItem](postitem.md) was posted.</span></span>  <br/> |
|[<span data-ttu-id="b591e-211">引用</span><span class="sxs-lookup"><span data-stu-id="b591e-211">References</span></span>](references.md) <br/> |<span data-ttu-id="b591e-212">代表用于将答复原始消息相关联的新闻标头。</span><span class="sxs-lookup"><span data-stu-id="b591e-212">Represents the Usenet header that is used to associate replies with the original messages.</span></span>  <br/> |
|[<span data-ttu-id="b591e-213">发件人</span><span class="sxs-lookup"><span data-stu-id="b591e-213">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="b591e-214">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="b591e-214">Identifies the sender of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b591e-215">父元素</span><span class="sxs-lookup"><span data-stu-id="b591e-215">Parent elements</span></span>

|<span data-ttu-id="b591e-216">**元素**</span><span class="sxs-lookup"><span data-stu-id="b591e-216">**Element**</span></span>|<span data-ttu-id="b591e-217">**说明**</span><span class="sxs-lookup"><span data-stu-id="b591e-217">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b591e-218">SetItemField</span><span class="sxs-lookup"><span data-stu-id="b591e-218">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="b591e-219">表示更新到单个 UpdateItem 操作中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="b591e-219">Represents an update to a single property of an item in an UpdateItem operation.</span></span>  <br/> |
|[<span data-ttu-id="b591e-220">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="b591e-220">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="b591e-221">标识要[UpdateItem 操作](updateitem-operation.md)期间追加到单个项目或文件夹的属性数据。</span><span class="sxs-lookup"><span data-stu-id="b591e-221">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b591e-222">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="b591e-222">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="b591e-223">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-223">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="b591e-224">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="b591e-224">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="b591e-225">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="b591e-225">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b591e-226">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="b591e-226">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="b591e-227">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="b591e-227">Identifies a single item to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b591e-228">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="b591e-228">ReadFlagChange</span></span>](readflagchange.md) <br/> |<span data-ttu-id="b591e-229">读取项目后，在[SyncFolderItems](syncfolderitems.md)响应中返回。</span><span class="sxs-lookup"><span data-stu-id="b591e-229">Returned in [SyncFolderItems](syncfolderitems.md) responses when an item has been read.</span></span> <span data-ttu-id="b591e-230">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b591e-230">This property is read-only.</span></span> <span data-ttu-id="b591e-231">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b591e-231">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b591e-232">Items</span><span class="sxs-lookup"><span data-stu-id="b591e-232">Items</span></span>](items.md) <br/> |<span data-ttu-id="b591e-233">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="b591e-233">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="b591e-234">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="b591e-234">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="b591e-235">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-235">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="b591e-236">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="b591e-236">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="b591e-237">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="b591e-237">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b591e-238">文本值</span><span class="sxs-lookup"><span data-stu-id="b591e-238">Text value</span></span>

<span data-ttu-id="b591e-239">无。</span><span class="sxs-lookup"><span data-stu-id="b591e-239">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b591e-240">备注</span><span class="sxs-lookup"><span data-stu-id="b591e-240">Remarks</span></span>

<span data-ttu-id="b591e-241">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b591e-241">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b591e-242">元素信息</span><span class="sxs-lookup"><span data-stu-id="b591e-242">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b591e-243">命名空间</span><span class="sxs-lookup"><span data-stu-id="b591e-243">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b591e-244">架构名称</span><span class="sxs-lookup"><span data-stu-id="b591e-244">Schema Name</span></span>  <br/> |<span data-ttu-id="b591e-245">类型架构</span><span class="sxs-lookup"><span data-stu-id="b591e-245">Types schema</span></span>  <br/> |
|<span data-ttu-id="b591e-246">验证文件</span><span class="sxs-lookup"><span data-stu-id="b591e-246">Validation File</span></span>  <br/> |<span data-ttu-id="b591e-247">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b591e-247">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b591e-248">可以为空</span><span class="sxs-lookup"><span data-stu-id="b591e-248">Can be Empty</span></span>  <br/> |<span data-ttu-id="b591e-249">False</span><span class="sxs-lookup"><span data-stu-id="b591e-249">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b591e-250">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b591e-250">See also</span></span>



- [<span data-ttu-id="b591e-251">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b591e-251">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

