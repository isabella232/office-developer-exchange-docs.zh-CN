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
description: UpdateItem 元素定义一个请求来更新邮箱中的项。
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838405"
---
# <a name="updateitem"></a><span data-ttu-id="abd33-103">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="abd33-103">UpdateItem</span></span>

<span data-ttu-id="abd33-104">**UpdateItem**元素定义一个请求来更新邮箱中的项。</span><span class="sxs-lookup"><span data-stu-id="abd33-104">The **UpdateItem** element defines a request to update an item in a mailbox.</span></span> 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 <span data-ttu-id="abd33-105">**UpdateItemType**</span><span class="sxs-lookup"><span data-stu-id="abd33-105">**UpdateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abd33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="abd33-106">Attributes and elements</span></span>

<span data-ttu-id="abd33-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="abd33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abd33-108">属性</span><span class="sxs-lookup"><span data-stu-id="abd33-108">Attributes</span></span>

|<span data-ttu-id="abd33-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="abd33-109">**Attribute**</span></span>|<span data-ttu-id="abd33-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="abd33-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abd33-111">**ConflictResolution**</span><span class="sxs-lookup"><span data-stu-id="abd33-111">**ConflictResolution**</span></span> <br/> |<span data-ttu-id="abd33-112">标识指定在冲突解决尝试更新期间的类型。</span><span class="sxs-lookup"><span data-stu-id="abd33-112">Identifies the type of conflict resolution to try during an update.</span></span> <span data-ttu-id="abd33-113">默认值是自动解析。</span><span class="sxs-lookup"><span data-stu-id="abd33-113">The default value is AutoResolve.</span></span>  <br/> |
|<span data-ttu-id="abd33-114">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="abd33-114">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="abd33-115">描述更新后如何处理项目。</span><span class="sxs-lookup"><span data-stu-id="abd33-115">Describes how the item will be handled after it is updated.</span></span> <span data-ttu-id="abd33-116">对于邮件项，包括会议消息，如会议取消、 会议请求和会议响应需要**MessageDisposition**属性。</span><span class="sxs-lookup"><span data-stu-id="abd33-116">The **MessageDisposition** attribute is required for message items, including meeting messages such as meeting cancellations, meeting requests, and meeting responses.</span></span>  <br/> |
|<span data-ttu-id="abd33-117">**SendMeetingInvitationsOrCancellations**</span><span class="sxs-lookup"><span data-stu-id="abd33-117">**SendMeetingInvitationsOrCancellations**</span></span> <br/> |<span data-ttu-id="abd33-118">介绍如何更新日历项目后传递会议更新。</span><span class="sxs-lookup"><span data-stu-id="abd33-118">Describes how meeting updates are communicated after a calendar item is updated.</span></span> <span data-ttu-id="abd33-119">此属性是必需的日历项目和日历项发生次数。</span><span class="sxs-lookup"><span data-stu-id="abd33-119">This attribute is required for calendar items and calendar item occurrences.</span></span>  <br/> |
|<span data-ttu-id="abd33-120">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="abd33-120">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="abd33-121">指示是否应禁止显示更新项已读的回执。</span><span class="sxs-lookup"><span data-stu-id="abd33-121">Indicates whether read receipts for the updated item should be suppressed.</span></span> <span data-ttu-id="abd33-122">文本值为**true**指示的 read 应禁止显示回执。</span><span class="sxs-lookup"><span data-stu-id="abd33-122">A text value of **true** indicates that read receipts should be suppressed.</span></span> <span data-ttu-id="abd33-123">如果值为**false**指示将向发件人发送已读的回执。</span><span class="sxs-lookup"><span data-stu-id="abd33-123">A value of **false** indicates that the read receipts will be sent to the sender.</span></span> <span data-ttu-id="abd33-124">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="abd33-124">This attribute is optional.</span></span>  <br/> <span data-ttu-id="abd33-125">此属性是在 Exchange Server 2013 SP1 中引入的。</span><span class="sxs-lookup"><span data-stu-id="abd33-125">This attribute was introduced in Exchange Server 2013 SP1.</span></span>  <br/> |
   
#### <a name="conflictresolution-attribute"></a><span data-ttu-id="abd33-126">ConflictResolution 属性</span><span class="sxs-lookup"><span data-stu-id="abd33-126">ConflictResolution Attribute</span></span>

|<span data-ttu-id="abd33-127">**值**</span><span class="sxs-lookup"><span data-stu-id="abd33-127">**Value**</span></span>|<span data-ttu-id="abd33-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="abd33-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abd33-129">NeverOverwrite</span><span class="sxs-lookup"><span data-stu-id="abd33-129">NeverOverwrite</span></span>  <br/> |<span data-ttu-id="abd33-130">如果没有冲突，更新操作失败，并返回一个错误。</span><span class="sxs-lookup"><span data-stu-id="abd33-130">If there is a conflict, the update operation fails and an error is returned.</span></span>  <br/> |
|<span data-ttu-id="abd33-131">自动解析</span><span class="sxs-lookup"><span data-stu-id="abd33-131">AutoResolve</span></span>  <br/> |<span data-ttu-id="abd33-132">更新操作自动解决任何冲突。</span><span class="sxs-lookup"><span data-stu-id="abd33-132">The update operation automatically resolves any conflict.</span></span>  <br/> |
|<span data-ttu-id="abd33-133">AlwaysOverwrite</span><span class="sxs-lookup"><span data-stu-id="abd33-133">AlwaysOverwrite</span></span>  <br/> |<span data-ttu-id="abd33-134">如果没有冲突，更新操作将覆盖信息。</span><span class="sxs-lookup"><span data-stu-id="abd33-134">If there is a conflict, the update operation will overwrite information.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="abd33-135">MessageDisposition 属性</span><span class="sxs-lookup"><span data-stu-id="abd33-135">MessageDisposition Attribute</span></span>

|<span data-ttu-id="abd33-136">**值**</span><span class="sxs-lookup"><span data-stu-id="abd33-136">**Value**</span></span>|<span data-ttu-id="abd33-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="abd33-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abd33-138">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="abd33-138">SaveOnly</span></span>  <br/> |<span data-ttu-id="abd33-139">项目更新并保存回其当前文件夹。</span><span class="sxs-lookup"><span data-stu-id="abd33-139">The item is updated and saved back to its current folder.</span></span>  <br/> |
|<span data-ttu-id="abd33-140">SendOnly</span><span class="sxs-lookup"><span data-stu-id="abd33-140">SendOnly</span></span>  <br/> |<span data-ttu-id="abd33-141">更新和发送项目，但没有副本保存。</span><span class="sxs-lookup"><span data-stu-id="abd33-141">The item is updated and sent but no copy is saved.</span></span>  <br/> |
|<span data-ttu-id="abd33-142">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="abd33-142">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="abd33-143">副本保存在由[SavedItemFolderId](saveditemfolderid.md)元素标识的文件夹和更新项目。</span><span class="sxs-lookup"><span data-stu-id="abd33-143">The item is updated and a copy is saved in the folder identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a><span data-ttu-id="abd33-144">SendMeetingInvitationsOrCancellations 属性</span><span class="sxs-lookup"><span data-stu-id="abd33-144">SendMeetingInvitationsOrCancellations Attribute</span></span>

|<span data-ttu-id="abd33-145">**值**</span><span class="sxs-lookup"><span data-stu-id="abd33-145">**Value**</span></span>|<span data-ttu-id="abd33-146">**说明**</span><span class="sxs-lookup"><span data-stu-id="abd33-146">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abd33-147">SendToNone</span><span class="sxs-lookup"><span data-stu-id="abd33-147">SendToNone</span></span>  <br/> |<span data-ttu-id="abd33-148">更新日历项目，但不是将更新发送给与会者。</span><span class="sxs-lookup"><span data-stu-id="abd33-148">The calendar item is updated but updates are not sent to attendees.</span></span>  <br/> |
|<span data-ttu-id="abd33-149">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="abd33-149">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="abd33-150">更新日历项和会议更新发送给所有与会者，但不是保存在已发送邮件文件夹中。</span><span class="sxs-lookup"><span data-stu-id="abd33-150">The calendar item is updated and the meeting update is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="abd33-151">SendOnlyToChanged</span><span class="sxs-lookup"><span data-stu-id="abd33-151">SendOnlyToChanged</span></span>  <br/> |<span data-ttu-id="abd33-152">会议更新仅发送给与会者受影响的会议中的更改和更新的日历项目。</span><span class="sxs-lookup"><span data-stu-id="abd33-152">The calendar item is updated and the meeting update is sent only to attendees that are affected by the change in the meeting.</span></span>  <br/> |
|<span data-ttu-id="abd33-153">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="abd33-153">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="abd33-154">更新日历项、 会议更新发送给所有与会者，和副本保存在已发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="abd33-154">The calendar item is updated, the meeting update is sent to all attendees, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="abd33-155">SendToChangedAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="abd33-155">SendToChangedAndSaveCopy</span></span>  <br/> |<span data-ttu-id="abd33-156">更新日历项、 会议更新发送到在会议中，更改影响的所有与会者和副本保存在已发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="abd33-156">The calendar item is updated, the meeting update is sent to all attendees that are affected by the change in the meeting, and a copy is saved in the Sent Items folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="abd33-157">子元素</span><span class="sxs-lookup"><span data-stu-id="abd33-157">Child elements</span></span>

|<span data-ttu-id="abd33-158">**元素**</span><span class="sxs-lookup"><span data-stu-id="abd33-158">**Element**</span></span>|<span data-ttu-id="abd33-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="abd33-159">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abd33-160">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="abd33-160">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="abd33-161">标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="abd33-161">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="abd33-162">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="abd33-162">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="abd33-163">包含确定项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="abd33-163">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abd33-164">父元素</span><span class="sxs-lookup"><span data-stu-id="abd33-164">Parent elements</span></span>

<span data-ttu-id="abd33-165">无。</span><span class="sxs-lookup"><span data-stu-id="abd33-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abd33-166">备注</span><span class="sxs-lookup"><span data-stu-id="abd33-166">Remarks</span></span>

<span data-ttu-id="abd33-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="abd33-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abd33-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="abd33-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abd33-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="abd33-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="abd33-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="abd33-170">Schema Name</span></span>  <br/> |<span data-ttu-id="abd33-171">消息架构</span><span class="sxs-lookup"><span data-stu-id="abd33-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="abd33-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="abd33-172">Validation File</span></span>  <br/> |<span data-ttu-id="abd33-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="abd33-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="abd33-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="abd33-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="abd33-175">False</span><span class="sxs-lookup"><span data-stu-id="abd33-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abd33-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="abd33-176">See also</span></span>



[<span data-ttu-id="abd33-177">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="abd33-177">UpdateItem operation</span></span>](updateitem-operation.md)

