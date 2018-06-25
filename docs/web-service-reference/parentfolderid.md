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
description: ParentFolderId 元素均表示包含的项目或文件夹的父文件夹的标识符。
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826687"
---
# <a name="parentfolderid"></a><span data-ttu-id="24472-103">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="24472-103">ParentFolderId</span></span>

<span data-ttu-id="24472-104">**ParentFolderId**元素均表示包含的项目或文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="24472-104">The **ParentFolderId** element represents the identifier of the parent folder that contains the item or folder.</span></span> 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

<span data-ttu-id="24472-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="24472-105">**FolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="24472-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="24472-106">Attributes and elements</span></span>

<span data-ttu-id="24472-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24472-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24472-108">属性</span><span class="sxs-lookup"><span data-stu-id="24472-108">Attributes</span></span>

|<span data-ttu-id="24472-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="24472-109">**Attribute**</span></span>|<span data-ttu-id="24472-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="24472-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24472-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="24472-111">**Id**</span></span> <br/> |<span data-ttu-id="24472-112">包含一个字符串，标识 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="24472-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="24472-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="24472-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="24472-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="24472-115">包含一个字符串，标识的文件夹的**Id**属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="24472-115">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="24472-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="24472-116">This attribute is optional.</span></span> <span data-ttu-id="24472-117">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="24472-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="24472-118">子元素</span><span class="sxs-lookup"><span data-stu-id="24472-118">Child elements</span></span>

<span data-ttu-id="24472-119">无。</span><span class="sxs-lookup"><span data-stu-id="24472-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24472-120">父元素</span><span class="sxs-lookup"><span data-stu-id="24472-120">Parent elements</span></span>

|<span data-ttu-id="24472-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="24472-121">**Element**</span></span>|<span data-ttu-id="24472-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="24472-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24472-123">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="24472-123">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="24472-124">表示邮箱中的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-124">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-125">日历项目</span><span class="sxs-lookup"><span data-stu-id="24472-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="24472-126">表示邮箱中的日历项目。</span><span class="sxs-lookup"><span data-stu-id="24472-126">Represents a calendar item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-127">Contact</span><span class="sxs-lookup"><span data-stu-id="24472-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="24472-128">表示邮箱中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="24472-128">Represents a contact item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-129">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="24472-129">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="24472-130">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-130">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-131">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="24472-131">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="24472-132">表示复制的项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-132">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="24472-133">CreatedEvent</span><span class="sxs-lookup"><span data-stu-id="24472-133">CreatedEvent</span></span>](createdevent.md) <br/> |<span data-ttu-id="24472-134">表示在其中创建项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-134">Represents an event in which an item or folder is created.</span></span>  <br/> |
|[<span data-ttu-id="24472-135">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="24472-135">DeletedEvent</span></span>](deletedevent.md) <br/> |<span data-ttu-id="24472-136">表示删除项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-136">Represents an event in which an item or folder is deleted.</span></span>  <br/> |
|[<span data-ttu-id="24472-137">DistributionList</span><span class="sxs-lookup"><span data-stu-id="24472-137">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="24472-138">表示邮箱中的私人通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="24472-138">Represents a private distribution list in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-139">Folder</span><span class="sxs-lookup"><span data-stu-id="24472-139">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="24472-140">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-140">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-141">Item</span><span class="sxs-lookup"><span data-stu-id="24472-141">Item</span></span>](item.md) <br/> |<span data-ttu-id="24472-142">表示的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="24472-142">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="24472-143">项目 (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="24472-143">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="24472-144">代表单个项目上载到邮箱。</span><span class="sxs-lookup"><span data-stu-id="24472-144">Represents a single item to upload into a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-145">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="24472-145">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="24472-146">表示邮箱中的取消会议。</span><span class="sxs-lookup"><span data-stu-id="24472-146">Represents a meeting cancellation in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-147">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="24472-147">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="24472-148">表示邮箱中的会议消息。</span><span class="sxs-lookup"><span data-stu-id="24472-148">Represents a meeting message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-149">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="24472-149">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="24472-150">表示邮箱中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="24472-150">Represents a meeting request in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-151">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="24472-151">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="24472-152">代表邮箱中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="24472-152">Represents a meeting response in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-153">Message</span><span class="sxs-lookup"><span data-stu-id="24472-153">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="24472-154">表示邮箱中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="24472-154">Represents an e-mail message in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-155">ModifiedEvent</span><span class="sxs-lookup"><span data-stu-id="24472-155">ModifiedEvent</span></span>](modifiedevent.md) <br/> |<span data-ttu-id="24472-156">表示在其中修改项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-156">Represents an event in which an item or folder is modified.</span></span>  <br/> |
|[<span data-ttu-id="24472-157">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="24472-157">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="24472-158">表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-158">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
|[<span data-ttu-id="24472-159">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="24472-159">NewMailEvent</span></span>](newmailevent.md) <br/> |<span data-ttu-id="24472-160">表示由邮箱中的一个新的邮件项目触发的事件。</span><span class="sxs-lookup"><span data-stu-id="24472-160">Represents an event that is triggered by a new mail item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-161">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="24472-161">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="24472-162">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="24472-162">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="24472-163">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="24472-163">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="24472-164">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="24472-164">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="24472-165">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="24472-165">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="24472-166">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="24472-166">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="24472-167">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="24472-167">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="24472-168">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="24472-168">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="24472-169">任务</span><span class="sxs-lookup"><span data-stu-id="24472-169">Task</span></span>](task.md) <br/> |<span data-ttu-id="24472-170">表示邮箱中的任务项。</span><span class="sxs-lookup"><span data-stu-id="24472-170">Represents a task item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-171">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="24472-171">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="24472-172">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="24472-172">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="24472-173">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="24472-173">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="24472-174">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="24472-174">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="24472-175">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="24472-175">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="24472-176">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="24472-176">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="24472-177">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="24472-177">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="24472-178">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="24472-178">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="24472-179">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="24472-179">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="24472-180">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-180">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="24472-181">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="24472-181">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="24472-182">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="24472-182">Represents a search folder in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24472-183">备注</span><span class="sxs-lookup"><span data-stu-id="24472-183">Remarks</span></span>

<span data-ttu-id="24472-184">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="24472-184">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24472-185">元素信息</span><span class="sxs-lookup"><span data-stu-id="24472-185">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24472-186">命名空间</span><span class="sxs-lookup"><span data-stu-id="24472-186">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24472-187">架构名称</span><span class="sxs-lookup"><span data-stu-id="24472-187">Schema Name</span></span>  <br/> |<span data-ttu-id="24472-188">类型架构</span><span class="sxs-lookup"><span data-stu-id="24472-188">Types schema</span></span>  <br/> |
|<span data-ttu-id="24472-189">验证文件</span><span class="sxs-lookup"><span data-stu-id="24472-189">Validation File</span></span>  <br/> |<span data-ttu-id="24472-190">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24472-190">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24472-191">可以为空</span><span class="sxs-lookup"><span data-stu-id="24472-191">Can be Empty</span></span>  <br/> |<span data-ttu-id="24472-192">False</span><span class="sxs-lookup"><span data-stu-id="24472-192">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24472-193">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24472-193">See also</span></span>

- [<span data-ttu-id="24472-194">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="24472-194">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

