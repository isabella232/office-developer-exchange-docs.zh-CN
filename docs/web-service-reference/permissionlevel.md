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
description: PermissionLevel 元素均表示用户对某个文件夹的权限级别。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 7cc734f5807fe039467065315c220341f47d3fb4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826730"
---
# <a name="permissionlevel"></a><span data-ttu-id="0a41d-104">PermissionLevel</span><span class="sxs-lookup"><span data-stu-id="0a41d-104">PermissionLevel</span></span>

<span data-ttu-id="0a41d-105">**PermissionLevel**元素均表示用户对某个文件夹的权限级别。</span><span class="sxs-lookup"><span data-stu-id="0a41d-105">The **PermissionLevel** element represents the permission level that a user has on a folder.</span></span> <span data-ttu-id="0a41d-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0a41d-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or Custom</PermissionLevel>
```

 <span data-ttu-id="0a41d-107">**PermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="0a41d-107">**PermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a41d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0a41d-108">Attributes and elements</span></span>

<span data-ttu-id="0a41d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0a41d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a41d-110">属性</span><span class="sxs-lookup"><span data-stu-id="0a41d-110">Attributes</span></span>

<span data-ttu-id="0a41d-111">无。</span><span class="sxs-lookup"><span data-stu-id="0a41d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a41d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0a41d-112">Child elements</span></span>

<span data-ttu-id="0a41d-113">无。</span><span class="sxs-lookup"><span data-stu-id="0a41d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a41d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="0a41d-114">Parent elements</span></span>

|<span data-ttu-id="0a41d-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a41d-115">**Element**</span></span>|<span data-ttu-id="0a41d-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a41d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a41d-117">权限</span><span class="sxs-lookup"><span data-stu-id="0a41d-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="0a41d-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0a41d-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a41d-120">文本值</span><span class="sxs-lookup"><span data-stu-id="0a41d-120">Text value</span></span>

<span data-ttu-id="0a41d-121">下表列出了**PermissionLevel**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="0a41d-121">The following table lists the possible values for the **PermissionLevel** element.</span></span> 
  
<span data-ttu-id="0a41d-122">**PermissionLevel 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="0a41d-122">**PermissionLevel element text values**</span></span>

|<span data-ttu-id="0a41d-123">**值**</span><span class="sxs-lookup"><span data-stu-id="0a41d-123">**Value**</span></span>|<span data-ttu-id="0a41d-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a41d-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a41d-125">无</span><span class="sxs-lookup"><span data-stu-id="0a41d-125">None</span></span>  <br/> |<span data-ttu-id="0a41d-126">指示用户具有对文件夹没有权限。</span><span class="sxs-lookup"><span data-stu-id="0a41d-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="0a41d-127">Owner</span><span class="sxs-lookup"><span data-stu-id="0a41d-127">Owner</span></span>  <br/> |<span data-ttu-id="0a41d-128">指示，用户可以创建、 读取、 编辑和删除文件夹中的所有项目和创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="0a41d-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="0a41d-129">用户是文件夹所有者和文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="0a41d-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="0a41d-130">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="0a41d-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="0a41d-131">指示，用户可以创建、 读取、 编辑和删除文件夹中的所有项目和创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="0a41d-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="0a41d-132">Editor</span><span class="sxs-lookup"><span data-stu-id="0a41d-132">Editor</span></span>  <br/> |<span data-ttu-id="0a41d-133">指示用户可以创建、 读取、 编辑和删除文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="0a41d-133">Indicates that the user can create, read, edit, and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="0a41d-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="0a41d-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="0a41d-135">指示用户可以创建和读取所有项的文件夹中，编辑和删除用户创建的项目并创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="0a41d-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="0a41d-136">作者</span><span class="sxs-lookup"><span data-stu-id="0a41d-136">Author</span></span>  <br/> |<span data-ttu-id="0a41d-137">指示用户可以创建和读取所有项的文件夹中，并编辑和删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="0a41d-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="0a41d-138">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="0a41d-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="0a41d-139">指示用户可以创建和读取所有项的文件夹中，并删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="0a41d-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="0a41d-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="0a41d-140">Reviewer</span></span>  <br/> |<span data-ttu-id="0a41d-141">指示用户可以读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="0a41d-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="0a41d-142">参与者</span><span class="sxs-lookup"><span data-stu-id="0a41d-142">Contributor</span></span>  <br/> |<span data-ttu-id="0a41d-143">指示用户可以创建的文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="0a41d-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="0a41d-144">不显示该文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="0a41d-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="0a41d-145">自定义</span><span class="sxs-lookup"><span data-stu-id="0a41d-145">Custom</span></span>  <br/> |<span data-ttu-id="0a41d-146">指示用户具有自定义访问权限的文件夹。</span><span class="sxs-lookup"><span data-stu-id="0a41d-146">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a41d-147">备注</span><span class="sxs-lookup"><span data-stu-id="0a41d-147">Remarks</span></span>

<span data-ttu-id="0a41d-148">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0a41d-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a41d-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="0a41d-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a41d-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="0a41d-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a41d-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="0a41d-151">Schema Name</span></span>  <br/> |<span data-ttu-id="0a41d-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="0a41d-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a41d-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="0a41d-153">Validation File</span></span>  <br/> |<span data-ttu-id="0a41d-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a41d-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a41d-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="0a41d-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a41d-156">False</span><span class="sxs-lookup"><span data-stu-id="0a41d-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a41d-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a41d-157">See also</span></span>



- [<span data-ttu-id="0a41d-158">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0a41d-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0a41d-159">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="0a41d-159">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

