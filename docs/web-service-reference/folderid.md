---
title: 文件夹 Id
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: 文件夹 Id 元素包含标识符和更改密钥的文件夹。
ms.openlocfilehash: 5764a164d5af183b8f313955ace5274dc6023a6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754393"
---
# <a name="folderid"></a><span data-ttu-id="4431c-103">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="4431c-103">FolderId</span></span>

<span data-ttu-id="4431c-104">**文件夹 Id**元素包含标识符和更改密钥的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-104">The **FolderId** element contains the identifier and change key of a folder.</span></span> 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="4431c-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="4431c-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4431c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4431c-106">Attributes and elements</span></span>

<span data-ttu-id="4431c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4431c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4431c-108">属性</span><span class="sxs-lookup"><span data-stu-id="4431c-108">Attributes</span></span>

|<span data-ttu-id="4431c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="4431c-109">**Attribute**</span></span>|<span data-ttu-id="4431c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="4431c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4431c-111">Id</span><span class="sxs-lookup"><span data-stu-id="4431c-111">Id</span></span>  <br/> |<span data-ttu-id="4431c-112">包含一个字符串，标识 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="4431c-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="4431c-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="4431c-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="4431c-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="4431c-115">包含一个字符串，标识的文件夹的 Id 属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="4431c-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="4431c-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="4431c-116">This attribute is optional.</span></span> <span data-ttu-id="4431c-117">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="4431c-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4431c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="4431c-118">Child elements</span></span>

<span data-ttu-id="4431c-119">无。</span><span class="sxs-lookup"><span data-stu-id="4431c-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4431c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="4431c-120">Parent elements</span></span>

|<span data-ttu-id="4431c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="4431c-121">**Element**</span></span>|<span data-ttu-id="4431c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="4431c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4431c-123">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="4431c-123">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="4431c-124">指示使用文件夹的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-124">Indicates the folder that is targeted for actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="4431c-125">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="4431c-125">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="4431c-126">表示复制的项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="4431c-126">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="4431c-127">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="4431c-127">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="4431c-128">指示副本的目标文件夹，并移动操作。</span><span class="sxs-lookup"><span data-stu-id="4431c-128">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="4431c-129">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="4431c-129">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="4431c-130">标识在其中创建新的文件夹或项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-130">Identifies the folder where a new folder or item is created.</span></span>  <br/><br/>  <span data-ttu-id="4431c-131">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="4431c-131">The following are the XPath expressions to this element:</span></span><br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="4431c-132">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="4431c-132">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="4431c-133">代表将用于确定搜索文件夹的内容的文件夹的集合。</span><span class="sxs-lookup"><span data-stu-id="4431c-133">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="4431c-134">删除 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="4431c-134">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="4431c-135">标识为在本地客户端库删除单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-135">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="4431c-136">Folder</span><span class="sxs-lookup"><span data-stu-id="4431c-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="4431c-137">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-137">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4431c-138">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-138">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="4431c-139">表示邮箱中的日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-139">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4431c-140">FolderChange</span><span class="sxs-lookup"><span data-stu-id="4431c-140">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="4431c-141">表示要在单个文件夹上进行的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="4431c-141">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="4431c-142">下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange`</span><span class="sxs-lookup"><span data-stu-id="4431c-142">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange`</span></span> <br/> |
|[<span data-ttu-id="4431c-143">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-143">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="4431c-144">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-144">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4431c-145">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-145">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="4431c-146">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-146">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4431c-147">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-147">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="4431c-148">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-148">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4431c-149">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="4431c-149">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="4431c-150">表示复制或移动项目或文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-150">Represents the destination folder for a copied or moved item or folder.</span></span> <br/> <br/>  <span data-ttu-id="4431c-151">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="4431c-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="4431c-152">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="4431c-152">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="4431c-153">标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-153">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/><br/>  <span data-ttu-id="4431c-154">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="4431c-154">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="4431c-155">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="4431c-155">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="4431c-156">代表包含要同步的项的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4431c-156">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="4431c-157">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4431c-157">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="4431c-158">代表用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="4431c-158">Represents the name of a user configuration object.</span></span> <span data-ttu-id="4431c-159">用户配置对象名称为用户配置对象的标识符。</span><span class="sxs-lookup"><span data-stu-id="4431c-159">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="4431c-160">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-160">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="4431c-161">标识的文件夹的电子邮件项目将被复制到的 ID。</span><span class="sxs-lookup"><span data-stu-id="4431c-161">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="4431c-162">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="4431c-162">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="4431c-163">标识的文件夹的电子邮件项目将移动到的 ID。</span><span class="sxs-lookup"><span data-stu-id="4431c-163">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4431c-164">文本值</span><span class="sxs-lookup"><span data-stu-id="4431c-164">Text value</span></span>

<span data-ttu-id="4431c-165">无。</span><span class="sxs-lookup"><span data-stu-id="4431c-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4431c-166">注解</span><span class="sxs-lookup"><span data-stu-id="4431c-166">Remarks</span></span>

<span data-ttu-id="4431c-167">所有**文件夹 Id**元素是**FolderIdType**类型。</span><span class="sxs-lookup"><span data-stu-id="4431c-167">All **FolderId** elements are of the **FolderIdType** type.</span></span> <span data-ttu-id="4431c-168">**文件夹 Id**元素中除其类型扩展**BaseFolderType**元素中每种情况下都需要或其中的**文件夹 Id**元素是选择的一部分。</span><span class="sxs-lookup"><span data-stu-id="4431c-168">The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice.</span></span> <span data-ttu-id="4431c-169">查看架构的详细信息。</span><span class="sxs-lookup"><span data-stu-id="4431c-169">Review the schema for more information.</span></span> 
  
<span data-ttu-id="4431c-170">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4431c-170">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4431c-171">元素信息</span><span class="sxs-lookup"><span data-stu-id="4431c-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4431c-172">命名空间</span><span class="sxs-lookup"><span data-stu-id="4431c-172">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4431c-173">架构名称</span><span class="sxs-lookup"><span data-stu-id="4431c-173">Schema Name</span></span>  <br/> |<span data-ttu-id="4431c-174">类型架构</span><span class="sxs-lookup"><span data-stu-id="4431c-174">Types schema</span></span>  <br/> |
|<span data-ttu-id="4431c-175">验证文件</span><span class="sxs-lookup"><span data-stu-id="4431c-175">Validation File</span></span>  <br/> |<span data-ttu-id="4431c-176">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4431c-176">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4431c-177">可以为空</span><span class="sxs-lookup"><span data-stu-id="4431c-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="4431c-178">False</span><span class="sxs-lookup"><span data-stu-id="4431c-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4431c-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4431c-179">See also</span></span>

- [<span data-ttu-id="4431c-180">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4431c-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4431c-181">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="4431c-181">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

