---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: ItemId 元素包含 Exchange 存储中项的唯一标识符和更改键。
localization_priority: Priority
ms.openlocfilehash: d5931702225c6864b1ca60a6f0753b65f65aca30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441560"
---
# <a name="itemid"></a><span data-ttu-id="21a04-103">ItemId</span><span class="sxs-lookup"><span data-stu-id="21a04-103">ItemId</span></span>

<span data-ttu-id="21a04-104">**ItemId**元素包含 Exchange 存储中项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="21a04-104">The **ItemId** element contains the unique identifier and change key of an item in the Exchange store.</span></span> 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 <span data-ttu-id="21a04-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="21a04-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21a04-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21a04-106">Attributes and elements</span></span>

<span data-ttu-id="21a04-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21a04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21a04-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="21a04-108">Attributes</span></span>

|<span data-ttu-id="21a04-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="21a04-109">**Attribute**</span></span>|<span data-ttu-id="21a04-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="21a04-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="21a04-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="21a04-111">**Id**</span></span> <br/> |<span data-ttu-id="21a04-112">标识 Exchange 存储中的特定项目。</span><span class="sxs-lookup"><span data-stu-id="21a04-112">Identifies a specific item in the Exchange store.</span></span> <span data-ttu-id="21a04-113">**Id**区分大小写;因此， **id**之间的比较必须区分大小写或二进制。</span><span class="sxs-lookup"><span data-stu-id="21a04-113">**Id** is case-sensitive; therefore, comparisons between **Ids** must be case-sensitive or binary.</span></span>  <br/> |
|<span data-ttu-id="21a04-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="21a04-114">**ChangeKey**</span></span> <br/> | <span data-ttu-id="21a04-115">标识项目的特定版本。</span><span class="sxs-lookup"><span data-stu-id="21a04-115">Identifies a specific version of an item.</span></span> <br/><br/><span data-ttu-id="21a04-116">在以下情况下， **ChangeKey**是必需的：</span><span class="sxs-lookup"><span data-stu-id="21a04-116">A **ChangeKey** is required for the following scenarios:</span></span> <br/> <br/><span data-ttu-id="21a04-117">-如果**ConflictResolution**属性设置为 "自动解析"，则[UpdateItem](updateitem.md)元素需要**ChangeKey** 。</span><span class="sxs-lookup"><span data-stu-id="21a04-117">-  The [UpdateItem](updateitem.md) element requires a **ChangeKey** if the **ConflictResolution** attribute is set to AutoResolve.</span></span> <span data-ttu-id="21a04-118">"自动解析" 是默认值。</span><span class="sxs-lookup"><span data-stu-id="21a04-118">AutoResolve is a default value.</span></span> <span data-ttu-id="21a04-119">如果不包含**ChangeKey**属性，则响应将返回一个等于**ErrorChangeKeyRequired**的[ResponseCode](responsecode.md)值。</span><span class="sxs-lookup"><span data-stu-id="21a04-119">If the **ChangeKey** attribute is not included, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorChangeKeyRequired**.</span></span>  <br/><br/><span data-ttu-id="21a04-120">- [SendItem](senditem.md)元素需要**ChangeKey**以测试尝试的操作是否将对项目的最新版本进行操作。</span><span class="sxs-lookup"><span data-stu-id="21a04-120">-  The [SendItem](senditem.md) element requires a **ChangeKey** to test whether the attempted operation will act upon the most recent version of an item.</span></span> <span data-ttu-id="21a04-121">如果**ChangeKey**属性未包含在**ItemId**中，或者如果**ChangeKey**为空，响应将返回一个等于**ErrorStaleObject**的[ResponseCode](responsecode.md)值。</span><span class="sxs-lookup"><span data-stu-id="21a04-121">If the **ChangeKey** attribute is not included in the **ItemId** or if the **ChangeKey** is empty, the response will return a [ResponseCode](responsecode.md) value equal to **ErrorStaleObject**.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="21a04-122">子元素</span><span class="sxs-lookup"><span data-stu-id="21a04-122">Child elements</span></span>

<span data-ttu-id="21a04-123">无。</span><span class="sxs-lookup"><span data-stu-id="21a04-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21a04-124">父元素</span><span class="sxs-lookup"><span data-stu-id="21a04-124">Parent elements</span></span>

|<span data-ttu-id="21a04-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="21a04-125">**Element**</span></span>|<span data-ttu-id="21a04-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="21a04-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21a04-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="21a04-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="21a04-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="21a04-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-129">Contact</span><span class="sxs-lookup"><span data-stu-id="21a04-129">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="21a04-130">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="21a04-130">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="21a04-132">代表复制项目或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-132">Represents an event when an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="21a04-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="21a04-134">表示创建项或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-134">Represents an event when an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="21a04-135">Delete （ItemSync）</span><span class="sxs-lookup"><span data-stu-id="21a04-135">Delete (ItemSync)</span></span>](delete-itemsync.md) <br/> |<span data-ttu-id="21a04-136">标识要在本地客户端存储中删除的单个项。</span><span class="sxs-lookup"><span data-stu-id="21a04-136">Identifies a single item to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-137">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-137">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="21a04-138">表示在删除项或文件夹时的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-138">Represents an event when an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="21a04-139">DistributionList</span><span class="sxs-lookup"><span data-stu-id="21a04-139">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="21a04-140">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="21a04-140">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="21a04-141">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="21a04-141">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="21a04-142">包含导出单个邮箱项目的请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="21a04-142">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-143">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="21a04-143">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="21a04-144">表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="21a04-144">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-145">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="21a04-145">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="21a04-146">包含邮箱中所有会话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="21a04-146">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="21a04-147">忽略</span><span class="sxs-lookup"><span data-stu-id="21a04-147">Ignore</span></span>](ignore.md) <br/> |<span data-ttu-id="21a04-148">确定在同步过程中要跳过的项。</span><span class="sxs-lookup"><span data-stu-id="21a04-148">Identifies items to skip during synchronization.</span></span>  <br/> |
|[<span data-ttu-id="21a04-149">项</span><span class="sxs-lookup"><span data-stu-id="21a04-149">Item</span></span>](item.md) <br/> |<span data-ttu-id="21a04-150">表示通用 Exchange 项。</span><span class="sxs-lookup"><span data-stu-id="21a04-150">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-151">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="21a04-151">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="21a04-152">代表要上传到邮箱中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="21a04-152">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="21a04-153">ItemChange</span><span class="sxs-lookup"><span data-stu-id="21a04-153">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="21a04-154">包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="21a04-154">Contains an item identifier and the updates to apply to the item.</span></span>  <br/><br/> <span data-ttu-id="21a04-155">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="21a04-155">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="21a04-156">ItemIds</span><span class="sxs-lookup"><span data-stu-id="21a04-156">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="21a04-157">包含项目、具体值项目和定期主项目的唯一标识，用于删除、发送、获取、移动或复制 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="21a04-157">Contains the unique identities of items, occurrence items, and recurring master items used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="21a04-158">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="21a04-158">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[<span data-ttu-id="21a04-159">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="21a04-159">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="21a04-160">包含项标识符的数组，这些标识符标识要从邮箱中导出的项。</span><span class="sxs-lookup"><span data-stu-id="21a04-160">Contains an array of item identifiers that identify the items to export from a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="21a04-161">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="21a04-161">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="21a04-162">表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-162">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-163">Mailbox</span><span class="sxs-lookup"><span data-stu-id="21a04-163">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="21a04-164">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="21a04-164">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="21a04-165">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="21a04-165">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="21a04-166">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="21a04-166">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-167">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="21a04-167">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="21a04-168">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="21a04-168">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-169">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="21a04-169">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="21a04-170">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="21a04-170">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-171">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="21a04-171">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="21a04-172">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="21a04-172">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-173">Message</span><span class="sxs-lookup"><span data-stu-id="21a04-173">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="21a04-174">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="21a04-174">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="21a04-175">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-175">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="21a04-176">代表修改项目时发生的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-176">Represents an event that occurs when an item is modified.</span></span>  <br/> |
|[<span data-ttu-id="21a04-177">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-177">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="21a04-178">表示在将项目从一个父文件夹移动到另一个父文件夹时发生的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-178">Represents an event that occurs when an item is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="21a04-179">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="21a04-179">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="21a04-180">代表由邮箱中的新邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-180">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="21a04-181">重复</span><span class="sxs-lookup"><span data-stu-id="21a04-181">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="21a04-182">代表定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="21a04-182">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-183">PlayOnPhone （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="21a04-183">PlayOnPhone (Exchange Web Services)</span></span>](playonphone-exchange-web-services.md) <br/> |<span data-ttu-id="21a04-184">表示在电话上读取项目的请求。</span><span class="sxs-lookup"><span data-stu-id="21a04-184">Represents a request to read an item on a telephone.</span></span>  <br/> |
|[<span data-ttu-id="21a04-185">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="21a04-185">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="21a04-186">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="21a04-186">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-187">RoomList</span><span class="sxs-lookup"><span data-stu-id="21a04-187">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="21a04-188">代表标识会议室列表的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="21a04-188">Represents an e-mail address that identifies a list of meeting rooms.</span></span>  <br/> |
|[<span data-ttu-id="21a04-189">任务</span><span class="sxs-lookup"><span data-stu-id="21a04-189">Task</span></span>](task.md) <br/> |<span data-ttu-id="21a04-190">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="21a04-190">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="21a04-191">UploadItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="21a04-191">UploadItemsResponseMessage</span></span>](uploaditemsresponsemessage.md) <br/> |<span data-ttu-id="21a04-192">包含上载单个邮箱项目的请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="21a04-192">Contains the status and results of a request to upload a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="21a04-193">UserConfiguration</span><span class="sxs-lookup"><span data-stu-id="21a04-193">UserConfiguration</span></span>](userconfiguration.md) <br/> |<span data-ttu-id="21a04-194">定义单个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="21a04-194">Defines a single user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21a04-195">文本值</span><span class="sxs-lookup"><span data-stu-id="21a04-195">Text value</span></span>

<span data-ttu-id="21a04-196">无。</span><span class="sxs-lookup"><span data-stu-id="21a04-196">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21a04-197">说明</span><span class="sxs-lookup"><span data-stu-id="21a04-197">Remarks</span></span>

<span data-ttu-id="21a04-198">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21a04-198">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21a04-199">元素信息</span><span class="sxs-lookup"><span data-stu-id="21a04-199">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21a04-200">命名空间</span><span class="sxs-lookup"><span data-stu-id="21a04-200">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21a04-201">架构名称</span><span class="sxs-lookup"><span data-stu-id="21a04-201">Schema Name</span></span>  <br/> |<span data-ttu-id="21a04-202">类型架构</span><span class="sxs-lookup"><span data-stu-id="21a04-202">Types schema</span></span>  <br/> |
|<span data-ttu-id="21a04-203">验证文件</span><span class="sxs-lookup"><span data-stu-id="21a04-203">Validation File</span></span>  <br/> |<span data-ttu-id="21a04-204">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21a04-204">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21a04-205">可以为空</span><span class="sxs-lookup"><span data-stu-id="21a04-205">Can be Empty</span></span>  <br/> |<span data-ttu-id="21a04-206">False</span><span class="sxs-lookup"><span data-stu-id="21a04-206">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21a04-207">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21a04-207">See also</span></span>

- [<span data-ttu-id="21a04-208">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="21a04-208">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="21a04-209">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="21a04-209">UploadItems operation</span></span>](uploaditems-operation.md) 
- [<span data-ttu-id="21a04-210">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="21a04-210">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="21a04-211">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21a04-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

