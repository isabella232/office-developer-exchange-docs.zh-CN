---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: DeleteItem 元素定义一个请求，以从 Exchange 存储中的邮箱中删除项目。
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529201"
---
# <a name="deleteitem"></a><span data-ttu-id="b2661-103">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="b2661-103">DeleteItem</span></span>

<span data-ttu-id="b2661-104">**DeleteItem**元素定义一个请求，以从 Exchange 存储中的邮箱中删除项目。</span><span class="sxs-lookup"><span data-stu-id="b2661-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="b2661-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="b2661-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2661-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b2661-106">Attributes and elements</span></span>

<span data-ttu-id="b2661-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b2661-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2661-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b2661-108">Attributes</span></span>

|<span data-ttu-id="b2661-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b2661-109">**Attribute**</span></span>|<span data-ttu-id="b2661-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2661-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2661-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="b2661-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="b2661-112">介绍如何删除项目。</span><span class="sxs-lookup"><span data-stu-id="b2661-112">Describes how an item is deleted.</span></span> <span data-ttu-id="b2661-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="b2661-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="b2661-114">**SendMeetingCancellations**</span><span class="sxs-lookup"><span data-stu-id="b2661-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="b2661-115">描述是否将日历项目删除操作传递给与会者。</span><span class="sxs-lookup"><span data-stu-id="b2661-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="b2661-116">删除日历项目时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="b2661-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="b2661-117">如果删除非日历项目，则此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2661-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="b2661-118">**AffectedTaskOccurrences**</span><span class="sxs-lookup"><span data-stu-id="b2661-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="b2661-119">描述任务实例或任务主控形状是否由[DeleteItem 操作](deleteitem-operation.md)删除。</span><span class="sxs-lookup"><span data-stu-id="b2661-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="b2661-120">删除任务时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="b2661-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="b2661-121">当非任务项目被删除时，此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2661-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="b2661-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="b2661-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="b2661-123">指示是否禁止显示已删除项目的已读回执。</span><span class="sxs-lookup"><span data-stu-id="b2661-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="b2661-124">如果文本值为**true**，则表示已取消阅读回执。</span><span class="sxs-lookup"><span data-stu-id="b2661-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="b2661-125">**如果值为 false** ，则表示已将已读回执发送到发件人。</span><span class="sxs-lookup"><span data-stu-id="b2661-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="b2661-126">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="b2661-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="b2661-127">DeleteType 属性</span><span class="sxs-lookup"><span data-stu-id="b2661-127">DeleteType attribute</span></span>

|<span data-ttu-id="b2661-128">**值**</span><span class="sxs-lookup"><span data-stu-id="b2661-128">**Value**</span></span>|<span data-ttu-id="b2661-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2661-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2661-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="b2661-130">HardDelete</span></span>  <br/> |<span data-ttu-id="b2661-131">项目已从存储区中永久删除。</span><span class="sxs-lookup"><span data-stu-id="b2661-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="b2661-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="b2661-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="b2661-133">如果启用了转储程序，则会将项目移动到转储程序。</span><span class="sxs-lookup"><span data-stu-id="b2661-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="b2661-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="b2661-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="b2661-135">将项目移动到"已删除邮件"文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b2661-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="b2661-136">SendMeetingCancellations 属性</span><span class="sxs-lookup"><span data-stu-id="b2661-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="b2661-137">**值**</span><span class="sxs-lookup"><span data-stu-id="b2661-137">**Value**</span></span>|<span data-ttu-id="b2661-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2661-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2661-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="b2661-139">SendToNone</span></span>  <br/> |<span data-ttu-id="b2661-140">删除日历项目，但不发送取消邮件。</span><span class="sxs-lookup"><span data-stu-id="b2661-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="b2661-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="b2661-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="b2661-142">删除日历项目并向所有与会者发送取消邮件。</span><span class="sxs-lookup"><span data-stu-id="b2661-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="b2661-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="b2661-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="b2661-144">删除日历项目并向所有与会者发送取消邮件。</span><span class="sxs-lookup"><span data-stu-id="b2661-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="b2661-145">取消邮件的副本保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b2661-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="b2661-146">AffectedTaskOccurrences 属性</span><span class="sxs-lookup"><span data-stu-id="b2661-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="b2661-147">**值**</span><span class="sxs-lookup"><span data-stu-id="b2661-147">**Value**</span></span>|<span data-ttu-id="b2661-148">**说明**</span><span class="sxs-lookup"><span data-stu-id="b2661-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b2661-149">AllOccurrences</span><span class="sxs-lookup"><span data-stu-id="b2661-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="b2661-150">"删除项目" 请求会删除主任务，从而删除与主任务相关联的所有定期任务。</span><span class="sxs-lookup"><span data-stu-id="b2661-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="b2661-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="b2661-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="b2661-152">"删除项目" 请求仅删除任务的特定事件。</span><span class="sxs-lookup"><span data-stu-id="b2661-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b2661-153">子元素</span><span class="sxs-lookup"><span data-stu-id="b2661-153">Child elements</span></span>

|<span data-ttu-id="b2661-154">**元素**</span><span class="sxs-lookup"><span data-stu-id="b2661-154">**Element**</span></span>|<span data-ttu-id="b2661-155">**描述**</span><span class="sxs-lookup"><span data-stu-id="b2661-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2661-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="b2661-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="b2661-157">包含要从 Exchange 存储中的邮箱中删除的项、具体值项和定期主项目的数组。</span><span class="sxs-lookup"><span data-stu-id="b2661-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="b2661-158">可以对任何项目类型执行[DeleteItem 操作](deleteitem-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="b2661-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2661-159">父元素</span><span class="sxs-lookup"><span data-stu-id="b2661-159">Parent elements</span></span>

<span data-ttu-id="b2661-160">无。</span><span class="sxs-lookup"><span data-stu-id="b2661-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2661-161">说明</span><span class="sxs-lookup"><span data-stu-id="b2661-161">Remarks</span></span>

<span data-ttu-id="b2661-p107">**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。</span><span class="sxs-lookup"><span data-stu-id="b2661-p107">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database. This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="b2661-164">Exchange 的不同目标版本的**SoftDelete**选项的工作方式不同。</span><span class="sxs-lookup"><span data-stu-id="b2661-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="b2661-165">**SoftDelete** for exchange 2007 在项目中设置一个位，以指示 exchange 数据库，该项目将在将来的不确定时间移动到转储程序文件夹中。</span><span class="sxs-lookup"><span data-stu-id="b2661-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="b2661-166">**SoftDelete** for Exchange 2010 立即将项目移动到转储程序。</span><span class="sxs-lookup"><span data-stu-id="b2661-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="b2661-167">**SoftDelete**不是文件夹删除的选项。</span><span class="sxs-lookup"><span data-stu-id="b2661-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="b2661-168">**SoftDelete**遍历项目和文件夹的搜索不会返回任何结果。</span><span class="sxs-lookup"><span data-stu-id="b2661-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="b2661-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b2661-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2661-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="b2661-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2661-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="b2661-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b2661-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="b2661-172">Schema Name</span></span>  <br/> |<span data-ttu-id="b2661-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="b2661-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b2661-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="b2661-174">Validation File</span></span>  <br/> |<span data-ttu-id="b2661-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b2661-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b2661-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="b2661-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="b2661-177">False</span><span class="sxs-lookup"><span data-stu-id="b2661-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2661-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b2661-178">See also</span></span>

- [<span data-ttu-id="b2661-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="b2661-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="b2661-180">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="b2661-180">DeleteItem operation</span></span>](deleteitem-operation.md)

