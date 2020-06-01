---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: ParentFolderId 元素表示包含项或文件夹的父文件夹的标识符。
ms.openlocfilehash: 3bad638aa21019472df8f487f1e065d2e725e750
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465749"
---
# <a name="parentfolderid"></a><span data-ttu-id="06493-103">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="06493-103">ParentFolderId</span></span>

<span data-ttu-id="06493-104">**ParentFolderId**元素表示包含项或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="06493-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="06493-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="06493-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="06493-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="06493-106">Attributes and elements</span></span>

<span data-ttu-id="06493-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="06493-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06493-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="06493-108">Attributes</span></span>

|<span data-ttu-id="06493-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="06493-109">**Attribute**</span></span>|<span data-ttu-id="06493-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="06493-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06493-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="06493-111">**Id**</span></span> <br/> |<span data-ttu-id="06493-112">包含标识 Exchange 存储中的文件夹的字符串。</span><span class="sxs-lookup"><span data-stu-id="06493-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="06493-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="06493-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="06493-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="06493-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="06493-115">包含标识由**Id**属性标识的文件夹版本的字符串。</span><span class="sxs-lookup"><span data-stu-id="06493-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="06493-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="06493-116">This attribute is optional.</span></span> <span data-ttu-id="06493-117">使用此属性可确保使用的是正确的文件夹版本。</span><span class="sxs-lookup"><span data-stu-id="06493-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06493-118">子元素</span><span class="sxs-lookup"><span data-stu-id="06493-118">Child elements</span></span>

<span data-ttu-id="06493-119">无。</span><span class="sxs-lookup"><span data-stu-id="06493-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06493-120">父元素</span><span class="sxs-lookup"><span data-stu-id="06493-120">Parent elements</span></span>

|<span data-ttu-id="06493-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="06493-121">**Element**</span></span>|<span data-ttu-id="06493-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="06493-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06493-123">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="06493-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="06493-124">代表邮箱中的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="06493-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="06493-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="06493-126">表示邮箱中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="06493-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-127">联系人</span><span class="sxs-lookup"><span data-stu-id="06493-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="06493-128">表示邮箱中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="06493-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-129">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="06493-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="06493-130">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="06493-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="06493-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="06493-132">表示在其中复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="06493-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="06493-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="06493-134">代表在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="06493-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="06493-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="06493-136">代表在其中删除项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="06493-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="06493-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="06493-138">表示邮箱中的专用通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="06493-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-139">Folder</span><span class="sxs-lookup"><span data-stu-id="06493-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="06493-140">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="06493-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-141">项</span><span class="sxs-lookup"><span data-stu-id="06493-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="06493-142">表示通用 Exchange 项。</span><span class="sxs-lookup"><span data-stu-id="06493-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="06493-143">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="06493-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="06493-144">代表要上传到邮箱中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="06493-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="06493-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="06493-146">表示邮箱中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="06493-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="06493-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="06493-148">表示邮箱中的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="06493-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="06493-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="06493-150">表示邮箱中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="06493-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="06493-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="06493-152">表示邮箱中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="06493-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-153">邮件</span><span class="sxs-lookup"><span data-stu-id="06493-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="06493-154">表示邮箱中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="06493-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="06493-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="06493-156">表示在其中修改项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="06493-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="06493-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="06493-158">代表将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="06493-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="06493-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="06493-160">代表由邮箱中的新邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="06493-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="06493-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="06493-162">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="06493-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="06493-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="06493-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="06493-164">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="06493-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="06493-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="06493-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="06493-166">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="06493-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="06493-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="06493-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="06493-168">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="06493-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06493-169">Task</span><span class="sxs-lookup"><span data-stu-id="06493-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="06493-170">表示邮箱中的任务项。</span><span class="sxs-lookup"><span data-stu-id="06493-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="06493-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="06493-172">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="06493-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06493-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="06493-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="06493-174">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="06493-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="06493-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="06493-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="06493-176">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="06493-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="06493-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="06493-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="06493-178">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="06493-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="06493-179">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="06493-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="06493-180">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="06493-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="06493-181">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="06493-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="06493-182">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="06493-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06493-183">说明</span><span class="sxs-lookup"><span data-stu-id="06493-183">Remarks</span></span>

<span data-ttu-id="06493-184">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="06493-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06493-185">元素信息</span><span class="sxs-lookup"><span data-stu-id="06493-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06493-186">命名空间</span><span class="sxs-lookup"><span data-stu-id="06493-186">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06493-187">架构名称</span><span class="sxs-lookup"><span data-stu-id="06493-187">Schema Name</span></span>  <br/> |<span data-ttu-id="06493-188">类型架构</span><span class="sxs-lookup"><span data-stu-id="06493-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="06493-189">验证文件</span><span class="sxs-lookup"><span data-stu-id="06493-189">Validation File</span></span>  <br/> |<span data-ttu-id="06493-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="06493-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06493-191">可以为空</span><span class="sxs-lookup"><span data-stu-id="06493-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="06493-192">False</span><span class="sxs-lookup"><span data-stu-id="06493-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06493-193">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06493-193">See also</span></span>

- [<span data-ttu-id="06493-194">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="06493-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

