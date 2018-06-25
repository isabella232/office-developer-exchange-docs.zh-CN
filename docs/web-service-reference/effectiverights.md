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
description: EffectiveRights 元素包含基于的项目或文件夹的权限设置的客户端的权限。 此元素是只读的。
ms.openlocfilehash: 610d9e214a8de648ece667799bb5e67dfcc358f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754030"
---
# <a name="effectiverights"></a><span data-ttu-id="0906b-104">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="0906b-104">EffectiveRights</span></span>

<span data-ttu-id="0906b-105">**EffectiveRights**元素包含基于的项目或文件夹的权限设置的客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="0906b-105">The **EffectiveRights** element contains the client's rights based on the permission settings for the item or folder.</span></span> <span data-ttu-id="0906b-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="0906b-106">This element is read-only.</span></span> 
  
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

 <span data-ttu-id="0906b-107">**EffectiveRightsType**</span><span class="sxs-lookup"><span data-stu-id="0906b-107">**EffectiveRightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0906b-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0906b-108">Attributes and elements</span></span>

<span data-ttu-id="0906b-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0906b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0906b-110">属性</span><span class="sxs-lookup"><span data-stu-id="0906b-110">Attributes</span></span>

<span data-ttu-id="0906b-111">无。</span><span class="sxs-lookup"><span data-stu-id="0906b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0906b-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0906b-112">Child elements</span></span>

|<span data-ttu-id="0906b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0906b-113">**Element**</span></span>|<span data-ttu-id="0906b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0906b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0906b-115">CreateAssociated</span><span class="sxs-lookup"><span data-stu-id="0906b-115">CreateAssociated</span></span>](createassociated.md) <br/> |<span data-ttu-id="0906b-116">指示客户端是否可以创建关联的内容表。</span><span class="sxs-lookup"><span data-stu-id="0906b-116">Indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="0906b-117">此属性仅可用于文件夹对象。</span><span class="sxs-lookup"><span data-stu-id="0906b-117">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0906b-118">CreateContents</span><span class="sxs-lookup"><span data-stu-id="0906b-118">CreateContents</span></span>](createcontents.md) <br/> |<span data-ttu-id="0906b-119">指示客户端是否可以创建内容表。</span><span class="sxs-lookup"><span data-stu-id="0906b-119">Indicates whether a client can create a contents table.</span></span> <span data-ttu-id="0906b-120">此属性仅可用于文件夹对象。</span><span class="sxs-lookup"><span data-stu-id="0906b-120">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0906b-121">CreateHierarchy</span><span class="sxs-lookup"><span data-stu-id="0906b-121">CreateHierarchy</span></span>](createhierarchy.md) <br/> |<span data-ttu-id="0906b-122">指示客户端是否可以创建层次结构表。</span><span class="sxs-lookup"><span data-stu-id="0906b-122">Indicates whether a client can create a hierarchy table.</span></span> <span data-ttu-id="0906b-123">此属性仅可用于文件夹对象。</span><span class="sxs-lookup"><span data-stu-id="0906b-123">This property is only used on folder objects.</span></span>  <br/> |
|[<span data-ttu-id="0906b-124">删除</span><span class="sxs-lookup"><span data-stu-id="0906b-124">Delete</span></span>](delete.md) <br/> |<span data-ttu-id="0906b-125">指示客户端是否可以删除文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-125">Indicates whether a client can delete a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-126">修改</span><span class="sxs-lookup"><span data-stu-id="0906b-126">Modify</span></span>](modify.md) <br/> |<span data-ttu-id="0906b-127">指示客户端是否可以修改文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-127">Indicates whether a client can modify a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-128">Read</span><span class="sxs-lookup"><span data-stu-id="0906b-128">Read</span></span>](read.md) <br/> |<span data-ttu-id="0906b-129">指示客户端是否可以读取文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-129">Indicates whether a client can read a folder or item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-130">ViewPrivateItems</span><span class="sxs-lookup"><span data-stu-id="0906b-130">ViewPrivateItems</span></span>](viewprivateitems.md) <br/> |<span data-ttu-id="0906b-131">指示是否可以查看的私有项。</span><span class="sxs-lookup"><span data-stu-id="0906b-131">Indicates whether a private item can be viewed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0906b-132">父元素</span><span class="sxs-lookup"><span data-stu-id="0906b-132">Parent elements</span></span>

|<span data-ttu-id="0906b-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="0906b-133">**Element**</span></span>|<span data-ttu-id="0906b-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="0906b-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0906b-135">Folder</span><span class="sxs-lookup"><span data-stu-id="0906b-135">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="0906b-136">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="0906b-136">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0906b-137">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="0906b-137">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="0906b-138">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="0906b-138">Represents a tasks folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0906b-139">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="0906b-139">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="0906b-140">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="0906b-140">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0906b-141">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="0906b-141">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="0906b-142">表示邮箱中的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="0906b-142">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0906b-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="0906b-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="0906b-144">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="0906b-144">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0906b-145">日历项目</span><span class="sxs-lookup"><span data-stu-id="0906b-145">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0906b-146">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="0906b-146">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-147">联系人</span><span class="sxs-lookup"><span data-stu-id="0906b-147">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="0906b-148">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-148">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-149">DistributionList</span><span class="sxs-lookup"><span data-stu-id="0906b-149">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="0906b-150">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="0906b-150">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="0906b-151">Item</span><span class="sxs-lookup"><span data-stu-id="0906b-151">Item</span></span>](item.md) <br/> |<span data-ttu-id="0906b-152">表示的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-152">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="0906b-153">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="0906b-153">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="0906b-154">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="0906b-154">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0906b-155">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="0906b-155">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="0906b-156">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="0906b-156">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0906b-157">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0906b-157">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0906b-158">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="0906b-158">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0906b-159">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="0906b-159">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="0906b-160">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="0906b-160">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0906b-161">Message</span><span class="sxs-lookup"><span data-stu-id="0906b-161">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0906b-162">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="0906b-162">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0906b-163">任务</span><span class="sxs-lookup"><span data-stu-id="0906b-163">Task</span></span>](task.md) <br/> |<span data-ttu-id="0906b-164">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="0906b-164">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0906b-165">PostItem</span><span class="sxs-lookup"><span data-stu-id="0906b-165">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="0906b-166">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="0906b-166">Represents a post item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0906b-167">文本值</span><span class="sxs-lookup"><span data-stu-id="0906b-167">Text value</span></span>

<span data-ttu-id="0906b-168">无。</span><span class="sxs-lookup"><span data-stu-id="0906b-168">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0906b-169">注解</span><span class="sxs-lookup"><span data-stu-id="0906b-169">Remarks</span></span>

<span data-ttu-id="0906b-170">GetFolder、 GetItem、 FindFolder、 FindItem、 SyncFolderHierarchy 和 SyncFolderItems 响应中支持**EffectiveRights** 。</span><span class="sxs-lookup"><span data-stu-id="0906b-170">**EffectiveRights** is supported in the GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy, and SyncFolderItems responses.</span></span> <span data-ttu-id="0906b-171">文件夹和项目的**AllProperties**形状中的公开**EffectiveRights**属性。</span><span class="sxs-lookup"><span data-stu-id="0906b-171">The **EffectiveRights** property is exposed in the **AllProperties** shape for folders and items.</span></span> 
  
<span data-ttu-id="0906b-172">此**EffectiveRights**属性提供对相同**PR_ACCESS MAPI**属性中提供的信息的访问。</span><span class="sxs-lookup"><span data-stu-id="0906b-172">This **EffectiveRights** property provides access to the same information that is provided in the **PR_ACCESS MAPI** property.</span></span> 
  
<span data-ttu-id="0906b-173">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0906b-173">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0906b-174">元素信息</span><span class="sxs-lookup"><span data-stu-id="0906b-174">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0906b-175">命名空间</span><span class="sxs-lookup"><span data-stu-id="0906b-175">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0906b-176">架构名称</span><span class="sxs-lookup"><span data-stu-id="0906b-176">Schema Name</span></span>  <br/> |<span data-ttu-id="0906b-177">类型架构</span><span class="sxs-lookup"><span data-stu-id="0906b-177">Types schema</span></span>  <br/> |
|<span data-ttu-id="0906b-178">验证文件</span><span class="sxs-lookup"><span data-stu-id="0906b-178">Validation File</span></span>  <br/> |<span data-ttu-id="0906b-179">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0906b-179">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0906b-180">可以为空</span><span class="sxs-lookup"><span data-stu-id="0906b-180">Can be Empty</span></span>  <br/> |<span data-ttu-id="0906b-181">False</span><span class="sxs-lookup"><span data-stu-id="0906b-181">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0906b-182">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0906b-182">See also</span></span>

- [<span data-ttu-id="0906b-183">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0906b-183">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0906b-184">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0906b-184">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

