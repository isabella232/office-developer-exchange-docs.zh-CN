---
title: 权限
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permission
api_type:
- schema
ms.assetid: b8d0429a-0e58-4480-9847-4901970c7033
description: 权限元素定义用户对文件夹所拥有的访问权限。
ms.openlocfilehash: 0f7515dbb06f8423f8d4d95e1391496e8ac73653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459256"
---
# <a name="permission"></a><span data-ttu-id="21e33-103">权限</span><span class="sxs-lookup"><span data-stu-id="21e33-103">Permission</span></span>

<span data-ttu-id="21e33-104">**权限**元素定义用户对文件夹所拥有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="21e33-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
```XML
<Permission>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <PermissionLevel/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="21e33-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="21e33-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21e33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21e33-106">Attributes and elements</span></span>

<span data-ttu-id="21e33-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21e33-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="21e33-108">Attributes</span></span>

<span data-ttu-id="21e33-109">无。</span><span class="sxs-lookup"><span data-stu-id="21e33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21e33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="21e33-110">Child elements</span></span>

|<span data-ttu-id="21e33-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="21e33-111">**Element**</span></span>|<span data-ttu-id="21e33-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="21e33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21e33-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="21e33-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="21e33-114">指示用户是否有权在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="21e33-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="21e33-115">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="21e33-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="21e33-117">指示用户是否有权在文件夹中创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="21e33-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="21e33-118">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="21e33-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="21e33-120">指示用户是否有权删除文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="21e33-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="21e33-121">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-122">EditItems</span><span class="sxs-lookup"><span data-stu-id="21e33-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="21e33-123">指示用户是否有权编辑文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="21e33-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="21e33-124">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="21e33-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="21e33-126">指示用户是否为文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="21e33-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="21e33-127">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="21e33-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="21e33-129">指示用户是否为文件夹的所有者。</span><span class="sxs-lookup"><span data-stu-id="21e33-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="21e33-130">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="21e33-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="21e33-132">指示用户是否可以查看文件夹。</span><span class="sxs-lookup"><span data-stu-id="21e33-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="21e33-133">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="21e33-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="21e33-135">代表用户对文件夹所拥有的权限的组合。</span><span class="sxs-lookup"><span data-stu-id="21e33-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="21e33-136">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-137">ReadItems （PermissionType）</span><span class="sxs-lookup"><span data-stu-id="21e33-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="21e33-138">指示用户是否有权读取文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="21e33-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="21e33-139">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21e33-140">UserId</span><span class="sxs-lookup"><span data-stu-id="21e33-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="21e33-141">标识代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="21e33-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="21e33-142">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21e33-143">父元素</span><span class="sxs-lookup"><span data-stu-id="21e33-143">Parent elements</span></span>

|<span data-ttu-id="21e33-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="21e33-144">**Element**</span></span>|<span data-ttu-id="21e33-145">**说明**</span><span class="sxs-lookup"><span data-stu-id="21e33-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21e33-146">权限</span><span class="sxs-lookup"><span data-stu-id="21e33-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="21e33-147">包含文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="21e33-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="21e33-148">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21e33-149">说明</span><span class="sxs-lookup"><span data-stu-id="21e33-149">Remarks</span></span>

<span data-ttu-id="21e33-150">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21e33-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="21e33-151">此元素是在 Exchange Server 2007 Service Pack 1 （SP1）中引入的。</span><span class="sxs-lookup"><span data-stu-id="21e33-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="21e33-152">版本差异</span><span class="sxs-lookup"><span data-stu-id="21e33-152">Version differences</span></span>

<span data-ttu-id="21e33-153">对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="21e33-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="21e33-154">若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="21e33-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="21e33-155">元素信息</span><span class="sxs-lookup"><span data-stu-id="21e33-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21e33-156">命名空间</span><span class="sxs-lookup"><span data-stu-id="21e33-156">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21e33-157">架构名称</span><span class="sxs-lookup"><span data-stu-id="21e33-157">Schema Name</span></span>  <br/> |<span data-ttu-id="21e33-158">类型架构</span><span class="sxs-lookup"><span data-stu-id="21e33-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="21e33-159">验证文件</span><span class="sxs-lookup"><span data-stu-id="21e33-159">Validation File</span></span>  <br/> |<span data-ttu-id="21e33-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21e33-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21e33-161">可以为空</span><span class="sxs-lookup"><span data-stu-id="21e33-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="21e33-162">False</span><span class="sxs-lookup"><span data-stu-id="21e33-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21e33-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21e33-163">See also</span></span>



- [<span data-ttu-id="21e33-164">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21e33-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="21e33-165">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="21e33-165">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

