---
title: ContactsFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: ContactsFolder元素表示的邮箱中包含联系人文件夹。
ms.openlocfilehash: 997b4f603198e6d05a011c4ef6bac7fe4dfbfe52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529432"
---
# <a name="contactsfolder"></a><span data-ttu-id="517ac-103">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="517ac-103">ContactsFolder</span></span>

<span data-ttu-id="517ac-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ContactsFolder**元素表示的邮箱中包含联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="517ac-104">The **ContactsFolder** element represents a contacts folder that is contained in a mailbox.</span></span> 
  
```xml
<ContactsFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</ContactsFolder>
```

 <span data-ttu-id="517ac-105">**ContactsFolderType**</span><span class="sxs-lookup"><span data-stu-id="517ac-105">**ContactsFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="517ac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="517ac-106">Attributes and elements</span></span>

<span data-ttu-id="517ac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="517ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="517ac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="517ac-108">Attributes</span></span>

<span data-ttu-id="517ac-109">无。</span><span class="sxs-lookup"><span data-stu-id="517ac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="517ac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="517ac-110">Child elements</span></span>

|<span data-ttu-id="517ac-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="517ac-111">**Element**</span></span>|<span data-ttu-id="517ac-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="517ac-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="517ac-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="517ac-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="517ac-114">包含联系人文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="517ac-114">Contains the identifier and change key of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="517ac-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="517ac-116">表示包含联系人文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="517ac-116">Represents the identifier of the parent folder that contains the contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="517ac-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="517ac-118">表示联系人文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="517ac-118">Represents the folder class for a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="517ac-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="517ac-120">包含联系人文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="517ac-120">Contains the display name of a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="517ac-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="517ac-122">表示联系人文件夹中的项的总计数。</span><span class="sxs-lookup"><span data-stu-id="517ac-122">Represents the total count of items within a contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="517ac-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="517ac-p101">代表联系人文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="517ac-p101">Represents the number of child folders that are contained within a contacts folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="517ac-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="517ac-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="517ac-127">标识联系人文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="517ac-127">Identifies extended properties on contacts folders.</span></span>  <br/> |
|[<span data-ttu-id="517ac-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="517ac-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="517ac-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="517ac-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="517ac-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="517ac-131">包含客户端的权利基础的项或文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="517ac-131">Contains the client's rights based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="517ac-132">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="517ac-132">SharingEffectiveRights (PermissionReadAccessType)</span></span>](sharingeffectiverights-permissionreadaccesstype.md) <br/> |<span data-ttu-id="517ac-133">指示用户必须为要共享的联系人数据的权限。</span><span class="sxs-lookup"><span data-stu-id="517ac-133">Indicates the permissions that the user has for the contact data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="517ac-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="517ac-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="517ac-135">包含文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="517ac-135">Contains all the configured permissions for a folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="517ac-136">父元素</span><span class="sxs-lookup"><span data-stu-id="517ac-136">Parent elements</span></span>

|<span data-ttu-id="517ac-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="517ac-137">**Element**</span></span>|<span data-ttu-id="517ac-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="517ac-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="517ac-139">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="517ac-139">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="517ac-140">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="517ac-140">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="517ac-141">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="517ac-141">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="517ac-142">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="517ac-142">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="517ac-143">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="517ac-143">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="517ac-144">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="517ac-144">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="517ac-145">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="517ac-145">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="517ac-146">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="517ac-146">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="517ac-147">Folders</span><span class="sxs-lookup"><span data-stu-id="517ac-147">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="517ac-148">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="517ac-148">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="517ac-149">文本值</span><span class="sxs-lookup"><span data-stu-id="517ac-149">Text value</span></span>

<span data-ttu-id="517ac-150">无。</span><span class="sxs-lookup"><span data-stu-id="517ac-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="517ac-151">说明</span><span class="sxs-lookup"><span data-stu-id="517ac-151">Remarks</span></span>

<span data-ttu-id="517ac-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="517ac-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="517ac-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="517ac-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="517ac-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="517ac-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="517ac-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="517ac-155">Schema Name</span></span>  <br/> |<span data-ttu-id="517ac-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="517ac-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="517ac-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="517ac-157">Validation File</span></span>  <br/> |<span data-ttu-id="517ac-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="517ac-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="517ac-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="517ac-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="517ac-160">False</span><span class="sxs-lookup"><span data-stu-id="517ac-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="517ac-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="517ac-161">See also</span></span>



- [<span data-ttu-id="517ac-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="517ac-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

