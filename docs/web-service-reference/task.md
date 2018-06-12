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
ms.openlocfilehash: 2c61fca6ac85290e34f1365b0cb9e841e1fe279f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838191"
---
# <a name="task"></a><span data-ttu-id="bdd22-103">任务</span><span class="sxs-lookup"><span data-stu-id="bdd22-103">Task</span></span>

<span data-ttu-id="bdd22-104">**Task**元素表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="bdd22-104">The **Task** element represents a task in the Exchange store.</span></span> 
  
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

<span data-ttu-id="bdd22-105">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="bdd22-105">**TaskType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bdd22-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bdd22-106">Attributes and elements</span></span>

<span data-ttu-id="bdd22-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bdd22-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdd22-108">属性</span><span class="sxs-lookup"><span data-stu-id="bdd22-108">Attributes</span></span>

<span data-ttu-id="bdd22-109">无。</span><span class="sxs-lookup"><span data-stu-id="bdd22-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bdd22-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bdd22-110">Child elements</span></span>

|<span data-ttu-id="bdd22-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bdd22-111">**Element**</span></span>|<span data-ttu-id="bdd22-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bdd22-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdd22-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="bdd22-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="bdd22-114">包含一个对象，表示 base64Binary 格式的本机多用途 Internet 邮件扩展 (MIME) 流。</span><span class="sxs-lookup"><span data-stu-id="bdd22-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="bdd22-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="bdd22-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="bdd22-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-117">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="bdd22-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="bdd22-118">表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="bdd22-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="bdd22-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="bdd22-120">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="bdd22-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-121">Subject</span><span class="sxs-lookup"><span data-stu-id="bdd22-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="bdd22-122">代表 Exchange 存储项和响应对象主题。</span><span class="sxs-lookup"><span data-stu-id="bdd22-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-123">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="bdd22-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="bdd22-124">包含项目的敏感度的状态。</span><span class="sxs-lookup"><span data-stu-id="bdd22-124">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-125">Body</span><span class="sxs-lookup"><span data-stu-id="bdd22-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="bdd22-126">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="bdd22-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-127">附件</span><span class="sxs-lookup"><span data-stu-id="bdd22-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bdd22-128">包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="bdd22-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="bdd22-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="bdd22-130">表示的日期和接收邮箱中的项目的时间。</span><span class="sxs-lookup"><span data-stu-id="bdd22-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-131">Size</span><span class="sxs-lookup"><span data-stu-id="bdd22-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="bdd22-132">表示的大小，以字节为单位的项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-132">Represents the size, in bytes, of an item.</span></span> <span data-ttu-id="bdd22-133">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="bdd22-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-134">类别</span><span class="sxs-lookup"><span data-stu-id="bdd22-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bdd22-135">表示标识的邮箱中项目所属的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd22-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-136">Importance</span><span class="sxs-lookup"><span data-stu-id="bdd22-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="bdd22-137">描述项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="bdd22-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="bdd22-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="bdd22-139">表示此项将答复到项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="bdd22-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="bdd22-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="bdd22-141">指示项目是否已提交到默认发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="bdd22-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="bdd22-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="bdd22-143">表示是否尚未发送项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="bdd22-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="bdd22-145">指示用户是否发送到他或她自己的项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="bdd22-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="bdd22-147">指示是否已以前被发送项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="bdd22-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="bdd22-149">指示是否已修改项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="bdd22-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="bdd22-151">代表在邮箱中某个项目中包含的所有 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd22-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="bdd22-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="bdd22-153">表示的日期和时间发送邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="bdd22-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="bdd22-155">表示的日期和给定的邮箱中项目的创建时间。</span><span class="sxs-lookup"><span data-stu-id="bdd22-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="bdd22-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="bdd22-157">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd22-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="bdd22-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="bdd22-159">表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="bdd22-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="bdd22-160">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="bdd22-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="bdd22-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="bdd22-162">指示是否已设置提醒的项在 Exchange 存储中。</span><span class="sxs-lookup"><span data-stu-id="bdd22-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="bdd22-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="bdd22-164">表示事件时显示提醒前的分钟数。</span><span class="sxs-lookup"><span data-stu-id="bdd22-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="bdd22-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="bdd22-166">表示用于抄送框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="bdd22-166">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="bdd22-167">这是连接的所有抄送收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="bdd22-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="bdd22-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="bdd22-169">表示用于收件人框的内容显示字符串。</span><span class="sxs-lookup"><span data-stu-id="bdd22-169">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="bdd22-170">这是连接的所有收件人的显示名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="bdd22-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="bdd22-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="bdd22-172">表示如果项目具有至少一个可见的附件设置为**true**的属性。</span><span class="sxs-lookup"><span data-stu-id="bdd22-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="bdd22-173">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="bdd22-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="bdd22-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="bdd22-175">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="bdd22-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-176">区域性</span><span class="sxs-lookup"><span data-stu-id="bdd22-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="bdd22-177">表示给定邮箱中项目的区域性。</span><span class="sxs-lookup"><span data-stu-id="bdd22-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-178">ActualWork</span><span class="sxs-lookup"><span data-stu-id="bdd22-178">ActualWork</span></span>](actualwork.md) <br/> |<span data-ttu-id="bdd22-179">代表对任务的实际所花费的时间量。</span><span class="sxs-lookup"><span data-stu-id="bdd22-179">Represents the actual amount of time that is spent on a task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-180">AssignedTime</span><span class="sxs-lookup"><span data-stu-id="bdd22-180">AssignedTime</span></span>](assignedtime.md) <br/> |<span data-ttu-id="bdd22-181">表示当一个任务分配给联系人的时间。</span><span class="sxs-lookup"><span data-stu-id="bdd22-181">Represents the time when a task is assigned to a contact.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-182">BillingInformation</span><span class="sxs-lookup"><span data-stu-id="bdd22-182">BillingInformation</span></span>](billinginformation.md) <br/> |<span data-ttu-id="bdd22-183">保留帐单任务的信息。</span><span class="sxs-lookup"><span data-stu-id="bdd22-183">Holds billing information for a task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-184">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="bdd22-184">ChangeCount</span></span>](changecount.md) <br/> |<span data-ttu-id="bdd22-185">指定任务的版本。</span><span class="sxs-lookup"><span data-stu-id="bdd22-185">Specifies the version of the task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-186">公司</span><span class="sxs-lookup"><span data-stu-id="bdd22-186">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="bdd22-187">代表与一个联系人或任务相关联的公司的集合。</span><span class="sxs-lookup"><span data-stu-id="bdd22-187">Represents the collection of companies that are associated with a contact or task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-188">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="bdd22-188">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="bdd22-189">代表在其完成任务的日期。</span><span class="sxs-lookup"><span data-stu-id="bdd22-189">Represents the date on which a task is completed.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-190">联系人</span><span class="sxs-lookup"><span data-stu-id="bdd22-190">Contacts</span></span>](contacts-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bdd22-191">包含与任务相关联的联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="bdd22-191">Contains a list of contacts that are associated with a task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-192">DelegationState</span><span class="sxs-lookup"><span data-stu-id="bdd22-192">DelegationState</span></span>](delegationstate.md) <br/> |<span data-ttu-id="bdd22-193">代表委派的任务的状态。</span><span class="sxs-lookup"><span data-stu-id="bdd22-193">Represents the status of a delegated task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-194">Delegator</span><span class="sxs-lookup"><span data-stu-id="bdd22-194">Delegator</span></span>](delegator.md) <br/> |<span data-ttu-id="bdd22-195">包含 delegator 分配任务的名称。</span><span class="sxs-lookup"><span data-stu-id="bdd22-195">Contains the name of the delegator who assigned the task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-196">DueDate</span><span class="sxs-lookup"><span data-stu-id="bdd22-196">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="bdd22-197">表示任务项目的到期日期。</span><span class="sxs-lookup"><span data-stu-id="bdd22-197">Represents the date when a task item is due.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-198">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="bdd22-198">IsAssignmentEditable</span></span>](isassignmenteditable.md) <br/> |<span data-ttu-id="bdd22-199">指示任务是否是可编辑。</span><span class="sxs-lookup"><span data-stu-id="bdd22-199">Indicates whether the task is editable or not.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-200">程序</span><span class="sxs-lookup"><span data-stu-id="bdd22-200">IsComplete</span></span>](iscomplete.md) <br/> |<span data-ttu-id="bdd22-201">指示任务是否已完成或未。</span><span class="sxs-lookup"><span data-stu-id="bdd22-201">Indicates whether the task has been completed or not.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-202">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="bdd22-202">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="bdd22-203">指示任务是否定期项的一部分。</span><span class="sxs-lookup"><span data-stu-id="bdd22-203">Indicates whether a task is part of a recurring item.</span></span> <span data-ttu-id="bdd22-204">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="bdd22-204">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-205">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="bdd22-205">IsTeamTask</span></span>](isteamtask.md) <br/> |<span data-ttu-id="bdd22-206">指示是否小组拥有任务。</span><span class="sxs-lookup"><span data-stu-id="bdd22-206">Indicates whether the task is owned by a team or not.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-207">里程</span><span class="sxs-lookup"><span data-stu-id="bdd22-207">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="bdd22-208">代表为任务项 mileage。</span><span class="sxs-lookup"><span data-stu-id="bdd22-208">Represents mileage for a task item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-209">Owner</span><span class="sxs-lookup"><span data-stu-id="bdd22-209">Owner</span></span>](owner.md) <br/> |<span data-ttu-id="bdd22-210">表示任务的所有者。</span><span class="sxs-lookup"><span data-stu-id="bdd22-210">Represents the owner of a task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-211">完成百分比</span><span class="sxs-lookup"><span data-stu-id="bdd22-211">PercentComplete</span></span>](percentcomplete.md) <br/> |<span data-ttu-id="bdd22-212">描述任务的完成状态。</span><span class="sxs-lookup"><span data-stu-id="bdd22-212">Describes the completion status of a task.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-213">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="bdd22-213">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="bdd22-214">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="bdd22-214">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-215">StartDate</span><span class="sxs-lookup"><span data-stu-id="bdd22-215">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="bdd22-216">代表任务项目的开始日期。</span><span class="sxs-lookup"><span data-stu-id="bdd22-216">Represents the start date of a task item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-217">Status</span><span class="sxs-lookup"><span data-stu-id="bdd22-217">Status</span></span>](status.md) <br/> |<span data-ttu-id="bdd22-218">表示任务项的状态。</span><span class="sxs-lookup"><span data-stu-id="bdd22-218">Represents the status of a task item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-219">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="bdd22-219">StatusDescription</span></span>](statusdescription.md) <br/> |<span data-ttu-id="bdd22-220">包含任务状态的说明。</span><span class="sxs-lookup"><span data-stu-id="bdd22-220">Contains an explanation of the task status.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-221">TotalWork</span><span class="sxs-lookup"><span data-stu-id="bdd22-221">TotalWork</span></span>](totalwork.md) <br/> |<span data-ttu-id="bdd22-222">包含多少工作量是与项关联的说明。</span><span class="sxs-lookup"><span data-stu-id="bdd22-222">Contains a description of how much work is associated with an item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-223">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="bdd22-223">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="bdd22-224">包含客户端基于的项目或文件夹的权限设置的权限。</span><span class="sxs-lookup"><span data-stu-id="bdd22-224">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="bdd22-225">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="bdd22-225">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-226">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="bdd22-226">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="bdd22-227">包含要修改的项目的最后一个用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="bdd22-227">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-228">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="bdd22-228">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="bdd22-229">指示上次修改的项。</span><span class="sxs-lookup"><span data-stu-id="bdd22-229">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-230">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="bdd22-230">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="bdd22-231">指示项目是否与文件夹关联。</span><span class="sxs-lookup"><span data-stu-id="bdd22-231">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-232">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="bdd22-232">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="bdd22-233">表示要连接到 Microsoft Office Outlook Web App 终结点读取 Outlook Web App 中的项目的 URL。</span><span class="sxs-lookup"><span data-stu-id="bdd22-233">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-234">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="bdd22-234">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="bdd22-235">表示要连接到 Outlook Web App 中编辑项目的 Outlook Web App 终结点的 URL。</span><span class="sxs-lookup"><span data-stu-id="bdd22-235">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-236">ConversationId</span><span class="sxs-lookup"><span data-stu-id="bdd22-236">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="bdd22-237">包含项目或会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="bdd22-237">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-238">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="bdd22-238">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="bdd22-239">代表一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="bdd22-239">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bdd22-240">父元素</span><span class="sxs-lookup"><span data-stu-id="bdd22-240">Parent elements</span></span>

|<span data-ttu-id="bdd22-241">**元素**</span><span class="sxs-lookup"><span data-stu-id="bdd22-241">**Element**</span></span>|<span data-ttu-id="bdd22-242">**说明**</span><span class="sxs-lookup"><span data-stu-id="bdd22-242">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bdd22-243">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="bdd22-243">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="bdd22-244">介绍所有彼此相邻的会议时间的日历项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-244">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-245">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="bdd22-245">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="bdd22-246">标识要追加到的项目/文件夹单个属性[UpdateItem 操作](updateitem-operation.md)期间数据。</span><span class="sxs-lookup"><span data-stu-id="bdd22-246">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bdd22-247">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="bdd22-247">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="bdd22-248">标识与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-248">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-249">创建 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="bdd22-249">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="bdd22-250">标识在本地客户端库中创建的单个项。</span><span class="sxs-lookup"><span data-stu-id="bdd22-250">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-251">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="bdd22-251">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="bdd22-252">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="bdd22-252">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-253">Items</span><span class="sxs-lookup"><span data-stu-id="bdd22-253">Items</span></span>](items.md) <br/> |<span data-ttu-id="bdd22-254">包含项的数组。</span><span class="sxs-lookup"><span data-stu-id="bdd22-254">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="bdd22-255">SetItemField</span><span class="sxs-lookup"><span data-stu-id="bdd22-255">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="bdd22-256">表示更新到单个[UpdateItem 操作](updateitem-operation.md)中的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="bdd22-256">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bdd22-257">更新 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="bdd22-257">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="bdd22-258">标识要更新本地客户端存储中的单个项。</span><span class="sxs-lookup"><span data-stu-id="bdd22-258">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bdd22-259">文本值</span><span class="sxs-lookup"><span data-stu-id="bdd22-259">Text value</span></span>

<span data-ttu-id="bdd22-260">无。</span><span class="sxs-lookup"><span data-stu-id="bdd22-260">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bdd22-261">备注</span><span class="sxs-lookup"><span data-stu-id="bdd22-261">Remarks</span></span>

<span data-ttu-id="bdd22-262">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bdd22-262">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdd22-263">元素信息</span><span class="sxs-lookup"><span data-stu-id="bdd22-263">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdd22-264">命名空间</span><span class="sxs-lookup"><span data-stu-id="bdd22-264">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bdd22-265">架构名称</span><span class="sxs-lookup"><span data-stu-id="bdd22-265">Schema name</span></span>  <br/> |<span data-ttu-id="bdd22-266">类型架构</span><span class="sxs-lookup"><span data-stu-id="bdd22-266">Types schema</span></span>  <br/> |
|<span data-ttu-id="bdd22-267">验证文件</span><span class="sxs-lookup"><span data-stu-id="bdd22-267">Validation file</span></span>  <br/> |<span data-ttu-id="bdd22-268">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bdd22-268">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bdd22-269">可以为空</span><span class="sxs-lookup"><span data-stu-id="bdd22-269">Can be empty</span></span>  <br/> |<span data-ttu-id="bdd22-270">False</span><span class="sxs-lookup"><span data-stu-id="bdd22-270">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bdd22-271">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bdd22-271">See also</span></span>

- [<span data-ttu-id="bdd22-272">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bdd22-272">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="bdd22-273">创建任务</span><span class="sxs-lookup"><span data-stu-id="bdd22-273">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [<span data-ttu-id="bdd22-274">删除任务</span><span class="sxs-lookup"><span data-stu-id="bdd22-274">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

