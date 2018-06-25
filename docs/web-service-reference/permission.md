---
title: Permission
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
description: 权限元素到文件夹定义用户拥有的访问权限。
ms.openlocfilehash: 600d60f481c4f1d407c3a39ab65d6ddcf46d04e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826735"
---
# <a name="permission"></a><span data-ttu-id="b6f4f-103">权限</span><span class="sxs-lookup"><span data-stu-id="b6f4f-103">Permission</span></span>

<span data-ttu-id="b6f4f-104">**权限**元素到文件夹定义用户拥有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-104">The **Permission** element defines the access that a user has to a folder.</span></span> 
  
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

 <span data-ttu-id="b6f4f-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="b6f4f-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6f4f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b6f4f-106">Attributes and elements</span></span>

<span data-ttu-id="b6f4f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6f4f-108">属性</span><span class="sxs-lookup"><span data-stu-id="b6f4f-108">Attributes</span></span>

<span data-ttu-id="b6f4f-109">无。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6f4f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b6f4f-110">Child elements</span></span>

|<span data-ttu-id="b6f4f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6f4f-111">**Element**</span></span>|<span data-ttu-id="b6f4f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6f4f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6f4f-113">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="b6f4f-113">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="b6f4f-114">指示用户是否有权文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-114">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="b6f4f-115">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-116">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="b6f4f-116">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="b6f4f-117">指示用户是否有权在创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-117">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="b6f4f-118">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-119">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="b6f4f-119">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="b6f4f-120">指示用户是否有权删除文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-120">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="b6f4f-121">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-122">EditItems</span><span class="sxs-lookup"><span data-stu-id="b6f4f-122">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="b6f4f-123">指示用户是否有权编辑文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-123">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="b6f4f-124">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-124">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-125">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="b6f4f-125">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="b6f4f-126">指示用户是否为文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-126">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="b6f4f-127">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-127">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-128">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="b6f4f-128">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="b6f4f-129">指示用户是否为文件夹的所有者。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-129">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="b6f4f-130">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-130">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-131">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="b6f4f-131">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="b6f4f-132">指示用户是否可以查看文件夹。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-132">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="b6f4f-133">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-133">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-134">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="b6f4f-134">PermissionLevel</span></span>](permissionlevel.md) <br/> |<span data-ttu-id="b6f4f-135">表示用户对某个文件夹的权限的组合。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-135">Represents the combination of permissions that a user has on a folder.</span></span> <span data-ttu-id="b6f4f-136">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-136">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-137">ReadItems (PermissionType)</span><span class="sxs-lookup"><span data-stu-id="b6f4f-137">ReadItems (PermissionType)</span></span>](readitems-permissiontype.md) <br/> |<span data-ttu-id="b6f4f-138">指示用户是否有权读取文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-138">Indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="b6f4f-139">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="b6f4f-140">用户 Id</span><span class="sxs-lookup"><span data-stu-id="b6f4f-140">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="b6f4f-141">标识委派用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-141">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="b6f4f-142">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-142">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6f4f-143">父元素</span><span class="sxs-lookup"><span data-stu-id="b6f4f-143">Parent elements</span></span>

|<span data-ttu-id="b6f4f-144">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6f4f-144">**Element**</span></span>|<span data-ttu-id="b6f4f-145">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6f4f-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6f4f-146">权限</span><span class="sxs-lookup"><span data-stu-id="b6f4f-146">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="b6f4f-147">包含文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-147">Contains all the configured permissions for a folder.</span></span> <span data-ttu-id="b6f4f-148">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-148">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6f4f-149">备注</span><span class="sxs-lookup"><span data-stu-id="b6f4f-149">Remarks</span></span>

<span data-ttu-id="b6f4f-150">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-150">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="b6f4f-151">此元素是在 Exchange Server 2007 Service Pack 1 (SP1) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-151">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="b6f4f-152">版本差异</span><span class="sxs-lookup"><span data-stu-id="b6f4f-152">Version differences</span></span>

<span data-ttu-id="b6f4f-153">应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-153">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="b6f4f-154">若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b6f4f-154">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b6f4f-155">元素信息</span><span class="sxs-lookup"><span data-stu-id="b6f4f-155">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6f4f-156">命名空间</span><span class="sxs-lookup"><span data-stu-id="b6f4f-156">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6f4f-157">架构名称</span><span class="sxs-lookup"><span data-stu-id="b6f4f-157">Schema Name</span></span>  <br/> |<span data-ttu-id="b6f4f-158">类型架构</span><span class="sxs-lookup"><span data-stu-id="b6f4f-158">Types schema</span></span>  <br/> |
|<span data-ttu-id="b6f4f-159">验证文件</span><span class="sxs-lookup"><span data-stu-id="b6f4f-159">Validation File</span></span>  <br/> |<span data-ttu-id="b6f4f-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b6f4f-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6f4f-161">可以为空</span><span class="sxs-lookup"><span data-stu-id="b6f4f-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6f4f-162">False</span><span class="sxs-lookup"><span data-stu-id="b6f4f-162">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6f4f-163">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6f4f-163">See also</span></span>



- [<span data-ttu-id="b6f4f-164">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b6f4f-164">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b6f4f-165">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="b6f4f-165">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

