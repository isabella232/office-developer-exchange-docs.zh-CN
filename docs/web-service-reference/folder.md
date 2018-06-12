---
title: Folder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folder
api_type:
- schema
ms.assetid: 812948d8-c7db-45ce-bb3a-77233a53a974
description: Folder 元素定义要创建、获取、查找、同步或更新的文件夹。
ms.openlocfilehash: ecfea52d2105599372a22b78778ac0d0d066bc60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754390"
---
# <a name="folder"></a><span data-ttu-id="b8d55-103">Folder</span><span class="sxs-lookup"><span data-stu-id="b8d55-103">Folder</span></span>

<span data-ttu-id="b8d55-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Folder** 元素定义要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b8d55-104">The **Folder** element defines a folder to create, get, find, synchronize, or update.</span></span> 
  
```xml
<Folder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</Folder>
```

 <span data-ttu-id="b8d55-105">**FolderType**</span><span class="sxs-lookup"><span data-stu-id="b8d55-105">**FolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8d55-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b8d55-106">Attributes and elements</span></span>

<span data-ttu-id="b8d55-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b8d55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d55-108">属性</span><span class="sxs-lookup"><span data-stu-id="b8d55-108">Attributes</span></span>

<span data-ttu-id="b8d55-109">无。</span><span class="sxs-lookup"><span data-stu-id="b8d55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d55-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b8d55-110">Child elements</span></span>

|<span data-ttu-id="b8d55-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b8d55-111">**Element**</span></span>|<span data-ttu-id="b8d55-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b8d55-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d55-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="b8d55-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="b8d55-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="b8d55-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="b8d55-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="b8d55-116">表示包含该文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="b8d55-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="b8d55-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="b8d55-118">表示给定文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="b8d55-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="b8d55-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b8d55-120">包含文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="b8d55-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="b8d55-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="b8d55-122">表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="b8d55-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="b8d55-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="b8d55-p101">表示文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="b8d55-p101">Represents the number of child folders that are contained within a folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="b8d55-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b8d55-127">标识文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="b8d55-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="b8d55-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="b8d55-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="b8d55-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="b8d55-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="b8d55-131">表示给定文件夹中未读项目的计数。</span><span class="sxs-lookup"><span data-stu-id="b8d55-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="b8d55-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="b8d55-p102">包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b8d55-p102">Contains all the configured permissions for a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="b8d55-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="b8d55-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="b8d55-p103">包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b8d55-p103">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8d55-139">父元素</span><span class="sxs-lookup"><span data-stu-id="b8d55-139">Parent elements</span></span>

|<span data-ttu-id="b8d55-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="b8d55-140">**Element**</span></span>|<span data-ttu-id="b8d55-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="b8d55-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d55-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="b8d55-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="b8d55-143">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="b8d55-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b8d55-144">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b8d55-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="b8d55-145">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="b8d55-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="b8d55-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="b8d55-147">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="b8d55-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="b8d55-148">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="b8d55-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="b8d55-149">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="b8d55-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="b8d55-150">Folders</span><span class="sxs-lookup"><span data-stu-id="b8d55-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b8d55-151">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b8d55-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8d55-152">备注</span><span class="sxs-lookup"><span data-stu-id="b8d55-152">Remarks</span></span>

<span data-ttu-id="b8d55-153">描述此元素的架构位于正在运行 Exchange 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b8d55-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8d55-154">元素信息</span><span class="sxs-lookup"><span data-stu-id="b8d55-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d55-155">命名空间</span><span class="sxs-lookup"><span data-stu-id="b8d55-155">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8d55-156">架构名称</span><span class="sxs-lookup"><span data-stu-id="b8d55-156">Schema Name</span></span>  <br/> |<span data-ttu-id="b8d55-157">类型架构</span><span class="sxs-lookup"><span data-stu-id="b8d55-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8d55-158">验证文件</span><span class="sxs-lookup"><span data-stu-id="b8d55-158">Validation File</span></span>  <br/> |<span data-ttu-id="b8d55-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8d55-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d55-160">可以为空</span><span class="sxs-lookup"><span data-stu-id="b8d55-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="b8d55-161">False</span><span class="sxs-lookup"><span data-stu-id="b8d55-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d55-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b8d55-162">See also</span></span>



[<span data-ttu-id="b8d55-163">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="b8d55-163">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="b8d55-164">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b8d55-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

