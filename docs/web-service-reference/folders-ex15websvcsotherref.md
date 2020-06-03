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
description: Folders 元素包含在文件夹操作中使用的一组文件夹。
ms.openlocfilehash: b087be0501f04390b80458458e7e7ccc24bf27bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530977"
---
# <a name="folders"></a><span data-ttu-id="2166c-103">Folders</span><span class="sxs-lookup"><span data-stu-id="2166c-103">Folders</span></span>

<span data-ttu-id="2166c-104">**Folders**元素包含在文件夹操作中使用的一组文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-104">The **Folders** element contains an array of folders that are used in folder operations.</span></span> 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

<span data-ttu-id="2166c-105">**ArrayOfFoldersType**或**NonEmptyArrayOfFoldersType**</span><span class="sxs-lookup"><span data-stu-id="2166c-105">**ArrayOfFoldersType** or **NonEmptyArrayOfFoldersType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2166c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2166c-106">Attributes and elements</span></span>

<span data-ttu-id="2166c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2166c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2166c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2166c-108">Attributes</span></span>

<span data-ttu-id="2166c-109">无。</span><span class="sxs-lookup"><span data-stu-id="2166c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2166c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2166c-110">Child elements</span></span>

|<span data-ttu-id="2166c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2166c-111">**Element**</span></span>|<span data-ttu-id="2166c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2166c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2166c-113">Folder</span><span class="sxs-lookup"><span data-stu-id="2166c-113">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="2166c-114">标识要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-114">Identifies a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="2166c-115">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="2166c-115">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="2166c-116">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-116">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="2166c-117">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="2166c-117">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="2166c-118">表示邮箱中的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-118">Represents a Contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2166c-119">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="2166c-119">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="2166c-120">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-120">Represents a Search folder contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2166c-121">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="2166c-121">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="2166c-122">表示邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-122">Represents a Tasks folder in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2166c-123">父元素</span><span class="sxs-lookup"><span data-stu-id="2166c-123">Parent elements</span></span>

|<span data-ttu-id="2166c-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="2166c-124">**Element**</span></span>|<span data-ttu-id="2166c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="2166c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2166c-126">CopyFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-126">CopyFolderResponseMessage</span></span>](copyfolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-127">包含单个[CopyFolder 操作](copyfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-127">Contains the status and result of a single [CopyFolder operation](copyfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2166c-128">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2166c-128">CreateFolder</span></span>](createfolder.md) <br/> |<span data-ttu-id="2166c-129">定义在 Exchange 存储区中创建文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="2166c-129">Defines a request to create a folder in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2166c-130">CreateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-130">CreateFolderResponseMessage</span></span>](createfolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-131">包含单个[CreateFolder 操作](createfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-131">Contains the status and result of a single [CreateFolder operation](createfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2166c-132">CreateManagedFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-132">CreateManagedFolderResponseMessage</span></span>](createmanagedfolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-133">包含单个[CreateManagedFolder 操作](createmanagedfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-133">Contains the status and result of a single [CreateManagedFolder operation](createmanagedfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2166c-134">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-134">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-135">包含[GetFolder 操作](getfolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-135">Contains the status and result of a [GetFolder operation](getfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2166c-136">MoveFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-136">MoveFolderResponseMessage</span></span>](movefolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-137">包含[MoveFolder 操作](movefolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-137">Contains the status and result of a [MoveFolder operation](movefolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="2166c-138">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="2166c-138">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="2166c-139">标识在其中创建新文件夹的文件夹。</span><span class="sxs-lookup"><span data-stu-id="2166c-139">Identifies the folder where a new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="2166c-140">RootFolder （FindFolderResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="2166c-140">RootFolder (FindFolderResponseMessage)</span></span>](rootfolder-findfolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-141">包含在[FindFolder 操作](findfolder-operation.md)过程中搜索单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-141">Contains the results from searching a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2166c-142">UpdateFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2166c-142">UpdateFolderResponseMessage</span></span>](updatefolderresponsemessage.md) <br/> |<span data-ttu-id="2166c-143">包含单个[UpdateFolder 操作](updatefolder-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="2166c-143">Contains the status and result of a single [UpdateFolder operation](updatefolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2166c-144">备注</span><span class="sxs-lookup"><span data-stu-id="2166c-144">Remarks</span></span>

<span data-ttu-id="2166c-145">此元素是[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素的必需子元素。</span><span class="sxs-lookup"><span data-stu-id="2166c-145">This element is a required child element of the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span> 
  
<span data-ttu-id="2166c-146">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2166c-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2166c-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="2166c-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2166c-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="2166c-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2166c-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="2166c-149">Schema Name</span></span>  <br/> |<span data-ttu-id="2166c-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="2166c-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="2166c-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="2166c-151">Validation File</span></span>  <br/> |<span data-ttu-id="2166c-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2166c-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2166c-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="2166c-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="2166c-154">False</span><span class="sxs-lookup"><span data-stu-id="2166c-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2166c-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2166c-155">See also</span></span>

- [<span data-ttu-id="2166c-156">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="2166c-156">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md)

