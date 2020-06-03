---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: EffectiveRights 元素包含客户端根据项目或文件夹的权限设置的权限。 此元素是只读的。
ms.openlocfilehash: 3055eb73056750508b48ead29136b56e7ce97ee9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459242"
---
# <a name="effectiverights"></a><span data-ttu-id="89ae5-104">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="89ae5-104">EffectiveRights</span></span>

<span data-ttu-id="89ae5-105">**EffectiveRights**元素包含客户端根据项目或文件夹的权限设置的权限。</span><span class="sxs-lookup"><span data-stu-id="89ae5-105">The **EffectiveRights** element contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="89ae5-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="89ae5-106">This element is read-only.</span></span> 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 <span data-ttu-id="89ae5-107">**EffectiveRightsType**</span><span class="sxs-lookup"><span data-stu-id="89ae5-107">**EffectiveRightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89ae5-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="89ae5-108">Attributes and elements</span></span>

<span data-ttu-id="89ae5-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89ae5-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89ae5-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="89ae5-110">Attributes</span></span>

<span data-ttu-id="89ae5-111">无。</span><span class="sxs-lookup"><span data-stu-id="89ae5-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89ae5-112">子元素</span><span class="sxs-lookup"><span data-stu-id="89ae5-112">Child elements</span></span>

|<span data-ttu-id="89ae5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="89ae5-113">**Element**</span></span>|<span data-ttu-id="89ae5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="89ae5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89ae5-115">CreateAssociated</span><span class="sxs-lookup"><span data-stu-id="89ae5-115">CreateAssociated</span></span>](createassociated.md) <br/> |<span data-ttu-id="89ae5-116">指示客户端是否可以创建关联的内容表。</span><span class="sxs-lookup"><span data-stu-id="89ae5-116">Indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="89ae5-117">此属性仅用于 folder 对象。</span><span class="sxs-lookup"><span data-stu-id="89ae5-117">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-118">CreateContents</span><span class="sxs-lookup"><span data-stu-id="89ae5-118">CreateContents</span></span>](createcontents.md) <br/> |<span data-ttu-id="89ae5-119">指示客户端是否可以创建内容表。</span><span class="sxs-lookup"><span data-stu-id="89ae5-119">Indicates whether a client can create a contents table.</span></span> <span data-ttu-id="89ae5-120">此属性仅用于 folder 对象。</span><span class="sxs-lookup"><span data-stu-id="89ae5-120">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-121">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="89ae5-121">CreateHierarchy</span></span>](createhierarchy.md) <br/> |<span data-ttu-id="89ae5-122">指示客户端是否可以创建层次结构表。</span><span class="sxs-lookup"><span data-stu-id="89ae5-122">Indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="89ae5-123">此属性仅用于 folder 对象。</span><span class="sxs-lookup"><span data-stu-id="89ae5-123">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-124">删除</span><span class="sxs-lookup"><span data-stu-id="89ae5-124">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="89ae5-125">指示客户端是否可以删除文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="89ae5-125">Indicates whether a client can delete a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-126">Modify</span><span class="sxs-lookup"><span data-stu-id="89ae5-126">Modify</span></span>](modify.md) <br/> |<span data-ttu-id="89ae5-127">指示客户端是否可以修改文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="89ae5-127">Indicates whether a client can modify a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-128">Read</span><span class="sxs-lookup"><span data-stu-id="89ae5-128">Read</span></span>](read.md) <br/> |<span data-ttu-id="89ae5-129">指示客户端是否可以读取文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="89ae5-129">Indicates whether a client can read a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-130">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="89ae5-130">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="89ae5-131">指示是否可以查看私有项目。</span><span class="sxs-lookup"><span data-stu-id="89ae5-131">Indicates whether a private item can be viewed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89ae5-132">父元素</span><span class="sxs-lookup"><span data-stu-id="89ae5-132">Parent elements</span></span>

|<span data-ttu-id="89ae5-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="89ae5-133">**Element**</span></span>|<span data-ttu-id="89ae5-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="89ae5-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89ae5-135">Folder</span><span class="sxs-lookup"><span data-stu-id="89ae5-135">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="89ae5-136">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="89ae5-136">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-137">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="89ae5-137">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="89ae5-138">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="89ae5-138">Represents a tasks folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-139">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="89ae5-139">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="89ae5-140">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="89ae5-140">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-141">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="89ae5-141">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="89ae5-142">代表邮箱中的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="89ae5-142">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="89ae5-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="89ae5-144">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="89ae5-144">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-145">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="89ae5-145">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="89ae5-146">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="89ae5-146">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-147">Contact</span><span class="sxs-lookup"><span data-stu-id="89ae5-147">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="89ae5-148">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="89ae5-148">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-149">DistributionList</span><span class="sxs-lookup"><span data-stu-id="89ae5-149">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="89ae5-150">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="89ae5-150">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-151">项</span><span class="sxs-lookup"><span data-stu-id="89ae5-151">Item</span></span>](item.md) <br/> |<span data-ttu-id="89ae5-152">表示通用 Exchange 项。</span><span class="sxs-lookup"><span data-stu-id="89ae5-152">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-153">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="89ae5-153">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="89ae5-154">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="89ae5-154">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-155">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="89ae5-155">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="89ae5-156">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="89ae5-156">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-157">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="89ae5-157">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="89ae5-158">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="89ae5-158">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-159">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="89ae5-159">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="89ae5-160">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="89ae5-160">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-161">Message</span><span class="sxs-lookup"><span data-stu-id="89ae5-161">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="89ae5-162">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="89ae5-162">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-163">任务</span><span class="sxs-lookup"><span data-stu-id="89ae5-163">Task</span></span>](task.md) <br/> |<span data-ttu-id="89ae5-164">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="89ae5-164">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="89ae5-165">PostItem</span><span class="sxs-lookup"><span data-stu-id="89ae5-165">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="89ae5-166">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="89ae5-166">Represents a post item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89ae5-167">文本值</span><span class="sxs-lookup"><span data-stu-id="89ae5-167">Text value</span></span>

<span data-ttu-id="89ae5-168">无。</span><span class="sxs-lookup"><span data-stu-id="89ae5-168">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89ae5-169">说明</span><span class="sxs-lookup"><span data-stu-id="89ae5-169">Remarks</span></span>

<span data-ttu-id="89ae5-170">**EffectiveRights**在 GetFolder、GetItem、FindFolder、FindItem、SyncFolderHierarchy 和 SyncFolderItems 响应中受支持。</span><span class="sxs-lookup"><span data-stu-id="89ae5-170">**EffectiveRights** is supported in the GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy, and SyncFolderItems responses.</span></span> <span data-ttu-id="89ae5-171">**EffectiveRights**属性在文件夹和项目的**AllProperties**形状中公开。</span><span class="sxs-lookup"><span data-stu-id="89ae5-171">The **EffectiveRights** property is exposed in the **AllProperties** shape for folders and items.</span></span> 
  
<span data-ttu-id="89ae5-172">此**EffectiveRights**属性提供对**PR_ACCESS MAPI**属性中提供的相同信息的访问权限。</span><span class="sxs-lookup"><span data-stu-id="89ae5-172">This **EffectiveRights** property provides access to the same information that is provided in the **PR_ACCESS MAPI** property.</span></span> 
  
<span data-ttu-id="89ae5-173">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="89ae5-173">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89ae5-174">元素信息</span><span class="sxs-lookup"><span data-stu-id="89ae5-174">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89ae5-175">命名空间</span><span class="sxs-lookup"><span data-stu-id="89ae5-175">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="89ae5-176">架构名称</span><span class="sxs-lookup"><span data-stu-id="89ae5-176">Schema Name</span></span>  <br/> |<span data-ttu-id="89ae5-177">类型架构</span><span class="sxs-lookup"><span data-stu-id="89ae5-177">Types schema</span></span>  <br/> |
|<span data-ttu-id="89ae5-178">验证文件</span><span class="sxs-lookup"><span data-stu-id="89ae5-178">Validation File</span></span>  <br/> |<span data-ttu-id="89ae5-179">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="89ae5-179">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="89ae5-180">可以为空</span><span class="sxs-lookup"><span data-stu-id="89ae5-180">Can be Empty</span></span>  <br/> |<span data-ttu-id="89ae5-181">False</span><span class="sxs-lookup"><span data-stu-id="89ae5-181">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89ae5-182">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89ae5-182">See also</span></span>

- [<span data-ttu-id="89ae5-183">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="89ae5-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="89ae5-184">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="89ae5-184">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

