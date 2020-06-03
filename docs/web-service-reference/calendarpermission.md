---
title: CalendarPermission
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermission
api_type:
- schema
ms.assetid: 3aafb221-a04b-41f6-804e-eda810f1ba28
description: CalendarPermission 元素定义用户对 "日历" 文件夹的访问权限。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: c43f75e6cf5abc2dce9af6c04122ec9a589dcd58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529474"
---
# <a name="calendarpermission"></a><span data-ttu-id="4fcd1-104">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="4fcd1-104">CalendarPermission</span></span>

<span data-ttu-id="4fcd1-105">**CalendarPermission**元素定义用户对 "日历" 文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-105">The **CalendarPermission** element defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="4fcd1-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Permission>
   <CalendarPermissionLevel/>
   <CanCreateItems/>
   <CanCreateSubfolders/>
   <IsFolderOwner/>
   <IsFolderVisible/>
   <IsFolderContact/>
   <EditItems/>
   <DeleteItems/>
   <ReadItems/>
   <UserId/>
</Permission>
```

 <span data-ttu-id="4fcd1-107">**CalendarPermissionType**</span><span class="sxs-lookup"><span data-stu-id="4fcd1-107">**CalendarPermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fcd1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4fcd1-108">Attributes and elements</span></span>

<span data-ttu-id="4fcd1-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fcd1-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="4fcd1-110">Attributes</span></span>

<span data-ttu-id="4fcd1-111">无。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4fcd1-112">子元素</span><span class="sxs-lookup"><span data-stu-id="4fcd1-112">Child elements</span></span>

|<span data-ttu-id="4fcd1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4fcd1-113">**Element**</span></span>|<span data-ttu-id="4fcd1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4fcd1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fcd1-115">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="4fcd1-115">CalendarPermissionLevel</span></span>](calendarpermissionlevel.md) <br/> |<span data-ttu-id="4fcd1-116">表示用户在 "日历" 文件夹上拥有的权限级别。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-116">Represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="4fcd1-117">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-118">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="4fcd1-118">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="4fcd1-119">指示用户是否有权在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-119">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="4fcd1-120">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-121">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="4fcd1-121">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="4fcd1-122">指示用户是否有权在文件夹中创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-122">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="4fcd1-123">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-124">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="4fcd1-124">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="4fcd1-125">指示用户是否有权删除文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-125">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="4fcd1-126">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-127">EditItems</span><span class="sxs-lookup"><span data-stu-id="4fcd1-127">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="4fcd1-128">指示用户是否有权编辑文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-128">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="4fcd1-129">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-130">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="4fcd1-130">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="4fcd1-131">指示用户是否为文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-131">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="4fcd1-132">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-133">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="4fcd1-133">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="4fcd1-134">指示用户是否为文件夹的所有者。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-134">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="4fcd1-135">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-135">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-136">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="4fcd1-136">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="4fcd1-137">指示用户是否可以查看文件夹。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-137">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="4fcd1-138">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-139">ReadItems （CalendarPermissionType）</span><span class="sxs-lookup"><span data-stu-id="4fcd1-139">ReadItems (CalendarPermissionType)</span></span>](readitems-calendarpermissiontype.md) <br/> |<span data-ttu-id="4fcd1-140">指示用户是否有权读取日历文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-140">Indicates whether a user has permission to read items within a calendar folder.</span></span> <span data-ttu-id="4fcd1-141">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-141">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="4fcd1-142">UserId</span><span class="sxs-lookup"><span data-stu-id="4fcd1-142">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="4fcd1-143">标识代理用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-143">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="4fcd1-144">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-144">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4fcd1-145">父元素</span><span class="sxs-lookup"><span data-stu-id="4fcd1-145">Parent elements</span></span>

|<span data-ttu-id="4fcd1-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="4fcd1-146">**Element**</span></span>|<span data-ttu-id="4fcd1-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="4fcd1-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fcd1-148">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="4fcd1-148">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="4fcd1-149">包含文件夹的日历权限数组。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-149">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="4fcd1-150">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-150">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fcd1-151">说明</span><span class="sxs-lookup"><span data-stu-id="4fcd1-151">Remarks</span></span>

<span data-ttu-id="4fcd1-152">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4fcd1-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fcd1-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="4fcd1-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fcd1-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="4fcd1-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4fcd1-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="4fcd1-155">Schema Name</span></span>  <br/> |<span data-ttu-id="4fcd1-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="4fcd1-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="4fcd1-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="4fcd1-157">Validation File</span></span>  <br/> |<span data-ttu-id="4fcd1-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4fcd1-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4fcd1-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="4fcd1-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="4fcd1-160">False</span><span class="sxs-lookup"><span data-stu-id="4fcd1-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fcd1-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4fcd1-161">See also</span></span>



- [<span data-ttu-id="4fcd1-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4fcd1-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4fcd1-163">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="4fcd1-163">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

