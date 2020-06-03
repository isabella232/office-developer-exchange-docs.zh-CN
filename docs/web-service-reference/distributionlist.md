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
description: DistributionList 元素表示通讯组列表。
ms.openlocfilehash: 5eb97bef349ca02848f65fa58370b9c81c6653d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457002"
---
# <a name="distributionlist"></a><span data-ttu-id="7b45a-103">DistributionList</span><span class="sxs-lookup"><span data-stu-id="7b45a-103">DistributionList</span></span>

<span data-ttu-id="7b45a-104">**DistributionList**元素表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="7b45a-104">The **DistributionList** element represents a distribution list.</span></span> 
  
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

 <span data-ttu-id="7b45a-105">**DistributionListType**</span><span class="sxs-lookup"><span data-stu-id="7b45a-105">**DistributionListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b45a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b45a-106">Attributes and elements</span></span>

<span data-ttu-id="7b45a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b45a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b45a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7b45a-108">Attributes</span></span>

<span data-ttu-id="7b45a-109">无。</span><span class="sxs-lookup"><span data-stu-id="7b45a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b45a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7b45a-110">Child elements</span></span>

|<span data-ttu-id="7b45a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b45a-111">**Element**</span></span>|<span data-ttu-id="7b45a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b45a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b45a-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="7b45a-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="7b45a-114">包含以 base64Binary 格式表示的对象的本机 MIME 流。</span><span class="sxs-lookup"><span data-stu-id="7b45a-114">Contains the native MIME stream of an object represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="7b45a-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7b45a-116">包含 Exchange 存储中的通讯组列表项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="7b45a-116">Contains the unique identifier and change key of a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="7b45a-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="7b45a-118">表示包含通讯组列表项的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="7b45a-118">Represents the identifier of the parent folder that contains the distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="7b45a-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="7b45a-120">表示通讯组列表项的邮件类。</span><span class="sxs-lookup"><span data-stu-id="7b45a-120">Represents the message class of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-121">主题</span><span class="sxs-lookup"><span data-stu-id="7b45a-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="7b45a-122">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="7b45a-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="7b45a-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="7b45a-124">包含通讯组列表项的敏感度状态。</span><span class="sxs-lookup"><span data-stu-id="7b45a-124">Contains the status for a distribution list item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-125">Body</span><span class="sxs-lookup"><span data-stu-id="7b45a-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="7b45a-126">表示通讯组列表项的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="7b45a-126">Represents the actual body content of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-127">附件</span><span class="sxs-lookup"><span data-stu-id="7b45a-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7b45a-128">包含附加到 Exchange 存储中的通讯组列表项的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="7b45a-128">Contains the items or files that are attached to a distribution list item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="7b45a-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="7b45a-130">表示接收邮箱中的通讯组列表项的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7b45a-130">Represents the date and time that a distribution list item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-131">大小</span><span class="sxs-lookup"><span data-stu-id="7b45a-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="7b45a-132">表示通讯组列表项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="7b45a-132">Represents the size, in bytes, of a distribution list item.</span></span> <span data-ttu-id="7b45a-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="7b45a-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-134">类别</span><span class="sxs-lookup"><span data-stu-id="7b45a-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7b45a-135">表示一个字符串集合，这些字符串标识邮箱中的通讯组列表项所属的类别。</span><span class="sxs-lookup"><span data-stu-id="7b45a-135">Represents a collection of strings that identify to which categories a distribution list item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-136">Importance</span><span class="sxs-lookup"><span data-stu-id="7b45a-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="7b45a-137">描述通讯组列表项的重要性。</span><span class="sxs-lookup"><span data-stu-id="7b45a-137">Describes the importance of a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="7b45a-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="7b45a-139">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="7b45a-139">Represents the identifier of the item which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="7b45a-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="7b45a-141">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="7b45a-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="7b45a-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="7b45a-143">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="7b45a-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="7b45a-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="7b45a-145">指示用户是否向其自身发送了项目。</span><span class="sxs-lookup"><span data-stu-id="7b45a-145">Indicates whether a user sent an item to itself.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="7b45a-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="7b45a-147">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="7b45a-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="7b45a-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="7b45a-149">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="7b45a-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-150">Message</span><span class="sxs-lookup"><span data-stu-id="7b45a-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="7b45a-151">表示邮箱中的项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="7b45a-151">Represents the collection of all Internet message headers contained within an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="7b45a-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="7b45a-153">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7b45a-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="7b45a-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="7b45a-155">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7b45a-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="7b45a-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="7b45a-157">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="7b45a-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="7b45a-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="7b45a-159">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="7b45a-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="7b45a-160">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="7b45a-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="7b45a-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="7b45a-162">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="7b45a-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="7b45a-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="7b45a-164">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="7b45a-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="7b45a-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="7b45a-166">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="7b45a-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="7b45a-167">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="7b45a-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="7b45a-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="7b45a-169">表示用于 "To" 行的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="7b45a-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="7b45a-170">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="7b45a-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="7b45a-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="7b45a-172">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="7b45a-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="7b45a-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="7b45a-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="7b45a-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="7b45a-175">标识通讯组列表项上的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="7b45a-175">Identifies extended properties on a distribution list item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-176">Culture</span><span class="sxs-lookup"><span data-stu-id="7b45a-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="7b45a-177">表示邮箱中的通讯组列表项的区域性。</span><span class="sxs-lookup"><span data-stu-id="7b45a-177">Represents the culture for a distribution list item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="7b45a-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="7b45a-p106">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="7b45a-p106">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="7b45a-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="7b45a-182">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7b45a-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="7b45a-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="7b45a-184">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="7b45a-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="7b45a-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="7b45a-186">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="7b45a-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7b45a-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="7b45a-188">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="7b45a-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="7b45a-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="7b45a-190">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="7b45a-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="7b45a-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="7b45a-192">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="7b45a-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="7b45a-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="7b45a-194">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="7b45a-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-195">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="7b45a-195">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="7b45a-196">定义通讯组列表的显示名称。</span><span class="sxs-lookup"><span data-stu-id="7b45a-196">Defines the display name of a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-197">FileAs</span><span class="sxs-lookup"><span data-stu-id="7b45a-197">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="7b45a-198">表示如何在 "联系人" 文件夹中存档通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="7b45a-198">Represents how a distribution list is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-199">ContactSource</span><span class="sxs-lookup"><span data-stu-id="7b45a-199">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="7b45a-200">描述联系人是否位于 Exchange 存储区或 Active Directory 域服务（AD DS）中。</span><span class="sxs-lookup"><span data-stu-id="7b45a-200">Describes whether the contact is located in the Exchange store or in Active Directory Domain Services (AD DS).</span></span>  <br/> |
|[<span data-ttu-id="7b45a-201">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="7b45a-201">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="7b45a-202">包含通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="7b45a-202">Contains a list of members of the distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b45a-203">父元素</span><span class="sxs-lookup"><span data-stu-id="7b45a-203">Parent elements</span></span>

|<span data-ttu-id="7b45a-204">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b45a-204">**Element**</span></span>|<span data-ttu-id="7b45a-205">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b45a-205">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b45a-206">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="7b45a-206">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="7b45a-207">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="7b45a-207">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-208">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="7b45a-208">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="7b45a-209">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到通讯组列表的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="7b45a-209">Identifies data to append to a single property of a distribution list during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="7b45a-210">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="7b45a-210">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="7b45a-211">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="7b45a-211">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-212">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="7b45a-212">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="7b45a-213">标识要在本地客户端存储中创建的单个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="7b45a-213">Identifies a single distribution list to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-214">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="7b45a-214">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="7b45a-215">标识要在本地客户端存储中更新的单个通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="7b45a-215">Identifies a single distribution list to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-216">Items</span><span class="sxs-lookup"><span data-stu-id="7b45a-216">Items</span></span>](items.md) <br/> |<span data-ttu-id="7b45a-217">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="7b45a-217">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-218">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="7b45a-218">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="7b45a-219">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="7b45a-219">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="7b45a-220">SetItemField</span><span class="sxs-lookup"><span data-stu-id="7b45a-220">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="7b45a-221">表示对[UpdateItem 操作](updateitem-operation.md)中的通讯组列表项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="7b45a-221">Represents an update to a single property of a distribution list item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7b45a-222">文本值</span><span class="sxs-lookup"><span data-stu-id="7b45a-222">Text value</span></span>

<span data-ttu-id="7b45a-223">无。</span><span class="sxs-lookup"><span data-stu-id="7b45a-223">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b45a-224">说明</span><span class="sxs-lookup"><span data-stu-id="7b45a-224">Remarks</span></span>

<span data-ttu-id="7b45a-225">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b45a-225">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b45a-226">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b45a-226">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b45a-227">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b45a-227">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b45a-228">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b45a-228">Schema Name</span></span>  <br/> |<span data-ttu-id="7b45a-229">类型架构</span><span class="sxs-lookup"><span data-stu-id="7b45a-229">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b45a-230">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b45a-230">Validation File</span></span>  <br/> |<span data-ttu-id="7b45a-231">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b45a-231">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b45a-232">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b45a-232">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b45a-233">False</span><span class="sxs-lookup"><span data-stu-id="7b45a-233">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b45a-234">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b45a-234">See also</span></span>

- [<span data-ttu-id="7b45a-235">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7b45a-235">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

