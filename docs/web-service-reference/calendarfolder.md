---
title: CalendarFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarFolder
api_type:
- schema
ms.assetid: 48687a78-e757-4c04-9641-bf4302c6b565
description: CalendarFolder元素表示主要包含日历项目的文件夹。
ms.openlocfilehash: dcd0ab9d7dea1152766997de0618b3dcceed5567
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461490"
---
# <a name="calendarfolder"></a><span data-ttu-id="8f450-103">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="8f450-103">CalendarFolder</span></span>

<span data-ttu-id="8f450-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CalendarFolder**元素表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f450-104">The **CalendarFolder** element represents a folder that primarily contains calendar items.</span></span> 
  
```xml
<CalendarFolder>
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
</CalendarFolder>
```

 <span data-ttu-id="8f450-105">**CalendarFolderType**</span><span class="sxs-lookup"><span data-stu-id="8f450-105">**CalendarFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8f450-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8f450-106">Attributes and elements</span></span>

<span data-ttu-id="8f450-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8f450-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f450-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8f450-108">Attributes</span></span>

<span data-ttu-id="8f450-109">无。</span><span class="sxs-lookup"><span data-stu-id="8f450-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f450-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8f450-110">Child elements</span></span>

|<span data-ttu-id="8f450-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8f450-111">**Element**</span></span>|<span data-ttu-id="8f450-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8f450-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f450-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="8f450-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="8f450-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="8f450-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="8f450-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="8f450-116">表示包含该文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="8f450-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="8f450-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="8f450-118">表示给定文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="8f450-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="8f450-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="8f450-120">包含文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="8f450-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="8f450-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="8f450-122">表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="8f450-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="8f450-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="8f450-p101">表示文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="8f450-p101">Represents the number of child folders that are contained within a folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="8f450-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="8f450-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="8f450-127">标识文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="8f450-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="8f450-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="8f450-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="8f450-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="8f450-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="8f450-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="8f450-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="8f450-p102">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="8f450-p102">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="8f450-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="8f450-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>](sharingeffectiverights-calendarpermissionreadaccesstype.md) <br/> |<span data-ttu-id="8f450-134">指示用户正在共享的日历数据的权限。</span><span class="sxs-lookup"><span data-stu-id="8f450-134">Indicates the permissions that the user has for the calendar data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="8f450-135">PermissionSet （CalendarPermissionSetType）</span><span class="sxs-lookup"><span data-stu-id="8f450-135">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="8f450-136">包含日历文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="8f450-136">Contains all the configured permissions for a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8f450-137">父元素</span><span class="sxs-lookup"><span data-stu-id="8f450-137">Parent elements</span></span>

|<span data-ttu-id="8f450-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="8f450-138">**Element**</span></span>|<span data-ttu-id="8f450-139">**说明**</span><span class="sxs-lookup"><span data-stu-id="8f450-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f450-140">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="8f450-140">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="8f450-141">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="8f450-141">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="8f450-142">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="8f450-142">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="8f450-143">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f450-143">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="8f450-144">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="8f450-144">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="8f450-145">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="8f450-145">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="8f450-146">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="8f450-146">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="8f450-147">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f450-147">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="8f450-148">Folders</span><span class="sxs-lookup"><span data-stu-id="8f450-148">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8f450-149">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f450-149">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f450-150">说明</span><span class="sxs-lookup"><span data-stu-id="8f450-150">Remarks</span></span>

<span data-ttu-id="8f450-151">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8f450-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f450-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="8f450-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f450-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="8f450-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8f450-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="8f450-154">Schema Name</span></span>  <br/> |<span data-ttu-id="8f450-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="8f450-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="8f450-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="8f450-156">Validation File</span></span>  <br/> |<span data-ttu-id="8f450-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8f450-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8f450-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="8f450-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="8f450-159">False</span><span class="sxs-lookup"><span data-stu-id="8f450-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f450-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f450-160">See also</span></span>



- [<span data-ttu-id="8f450-161">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8f450-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

