---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: UpdateItem 元素定义一个请求以更新邮箱中的项目。
ms.openlocfilehash: 43821db58457ffce22be918a7ba6427f57230010
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466568"
---
# <a name="updateitem"></a><span data-ttu-id="cb689-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="cb689-103">UpdateItem</span></span>

<span data-ttu-id="cb689-104">**UpdateItem**元素定义一个请求以更新邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="cb689-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="cb689-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="cb689-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb689-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb689-106">Attributes and elements</span></span>

<span data-ttu-id="cb689-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb689-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb689-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cb689-108">Attributes</span></span>

|<span data-ttu-id="cb689-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="cb689-109">**Attribute**</span></span>|<span data-ttu-id="cb689-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb689-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb689-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="cb689-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="cb689-112">标识在更新过程中要尝试的冲突解决的类型。</span><span class="sxs-lookup"><span data-stu-id="cb689-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="cb689-113">默认值为 "自动解析"。</span><span class="sxs-lookup"><span data-stu-id="cb689-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="cb689-114">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="cb689-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="cb689-115">介绍如何在更新项目后对其进行处理。</span><span class="sxs-lookup"><span data-stu-id="cb689-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="cb689-116">邮件项目（包括会议邮件（如会议取消、会议请求和会议响应）需要**MessageDisposition**属性。</span><span class="sxs-lookup"><span data-stu-id="cb689-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="cb689-117">**SendMeetingInvitationsOrCancellations**</span><span class="sxs-lookup"><span data-stu-id="cb689-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="cb689-118">介绍如何在更新日历项目后传达会议更新。</span><span class="sxs-lookup"><span data-stu-id="cb689-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="cb689-119">此属性是日历项目和日历项目发生的必要条件。</span><span class="sxs-lookup"><span data-stu-id="cb689-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="cb689-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="cb689-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="cb689-121">指示是否应禁止显示已更新项目的已读回执。</span><span class="sxs-lookup"><span data-stu-id="cb689-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="cb689-122">如果文本值**为 true，则**表示应禁止显示已读回执。</span><span class="sxs-lookup"><span data-stu-id="cb689-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="cb689-123">**如果值为 false** ，则表示已将已读回执发送给发件人。</span><span class="sxs-lookup"><span data-stu-id="cb689-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="cb689-124">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="cb689-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="cb689-125">此属性是在 Exchange Server 2013 SP1 中引入的。</span><span class="sxs-lookup"><span data-stu-id="cb689-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="cb689-126">ConflictResolution 属性</span><span class="sxs-lookup"><span data-stu-id="cb689-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="cb689-127">**值**</span><span class="sxs-lookup"><span data-stu-id="cb689-127">**Value**</span></span>|<span data-ttu-id="cb689-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb689-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb689-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="cb689-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="cb689-130">如果存在冲突，更新操作将失败并返回错误。</span><span class="sxs-lookup"><span data-stu-id="cb689-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="cb689-131">解决</span><span class="sxs-lookup"><span data-stu-id="cb689-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="cb689-132">更新操作将自动解决任何冲突。</span><span class="sxs-lookup"><span data-stu-id="cb689-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="cb689-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="cb689-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="cb689-134">如果存在冲突，更新操作将覆盖信息。</span><span class="sxs-lookup"><span data-stu-id="cb689-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="cb689-135">MessageDisposition 属性</span><span class="sxs-lookup"><span data-stu-id="cb689-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="cb689-136">**值**</span><span class="sxs-lookup"><span data-stu-id="cb689-136">**Value**</span></span>|<span data-ttu-id="cb689-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb689-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb689-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="cb689-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="cb689-139">更新项目并将其保存回其当前文件夹。</span><span class="sxs-lookup"><span data-stu-id="cb689-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="cb689-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="cb689-140">SendOnly</span></span>  <br/> |<span data-ttu-id="cb689-141">更新并发送项目，但不保存副本。</span><span class="sxs-lookup"><span data-stu-id="cb689-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="cb689-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="cb689-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="cb689-143">更新项目并将副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cb689-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="cb689-144">SendMeetingInvitationsOrCancellations 属性</span><span class="sxs-lookup"><span data-stu-id="cb689-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="cb689-145">**值**</span><span class="sxs-lookup"><span data-stu-id="cb689-145">**Value**</span></span>|<span data-ttu-id="cb689-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb689-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb689-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="cb689-147">SendToNone</span></span>  <br/> |<span data-ttu-id="cb689-148">日历项目已更新，但未将更新发送给与会者。</span><span class="sxs-lookup"><span data-stu-id="cb689-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="cb689-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="cb689-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="cb689-150">将更新日历项目并将会议更新发送给所有与会者，但不会将其保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cb689-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="cb689-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="cb689-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="cb689-152">将更新日历项目，并且仅向受会议更改影响的与会者发送会议更新。</span><span class="sxs-lookup"><span data-stu-id="cb689-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="cb689-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="cb689-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="cb689-154">更新日历项目，将会议更新发送给所有与会者，并将副本保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cb689-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="cb689-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="cb689-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="cb689-156">更新日历项目，将会议更新发送给受会议更改影响的所有与会者，并将副本保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="cb689-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb689-157">子元素</span><span class="sxs-lookup"><span data-stu-id="cb689-157">Child elements</span></span>

|<span data-ttu-id="cb689-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb689-158">**Element**</span></span>|<span data-ttu-id="cb689-159">**描述**</span><span class="sxs-lookup"><span data-stu-id="cb689-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb689-160">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="cb689-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="cb689-161">标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="cb689-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cb689-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="cb689-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="cb689-163">包含标识项目和要应用于项目的更新的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="cb689-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb689-164">父元素</span><span class="sxs-lookup"><span data-stu-id="cb689-164">Parent elements</span></span>

<span data-ttu-id="cb689-165">无。</span><span class="sxs-lookup"><span data-stu-id="cb689-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb689-166">说明</span><span class="sxs-lookup"><span data-stu-id="cb689-166">Remarks</span></span>

<span data-ttu-id="cb689-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cb689-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb689-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb689-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb689-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb689-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb689-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb689-170">Schema Name</span></span>  <br/> |<span data-ttu-id="cb689-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="cb689-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb689-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb689-172">Validation File</span></span>  <br/> |<span data-ttu-id="cb689-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cb689-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb689-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb689-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb689-175">False</span><span class="sxs-lookup"><span data-stu-id="cb689-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb689-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb689-176">See also</span></span>



[<span data-ttu-id="cb689-177">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="cb689-177">UpdateItem operation</span></span>](updateitem-operation.md)

