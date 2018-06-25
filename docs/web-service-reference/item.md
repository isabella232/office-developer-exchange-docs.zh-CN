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
description: Item 元素表示 Exchange 存储中的泛型项。
ms.openlocfilehash: 7af8e063c3bfd77bd87b80463c11c58d996626b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826143"
---
# <a name="item"></a><span data-ttu-id="f4ced-103">项目</span><span class="sxs-lookup"><span data-stu-id="f4ced-103">Item</span></span>

<span data-ttu-id="f4ced-104">**Item**元素表示 Exchange 存储中的泛型项。</span><span class="sxs-lookup"><span data-stu-id="f4ced-104">The **Item** element represents a generic item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="f4ced-105">**ItemType**</span><span class="sxs-lookup"><span data-stu-id="f4ced-105">**ItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4ced-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f4ced-106">Attributes and elements</span></span>

<span data-ttu-id="f4ced-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f4ced-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4ced-108">属性</span><span class="sxs-lookup"><span data-stu-id="f4ced-108">Attributes</span></span>

<span data-ttu-id="f4ced-109">无。</span><span class="sxs-lookup"><span data-stu-id="f4ced-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4ced-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f4ced-110">Child elements</span></span>

|<span data-ttu-id="f4ced-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4ced-111">**Element**</span></span>|<span data-ttu-id="f4ced-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4ced-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4ced-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="f4ced-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="f4ced-114">包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="f4ced-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="f4ced-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="f4ced-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="f4ced-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="f4ced-117">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="f4ced-117">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-118">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="f4ced-118">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="f4ced-119">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f4ced-119">Represents the identifier of the parent folder that contains the item or folder.</span></span> <span data-ttu-id="f4ced-120">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="f4ced-120">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-121">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f4ced-121">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="f4ced-122">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="f4ced-122">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-123">Subject</span><span class="sxs-lookup"><span data-stu-id="f4ced-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="f4ced-124">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="f4ced-124">Represents the subject for Exchange store items and response objects.</span></span> <span data-ttu-id="f4ced-125">主题被限制为 255 个字符。</span><span class="sxs-lookup"><span data-stu-id="f4ced-125">The subject is limited to 255 characters.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-126">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="f4ced-126">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="f4ced-127">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="f4ced-127">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-128">Body</span><span class="sxs-lookup"><span data-stu-id="f4ced-128">Body</span></span>](body.md) <br/> |<span data-ttu-id="f4ced-129">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="f4ced-129">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-130">附件</span><span class="sxs-lookup"><span data-stu-id="f4ced-130">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f4ced-131">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="f4ced-131">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-132">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="f4ced-132">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="f4ced-133">表示的日期和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="f4ced-133">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-134">Size</span><span class="sxs-lookup"><span data-stu-id="f4ced-134">Size</span></span>](size.md) <br/> |<span data-ttu-id="f4ced-135">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="f4ced-135">Represents the size in bytes of an item.</span></span> <span data-ttu-id="f4ced-136">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="f4ced-136">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-137">类别</span><span class="sxs-lookup"><span data-stu-id="f4ced-137">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f4ced-138">表示标识的邮箱中项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="f4ced-138">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-139">Importance</span><span class="sxs-lookup"><span data-stu-id="f4ced-139">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="f4ced-140">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="f4ced-140">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-141">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="f4ced-141">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="f4ced-142">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="f4ced-142">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-143">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="f4ced-143">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="f4ced-144">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="f4ced-144">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-145">IsDraft</span><span class="sxs-lookup"><span data-stu-id="f4ced-145">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="f4ced-146">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-146">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-147">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="f4ced-147">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="f4ced-148">指示用户是否发送到其自身的项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-148">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="f4ced-149">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="f4ced-150">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-150">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-151">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="f4ced-151">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="f4ced-152">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-152">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-153">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="f4ced-153">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="f4ced-154">代表包含在邮箱中项目的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="f4ced-154">Represents the collection of all Internet message headers that are contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-155">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="f4ced-155">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="f4ced-156">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-156">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-157">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="f4ced-157">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="f4ced-158">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="f4ced-158">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-159">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="f4ced-159">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="f4ced-160">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="f4ced-160">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-161">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="f4ced-161">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="f4ced-162">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="f4ced-162">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="f4ced-163">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="f4ced-163">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-164">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="f4ced-164">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="f4ced-165">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="f4ced-165">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-166">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="f4ced-166">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="f4ced-167">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="f4ced-167">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-168">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="f4ced-168">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="f4ced-169">表示用于抄送框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="f4ced-169">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="f4ced-170">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="f4ced-170">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-171">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="f4ced-171">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="f4ced-172">表示用于收件人框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="f4ced-172">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="f4ced-173">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="f4ced-173">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-174">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="f4ced-174">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="f4ced-175">表示一个属性，如果项目的附件设置为**true** ，至少在一个可见的附件。</span><span class="sxs-lookup"><span data-stu-id="f4ced-175">Represents a property that is set to **true** if an item has attachments at least one visible attachment.</span></span> <span data-ttu-id="f4ced-176">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="f4ced-176">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-177">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="f4ced-177">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="f4ced-178">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="f4ced-178">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-179">区域性</span><span class="sxs-lookup"><span data-stu-id="f4ced-179">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="f4ced-180">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="f4ced-180">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-181">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="f4ced-181">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="f4ced-p109">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="f4ced-p109">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-184">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="f4ced-184">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="f4ced-185">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="f4ced-185">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-186">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="f4ced-186">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="f4ced-187">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="f4ced-187">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-188">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="f4ced-188">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="f4ced-189">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="f4ced-189">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-190">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f4ced-190">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="f4ced-191">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="f4ced-191">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-192">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="f4ced-192">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="f4ced-193">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="f4ced-193">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-194">ConversationId</span><span class="sxs-lookup"><span data-stu-id="f4ced-194">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="f4ced-195">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="f4ced-195">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-196">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="f4ced-196">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="f4ced-197">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="f4ced-197">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4ced-198">父元素</span><span class="sxs-lookup"><span data-stu-id="f4ced-198">Parent elements</span></span>

|<span data-ttu-id="f4ced-199">**元素**</span><span class="sxs-lookup"><span data-stu-id="f4ced-199">**Element**</span></span>|<span data-ttu-id="f4ced-200">**说明**</span><span class="sxs-lookup"><span data-stu-id="f4ced-200">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4ced-201">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="f4ced-201">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="f4ced-202">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-202">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-203">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="f4ced-203">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="f4ced-204">标识要追加到的项目/文件夹单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。</span><span class="sxs-lookup"><span data-stu-id="f4ced-204">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f4ced-205">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="f4ced-205">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="f4ced-206">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-206">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-207">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f4ced-207">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="f4ced-208">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="f4ced-208">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-209">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f4ced-209">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="f4ced-210">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-210">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-211">Items</span><span class="sxs-lookup"><span data-stu-id="f4ced-211">Items</span></span>](items.md) <br/> |<span data-ttu-id="f4ced-212">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="f4ced-212">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-213">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f4ced-213">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="f4ced-214">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="f4ced-214">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="f4ced-215">SetItemField</span><span class="sxs-lookup"><span data-stu-id="f4ced-215">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="f4ced-216">表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="f4ced-216">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="f4ced-217">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="f4ced-217">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="f4ced-218">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="f4ced-218">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f4ced-219">文本值</span><span class="sxs-lookup"><span data-stu-id="f4ced-219">Text value</span></span>

<span data-ttu-id="f4ced-220">无。</span><span class="sxs-lookup"><span data-stu-id="f4ced-220">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4ced-221">注解</span><span class="sxs-lookup"><span data-stu-id="f4ced-221">Remarks</span></span>

<span data-ttu-id="f4ced-222">请务必注意**ItemType**是[任务](task.md)、[日历项目](calendaritem.md)、[联系人](contact.md)、 [DistributionList](distributionlist.md)和[消息](message-ex15websvcsotherref.md)的基类型。</span><span class="sxs-lookup"><span data-stu-id="f4ced-222">It is important to note that **ItemType** is the base type for [Task](task.md), [CalendarItem](calendaritem.md), [Contact](contact.md), [DistributionList](distributionlist.md), and [Message](message-ex15websvcsotherref.md).</span></span>
  
<span data-ttu-id="f4ced-223">[消息](message-ex15websvcsotherref.md)元素表示电子邮件和非 Exchange Web Services (EWS) 架构的强类型的所有其他项目。</span><span class="sxs-lookup"><span data-stu-id="f4ced-223">[Message](message-ex15websvcsotherref.md) elements represent e-mail messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="f4ced-224">如 IPM 的项目。共享和**消息**元素以返回 IPM.InfoPath。</span><span class="sxs-lookup"><span data-stu-id="f4ced-224">Items such as IPM.Sharing and IPM.InfoPath are returned as **Message** elements.</span></span> <span data-ttu-id="f4ced-225">Microsoft Exchange Server 2010 不在响应中返回基本的**Item**元素。</span><span class="sxs-lookup"><span data-stu-id="f4ced-225">Microsoft Exchange Server 2010 does not return the base **Item** element in responses.</span></span> 
  
<span data-ttu-id="f4ced-226">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f4ced-226">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4ced-227">元素信息</span><span class="sxs-lookup"><span data-stu-id="f4ced-227">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4ced-228">命名空间</span><span class="sxs-lookup"><span data-stu-id="f4ced-228">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f4ced-229">架构名称</span><span class="sxs-lookup"><span data-stu-id="f4ced-229">Schema Name</span></span>  <br/> |<span data-ttu-id="f4ced-230">类型架构</span><span class="sxs-lookup"><span data-stu-id="f4ced-230">Types schema</span></span>  <br/> |
|<span data-ttu-id="f4ced-231">验证文件</span><span class="sxs-lookup"><span data-stu-id="f4ced-231">Validation File</span></span>  <br/> |<span data-ttu-id="f4ced-232">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f4ced-232">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f4ced-233">可以为空</span><span class="sxs-lookup"><span data-stu-id="f4ced-233">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4ced-234">False</span><span class="sxs-lookup"><span data-stu-id="f4ced-234">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4ced-235">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4ced-235">See also</span></span>



- [<span data-ttu-id="f4ced-236">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f4ced-236">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="f4ced-237">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="f4ced-237">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

