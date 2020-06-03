---
title: PermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionLevel
api_type:
- schema
ms.assetid: 87978600-3523-451e-a725-ef092c543e2a
description: PermissionLevel 元素表示用户对文件夹拥有的权限级别。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e1e441c53b5c40c16051eb852a6b35a8af7476e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458038"
---
# <a name="permissionlevel"></a><span data-ttu-id="558d7-104">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="558d7-104">PermissionLevel</span></span>

<span data-ttu-id="558d7-105">**PermissionLevel**元素表示用户对文件夹拥有的权限级别。</span><span class="sxs-lookup"><span data-stu-id="558d7-105">The **PermissionLevel** element represents the permission level that a user has on a folder.</span></span> <span data-ttu-id="558d7-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="558d7-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 <span data-ttu-id="558d7-107">**PermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="558d7-107">**PermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="558d7-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="558d7-108">Attributes and elements</span></span>

<span data-ttu-id="558d7-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="558d7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="558d7-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="558d7-110">Attributes</span></span>

<span data-ttu-id="558d7-111">无。</span><span class="sxs-lookup"><span data-stu-id="558d7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="558d7-112">子元素</span><span class="sxs-lookup"><span data-stu-id="558d7-112">Child elements</span></span>

<span data-ttu-id="558d7-113">无。</span><span class="sxs-lookup"><span data-stu-id="558d7-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="558d7-114">父元素</span><span class="sxs-lookup"><span data-stu-id="558d7-114">Parent elements</span></span>

|<span data-ttu-id="558d7-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="558d7-115">**Element**</span></span>|<span data-ttu-id="558d7-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="558d7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="558d7-117">权限</span><span class="sxs-lookup"><span data-stu-id="558d7-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="558d7-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="558d7-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="558d7-120">文本值</span><span class="sxs-lookup"><span data-stu-id="558d7-120">Text value</span></span>

<span data-ttu-id="558d7-121">下表列出了**PermissionLevel**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="558d7-121">The following table lists the possible values for the **PermissionLevel** element.</span></span> 
  
<span data-ttu-id="558d7-122">**PermissionLevel 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="558d7-122">**PermissionLevel element text values**</span></span>

|<span data-ttu-id="558d7-123">**值**</span><span class="sxs-lookup"><span data-stu-id="558d7-123">**Value**</span></span>|<span data-ttu-id="558d7-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="558d7-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="558d7-125">无</span><span class="sxs-lookup"><span data-stu-id="558d7-125">None</span></span>  <br/> |<span data-ttu-id="558d7-126">指示用户对文件夹没有权限。</span><span class="sxs-lookup"><span data-stu-id="558d7-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="558d7-127">所有者</span><span class="sxs-lookup"><span data-stu-id="558d7-127">Owner</span></span>  <br/> |<span data-ttu-id="558d7-128">指示用户可以创建、读取、编辑和删除文件夹中的所有项目，并创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="558d7-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="558d7-129">用户是文件夹所有者和文件夹联系人。</span><span class="sxs-lookup"><span data-stu-id="558d7-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="558d7-130">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="558d7-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="558d7-131">指示用户可以创建、读取、编辑和删除文件夹中的所有项目，并创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="558d7-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="558d7-132">编辑器</span><span class="sxs-lookup"><span data-stu-id="558d7-132">Editor</span></span>  <br/> |<span data-ttu-id="558d7-133">指示用户可以创建、读取、编辑和删除文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="558d7-133">Indicates that the user can create, read, edit, and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="558d7-134">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="558d7-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="558d7-135">指示用户可以创建和读取文件夹中的所有项目、仅编辑和删除用户创建的项目以及创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="558d7-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="558d7-136">作者</span><span class="sxs-lookup"><span data-stu-id="558d7-136">Author</span></span>  <br/> |<span data-ttu-id="558d7-137">指示用户可以创建和读取文件夹中的所有项目，并只编辑和删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="558d7-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="558d7-138">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="558d7-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="558d7-139">指示用户可以创建和读取文件夹中的所有项目，并只删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="558d7-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="558d7-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="558d7-140">Reviewer</span></span>  <br/> |<span data-ttu-id="558d7-141">指示用户可以读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="558d7-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="558d7-142">参与者</span><span class="sxs-lookup"><span data-stu-id="558d7-142">Contributor</span></span>  <br/> |<span data-ttu-id="558d7-143">指示用户可以在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="558d7-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="558d7-144">不显示文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="558d7-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="558d7-145">自定义警报</span><span class="sxs-lookup"><span data-stu-id="558d7-145">Custom</span></span>  <br/> |<span data-ttu-id="558d7-146">指示用户对该文件夹具有自定义访问权限。</span><span class="sxs-lookup"><span data-stu-id="558d7-146">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="558d7-147">说明</span><span class="sxs-lookup"><span data-stu-id="558d7-147">Remarks</span></span>

<span data-ttu-id="558d7-148">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="558d7-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="558d7-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="558d7-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="558d7-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="558d7-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="558d7-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="558d7-151">Schema Name</span></span>  <br/> |<span data-ttu-id="558d7-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="558d7-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="558d7-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="558d7-153">Validation File</span></span>  <br/> |<span data-ttu-id="558d7-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="558d7-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="558d7-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="558d7-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="558d7-156">False</span><span class="sxs-lookup"><span data-stu-id="558d7-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="558d7-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="558d7-157">See also</span></span>



- [<span data-ttu-id="558d7-158">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="558d7-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="558d7-159">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="558d7-159">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

