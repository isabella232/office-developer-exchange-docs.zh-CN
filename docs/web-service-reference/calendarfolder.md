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
ms.openlocfilehash: 7dc90706eb45eb4617a68b9fdcf37669921af966
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753409"
---
# <a name="calendarfolder"></a><span data-ttu-id="da9e3-103">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="da9e3-103">CalendarFolder</span></span>

<span data-ttu-id="da9e3-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CalendarFolder**元素表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="da9e3-104">The **CalendarFolder** element represents a folder that primarily contains calendar items.</span></span> 
  
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

 <span data-ttu-id="da9e3-105">**CalendarFolderType**</span><span class="sxs-lookup"><span data-stu-id="da9e3-105">**CalendarFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da9e3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da9e3-106">Attributes and elements</span></span>

<span data-ttu-id="da9e3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da9e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da9e3-108">属性</span><span class="sxs-lookup"><span data-stu-id="da9e3-108">Attributes</span></span>

<span data-ttu-id="da9e3-109">无。</span><span class="sxs-lookup"><span data-stu-id="da9e3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da9e3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="da9e3-110">Child elements</span></span>

|<span data-ttu-id="da9e3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="da9e3-111">**Element**</span></span>|<span data-ttu-id="da9e3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="da9e3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da9e3-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="da9e3-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="da9e3-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="da9e3-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="da9e3-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="da9e3-116">表示包含该文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="da9e3-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="da9e3-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="da9e3-118">表示给定文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="da9e3-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="da9e3-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="da9e3-120">包含文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="da9e3-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="da9e3-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="da9e3-122">表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="da9e3-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="da9e3-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="da9e3-p101">表示文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="da9e3-p101">Represents the number of child folders that are contained within a folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="da9e3-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="da9e3-127">标识文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="da9e3-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="da9e3-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="da9e3-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="da9e3-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-130">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="da9e3-130">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="da9e3-p102">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="da9e3-p102">Contains the client's rights based on the permission settings for the item or folder. This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="da9e3-133">SharingEffectiveRights (CalendarPermissionReadAccessType)</span></span>](sharingeffectiverights-calendarpermissionreadaccesstype.md) <br/> |<span data-ttu-id="da9e3-134">指示用户正在共享的日历数据的权限。</span><span class="sxs-lookup"><span data-stu-id="da9e3-134">Indicates the permissions that the user has for the calendar data that is being shared.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-135">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="da9e3-135">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="da9e3-136">包含日历文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="da9e3-136">Contains all the configured permissions for a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da9e3-137">父元素</span><span class="sxs-lookup"><span data-stu-id="da9e3-137">Parent elements</span></span>

|<span data-ttu-id="da9e3-138">**元素**</span><span class="sxs-lookup"><span data-stu-id="da9e3-138">**Element**</span></span>|<span data-ttu-id="da9e3-139">**说明**</span><span class="sxs-lookup"><span data-stu-id="da9e3-139">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da9e3-140">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="da9e3-140">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="da9e3-141">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="da9e3-141">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="da9e3-142">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="da9e3-142">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="da9e3-143">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="da9e3-143">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-144">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="da9e3-144">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="da9e3-145">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="da9e3-145">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="da9e3-146">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="da9e3-146">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="da9e3-147">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="da9e3-147">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="da9e3-148">Folders</span><span class="sxs-lookup"><span data-stu-id="da9e3-148">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="da9e3-149">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="da9e3-149">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da9e3-150">备注</span><span class="sxs-lookup"><span data-stu-id="da9e3-150">Remarks</span></span>

<span data-ttu-id="da9e3-151">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da9e3-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da9e3-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="da9e3-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da9e3-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="da9e3-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da9e3-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="da9e3-154">Schema Name</span></span>  <br/> |<span data-ttu-id="da9e3-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="da9e3-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="da9e3-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="da9e3-156">Validation File</span></span>  <br/> |<span data-ttu-id="da9e3-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="da9e3-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da9e3-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="da9e3-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="da9e3-159">False</span><span class="sxs-lookup"><span data-stu-id="da9e3-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da9e3-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da9e3-160">See also</span></span>



- [<span data-ttu-id="da9e3-161">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da9e3-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

