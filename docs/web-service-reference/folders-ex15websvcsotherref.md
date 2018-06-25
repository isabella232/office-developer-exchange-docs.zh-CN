---
title: 文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: 文件夹元素包含在文件夹操作中使用的文件夹的数组。
ms.openlocfilehash: e1b9e337f633dbf6fda159c28725d3fb8dcd55a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754396"
---
# <a name="folders"></a><span data-ttu-id="a024e-103">文件夹</span><span class="sxs-lookup"><span data-stu-id="a024e-103">Folders</span></span>

<span data-ttu-id="a024e-104">**文件夹**元素包含在文件夹操作中使用的文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="a024e-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

 <span data-ttu-id="a024e-105">**ArrayOfFoldersType**或**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="a024e-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a024e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a024e-106">Attributes and elements</span></span>

<span data-ttu-id="a024e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a024e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a024e-108">属性</span><span class="sxs-lookup"><span data-stu-id="a024e-108">Attributes</span></span>

<span data-ttu-id="a024e-109">无。</span><span class="sxs-lookup"><span data-stu-id="a024e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a024e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a024e-110">Child elements</span></span>

|<span data-ttu-id="a024e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a024e-111">**Element**</span></span>|<span data-ttu-id="a024e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a024e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a024e-113">Folder</span><span class="sxs-lookup"><span data-stu-id="a024e-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="a024e-114">标识要创建、 获取、 查找、 同步，或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="a024e-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="a024e-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="a024e-116">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="a024e-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="a024e-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="a024e-118">表示邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a024e-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a024e-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a024e-120">表示邮箱中所包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a024e-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="a024e-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="a024e-122">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a024e-123">父元素</span><span class="sxs-lookup"><span data-stu-id="a024e-123">Parent elements</span></span>

|<span data-ttu-id="a024e-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="a024e-124">**Element**</span></span>|<span data-ttu-id="a024e-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="a024e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a024e-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-127">包含状态和的单个结果[CopyFolder 操作](copyfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a024e-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a024e-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="a024e-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="a024e-129">定义一个请求在 Exchange 存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a024e-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-131">包含状态和的单个结果[CreateFolder 操作](createfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a024e-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a024e-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-133">包含状态和的单个结果[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a024e-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a024e-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-135">包含状态和[GetFolder 操作](getfolder-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a024e-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a024e-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-137">包含状态和[MoveFolder 操作](movefolder-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a024e-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a024e-138">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="a024e-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="a024e-139">标识在其中创建新文件夹的文件夹。</span><span class="sxs-lookup"><span data-stu-id="a024e-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="a024e-140">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="a024e-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-141">包含搜索[FindFolder 操作](findfolder-operation.md)过程中的单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="a024e-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a024e-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a024e-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="a024e-143">包含状态和的单个结果[UpdateFolder 操作](updatefolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a024e-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a024e-144">注解</span><span class="sxs-lookup"><span data-stu-id="a024e-144">Remarks</span></span>

<span data-ttu-id="a024e-145">此元素是[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="a024e-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="a024e-146">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a024e-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a024e-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="a024e-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a024e-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="a024e-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a024e-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="a024e-149">Schema Name</span></span>  <br/> |<span data-ttu-id="a024e-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="a024e-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="a024e-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="a024e-151">Validation File</span></span>  <br/> |<span data-ttu-id="a024e-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a024e-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a024e-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="a024e-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="a024e-154">False</span><span class="sxs-lookup"><span data-stu-id="a024e-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a024e-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a024e-155">See also</span></span>



[<span data-ttu-id="a024e-156">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="a024e-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)

