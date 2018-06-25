---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: ItemId 元素包含在 Exchange 存储中的项目的唯一标识符和更改的键。
ms.openlocfilehash: 9c5d71a23e1e4b77d2a50016aa4d765d872d04cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826157"
---
# <a name="itemid"></a><span data-ttu-id="52bf7-103">ItemId</span><span class="sxs-lookup"><span data-stu-id="52bf7-103">ItemId</span></span>

<span data-ttu-id="52bf7-104">**ItemId**元素包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="52bf7-104">The **ItemId** element contains the unique identifier and change key of an item in the Exchange store.</span></span> 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="52bf7-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="52bf7-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52bf7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52bf7-106">Attributes and elements</span></span>

<span data-ttu-id="52bf7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52bf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52bf7-108">属性</span><span class="sxs-lookup"><span data-stu-id="52bf7-108">Attributes</span></span>

|<span data-ttu-id="52bf7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="52bf7-109">**Attribute**</span></span>|<span data-ttu-id="52bf7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="52bf7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52bf7-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="52bf7-111">**Id**</span></span> <br/> |<span data-ttu-id="52bf7-112">标识 Exchange 存储中的特定项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-112">Identifies a specific item in the Exchange store.</span></span> <span data-ttu-id="52bf7-113">**Id**是区分大小写。因此， **Id**之间的比较必须区分大小写或二进制。</span><span class="sxs-lookup"><span data-stu-id="52bf7-113">**Id** is case-sensitive; therefore, comparisons between **Ids** must be case-sensitive or binary.</span></span>  <br/> |
|<span data-ttu-id="52bf7-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="52bf7-114">**ChangeKey**</span></span> <br/> | <span data-ttu-id="52bf7-115">标识项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="52bf7-115">Identifies a specific version of an item.</span></span> <br/><br/><span data-ttu-id="52bf7-116">**更改密钥**时，需要以下方案：</span><span class="sxs-lookup"><span data-stu-id="52bf7-116">A **ChangeKey** is required for the following scenarios:</span></span> <br/> <br/><span data-ttu-id="52bf7-117">如果**ConflictResolution**属性设置为自动解析，- [UpdateItem](updateitem.md)元素将需要**更改密钥**。</span><span class="sxs-lookup"><span data-stu-id="52bf7-117">-  The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="52bf7-118">自动解析为默认值。</span><span class="sxs-lookup"><span data-stu-id="52bf7-118">AutoResolve is a default value.</span></span> <span data-ttu-id="52bf7-119">如果不包括**更改密钥**属性，则响应将返回[ResponseCode](responsecode.md)值等于**ErrorChangeKeyRequired**。</span><span class="sxs-lookup"><span data-stu-id="52bf7-119">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span>  <br/><br/><span data-ttu-id="52bf7-120">- [SendItem](senditem.md)元素需要**更改密钥**来测试是否尝试的操作将作用于项目的最新版本。</span><span class="sxs-lookup"><span data-stu-id="52bf7-120">-  The [SendItem](senditem.md) element requires a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="52bf7-121">如果**更改密钥**属性不包括在**ItemId**或**更改密钥**为空，响应将返回[ResponseCode](responsecode.md)值等于**ErrorStaleObject**。</span><span class="sxs-lookup"><span data-stu-id="52bf7-121">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52bf7-122">子元素</span><span class="sxs-lookup"><span data-stu-id="52bf7-122">Child elements</span></span>

<span data-ttu-id="52bf7-123">无。</span><span class="sxs-lookup"><span data-stu-id="52bf7-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52bf7-124">父元素</span><span class="sxs-lookup"><span data-stu-id="52bf7-124">Parent elements</span></span>

|<span data-ttu-id="52bf7-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="52bf7-125">**Element**</span></span>|<span data-ttu-id="52bf7-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="52bf7-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52bf7-127">日历项目</span><span class="sxs-lookup"><span data-stu-id="52bf7-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="52bf7-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="52bf7-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-129">联系人</span><span class="sxs-lookup"><span data-stu-id="52bf7-129">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="52bf7-130">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-130">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="52bf7-132">表示复制的项或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-132">Represents an event when an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="52bf7-134">表示在创建项目或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-134">Represents an event when an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-135">删除 (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="52bf7-135">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="52bf7-136">标识要删除在本地客户端库中的单个项。</span><span class="sxs-lookup"><span data-stu-id="52bf7-136">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-137">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-137">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="52bf7-138">表示删除项目或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-138">Represents an event when an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-139">DistributionList</span><span class="sxs-lookup"><span data-stu-id="52bf7-139">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="52bf7-140">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="52bf7-140">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-141">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52bf7-141">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="52bf7-142">包含状态和请求导出的单个邮箱项目的结果。</span><span class="sxs-lookup"><span data-stu-id="52bf7-142">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-143">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="52bf7-143">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="52bf7-144">代表定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="52bf7-144">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-145">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="52bf7-145">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="52bf7-146">包含的项标识符的邮箱中的所有对话项的集合。</span><span class="sxs-lookup"><span data-stu-id="52bf7-146">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-147">忽略</span><span class="sxs-lookup"><span data-stu-id="52bf7-147">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="52bf7-148">标识同步过程中跳过的项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-148">Identifies items to skip during synchronization.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-149">Item</span><span class="sxs-lookup"><span data-stu-id="52bf7-149">Item</span></span>](item.md) <br/> |<span data-ttu-id="52bf7-150">表示的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-150">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-151">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="52bf7-151">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="52bf7-152">代表单个项目上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="52bf7-152">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-153">ItemChange</span><span class="sxs-lookup"><span data-stu-id="52bf7-153">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="52bf7-154">包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="52bf7-154">Contains an item identifier and the updates to apply to the item.</span></span>  <br/><br/> <span data-ttu-id="52bf7-155">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="52bf7-155">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="52bf7-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="52bf7-156">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="52bf7-157">包含唯一标识的项目、 匹配项和删除、 发送、 获取、 移动或在 Exchange 存储中复制项所用于的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-157">Contains the unique identities of items, occurrence items, and recurring master items used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="52bf7-158">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="52bf7-158">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[<span data-ttu-id="52bf7-159">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="52bf7-159">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="52bf7-160">包含确定要导出邮箱中的项的项标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="52bf7-160">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-161">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="52bf7-161">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="52bf7-162">代表定期日历项目的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="52bf7-162">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-163">Mailbox</span><span class="sxs-lookup"><span data-stu-id="52bf7-163">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="52bf7-164">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="52bf7-164">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-165">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="52bf7-165">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="52bf7-166">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="52bf7-166">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-167">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="52bf7-167">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="52bf7-168">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="52bf7-168">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-169">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="52bf7-169">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="52bf7-170">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="52bf7-170">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-171">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="52bf7-171">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="52bf7-172">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="52bf7-172">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-173">Message</span><span class="sxs-lookup"><span data-stu-id="52bf7-173">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="52bf7-174">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-174">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-175">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-175">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="52bf7-176">表示修改项目时发生的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-176">Represents an event that occurs when an item is modified.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-177">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-177">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="52bf7-178">表示项目从一个父文件夹移动到另一个父文件夹时发生的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-178">Represents an event that occurs when an item is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-179">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="52bf7-179">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="52bf7-180">表示由邮箱中的一个新的邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="52bf7-180">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-181">匹配项</span><span class="sxs-lookup"><span data-stu-id="52bf7-181">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="52bf7-182">代表定期日历项目的一个已修改匹配项。</span><span class="sxs-lookup"><span data-stu-id="52bf7-182">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-183">PlayOnPhone （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="52bf7-183">PlayOnPhone (Exchange Web Services)</span></span>](playonphone-exchange-web-services.md) <br/> |<span data-ttu-id="52bf7-184">表示读取电话上的项的请求。</span><span class="sxs-lookup"><span data-stu-id="52bf7-184">Represents a request to read an item on a telephone.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-185">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="52bf7-185">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="52bf7-186">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="52bf7-186">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-187">RoomList</span><span class="sxs-lookup"><span data-stu-id="52bf7-187">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="52bf7-188">表示标识的会议室列表的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="52bf7-188">Represents an e-mail address that identifies a list of meeting rooms.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-189">任务</span><span class="sxs-lookup"><span data-stu-id="52bf7-189">Task</span></span>](task.md) <br/> |<span data-ttu-id="52bf7-190">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="52bf7-190">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-191">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52bf7-191">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md) <br/> |<span data-ttu-id="52bf7-192">包含状态和请求上载单个邮箱项目的结果。</span><span class="sxs-lookup"><span data-stu-id="52bf7-192">Contains the status and results of a request to upload a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="52bf7-193">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="52bf7-193">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="52bf7-194">定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="52bf7-194">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52bf7-195">文本值</span><span class="sxs-lookup"><span data-stu-id="52bf7-195">Text value</span></span>

<span data-ttu-id="52bf7-196">无。</span><span class="sxs-lookup"><span data-stu-id="52bf7-196">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52bf7-197">备注</span><span class="sxs-lookup"><span data-stu-id="52bf7-197">Remarks</span></span>

<span data-ttu-id="52bf7-198">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52bf7-198">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52bf7-199">元素信息</span><span class="sxs-lookup"><span data-stu-id="52bf7-199">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52bf7-200">命名空间</span><span class="sxs-lookup"><span data-stu-id="52bf7-200">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52bf7-201">架构名称</span><span class="sxs-lookup"><span data-stu-id="52bf7-201">Schema Name</span></span>  <br/> |<span data-ttu-id="52bf7-202">类型架构</span><span class="sxs-lookup"><span data-stu-id="52bf7-202">Types schema</span></span>  <br/> |
|<span data-ttu-id="52bf7-203">验证文件</span><span class="sxs-lookup"><span data-stu-id="52bf7-203">Validation File</span></span>  <br/> |<span data-ttu-id="52bf7-204">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52bf7-204">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52bf7-205">可以为空</span><span class="sxs-lookup"><span data-stu-id="52bf7-205">Can be Empty</span></span>  <br/> |<span data-ttu-id="52bf7-206">False</span><span class="sxs-lookup"><span data-stu-id="52bf7-206">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52bf7-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52bf7-207">See also</span></span>

- [<span data-ttu-id="52bf7-208">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="52bf7-208">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="52bf7-209">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="52bf7-209">UploadItems operation</span></span>](uploaditems-operation.md) 
- [<span data-ttu-id="52bf7-210">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="52bf7-210">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="52bf7-211">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52bf7-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

