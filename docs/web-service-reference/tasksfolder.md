---
title: TasksFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: TasksFolder元素表示包含在邮箱任务文件夹。
ms.openlocfilehash: 522fe485482bd8159927f9925b7a5582ba2e1c22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465336"
---
# <a name="tasksfolder"></a><span data-ttu-id="bba9b-103">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="bba9b-103">TasksFolder</span></span>

<span data-ttu-id="bba9b-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **TasksFolder**元素表示包含在邮箱任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="bba9b-104">The **TasksFolder** element represents a Tasks folder that is contained in a mailbox.</span></span> 
  
```xml
<TasksFolder>
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
</TasksFolder>
```

<span data-ttu-id="bba9b-105">**TasksFolderType**</span><span class="sxs-lookup"><span data-stu-id="bba9b-105">**TasksFolderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bba9b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bba9b-106">Attributes and elements</span></span>

<span data-ttu-id="bba9b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bba9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bba9b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bba9b-108">Attributes</span></span>

<span data-ttu-id="bba9b-109">无。</span><span class="sxs-lookup"><span data-stu-id="bba9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bba9b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bba9b-110">Child elements</span></span>

|<span data-ttu-id="bba9b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bba9b-111">**Element**</span></span>|<span data-ttu-id="bba9b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bba9b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bba9b-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="bba9b-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="bba9b-114">包含任务文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="bba9b-114">Contains the identifier and change key of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="bba9b-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="bba9b-116">表示包含任务文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="bba9b-116">Represents the identifier of the parent folder that contains the Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="bba9b-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="bba9b-118">代表任务文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="bba9b-118">Represents the folder class for a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="bba9b-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="bba9b-120">包含任务文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="bba9b-120">Contains the display name of a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="bba9b-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="bba9b-122">代表任务文件夹中的项的总计数。</span><span class="sxs-lookup"><span data-stu-id="bba9b-122">Represents the total count of items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="bba9b-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="bba9b-p101">代表任务文件夹中所包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="bba9b-p101">Represents the number of child folders that are contained within a Tasks folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="bba9b-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="bba9b-127">标识任务文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="bba9b-127">Identifies extended properties on a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="bba9b-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="bba9b-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="bba9b-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="bba9b-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="bba9b-131">代表任务文件夹中未阅读项的计数。</span><span class="sxs-lookup"><span data-stu-id="bba9b-131">Represents the count of unread items within a Tasks folder.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-132">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="bba9b-132">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="bba9b-p102">包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bba9b-p102">Contains all the configured permissions for a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="bba9b-135">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="bba9b-135">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="bba9b-p103">包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。在 Microsoft Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bba9b-p103">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Microsoft Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bba9b-139">父元素</span><span class="sxs-lookup"><span data-stu-id="bba9b-139">Parent elements</span></span>

|<span data-ttu-id="bba9b-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="bba9b-140">**Element**</span></span>|<span data-ttu-id="bba9b-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="bba9b-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bba9b-142">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="bba9b-142">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="bba9b-143">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="bba9b-143">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bba9b-144">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bba9b-144">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="bba9b-145">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="bba9b-145">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-146">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="bba9b-146">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="bba9b-147">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="bba9b-147">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="bba9b-148">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="bba9b-148">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="bba9b-149">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="bba9b-149">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="bba9b-150">Folders</span><span class="sxs-lookup"><span data-stu-id="bba9b-150">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bba9b-151">包含一数组的文件夹操作中使用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="bba9b-151">Contains an array of folders that are used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bba9b-152">说明</span><span class="sxs-lookup"><span data-stu-id="bba9b-152">Remarks</span></span>

<span data-ttu-id="bba9b-153">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bba9b-153">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bba9b-154">元素信息</span><span class="sxs-lookup"><span data-stu-id="bba9b-154">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bba9b-155">命名空间</span><span class="sxs-lookup"><span data-stu-id="bba9b-155">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bba9b-156">架构名称</span><span class="sxs-lookup"><span data-stu-id="bba9b-156">Schema Name</span></span>  <br/> |<span data-ttu-id="bba9b-157">类型架构</span><span class="sxs-lookup"><span data-stu-id="bba9b-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="bba9b-158">验证文件</span><span class="sxs-lookup"><span data-stu-id="bba9b-158">Validation File</span></span>  <br/> |<span data-ttu-id="bba9b-159">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bba9b-159">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bba9b-160">可以为空</span><span class="sxs-lookup"><span data-stu-id="bba9b-160">Can be Empty</span></span>  <br/> |<span data-ttu-id="bba9b-161">False</span><span class="sxs-lookup"><span data-stu-id="bba9b-161">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bba9b-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bba9b-162">See also</span></span>

- [<span data-ttu-id="bba9b-163">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bba9b-163">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

