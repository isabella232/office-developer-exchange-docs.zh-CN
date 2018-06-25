---
title: 删除项
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
description: 删除项元素定义从 Exchange 存储中的邮箱中删除项目的请求。
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753816"
---
# <a name="deleteitem"></a><span data-ttu-id="0a1d0-103">删除项</span><span class="sxs-lookup"><span data-stu-id="0a1d0-103">DeleteItem</span></span>

<span data-ttu-id="0a1d0-104">**删除项**元素定义从 Exchange 存储中的邮箱中删除项目的请求。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-104">The **DeleteItem** element defines a request to delete an item from a mailbox in the Exchange store.</span></span> 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 <span data-ttu-id="0a1d0-105">**DeleteItemType**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-105">**DeleteItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a1d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a1d0-106">Attributes and elements</span></span>

<span data-ttu-id="0a1d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a1d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="0a1d0-108">Attributes</span></span>

|<span data-ttu-id="0a1d0-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-109">**Attribute**</span></span>|<span data-ttu-id="0a1d0-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a1d0-111">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-111">**DeleteType**</span></span> <br/> |<span data-ttu-id="0a1d0-112">介绍如何删除项目。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-112">Describes how an item is deleted.</span></span> <span data-ttu-id="0a1d0-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-114">**SendMeetingCancellations**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-114">**SendMeetingCancellations**</span></span> <br/> |<span data-ttu-id="0a1d0-115">描述是否将日历项删除传送给与会者。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-115">Describes whether a calendar item deletion is communicated to attendees.</span></span> <span data-ttu-id="0a1d0-116">删除日历项目时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-116">This attribute is required when calendar items are deleted.</span></span> <span data-ttu-id="0a1d0-117">此属性是可选的如果删除非日历项目。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-117">This attribute is optional if non-calendar items are deleted.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-118">**AffectedTaskOccurrences**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-118">**AffectedTaskOccurrences**</span></span> <br/> |<span data-ttu-id="0a1d0-119">描述是否通过[删除项操作](deleteitem-operation.md)删除任务实例或任务主控形状。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-119">Describes whether a task instance or a task master is deleted by a [DeleteItem operation](deleteitem-operation.md).</span></span> <span data-ttu-id="0a1d0-120">在删除任务时，此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-120">This attribute is required when tasks are deleted.</span></span> <span data-ttu-id="0a1d0-121">非任务项将被删除时，此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-121">This attribute is optional when non-task items are deleted.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-122">**SuppressReadReceipts**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-122">**SuppressReadReceipts**</span></span> <br/> |<span data-ttu-id="0a1d0-123">指示是否将禁止显示已删除项已读的回执。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-123">Indicates whether read receipts for the deleted item are suppressed.</span></span> <span data-ttu-id="0a1d0-124">文本值为**true**，指示已读的回执被禁止。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-124">A text value of **true**, indicates that the read receipts are suppressed.</span></span> <span data-ttu-id="0a1d0-125">如果值为**false**指示已读的回执，会向发件人发送。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-125">A value of **false** indicates that the read receipts are sent to the sender.</span></span> <span data-ttu-id="0a1d0-126">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-126">This attribute is optional.</span></span>  <br/> |
   
#### <a name="deletetype-attribute"></a><span data-ttu-id="0a1d0-127">DeleteType 属性</span><span class="sxs-lookup"><span data-stu-id="0a1d0-127">DeleteType attribute</span></span>

|<span data-ttu-id="0a1d0-128">**值**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-128">**Value**</span></span>|<span data-ttu-id="0a1d0-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a1d0-130">HardDelete</span><span class="sxs-lookup"><span data-stu-id="0a1d0-130">HardDelete</span></span>  <br/> |<span data-ttu-id="0a1d0-131">从存储永久删除项目。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-131">An item is permanently removed from the store.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-132">SoftDelete</span><span class="sxs-lookup"><span data-stu-id="0a1d0-132">SoftDelete</span></span>  <br/> |<span data-ttu-id="0a1d0-133">将项目移动到转储程序如果转储程序已启用。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-133">An item is moved to the dumpster if the dumpster is enabled.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-134">MoveToDeletedItems</span><span class="sxs-lookup"><span data-stu-id="0a1d0-134">MoveToDeletedItems</span></span>  <br/> |<span data-ttu-id="0a1d0-135">将项目移动到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-135">An item is moved to the Deleted Items folder.</span></span>  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a><span data-ttu-id="0a1d0-136">SendMeetingCancellations 属性</span><span class="sxs-lookup"><span data-stu-id="0a1d0-136">SendMeetingCancellations attribute</span></span>

|<span data-ttu-id="0a1d0-137">**值**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-137">**Value**</span></span>|<span data-ttu-id="0a1d0-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-138">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a1d0-139">SendToNone</span><span class="sxs-lookup"><span data-stu-id="0a1d0-139">SendToNone</span></span>  <br/> |<span data-ttu-id="0a1d0-140">日历项目而不发送取消邮件中删除。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-140">A calendar item is deleted without sending a cancellation message.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-141">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="0a1d0-141">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="0a1d0-142">日历项目被删除，取消邮件发送给所有与会者。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-142">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-143">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="0a1d0-143">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="0a1d0-144">日历项目被删除，取消邮件发送给所有与会者。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-144">A calendar item is deleted and a cancellation message is sent to all attendees.</span></span> <span data-ttu-id="0a1d0-145">在已发送邮件文件夹中保存一份取消邮件。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-145">A copy of the cancellation message is saved in the Sent Items folder.</span></span>  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a><span data-ttu-id="0a1d0-146">AffectedTaskOccurrences 属性</span><span class="sxs-lookup"><span data-stu-id="0a1d0-146">AffectedTaskOccurrences attribute</span></span>

|<span data-ttu-id="0a1d0-147">**值**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-147">**Value**</span></span>|<span data-ttu-id="0a1d0-148">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-148">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a1d0-149">AllOccurrences</span><span class="sxs-lookup"><span data-stu-id="0a1d0-149">AllOccurrences</span></span>  <br/> |<span data-ttu-id="0a1d0-150">删除项目请求删除主控形状的任务中，，因此所有定期任务的与主任务关联。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-150">A delete item request deletes the master task, and therefore all recurring tasks that are associated with the master task.</span></span>  <br/> |
|<span data-ttu-id="0a1d0-151">SpecifiedOccurrenceOnly</span><span class="sxs-lookup"><span data-stu-id="0a1d0-151">SpecifiedOccurrenceOnly</span></span>  <br/> |<span data-ttu-id="0a1d0-152">删除项目请求删除任务的仅特定事件。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-152">A delete item request deletes only specific occurrences of a task.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0a1d0-153">子元素</span><span class="sxs-lookup"><span data-stu-id="0a1d0-153">Child elements</span></span>

|<span data-ttu-id="0a1d0-154">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-154">**Element**</span></span>|<span data-ttu-id="0a1d0-155">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-155">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a1d0-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="0a1d0-156">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="0a1d0-157">包含项目、 匹配项和定期主项目以从 Exchange 存储的邮箱中删除一个数组。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-157">Contains an array of items, occurrence items, and recurring master items to delete from a mailbox in the Exchange store.</span></span> <span data-ttu-id="0a1d0-158">可以在任何项类型上执行[删除项操作](deleteitem-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-158">The [DeleteItem operation](deleteitem-operation.md) can be performed on any item type.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0a1d0-159">父元素</span><span class="sxs-lookup"><span data-stu-id="0a1d0-159">Parent elements</span></span>

<span data-ttu-id="0a1d0-160">无。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-160">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a1d0-161">备注</span><span class="sxs-lookup"><span data-stu-id="0a1d0-161">Remarks</span></span>

<span data-ttu-id="0a1d0-p107">**MoveToDeletedItems** 和 **HardDelete** 选项是事务性的这意味着，Web 服务调用完成时，数据库将邮件移至已删除邮件文件夹或从Exchange数据库中永久删除该项目。这种行为是相同的MicrosoftExchange Server 2007和Exchange Server 2010。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-p107">The **MoveToDeletedItems** and **HardDelete** options are transactional, which means that by the time a Web service call completes, the database has moved the item to the Deleted Items folder or permanently removed the item from the Exchange database. This behavior is the same for MicrosoftExchange Server 2007 and Exchange Server 2010.</span></span> 
  
<span data-ttu-id="0a1d0-164">**SoftDelete**选项不同的目标版本的 Exchange 的工作方式。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-164">The **SoftDelete** option works differently for different target versions of Exchange.</span></span> <span data-ttu-id="0a1d0-165">Exchange 2007 **SoftDelete**在表示项目将移至 Exchange 数据库的项目上设置位转储程序文件夹的将来确定的时间。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-165">**SoftDelete** for Exchange 2007 sets a bit on the item that indicates to the Exchange database that the item will be moved to the dumpster folder at an indeterminate time in the future.</span></span> <span data-ttu-id="0a1d0-166">对于 Exchange 2010 **SoftDelete**立即移动到的项转储程序。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-166">**SoftDelete** for Exchange 2010 immediately moves the item to the dumpster.</span></span> <span data-ttu-id="0a1d0-167">**SoftDelete**不为文件夹删除选项。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-167">**SoftDelete** is not an option for folder deletion.</span></span> <span data-ttu-id="0a1d0-168">项目和文件夹的**SoftDelete**遍历搜索不会返回任何结果。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-168">**SoftDelete** traversal searches for items and folders will not return any results.</span></span> 
  
<span data-ttu-id="0a1d0-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a1d0-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a1d0-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a1d0-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a1d0-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a1d0-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0a1d0-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a1d0-172">Schema Name</span></span>  <br/> |<span data-ttu-id="0a1d0-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="0a1d0-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0a1d0-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a1d0-174">Validation File</span></span>  <br/> |<span data-ttu-id="0a1d0-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0a1d0-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0a1d0-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a1d0-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a1d0-177">False</span><span class="sxs-lookup"><span data-stu-id="0a1d0-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a1d0-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a1d0-178">See also</span></span>

- [<span data-ttu-id="0a1d0-179">DeleteItemResponse</span><span class="sxs-lookup"><span data-stu-id="0a1d0-179">DeleteItemResponse</span></span>](deleteitemresponse.md)  
- [<span data-ttu-id="0a1d0-180">删除项操作</span><span class="sxs-lookup"><span data-stu-id="0a1d0-180">DeleteItem operation</span></span>](deleteitem-operation.md)

