---
title: FolderId
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
description: FolderId 元素包含文件夹的标识符和更改键。
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461385"
---
# <a name="folderid"></a><span data-ttu-id="7753e-103">FolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-103">FolderId</span></span>

<span data-ttu-id="7753e-104">**FolderId**元素包含文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="7753e-104">The **FolderId** element contains the identifier and change key of a folder.</span></span> 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="7753e-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="7753e-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7753e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7753e-106">Attributes and elements</span></span>

<span data-ttu-id="7753e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7753e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7753e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7753e-108">Attributes</span></span>

|<span data-ttu-id="7753e-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7753e-109">**Attribute**</span></span>|<span data-ttu-id="7753e-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7753e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7753e-111">Id</span><span class="sxs-lookup"><span data-stu-id="7753e-111">Id</span></span>  <br/> |<span data-ttu-id="7753e-112">包含标识 Exchange 存储中的文件夹的字符串。</span><span class="sxs-lookup"><span data-stu-id="7753e-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="7753e-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7753e-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="7753e-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="7753e-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="7753e-115">包含标识由 Id 属性标识的文件夹版本的字符串。</span><span class="sxs-lookup"><span data-stu-id="7753e-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="7753e-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="7753e-116">This attribute is optional.</span></span> <span data-ttu-id="7753e-117">使用此属性可确保使用的是正确的文件夹版本。</span><span class="sxs-lookup"><span data-stu-id="7753e-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7753e-118">子元素</span><span class="sxs-lookup"><span data-stu-id="7753e-118">Child elements</span></span>

<span data-ttu-id="7753e-119">无。</span><span class="sxs-lookup"><span data-stu-id="7753e-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7753e-120">父元素</span><span class="sxs-lookup"><span data-stu-id="7753e-120">Parent elements</span></span>

|<span data-ttu-id="7753e-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="7753e-121">**Element**</span></span>|<span data-ttu-id="7753e-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="7753e-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7753e-123">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-123">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="7753e-124">指示针对使用文件夹的操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-124">Indicates the folder that is targeted for actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="7753e-125">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="7753e-125">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="7753e-126">表示在其中复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7753e-126">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="7753e-127">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-127">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="7753e-128">指示复制和移动操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-128">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="7753e-129">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="7753e-129">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="7753e-130">标识在其中创建新文件夹或项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-130">Identifies the folder where a new folder or item is created.</span></span>  <br/><br/>  <span data-ttu-id="7753e-131">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7753e-131">The following are the XPath expressions to this element:</span></span><br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="7753e-132">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="7753e-132">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="7753e-133">表示将挖掘的文件夹集合，以确定搜索文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="7753e-133">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="7753e-134">Delete （FolderSync）</span><span class="sxs-lookup"><span data-stu-id="7753e-134">Delete (FolderSync)</span></span>](delete-foldersync.md) <br/> |<span data-ttu-id="7753e-135">标识要在本地客户端存储中删除的单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-135">Identifies a single folder to delete in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="7753e-136">Folder</span><span class="sxs-lookup"><span data-stu-id="7753e-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="7753e-137">表示邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-137">Represents a folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7753e-138">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-138">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="7753e-139">代表邮箱中的 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-139">Represents a calendar folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7753e-140">FolderChange</span><span class="sxs-lookup"><span data-stu-id="7753e-140">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="7753e-141">表示要在单个文件夹上进行的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="7753e-141">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <span data-ttu-id="7753e-142">下面是此元素的 XPath 表达式:  `/UpdateFolder/FolderChanges/FolderChange`</span><span class="sxs-lookup"><span data-stu-id="7753e-142">The following is the XPath expression to this element:  `/UpdateFolder/FolderChanges/FolderChange`</span></span> <br/> |
|[<span data-ttu-id="7753e-143">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-143">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="7753e-144">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-144">Represents a contact folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7753e-145">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-145">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="7753e-146">表示邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-146">Represents a search folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7753e-147">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-147">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="7753e-148">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-148">Represents a task folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="7753e-149">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-149">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="7753e-150">代表复制或移动的项或文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-150">Represents the destination folder for a copied or moved item or folder.</span></span> <br/> <br/>  <span data-ttu-id="7753e-151">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7753e-151">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="7753e-152">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-152">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="7753e-153">标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-153">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/><br/>  <span data-ttu-id="7753e-154">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7753e-154">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="7753e-155">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="7753e-155">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="7753e-156">表示包含要同步的项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7753e-156">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="7753e-157">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7753e-157">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="7753e-158">表示用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="7753e-158">Represents the name of a user configuration object.</span></span> <span data-ttu-id="7753e-159">"用户配置" 对象名称是 "用户配置" 对象的标识符。</span><span class="sxs-lookup"><span data-stu-id="7753e-159">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="7753e-160">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-160">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="7753e-161">标识电子邮件项目将复制到的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="7753e-161">Identifies the ID of the folder that e-mail items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="7753e-162">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="7753e-162">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="7753e-163">标识电子邮件项目将移动到的文件夹的 ID。</span><span class="sxs-lookup"><span data-stu-id="7753e-163">Identifies the ID of the folder that e-mail items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7753e-164">文本值</span><span class="sxs-lookup"><span data-stu-id="7753e-164">Text value</span></span>

<span data-ttu-id="7753e-165">无。</span><span class="sxs-lookup"><span data-stu-id="7753e-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7753e-166">说明</span><span class="sxs-lookup"><span data-stu-id="7753e-166">Remarks</span></span>

<span data-ttu-id="7753e-167">所有**FolderId**元素均属于**FolderIdType**类型。</span><span class="sxs-lookup"><span data-stu-id="7753e-167">All **FolderId** elements are of the **FolderIdType** type.</span></span> <span data-ttu-id="7753e-168">除了其类型扩展了**BaseFolderType**的元素或**FolderId**元素是选项的一部分的元素中， **FolderId**元素都是必需的。</span><span class="sxs-lookup"><span data-stu-id="7753e-168">The **FolderId** element is required in every case except in elements whose type extends the **BaseFolderType** or where the **FolderId** element is a part of a choice.</span></span> <span data-ttu-id="7753e-169">有关详细信息，请查看架构。</span><span class="sxs-lookup"><span data-stu-id="7753e-169">Review the schema for more information.</span></span> 
  
<span data-ttu-id="7753e-170">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7753e-170">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7753e-171">元素信息</span><span class="sxs-lookup"><span data-stu-id="7753e-171">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7753e-172">命名空间</span><span class="sxs-lookup"><span data-stu-id="7753e-172">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7753e-173">架构名称</span><span class="sxs-lookup"><span data-stu-id="7753e-173">Schema Name</span></span>  <br/> |<span data-ttu-id="7753e-174">类型架构</span><span class="sxs-lookup"><span data-stu-id="7753e-174">Types schema</span></span>  <br/> |
|<span data-ttu-id="7753e-175">验证文件</span><span class="sxs-lookup"><span data-stu-id="7753e-175">Validation File</span></span>  <br/> |<span data-ttu-id="7753e-176">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7753e-176">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7753e-177">可以为空</span><span class="sxs-lookup"><span data-stu-id="7753e-177">Can be Empty</span></span>  <br/> |<span data-ttu-id="7753e-178">False</span><span class="sxs-lookup"><span data-stu-id="7753e-178">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7753e-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7753e-179">See also</span></span>

- [<span data-ttu-id="7753e-180">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7753e-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7753e-181">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="7753e-181">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

