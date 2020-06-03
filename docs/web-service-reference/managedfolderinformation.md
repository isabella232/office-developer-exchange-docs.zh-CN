---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: ManagedFolderInformation 元素包含有关托管自定义文件夹的信息。
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44450947"
---
# <a name="managedfolderinformation"></a><span data-ttu-id="3a5fe-103">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="3a5fe-103">ManagedFolderInformation</span></span>

<span data-ttu-id="3a5fe-104">**ManagedFolderInformation**元素包含有关托管自定义文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-104">The **ManagedFolderInformation** element contains information about a managed custom folder.</span></span> 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 <span data-ttu-id="3a5fe-105">**ManagedFolderInformationType**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-105">**ManagedFolderInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a5fe-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3a5fe-106">Attributes and elements</span></span>

<span data-ttu-id="3a5fe-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a5fe-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3a5fe-108">Attributes</span></span>

<span data-ttu-id="3a5fe-109">无。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a5fe-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3a5fe-110">Child elements</span></span>

|<span data-ttu-id="3a5fe-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-111">**Element**</span></span>|<span data-ttu-id="3a5fe-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5fe-113">CanDelete</span><span class="sxs-lookup"><span data-stu-id="3a5fe-113">CanDelete</span></span>](candelete.md) <br/> |<span data-ttu-id="3a5fe-114">指示托管文件夹是否可由客户删除。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-114">Indicates whether a managed folder can be deleted by a customer.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-115">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="3a5fe-115">CanRenameOrMove</span></span>](canrenameormove.md) <br/> |<span data-ttu-id="3a5fe-116">指示客户是否可以重命名或移动给定的托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-116">Indicates whether a given managed folder can be renamed or moved by the customer.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-117">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="3a5fe-117">MustDisplayComment</span></span>](mustdisplaycomment.md) <br/> |<span data-ttu-id="3a5fe-118">指示是否必须显示托管文件夹注释。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-118">Indicates whether the managed folder comment must be displayed.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-119">HasQuota</span><span class="sxs-lookup"><span data-stu-id="3a5fe-119">HasQuota</span></span>](hasquota.md) <br/> |<span data-ttu-id="3a5fe-120">指示托管文件夹是否具有配额。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-120">Indicates whether the managed folder has a quota.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-121">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="3a5fe-121">IsManagedFoldersRoot</span></span>](ismanagedfoldersroot.md) <br/> |<span data-ttu-id="3a5fe-122">指示托管文件夹是否为所有托管文件夹的根。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-122">Indicates whether the managed folder is the root for all managed folders.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-123">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="3a5fe-123">ManagedFolderId</span></span>](managedfolderid.md) <br/> |<span data-ttu-id="3a5fe-124">包含托管文件夹的文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-124">Contains the folder ID of the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-125">Comment</span><span class="sxs-lookup"><span data-stu-id="3a5fe-125">Comment</span></span>](comment.md) <br/> |<span data-ttu-id="3a5fe-126">包含与托管文件夹相关联的注释。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-126">Contains the comment that is associated with a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-127">StorageQuota</span><span class="sxs-lookup"><span data-stu-id="3a5fe-127">StorageQuota</span></span>](storagequota.md) <br/> |<span data-ttu-id="3a5fe-128">描述托管文件夹的存储配额。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-128">Describes the storage quota for the managed folder.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-129">FolderSize</span><span class="sxs-lookup"><span data-stu-id="3a5fe-129">FolderSize</span></span>](foldersize.md) <br/> |<span data-ttu-id="3a5fe-130">描述托管文件夹中所有内容的总大小。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-130">Describes the total size of all the contents of a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-131">HomePage</span><span class="sxs-lookup"><span data-stu-id="3a5fe-131">HomePage</span></span>](homepage.md) <br/> |<span data-ttu-id="3a5fe-132">指定将作为托管文件夹的默认主页的 URL。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-132">Specifies the URL that will be the default home page for the managed folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a5fe-133">父元素</span><span class="sxs-lookup"><span data-stu-id="3a5fe-133">Parent elements</span></span>

|<span data-ttu-id="3a5fe-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-134">**Element**</span></span>|<span data-ttu-id="3a5fe-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5fe-136">Folder</span><span class="sxs-lookup"><span data-stu-id="3a5fe-136">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="3a5fe-137">表示 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-137">Represents a folder in the Exchange store.</span></span> <span data-ttu-id="3a5fe-138">托管自定义文件夹只能是名为 "**托管文件夹**" 的文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-138">Managed custom folders can only be subfolders of the folder named **Managed Folders**.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-139">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="3a5fe-139">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="3a5fe-140">不适用。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-140">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-141">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="3a5fe-141">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="3a5fe-142">不适用。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-142">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-143">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="3a5fe-143">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="3a5fe-144">不适用。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-144">Not applicable.</span></span>  <br/> |
|[<span data-ttu-id="3a5fe-145">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="3a5fe-145">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="3a5fe-146">不适用。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-146">Not applicable.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a5fe-147">注解</span><span class="sxs-lookup"><span data-stu-id="3a5fe-147">Remarks</span></span>

<span data-ttu-id="3a5fe-148">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3a5fe-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a5fe-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="3a5fe-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a5fe-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a5fe-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a5fe-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="3a5fe-151">Schema name</span></span>  <br/> |<span data-ttu-id="3a5fe-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="3a5fe-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a5fe-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="3a5fe-153">Validation file</span></span>  <br/> |<span data-ttu-id="3a5fe-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a5fe-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a5fe-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="3a5fe-155">Can be empty</span></span>  <br/> |<span data-ttu-id="3a5fe-156">False</span><span class="sxs-lookup"><span data-stu-id="3a5fe-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a5fe-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a5fe-157">See also</span></span>



[<span data-ttu-id="3a5fe-158">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="3a5fe-158">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="3a5fe-159">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3a5fe-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="3a5fe-160">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="3a5fe-160">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

