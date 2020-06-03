---
title: Contact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: Contact 元素表示 Exchange 存储中的联系人项目。
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44445648"
---
# <a name="contact"></a><span data-ttu-id="254da-103">Contact</span><span class="sxs-lookup"><span data-stu-id="254da-103">Contact</span></span>

<span data-ttu-id="254da-104">**Contact**元素表示 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="254da-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
```XML
<Contact>
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
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 <span data-ttu-id="254da-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="254da-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="254da-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="254da-106">Attributes and elements</span></span>

<span data-ttu-id="254da-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="254da-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="254da-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="254da-108">Attributes</span></span>

<span data-ttu-id="254da-109">无。</span><span class="sxs-lookup"><span data-stu-id="254da-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="254da-110">子元素</span><span class="sxs-lookup"><span data-stu-id="254da-110">Child elements</span></span>

|<span data-ttu-id="254da-111">**元素名**</span><span class="sxs-lookup"><span data-stu-id="254da-111">**Element name**</span></span>|<span data-ttu-id="254da-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="254da-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="254da-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="254da-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="254da-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="254da-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="254da-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="254da-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="254da-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="254da-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="254da-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="254da-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="254da-118">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="254da-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="254da-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="254da-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="254da-120">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="254da-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="254da-121">主题</span><span class="sxs-lookup"><span data-stu-id="254da-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="254da-122">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="254da-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="254da-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="254da-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="254da-124">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="254da-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="254da-125">Body</span><span class="sxs-lookup"><span data-stu-id="254da-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="254da-126">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="254da-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="254da-127">附件</span><span class="sxs-lookup"><span data-stu-id="254da-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="254da-128">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="254da-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="254da-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="254da-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="254da-130">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="254da-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="254da-131">大小</span><span class="sxs-lookup"><span data-stu-id="254da-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="254da-132">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="254da-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="254da-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="254da-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="254da-134">类别</span><span class="sxs-lookup"><span data-stu-id="254da-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="254da-135">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="254da-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="254da-136">Importance</span><span class="sxs-lookup"><span data-stu-id="254da-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="254da-137">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="254da-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="254da-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="254da-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="254da-139">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="254da-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="254da-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="254da-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="254da-141">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="254da-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="254da-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="254da-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="254da-143">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="254da-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="254da-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="254da-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="254da-145">指示用户是否向自己发送了一个项目。</span><span class="sxs-lookup"><span data-stu-id="254da-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="254da-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="254da-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="254da-147">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="254da-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="254da-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="254da-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="254da-149">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="254da-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="254da-150">Message</span><span class="sxs-lookup"><span data-stu-id="254da-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="254da-151">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="254da-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="254da-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="254da-153">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="254da-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="254da-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="254da-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="254da-155">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="254da-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="254da-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="254da-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="254da-157">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="254da-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="254da-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="254da-159">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="254da-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="254da-160">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="254da-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="254da-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="254da-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="254da-162">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="254da-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="254da-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="254da-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="254da-164">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="254da-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="254da-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="254da-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="254da-166">代表用于 "抄送" 行内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="254da-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="254da-167">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="254da-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="254da-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="254da-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="254da-169">表示用于 "To" 行的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="254da-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="254da-170">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="254da-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="254da-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="254da-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="254da-172">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="254da-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="254da-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="254da-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="254da-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="254da-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="254da-175">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="254da-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="254da-176">Culture</span><span class="sxs-lookup"><span data-stu-id="254da-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="254da-177">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="254da-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="254da-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="254da-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="254da-p106">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="254da-p106">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="254da-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="254da-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="254da-182">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="254da-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="254da-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="254da-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="254da-184">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="254da-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="254da-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="254da-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="254da-186">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="254da-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="254da-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="254da-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="254da-188">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="254da-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="254da-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="254da-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="254da-190">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="254da-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="254da-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="254da-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="254da-192">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="254da-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="254da-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="254da-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="254da-194">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="254da-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="254da-195">FileAs</span><span class="sxs-lookup"><span data-stu-id="254da-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="254da-196">表示联系人在 "联系人" 文件夹中的存档方式。</span><span class="sxs-lookup"><span data-stu-id="254da-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="254da-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="254da-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="254da-198">定义如何构建联系人的显示内容。</span><span class="sxs-lookup"><span data-stu-id="254da-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-199">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="254da-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="254da-200">定义联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="254da-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-201">GivenName</span><span class="sxs-lookup"><span data-stu-id="254da-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="254da-202">包含联系人的名称。</span><span class="sxs-lookup"><span data-stu-id="254da-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="254da-203">缩写</span><span class="sxs-lookup"><span data-stu-id="254da-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="254da-204">代表联系人的缩写。</span><span class="sxs-lookup"><span data-stu-id="254da-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="254da-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="254da-206">表示联系人的中间名。</span><span class="sxs-lookup"><span data-stu-id="254da-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-207">昵称</span><span class="sxs-lookup"><span data-stu-id="254da-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="254da-208">表示联系人的昵称。</span><span class="sxs-lookup"><span data-stu-id="254da-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-209">CompleteName</span><span class="sxs-lookup"><span data-stu-id="254da-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="254da-210">表示某个联系人的完整名称。</span><span class="sxs-lookup"><span data-stu-id="254da-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-211">CompanyName</span><span class="sxs-lookup"><span data-stu-id="254da-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="254da-212">表示与联系人关联的公司名称。</span><span class="sxs-lookup"><span data-stu-id="254da-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="254da-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="254da-214">表示联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="254da-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="254da-216">包含与联系人关联的物理地址的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="254da-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="254da-218">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="254da-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="254da-220">表示联系人的助理。</span><span class="sxs-lookup"><span data-stu-id="254da-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-221">生日</span><span class="sxs-lookup"><span data-stu-id="254da-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="254da-222">表示联系人的出生日期。</span><span class="sxs-lookup"><span data-stu-id="254da-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="254da-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="254da-224">表示联系人的主页（Web 地址）。</span><span class="sxs-lookup"><span data-stu-id="254da-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-225">子女</span><span class="sxs-lookup"><span data-stu-id="254da-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="254da-226">包含联系人子女的姓名。</span><span class="sxs-lookup"><span data-stu-id="254da-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="254da-227">Companies</span><span class="sxs-lookup"><span data-stu-id="254da-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="254da-228">表示与联系人关联的公司的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="254da-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="254da-230">描述联系人是否位于 Exchange 存储或 Active Directory 目录服务中。</span><span class="sxs-lookup"><span data-stu-id="254da-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="254da-231">Department</span><span class="sxs-lookup"><span data-stu-id="254da-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="254da-232">代表工作中联系人的部门。</span><span class="sxs-lookup"><span data-stu-id="254da-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="254da-233">生成</span><span class="sxs-lookup"><span data-stu-id="254da-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="254da-234">代表联系人的全名后面的代缩写。</span><span class="sxs-lookup"><span data-stu-id="254da-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-235">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="254da-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="254da-236">表示联系人的即时消息地址的集合。</span><span class="sxs-lookup"><span data-stu-id="254da-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="254da-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="254da-238">表示联系人的职务。</span><span class="sxs-lookup"><span data-stu-id="254da-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-239">Manager</span><span class="sxs-lookup"><span data-stu-id="254da-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="254da-240">表示联系人的经理。</span><span class="sxs-lookup"><span data-stu-id="254da-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="254da-241">Mileage</span><span class="sxs-lookup"><span data-stu-id="254da-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="254da-242">表示联系人项目的里程。</span><span class="sxs-lookup"><span data-stu-id="254da-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="254da-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="254da-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="254da-244">表示联系人的办公室位置。</span><span class="sxs-lookup"><span data-stu-id="254da-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="254da-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="254da-246">表示物理地址的显示类型。</span><span class="sxs-lookup"><span data-stu-id="254da-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="254da-247">职业</span><span class="sxs-lookup"><span data-stu-id="254da-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="254da-248">表示联系人的职业。</span><span class="sxs-lookup"><span data-stu-id="254da-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-249">SpouseName</span><span class="sxs-lookup"><span data-stu-id="254da-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="254da-250">表示联系人配偶/伴侣的名称。</span><span class="sxs-lookup"><span data-stu-id="254da-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="254da-251">姓氏</span><span class="sxs-lookup"><span data-stu-id="254da-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="254da-252">表示联系人的姓氏。</span><span class="sxs-lookup"><span data-stu-id="254da-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="254da-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="254da-254">包含联系人的婚礼周年纪念。</span><span class="sxs-lookup"><span data-stu-id="254da-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="254da-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="254da-256">指示联系人项目是否具有表示联系人图片的文件附件。</span><span class="sxs-lookup"><span data-stu-id="254da-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="254da-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="254da-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="254da-258">包含联系人的全名，包括名字和姓氏（按发音拼写）。</span><span class="sxs-lookup"><span data-stu-id="254da-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="254da-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="254da-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="254da-260">包含按发音拼写的联系人的第一个名称。</span><span class="sxs-lookup"><span data-stu-id="254da-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="254da-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="254da-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="254da-262">包含按发音拼写的联系人的姓氏。</span><span class="sxs-lookup"><span data-stu-id="254da-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="254da-263">Alias</span><span class="sxs-lookup"><span data-stu-id="254da-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="254da-264">包含联系人的电子邮件别名。</span><span class="sxs-lookup"><span data-stu-id="254da-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-265">注释（联系人）</span><span class="sxs-lookup"><span data-stu-id="254da-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="254da-266">包含附属联系人信息。</span><span class="sxs-lookup"><span data-stu-id="254da-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="254da-267">照片</span><span class="sxs-lookup"><span data-stu-id="254da-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="254da-268">包含对联系人的照片进行编码的值。</span><span class="sxs-lookup"><span data-stu-id="254da-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="254da-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="254da-270">包含对联系人的 SMIME 证书进行编码的值。</span><span class="sxs-lookup"><span data-stu-id="254da-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="254da-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="254da-272">包含对联系人的 Microsoft Exchange 证书进行编码的值。</span><span class="sxs-lookup"><span data-stu-id="254da-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-273">DirectoryId</span><span class="sxs-lookup"><span data-stu-id="254da-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="254da-274">包含联系人的目录 ID。</span><span class="sxs-lookup"><span data-stu-id="254da-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-275">ManagerMailbox</span><span class="sxs-lookup"><span data-stu-id="254da-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="254da-276">包含标识联系人的经理邮箱的 SMTP 信息。</span><span class="sxs-lookup"><span data-stu-id="254da-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="254da-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="254da-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="254da-278">包含标识联系人的直接下属的 SMTP 信息。</span><span class="sxs-lookup"><span data-stu-id="254da-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="254da-279">父元素</span><span class="sxs-lookup"><span data-stu-id="254da-279">Parent elements</span></span>

|<span data-ttu-id="254da-280">**元素名**</span><span class="sxs-lookup"><span data-stu-id="254da-280">**Element name**</span></span>|<span data-ttu-id="254da-281">**说明**</span><span class="sxs-lookup"><span data-stu-id="254da-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="254da-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="254da-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="254da-283">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="254da-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="254da-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="254da-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="254da-285">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项或文件夹的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="254da-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="254da-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="254da-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="254da-287">标识与会议时间冲突的所有项</span><span class="sxs-lookup"><span data-stu-id="254da-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="254da-288">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="254da-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="254da-289">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="254da-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="254da-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="254da-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="254da-291">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="254da-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="254da-292">Items</span><span class="sxs-lookup"><span data-stu-id="254da-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="254da-293">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="254da-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="254da-294">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="254da-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="254da-295">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="254da-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="254da-296">解决方法</span><span class="sxs-lookup"><span data-stu-id="254da-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="254da-297">包含单个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="254da-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="254da-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="254da-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="254da-299">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="254da-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="254da-300">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="254da-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="254da-301">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="254da-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="254da-302">文本值</span><span class="sxs-lookup"><span data-stu-id="254da-302">Text value</span></span>

<span data-ttu-id="254da-303">无。</span><span class="sxs-lookup"><span data-stu-id="254da-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="254da-304">说明</span><span class="sxs-lookup"><span data-stu-id="254da-304">Remarks</span></span>

<span data-ttu-id="254da-305">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="254da-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="254da-306">元素信息</span><span class="sxs-lookup"><span data-stu-id="254da-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="254da-307">命名空间</span><span class="sxs-lookup"><span data-stu-id="254da-307">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="254da-308">架构名称</span><span class="sxs-lookup"><span data-stu-id="254da-308">Schema name</span></span>  <br/> |<span data-ttu-id="254da-309">类型架构</span><span class="sxs-lookup"><span data-stu-id="254da-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="254da-310">验证文件</span><span class="sxs-lookup"><span data-stu-id="254da-310">Validation file</span></span>  <br/> |<span data-ttu-id="254da-311">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="254da-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="254da-312">可以为空</span><span class="sxs-lookup"><span data-stu-id="254da-312">Can be empty</span></span>  <br/> |<span data-ttu-id="254da-313">False</span><span class="sxs-lookup"><span data-stu-id="254da-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="254da-314">另请参阅</span><span class="sxs-lookup"><span data-stu-id="254da-314">See also</span></span>



- [<span data-ttu-id="254da-315">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="254da-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="254da-316">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="254da-316">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="254da-317">更新联系人</span><span class="sxs-lookup"><span data-stu-id="254da-317">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="254da-318">删除联系人</span><span class="sxs-lookup"><span data-stu-id="254da-318">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

