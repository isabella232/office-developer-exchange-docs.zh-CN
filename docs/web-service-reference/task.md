---
title: 任务
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: Task 元素表示 Exchange 存储中的任务。
ms.openlocfilehash: 669f90dfa74cd085091e9836a1d31ca53bbf165e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458941"
---
# <a name="task"></a><span data-ttu-id="2a83e-103">任务</span><span class="sxs-lookup"><span data-stu-id="2a83e-103">Task</span></span>

<span data-ttu-id="2a83e-104">**Task**元素表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="2a83e-104">The **Task** element represents a task in the Exchange store.</span></span> 
  
```xml
<Task>
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
   <ActualWork/>
   <AssignedTime/>
   <BillingInformation/>
   <ChangeCount/>
   <Companies/>
   <CompleteDate/>
   <Contacts/>
   <DelegationState/>
   <Delegator/>
   <DueDate/>
   <IsAssignmentEditable/>
   <IsComplete/>
   <IsRecurring/>
   <IsTeamTask/>
   <Mileage/>
   <Owner/>
   <PercentComplete/>
   <Recurrence/>
   <StartDate/>
   <Status/>
   <StatusDescription/>
   <TotalWork/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Task>
```

<span data-ttu-id="2a83e-105">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="2a83e-105">**TaskType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2a83e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2a83e-106">Attributes and elements</span></span>

<span data-ttu-id="2a83e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2a83e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a83e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2a83e-108">Attributes</span></span>

<span data-ttu-id="2a83e-109">无。</span><span class="sxs-lookup"><span data-stu-id="2a83e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a83e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2a83e-110">Child elements</span></span>

|<span data-ttu-id="2a83e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a83e-111">**Element**</span></span>|<span data-ttu-id="2a83e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a83e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a83e-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="2a83e-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="2a83e-114">包含以 base64Binary 格式表示的对象的本机多用途 Internet 邮件扩展（MIME）流。</span><span class="sxs-lookup"><span data-stu-id="2a83e-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="2a83e-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="2a83e-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="2a83e-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="2a83e-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="2a83e-118">表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="2a83e-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="2a83e-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="2a83e-120">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="2a83e-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-121">主题</span><span class="sxs-lookup"><span data-stu-id="2a83e-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="2a83e-122">表示 Exchange 存储项和响应对象的主题。</span><span class="sxs-lookup"><span data-stu-id="2a83e-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="2a83e-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="2a83e-124">包含项目敏感度的状态。</span><span class="sxs-lookup"><span data-stu-id="2a83e-124">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-125">Body</span><span class="sxs-lookup"><span data-stu-id="2a83e-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="2a83e-126">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="2a83e-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-127">附件</span><span class="sxs-lookup"><span data-stu-id="2a83e-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2a83e-128">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="2a83e-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="2a83e-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="2a83e-130">表示邮箱中的项目的接收日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-131">大小</span><span class="sxs-lookup"><span data-stu-id="2a83e-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="2a83e-132">表示项的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="2a83e-132">Represents the size, in bytes, of an item.</span></span> <span data-ttu-id="2a83e-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="2a83e-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-134">类别</span><span class="sxs-lookup"><span data-stu-id="2a83e-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2a83e-135">表示一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="2a83e-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-136">Importance</span><span class="sxs-lookup"><span data-stu-id="2a83e-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="2a83e-137">介绍项的重要性。</span><span class="sxs-lookup"><span data-stu-id="2a83e-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="2a83e-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="2a83e-139">表示此项是其回复项的标识符。</span><span class="sxs-lookup"><span data-stu-id="2a83e-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="2a83e-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="2a83e-141">指示是否已将项目提交到 "发件箱" 默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="2a83e-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="2a83e-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="2a83e-143">表示是否尚未发送某个项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="2a83e-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="2a83e-145">指示用户是否向他或她发送了一项。</span><span class="sxs-lookup"><span data-stu-id="2a83e-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="2a83e-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="2a83e-147">指示以前是否已发送过该项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="2a83e-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="2a83e-149">指示项目是否已被修改。</span><span class="sxs-lookup"><span data-stu-id="2a83e-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-150">Message</span><span class="sxs-lookup"><span data-stu-id="2a83e-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="2a83e-151">表示邮箱中的项目所包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="2a83e-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="2a83e-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="2a83e-153">表示邮箱中的项目的发送日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="2a83e-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="2a83e-155">表示邮箱中的给定项目的创建日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="2a83e-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="2a83e-157">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="2a83e-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="2a83e-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="2a83e-159">表示事件发生的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="2a83e-160">[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素使用此元素来确定何时显示提醒。</span><span class="sxs-lookup"><span data-stu-id="2a83e-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="2a83e-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="2a83e-162">指示是否已为 Exchange 存储中的某个项目设置提醒。</span><span class="sxs-lookup"><span data-stu-id="2a83e-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="2a83e-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="2a83e-164">表示在显示提醒时事件之前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="2a83e-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="2a83e-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="2a83e-166">表示用于 "抄送" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="2a83e-166">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="2a83e-167">这是所有 Cc 收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="2a83e-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="2a83e-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="2a83e-169">表示用于 "To" 框中的内容的显示字符串。</span><span class="sxs-lookup"><span data-stu-id="2a83e-169">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="2a83e-170">这是所有收件人显示名称的串联字符串。</span><span class="sxs-lookup"><span data-stu-id="2a83e-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="2a83e-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="2a83e-172">表示一个属性，如果一个项目至少有一个可见的附件，则设置为**true** 。</span><span class="sxs-lookup"><span data-stu-id="2a83e-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="2a83e-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="2a83e-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="2a83e-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="2a83e-175">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="2a83e-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-176">Culture</span><span class="sxs-lookup"><span data-stu-id="2a83e-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="2a83e-177">表示邮箱中给定项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="2a83e-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-178">ActualWork</span><span class="sxs-lookup"><span data-stu-id="2a83e-178">ActualWork</span></span>](actualwork.md) <br/> |<span data-ttu-id="2a83e-179">表示任务所用的实际时间量。</span><span class="sxs-lookup"><span data-stu-id="2a83e-179">Represents the actual amount of time that is spent on a task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-180">AssignedTime</span><span class="sxs-lookup"><span data-stu-id="2a83e-180">AssignedTime</span></span>](assignedtime.md) <br/> |<span data-ttu-id="2a83e-181">表示将任务分配给联系人的时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-181">Represents the time when a task is assigned to a contact.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-182">BillingInformation</span><span class="sxs-lookup"><span data-stu-id="2a83e-182">BillingInformation</span></span>](billinginformation.md) <br/> |<span data-ttu-id="2a83e-183">保留任务的记帐信息。</span><span class="sxs-lookup"><span data-stu-id="2a83e-183">Holds billing information for a task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-184">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="2a83e-184">ChangeCount</span></span>](changecount.md) <br/> |<span data-ttu-id="2a83e-185">指定任务的版本。</span><span class="sxs-lookup"><span data-stu-id="2a83e-185">Specifies the version of the task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-186">Companies</span><span class="sxs-lookup"><span data-stu-id="2a83e-186">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="2a83e-187">表示与某个联系人或任务相关联的公司的集合。</span><span class="sxs-lookup"><span data-stu-id="2a83e-187">Represents the collection of companies that are associated with a contact or task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-188">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="2a83e-188">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="2a83e-189">表示任务完成的日期。</span><span class="sxs-lookup"><span data-stu-id="2a83e-189">Represents the date on which a task is completed.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-190">联系人</span><span class="sxs-lookup"><span data-stu-id="2a83e-190">Contacts</span></span>](contacts-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2a83e-191">包含与任务相关联的联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="2a83e-191">Contains a list of contacts that are associated with a task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-192">DelegationState</span><span class="sxs-lookup"><span data-stu-id="2a83e-192">DelegationState</span></span>](delegationstate.md) <br/> |<span data-ttu-id="2a83e-193">表示委派任务的状态。</span><span class="sxs-lookup"><span data-stu-id="2a83e-193">Represents the status of a delegated task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-194">Delegator</span><span class="sxs-lookup"><span data-stu-id="2a83e-194">Delegator</span></span>](delegator.md) <br/> |<span data-ttu-id="2a83e-195">包含分配了任务的代理者的名称。</span><span class="sxs-lookup"><span data-stu-id="2a83e-195">Contains the name of the delegator who assigned the task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-196">DueDate</span><span class="sxs-lookup"><span data-stu-id="2a83e-196">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="2a83e-197">表示任务项目的截止日期。</span><span class="sxs-lookup"><span data-stu-id="2a83e-197">Represents the date when a task item is due.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-198">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="2a83e-198">IsAssignmentEditable</span></span>](isassignmenteditable.md) <br/> |<span data-ttu-id="2a83e-199">指示任务是否可编辑。</span><span class="sxs-lookup"><span data-stu-id="2a83e-199">Indicates whether the task is editable or not.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-200">IsComplete</span><span class="sxs-lookup"><span data-stu-id="2a83e-200">IsComplete</span></span>](iscomplete.md) <br/> |<span data-ttu-id="2a83e-201">指示任务是否已完成。</span><span class="sxs-lookup"><span data-stu-id="2a83e-201">Indicates whether the task has been completed or not.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-202">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="2a83e-202">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="2a83e-203">指示任务是否为定期项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="2a83e-203">Indicates whether a task is part of a recurring item.</span></span> <span data-ttu-id="2a83e-204">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="2a83e-204">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-205">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="2a83e-205">IsTeamTask</span></span>](isteamtask.md) <br/> |<span data-ttu-id="2a83e-206">指示任务是否归团队所有。</span><span class="sxs-lookup"><span data-stu-id="2a83e-206">Indicates whether the task is owned by a team or not.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-207">Mileage</span><span class="sxs-lookup"><span data-stu-id="2a83e-207">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="2a83e-208">表示任务项的里程。</span><span class="sxs-lookup"><span data-stu-id="2a83e-208">Represents mileage for a task item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-209">Owner</span><span class="sxs-lookup"><span data-stu-id="2a83e-209">Owner</span></span>](owner.md) <br/> |<span data-ttu-id="2a83e-210">代表任务的所有者。</span><span class="sxs-lookup"><span data-stu-id="2a83e-210">Represents the owner of a task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-211">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="2a83e-211">PercentComplete</span></span>](percentcomplete.md) <br/> |<span data-ttu-id="2a83e-212">描述任务的完成状态。</span><span class="sxs-lookup"><span data-stu-id="2a83e-212">Describes the completion status of a task.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-213">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="2a83e-213">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="2a83e-214">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="2a83e-214">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-215">StartDate</span><span class="sxs-lookup"><span data-stu-id="2a83e-215">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="2a83e-216">表示任务项的开始日期。</span><span class="sxs-lookup"><span data-stu-id="2a83e-216">Represents the start date of a task item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-217">Status</span><span class="sxs-lookup"><span data-stu-id="2a83e-217">Status</span></span>](status.md) <br/> |<span data-ttu-id="2a83e-218">表示任务项的状态。</span><span class="sxs-lookup"><span data-stu-id="2a83e-218">Represents the status of a task item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-219">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="2a83e-219">StatusDescription</span></span>](statusdescription.md) <br/> |<span data-ttu-id="2a83e-220">包含任务状态的说明。</span><span class="sxs-lookup"><span data-stu-id="2a83e-220">Contains an explanation of the task status.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-221">TotalWork</span><span class="sxs-lookup"><span data-stu-id="2a83e-221">TotalWork</span></span>](totalwork.md) <br/> |<span data-ttu-id="2a83e-222">包含与项目相关联的工时的说明。</span><span class="sxs-lookup"><span data-stu-id="2a83e-222">Contains a description of how much work is associated with an item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-223">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="2a83e-223">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="2a83e-224">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="2a83e-224">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="2a83e-225">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="2a83e-225">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-226">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="2a83e-226">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="2a83e-227">包含上次修改项目的用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="2a83e-227">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-228">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="2a83e-228">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="2a83e-229">指示项目的上次修改时间。</span><span class="sxs-lookup"><span data-stu-id="2a83e-229">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-230">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="2a83e-230">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="2a83e-231">指示项目是否与文件夹相关联。</span><span class="sxs-lookup"><span data-stu-id="2a83e-231">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-232">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="2a83e-232">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="2a83e-233">表示连接到 Microsoft Office Outlook Web App 终结点以在 Outlook Web App 中读取项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="2a83e-233">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-234">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="2a83e-234">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="2a83e-235">表示用于连接到 Outlook web App 终结点以在 Outlook Web App 中编辑项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="2a83e-235">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-236">ConversationId</span><span class="sxs-lookup"><span data-stu-id="2a83e-236">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="2a83e-237">包含项或对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="2a83e-237">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-238">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="2a83e-238">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="2a83e-239">表示一个 HTML 片段或纯文本，它表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="2a83e-239">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a83e-240">父元素</span><span class="sxs-lookup"><span data-stu-id="2a83e-240">Parent elements</span></span>

|<span data-ttu-id="2a83e-241">**元素**</span><span class="sxs-lookup"><span data-stu-id="2a83e-241">**Element**</span></span>|<span data-ttu-id="2a83e-242">**说明**</span><span class="sxs-lookup"><span data-stu-id="2a83e-242">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a83e-243">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="2a83e-243">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="2a83e-244">介绍与会议时间相邻的所有日历项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-244">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-245">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="2a83e-245">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="2a83e-246">标识在[UpdateItem 操作](updateitem-operation.md)过程中追加到项目/文件夹的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="2a83e-246">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2a83e-247">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="2a83e-247">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="2a83e-248">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-248">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-249">创建（ItemSync）</span><span class="sxs-lookup"><span data-stu-id="2a83e-249">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="2a83e-250">标识要在本地客户端存储中创建的单个项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-250">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-251">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="2a83e-251">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="2a83e-252">表示附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-252">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-253">Items</span><span class="sxs-lookup"><span data-stu-id="2a83e-253">Items</span></span>](items.md) <br/> |<span data-ttu-id="2a83e-254">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="2a83e-254">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="2a83e-255">SetItemField</span><span class="sxs-lookup"><span data-stu-id="2a83e-255">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="2a83e-256">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="2a83e-256">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2a83e-257">Update （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="2a83e-257">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="2a83e-258">标识要在本地客户端存储中更新的单个项目。</span><span class="sxs-lookup"><span data-stu-id="2a83e-258">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a83e-259">文本值</span><span class="sxs-lookup"><span data-stu-id="2a83e-259">Text value</span></span>

<span data-ttu-id="2a83e-260">无。</span><span class="sxs-lookup"><span data-stu-id="2a83e-260">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a83e-261">说明</span><span class="sxs-lookup"><span data-stu-id="2a83e-261">Remarks</span></span>

<span data-ttu-id="2a83e-262">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2a83e-262">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a83e-263">元素信息</span><span class="sxs-lookup"><span data-stu-id="2a83e-263">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a83e-264">命名空间</span><span class="sxs-lookup"><span data-stu-id="2a83e-264">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a83e-265">架构名称</span><span class="sxs-lookup"><span data-stu-id="2a83e-265">Schema name</span></span>  <br/> |<span data-ttu-id="2a83e-266">类型架构</span><span class="sxs-lookup"><span data-stu-id="2a83e-266">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a83e-267">验证文件</span><span class="sxs-lookup"><span data-stu-id="2a83e-267">Validation file</span></span>  <br/> |<span data-ttu-id="2a83e-268">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a83e-268">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a83e-269">可以为空</span><span class="sxs-lookup"><span data-stu-id="2a83e-269">Can be empty</span></span>  <br/> |<span data-ttu-id="2a83e-270">False</span><span class="sxs-lookup"><span data-stu-id="2a83e-270">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a83e-271">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2a83e-271">See also</span></span>

- [<span data-ttu-id="2a83e-272">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2a83e-272">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2a83e-273">创建任务</span><span class="sxs-lookup"><span data-stu-id="2a83e-273">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [<span data-ttu-id="2a83e-274">删除任务</span><span class="sxs-lookup"><span data-stu-id="2a83e-274">Deleting Tasks</span></span>](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

