---
title: 联系人
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
description: 联系人元素表示 Exchange 存储中的联系人项目。
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753499"
---
# <a name="contact"></a><span data-ttu-id="6b3c2-103">联系人</span><span class="sxs-lookup"><span data-stu-id="6b3c2-103">Contact</span></span>

<span data-ttu-id="6b3c2-104">**联系人**元素表示 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-104">The **Contact** element represents a contact item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="6b3c2-105">**ContactItemType**</span><span class="sxs-lookup"><span data-stu-id="6b3c2-105">**ContactItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b3c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6b3c2-106">Attributes and elements</span></span>

<span data-ttu-id="6b3c2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b3c2-108">属性</span><span class="sxs-lookup"><span data-stu-id="6b3c2-108">Attributes</span></span>

<span data-ttu-id="6b3c2-109">无。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b3c2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6b3c2-110">Child elements</span></span>

|<span data-ttu-id="6b3c2-111">**元素名**</span><span class="sxs-lookup"><span data-stu-id="6b3c2-111">**Element name**</span></span>|<span data-ttu-id="6b3c2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b3c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b3c2-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="6b3c2-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="6b3c2-114">包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="6b3c2-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="6b3c2-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="6b3c2-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="6b3c2-118">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="6b3c2-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="6b3c2-120">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-121">Subject</span><span class="sxs-lookup"><span data-stu-id="6b3c2-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="6b3c2-122">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="6b3c2-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="6b3c2-124">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-124">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-125">Body</span><span class="sxs-lookup"><span data-stu-id="6b3c2-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="6b3c2-126">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-127">附件</span><span class="sxs-lookup"><span data-stu-id="6b3c2-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6b3c2-128">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="6b3c2-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="6b3c2-130">表示的日期和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-131">Size</span><span class="sxs-lookup"><span data-stu-id="6b3c2-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="6b3c2-132">表示以字节为单位的项目的大小。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-132">Represents the size in bytes of an item.</span></span> <span data-ttu-id="6b3c2-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-134">类别</span><span class="sxs-lookup"><span data-stu-id="6b3c2-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6b3c2-135">表示标识的邮箱中项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-136">Importance</span><span class="sxs-lookup"><span data-stu-id="6b3c2-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="6b3c2-137">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="6b3c2-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="6b3c2-139">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="6b3c2-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="6b3c2-141">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="6b3c2-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="6b3c2-143">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="6b3c2-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="6b3c2-145">指示用户是否发送给自己的项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-145">Indicates whether a user sent an item to himself or herself.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="6b3c2-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="6b3c2-147">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="6b3c2-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="6b3c2-149">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="6b3c2-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="6b3c2-151">代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="6b3c2-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="6b3c2-153">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="6b3c2-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="6b3c2-155">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="6b3c2-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="6b3c2-157">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="6b3c2-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="6b3c2-159">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="6b3c2-160">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="6b3c2-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="6b3c2-162">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="6b3c2-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="6b3c2-164">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="6b3c2-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="6b3c2-166">表示用于 Cc 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-166">Represents the display string that is used for the contents of the Cc line.</span></span> <span data-ttu-id="6b3c2-167">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="6b3c2-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="6b3c2-169">表示用于 To 行的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-169">Represents the display string that is used for the contents of the To line.</span></span> <span data-ttu-id="6b3c2-170">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="6b3c2-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="6b3c2-172">表示如果项目具有至少一个可见的附件设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="6b3c2-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="6b3c2-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="6b3c2-175">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-176">区域性</span><span class="sxs-lookup"><span data-stu-id="6b3c2-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="6b3c2-177">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-178">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="6b3c2-178">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="6b3c2-p106">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-p106">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-181">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-181">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="6b3c2-182">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-182">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-183">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="6b3c2-183">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="6b3c2-184">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-184">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-185">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="6b3c2-185">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="6b3c2-186">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-186">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-187">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="6b3c2-187">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="6b3c2-188">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-188">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-189">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="6b3c2-189">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="6b3c2-190">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-190">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-191">ConversationId</span><span class="sxs-lookup"><span data-stu-id="6b3c2-191">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="6b3c2-192">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-192">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-193">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="6b3c2-193">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="6b3c2-194">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-194">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-195">FileAs</span><span class="sxs-lookup"><span data-stu-id="6b3c2-195">FileAs</span></span>](fileas.md) <br/> |<span data-ttu-id="6b3c2-196">代表联系人联系人文件夹中的存档的方式。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-196">Represents how a contact is filed in the Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-197">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="6b3c2-197">FileAsMapping</span></span>](fileasmapping.md) <br/> |<span data-ttu-id="6b3c2-198">定义如何构造联系人显示的内容。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-198">Defines how to construct what is displayed for a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-199">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="6b3c2-199">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="6b3c2-200">定义一个联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-200">Defines the display name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-201">GivenName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-201">GivenName</span></span>](givenname.md) <br/> |<span data-ttu-id="6b3c2-202">包含联系人的名字。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-202">Contains a contact's given name.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-203">首字母缩写</span><span class="sxs-lookup"><span data-stu-id="6b3c2-203">Initials</span></span>](initials.md) <br/> |<span data-ttu-id="6b3c2-204">代表联系人的姓名缩写。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-204">Represents the initials of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-205">MiddleName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-205">MiddleName</span></span>](middlename.md) <br/> |<span data-ttu-id="6b3c2-206">代表中间名的联系人。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-206">Represents the middle name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-207">昵称</span><span class="sxs-lookup"><span data-stu-id="6b3c2-207">Nickname</span></span>](nickname.md) <br/> |<span data-ttu-id="6b3c2-208">代表联系人的别名。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-208">Represents the nickname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-209">CompleteName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-209">CompleteName</span></span>](completename.md) <br/> |<span data-ttu-id="6b3c2-210">表示某个联系人的完整名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-210">Represents the complete name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-211">公司名称</span><span class="sxs-lookup"><span data-stu-id="6b3c2-211">CompanyName</span></span>](companyname.md) <br/> |<span data-ttu-id="6b3c2-212">表示与联系人关联的公司名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-212">Represents the company name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-213">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="6b3c2-213">EmailAddresses</span></span>](emailaddresses.md) <br/> |<span data-ttu-id="6b3c2-214">表示一个联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-214">Represents a collection of e-mail addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-215">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="6b3c2-215">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="6b3c2-216">包含与联系人关联的物理地址的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-216">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-217">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="6b3c2-217">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="6b3c2-218">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-218">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-219">AssistantName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-219">AssistantName</span></span>](assistantname.md) <br/> |<span data-ttu-id="6b3c2-220">向联系人代表助理。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-220">Represents an assistant to a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-221">生日</span><span class="sxs-lookup"><span data-stu-id="6b3c2-221">Birthday</span></span>](birthday.md) <br/> |<span data-ttu-id="6b3c2-222">表示联系人出生日期。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-222">Represents the birth date of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-223">BusinessHomePage</span><span class="sxs-lookup"><span data-stu-id="6b3c2-223">BusinessHomePage</span></span>](businesshomepage.md) <br/> |<span data-ttu-id="6b3c2-224">代表联系人主页上 （Web 地址）。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-224">Represents the Home page (Web address) for the contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-225">子女</span><span class="sxs-lookup"><span data-stu-id="6b3c2-225">Children</span></span>](children.md) <br/> |<span data-ttu-id="6b3c2-226">包含联系人的子级的名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-226">Contains the names of a contact's children.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-227">公司</span><span class="sxs-lookup"><span data-stu-id="6b3c2-227">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="6b3c2-228">代表与联系人关联的公司的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-228">Represents the collection of companies that are associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-229">ContactSource</span><span class="sxs-lookup"><span data-stu-id="6b3c2-229">ContactSource</span></span>](contactsource.md) <br/> |<span data-ttu-id="6b3c2-230">描述联系人是否位于 Exchange 存储或 Active Directory 目录服务。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-230">Describes whether the contact is located in the Exchange store or the Active Directory directory service.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-231">部门</span><span class="sxs-lookup"><span data-stu-id="6b3c2-231">Department</span></span>](department.md) <br/> |<span data-ttu-id="6b3c2-232">代表在工作场所的联系人所在的部门。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-232">Represents the contact's department at work.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-233">生成</span><span class="sxs-lookup"><span data-stu-id="6b3c2-233">Generation</span></span>](generation.md) <br/> |<span data-ttu-id="6b3c2-234">代表代缩写的联系人的完整名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-234">Represents a generational abbreviation that follows the full name of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-235">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="6b3c2-235">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="6b3c2-236">表示一个联系人的即时消息地址的集合。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-236">Represents a collection of instant messaging addresses for a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-237">JobTitle</span><span class="sxs-lookup"><span data-stu-id="6b3c2-237">JobTitle</span></span>](jobtitle.md) <br/> |<span data-ttu-id="6b3c2-238">代表联系人的职务。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-238">Represents the job title of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-239">Manager</span><span class="sxs-lookup"><span data-stu-id="6b3c2-239">Manager</span></span>](manager.md) <br/> |<span data-ttu-id="6b3c2-240">代表联系人管理器。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-240">Represents a contact's manager.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-241">里程</span><span class="sxs-lookup"><span data-stu-id="6b3c2-241">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="6b3c2-242">代表为联系人项 mileage。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-242">Represents mileage for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-243">OfficeLocation</span><span class="sxs-lookup"><span data-stu-id="6b3c2-243">OfficeLocation</span></span>](officelocation.md) <br/> |<span data-ttu-id="6b3c2-244">代表联系人的办公室位置。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-244">Represents the office location of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-245">PostalAddressIndex</span><span class="sxs-lookup"><span data-stu-id="6b3c2-245">PostalAddressIndex</span></span>](postaladdressindex.md) <br/> |<span data-ttu-id="6b3c2-246">表示物理地址的显示类型。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-246">Represents the display types for physical addresses.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-247">Profession</span><span class="sxs-lookup"><span data-stu-id="6b3c2-247">Profession</span></span>](profession.md) <br/> |<span data-ttu-id="6b3c2-248">代表联系人的职业。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-248">Represents the profession of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-249">配偶姓名</span><span class="sxs-lookup"><span data-stu-id="6b3c2-249">SpouseName</span></span>](spousename.md) <br/> |<span data-ttu-id="6b3c2-250">表示联系人的配偶的名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-250">Represents the name of a contact's spouse/partner.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-251">姓</span><span class="sxs-lookup"><span data-stu-id="6b3c2-251">Surname</span></span>](surname.md) <br/> |<span data-ttu-id="6b3c2-252">代表联系人的姓。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-252">Represents the surname of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-253">WeddingAnniversary</span><span class="sxs-lookup"><span data-stu-id="6b3c2-253">WeddingAnniversary</span></span>](weddinganniversary.md) <br/> |<span data-ttu-id="6b3c2-254">包含联系人的婚礼周年的日。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-254">Contains the wedding anniversary of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-255">HasPicture</span><span class="sxs-lookup"><span data-stu-id="6b3c2-255">HasPicture</span></span>](haspicture.md) <br/> |<span data-ttu-id="6b3c2-256">指示联系人项目是否有代表联系人的图片的文件附件。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-256">Indicates whether the contact item has a file attachment that represents the contact's picture.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-257">PhoneticFullName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-257">PhoneticFullName</span></span>](phoneticfullname.md) <br/> |<span data-ttu-id="6b3c2-258">包含一个联系人，包括第一个和最后一个名称，按发音拼写的完整名称。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-258">Contains the full name of a contact, including the first and last name, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-259">PhoneticFirstName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-259">PhoneticFirstName</span></span>](phoneticfirstname.md) <br/> |<span data-ttu-id="6b3c2-260">包含名的联系人，按发音拼写。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-260">Contains the first name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-261">PhoneticLastName</span><span class="sxs-lookup"><span data-stu-id="6b3c2-261">PhoneticLastName</span></span>](phoneticlastname.md) <br/> |<span data-ttu-id="6b3c2-262">包含最后一个联系人的姓名，拼写发音排序。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-262">Contains the last name of a contact, spelled phonetically.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-263">Alias</span><span class="sxs-lookup"><span data-stu-id="6b3c2-263">Alias</span></span>](alias.md) <br/> |<span data-ttu-id="6b3c2-264">包含联系人的电子邮件别名。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-264">Contains the email alias of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-265">备注 （联系人）</span><span class="sxs-lookup"><span data-stu-id="6b3c2-265">Notes (Contact)</span></span>](notes-contact.md) <br/> |<span data-ttu-id="6b3c2-266">包含联系人的补充信息。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-266">Contains supplementary contact information.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-267">照片</span><span class="sxs-lookup"><span data-stu-id="6b3c2-267">Photo</span></span>](photo.md) <br/> |<span data-ttu-id="6b3c2-268">包含一个值，它将编码的联系人的照片。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-268">Contains a value that encodes the photo of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-269">UserSMIMECertificate</span><span class="sxs-lookup"><span data-stu-id="6b3c2-269">UserSMIMECertificate</span></span>](usersmimecertificate.md) <br/> |<span data-ttu-id="6b3c2-270">包含一个值，它将编码的联系人的 SMIME 证书。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-270">Contains a value that encodes the SMIME certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-271">MSExchangeCertificate</span><span class="sxs-lookup"><span data-stu-id="6b3c2-271">MSExchangeCertificate</span></span>](msexchangecertificate.md) <br/> |<span data-ttu-id="6b3c2-272">包含一个值，它将编码的联系人的 Microsoft Exchange 证书。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-272">Contains a value that encodes the Microsoft Exchange certificate of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-273">DirectoryId</span><span class="sxs-lookup"><span data-stu-id="6b3c2-273">DirectoryId</span></span>](directoryid.md) <br/> |<span data-ttu-id="6b3c2-274">包含目录 ID 的联系人。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-274">Contains the directory ID of a contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-275">ManagerMailbox</span><span class="sxs-lookup"><span data-stu-id="6b3c2-275">ManagerMailbox</span></span>](managermailbox.md) <br/> |<span data-ttu-id="6b3c2-276">包含标识的联系人管理器邮箱的 SMTP 信息。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-276">Contains SMTP information that identifies the manager mailbox of the contact.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-277">DirectReports</span><span class="sxs-lookup"><span data-stu-id="6b3c2-277">DirectReports</span></span>](directreports.md) <br/> |<span data-ttu-id="6b3c2-278">包含标识联系人的直接下属的 SMTP 信息。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-278">Contains SMTP information that identifies the direct reports of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b3c2-279">父元素</span><span class="sxs-lookup"><span data-stu-id="6b3c2-279">Parent elements</span></span>

|<span data-ttu-id="6b3c2-280">**元素名**</span><span class="sxs-lookup"><span data-stu-id="6b3c2-280">**Element name**</span></span>|<span data-ttu-id="6b3c2-281">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b3c2-281">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b3c2-282">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="6b3c2-282">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="6b3c2-283">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-283">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-284">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="6b3c2-284">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="6b3c2-285">标识要[UpdateItem 操作](updateitem-operation.md)期间追加到单个项目或文件夹的属性数据。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-285">Identifies data to append to a single property of an item or folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-286">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="6b3c2-286">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="6b3c2-287">标识与会议时间冲突的所有项目</span><span class="sxs-lookup"><span data-stu-id="6b3c2-287">Identifies all items that conflict with a meeting time</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-288">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="6b3c2-288">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="6b3c2-289">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-289">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-290">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="6b3c2-290">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="6b3c2-291">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-291">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-292">Items</span><span class="sxs-lookup"><span data-stu-id="6b3c2-292">Items</span></span>](items.md) <br/> |<span data-ttu-id="6b3c2-293">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-293">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-294">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="6b3c2-294">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="6b3c2-295">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-295">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-296">解决方法</span><span class="sxs-lookup"><span data-stu-id="6b3c2-296">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="6b3c2-297">包含单个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-297">Contains a single resolved entity.</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-298">SetItemField</span><span class="sxs-lookup"><span data-stu-id="6b3c2-298">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="6b3c2-299">表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-299">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="6b3c2-300">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="6b3c2-300">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="6b3c2-301">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-301">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6b3c2-302">文本值</span><span class="sxs-lookup"><span data-stu-id="6b3c2-302">Text value</span></span>

<span data-ttu-id="6b3c2-303">无。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-303">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b3c2-304">备注</span><span class="sxs-lookup"><span data-stu-id="6b3c2-304">Remarks</span></span>

<span data-ttu-id="6b3c2-305">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6b3c2-305">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b3c2-306">元素信息</span><span class="sxs-lookup"><span data-stu-id="6b3c2-306">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b3c2-307">命名空间</span><span class="sxs-lookup"><span data-stu-id="6b3c2-307">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b3c2-308">架构名称</span><span class="sxs-lookup"><span data-stu-id="6b3c2-308">Schema name</span></span>  <br/> |<span data-ttu-id="6b3c2-309">类型架构</span><span class="sxs-lookup"><span data-stu-id="6b3c2-309">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b3c2-310">验证文件</span><span class="sxs-lookup"><span data-stu-id="6b3c2-310">Validation file</span></span>  <br/> |<span data-ttu-id="6b3c2-311">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6b3c2-311">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b3c2-312">可以为空</span><span class="sxs-lookup"><span data-stu-id="6b3c2-312">Can be empty</span></span>  <br/> |<span data-ttu-id="6b3c2-313">False</span><span class="sxs-lookup"><span data-stu-id="6b3c2-313">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b3c2-314">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b3c2-314">See also</span></span>



- [<span data-ttu-id="6b3c2-315">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6b3c2-315">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6b3c2-316">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="6b3c2-316">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="6b3c2-317">更新联系人</span><span class="sxs-lookup"><span data-stu-id="6b3c2-317">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="6b3c2-318">删除联系人</span><span class="sxs-lookup"><span data-stu-id="6b3c2-318">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

