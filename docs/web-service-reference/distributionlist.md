---
title: DistributionList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistributionList
api_type:
- schema
ms.assetid: f65aea01-e870-44a2-8571-fa6c001341cc
description: DistributionList 元素均表示通讯组列表。
ms.openlocfilehash: 5edcc83eef6a5b16470e6c290aacd057ceecceb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753961"
---
# <a name="distributionlist"></a><span data-ttu-id="b2229-103">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b2229-103">DistributionList</span></span>

<span data-ttu-id="b2229-104">**DistributionList**元素均表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b2229-104">The **DistributionList** element represents a distribution list.</span></span> 
  
```xml
<DistributionList>
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
   <DisplayName/>
   <FileAs/>
   <ContactSource/>
   <Members/>
</DistributionList>
```

 <span data-ttu-id="b2229-105">**DistributionListType**</span><span class="sxs-lookup"><span data-stu-id="b2229-105">**DistributionListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2229-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b2229-106">Attributes and elements</span></span>

<span data-ttu-id="b2229-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b2229-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2229-108">属性</span><span class="sxs-lookup"><span data-stu-id="b2229-108">Attributes</span></span>

<span data-ttu-id="b2229-109">无。</span><span class="sxs-lookup"><span data-stu-id="b2229-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2229-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b2229-110">Child elements</span></span>

|<span data-ttu-id="b2229-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2229-111">**Element**</span></span>|<span data-ttu-id="b2229-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2229-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2229-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="b2229-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="b2229-114">包含 base64Binary 格式表示的对象的本机 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="b2229-114">Contains the native MIME stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="b2229-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="b2229-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b2229-116">包含在 Exchange 存储中的通讯组列表项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="b2229-116">Contains the unique identifier and change key of a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b2229-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="b2229-118">表示包含通讯组列表项的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="b2229-118">Represents the identifier of the parent folder that contains the distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="b2229-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="b2229-120">表示通讯组列表项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="b2229-120">Represents the message class of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-121">Subject</span><span class="sxs-lookup"><span data-stu-id="b2229-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="b2229-122">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="b2229-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="b2229-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="b2229-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="b2229-124">包含通讯组列表项的敏感度的状态。</span><span class="sxs-lookup"><span data-stu-id="b2229-124">Contains the status for a distribution list item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="b2229-125">Body</span><span class="sxs-lookup"><span data-stu-id="b2229-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="b2229-126">表示通讯组列表项目的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="b2229-126">Represents the actual body content of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-127">附件</span><span class="sxs-lookup"><span data-stu-id="b2229-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b2229-128">包含的项或附加到 Exchange 存储中的通讯组列表项的文件。</span><span class="sxs-lookup"><span data-stu-id="b2229-128">Contains the items or files that are attached to a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="b2229-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="b2229-130">表示的日期和已接收邮箱中的通讯组列表项的时间。</span><span class="sxs-lookup"><span data-stu-id="b2229-130">Represents the date and time that a distribution list item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="b2229-131">Size</span><span class="sxs-lookup"><span data-stu-id="b2229-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="b2229-132">表示的大小，以字节为单位的通讯组列表项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-132">Represents the size, in bytes, of a distribution list item.</span></span> <span data-ttu-id="b2229-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b2229-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b2229-134">类别</span><span class="sxs-lookup"><span data-stu-id="b2229-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b2229-135">表示标识的邮箱中通讯组列表项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="b2229-135">Represents a collection of strings that identify to which categories a distribution list item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="b2229-136">Importance</span><span class="sxs-lookup"><span data-stu-id="b2229-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="b2229-137">介绍通讯组列表项的重要性。</span><span class="sxs-lookup"><span data-stu-id="b2229-137">Describes the importance of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="b2229-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="b2229-139">表示此项是答复 （英文） 中的项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="b2229-139">Represents the identifier of the item which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="b2229-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="b2229-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="b2229-141">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="b2229-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="b2229-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="b2229-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="b2229-143">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="b2229-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="b2229-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="b2229-145">指示用户是否发送到其自身的项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-145">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="b2229-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="b2229-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="b2229-147">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="b2229-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="b2229-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="b2229-149">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="b2229-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b2229-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b2229-151">代表邮箱中的一个项内包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="b2229-151">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b2229-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="b2229-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="b2229-153">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="b2229-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="b2229-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="b2229-155">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="b2229-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="b2229-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="b2229-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="b2229-157">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="b2229-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="b2229-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="b2229-159">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="b2229-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="b2229-160">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="b2229-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b2229-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="b2229-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="b2229-162">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="b2229-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="b2229-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="b2229-164">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="b2229-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="b2229-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="b2229-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="b2229-166">表示用于 Cc 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b2229-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="b2229-167">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="b2229-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b2229-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="b2229-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="b2229-169">表示用于 To 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="b2229-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="b2229-170">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="b2229-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="b2229-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="b2229-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="b2229-172">表示如果项目具有至少一个可见的附件设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="b2229-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="b2229-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b2229-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b2229-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="b2229-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b2229-175">标识通讯组列表项上的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b2229-175">Identifies extended properties on a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-176">区域性</span><span class="sxs-lookup"><span data-stu-id="b2229-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="b2229-177">表示邮箱中的通讯组列表项的区域性。</span><span class="sxs-lookup"><span data-stu-id="b2229-177">Represents the culture for a distribution list item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="b2229-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b2229-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b2229-p106">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="b2229-p106">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b2229-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="b2229-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="b2229-182">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b2229-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="b2229-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="b2229-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="b2229-184">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="b2229-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="b2229-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="b2229-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="b2229-186">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="b2229-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="b2229-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b2229-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="b2229-188">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2229-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b2229-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="b2229-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="b2229-190">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2229-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="b2229-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="b2229-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="b2229-192">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="b2229-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="b2229-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="b2229-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="b2229-194">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="b2229-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="b2229-195">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="b2229-195">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b2229-196">定义通讯组列表的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b2229-196">Defines the display name of a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="b2229-197">FileAs</span><span class="sxs-lookup"><span data-stu-id="b2229-197">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="b2229-198">表示通讯组列表联系人文件夹中的字段如何。</span><span class="sxs-lookup"><span data-stu-id="b2229-198">Represents how a distribution list is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="b2229-199">ContactSource</span><span class="sxs-lookup"><span data-stu-id="b2229-199">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="b2229-200">描述联系人是否位于 Exchange 存储中或 Active Directory 域服务 (AD DS) 中。</span><span class="sxs-lookup"><span data-stu-id="b2229-200">Describes whether the contact is located in the Exchange store or in Active Directory Domain Services (AD DS).</span></span>  <br/> |
|[<span data-ttu-id="b2229-201">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="b2229-201">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="b2229-202">包含通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="b2229-202">Contains a list of members of the distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2229-203">父元素</span><span class="sxs-lookup"><span data-stu-id="b2229-203">Parent elements</span></span>

|<span data-ttu-id="b2229-204">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2229-204">**Element**</span></span>|<span data-ttu-id="b2229-205">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2229-205">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2229-206">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="b2229-206">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="b2229-207">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-207">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="b2229-208">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="b2229-208">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="b2229-209">标识要追加到通讯组列表的单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。</span><span class="sxs-lookup"><span data-stu-id="b2229-209">Identifies data to append to a single property of a distribution list during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b2229-210">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="b2229-210">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="b2229-211">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="b2229-211">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="b2229-212">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="b2229-212">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="b2229-213">标识本地客户端存储中创建的单个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b2229-213">Identifies a single distribution list to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-214">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="b2229-214">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="b2229-215">标识更新本地客户端存储中的单个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b2229-215">Identifies a single distribution list to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b2229-216">Items</span><span class="sxs-lookup"><span data-stu-id="b2229-216">Items</span></span>](items.md) <br/> |<span data-ttu-id="b2229-217">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="b2229-217">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="b2229-218">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="b2229-218">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="b2229-219">包含在由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="b2229-219">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="b2229-220">SetItemField</span><span class="sxs-lookup"><span data-stu-id="b2229-220">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="b2229-221">向通讯组列表项[UpdateItem 操作](updateitem-operation.md)中的单个属性表示更新。</span><span class="sxs-lookup"><span data-stu-id="b2229-221">Represents an update to a single property of a distribution list item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b2229-222">文本值</span><span class="sxs-lookup"><span data-stu-id="b2229-222">Text value</span></span>

<span data-ttu-id="b2229-223">无。</span><span class="sxs-lookup"><span data-stu-id="b2229-223">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2229-224">备注</span><span class="sxs-lookup"><span data-stu-id="b2229-224">Remarks</span></span>

<span data-ttu-id="b2229-225">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b2229-225">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2229-226">元素信息</span><span class="sxs-lookup"><span data-stu-id="b2229-226">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2229-227">命名空间</span><span class="sxs-lookup"><span data-stu-id="b2229-227">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b2229-228">架构名称</span><span class="sxs-lookup"><span data-stu-id="b2229-228">Schema Name</span></span>  <br/> |<span data-ttu-id="b2229-229">类型架构</span><span class="sxs-lookup"><span data-stu-id="b2229-229">Types schema</span></span>  <br/> |
|<span data-ttu-id="b2229-230">验证文件</span><span class="sxs-lookup"><span data-stu-id="b2229-230">Validation File</span></span>  <br/> |<span data-ttu-id="b2229-231">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b2229-231">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b2229-232">可以为空</span><span class="sxs-lookup"><span data-stu-id="b2229-232">Can be Empty</span></span>  <br/> |<span data-ttu-id="b2229-233">False</span><span class="sxs-lookup"><span data-stu-id="b2229-233">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2229-234">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2229-234">See also</span></span>

- [<span data-ttu-id="b2229-235">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b2229-235">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

