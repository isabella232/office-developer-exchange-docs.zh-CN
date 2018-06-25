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
description: CalendarPermission 元素定义日历文件夹的用户具有访问权限。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 7f6ceb6895add3fdd82cdd595463b3a80db822e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753417"
---
# <a name="calendarpermission"></a><span data-ttu-id="1235f-104">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="1235f-104">CalendarPermission</span></span>

<span data-ttu-id="1235f-105">**CalendarPermission**元素定义日历文件夹的用户具有访问权限。</span><span class="sxs-lookup"><span data-stu-id="1235f-105">The **CalendarPermission** element defines the access that a user has to a Calendar folder.</span></span> <span data-ttu-id="1235f-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

 <span data-ttu-id="1235f-107">**CalendarPermissionType**</span><span class="sxs-lookup"><span data-stu-id="1235f-107">**CalendarPermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1235f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1235f-108">Attributes and elements</span></span>

<span data-ttu-id="1235f-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1235f-110">属性</span><span class="sxs-lookup"><span data-stu-id="1235f-110">Attributes</span></span>

<span data-ttu-id="1235f-111">无。</span><span class="sxs-lookup"><span data-stu-id="1235f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1235f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1235f-112">Child elements</span></span>

|<span data-ttu-id="1235f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1235f-113">**Element**</span></span>|<span data-ttu-id="1235f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1235f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1235f-115">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="1235f-115">CalendarPermissionLevel</span></span>](calendarpermissionlevel.md) <br/> |<span data-ttu-id="1235f-116">表示用户对日历文件夹的权限级别。</span><span class="sxs-lookup"><span data-stu-id="1235f-116">Represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="1235f-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-118">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="1235f-118">CanCreateItems</span></span>](cancreateitems.md) <br/> |<span data-ttu-id="1235f-119">指示用户是否有权文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="1235f-119">Indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="1235f-120">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-121">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="1235f-121">CanCreateSubFolders</span></span>](cancreatesubfolders.md) <br/> |<span data-ttu-id="1235f-122">指示用户是否有权在创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="1235f-122">Indicates whether a user has permission to create subfolders in a folder.</span></span> <span data-ttu-id="1235f-123">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-124">DeleteItems</span><span class="sxs-lookup"><span data-stu-id="1235f-124">DeleteItems</span></span>](deleteitems.md) <br/> |<span data-ttu-id="1235f-125">指示用户是否有权删除文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="1235f-125">Indicates whether a user has permission to delete items in a folder.</span></span> <span data-ttu-id="1235f-126">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-127">EditItems</span><span class="sxs-lookup"><span data-stu-id="1235f-127">EditItems</span></span>](edititems.md) <br/> |<span data-ttu-id="1235f-128">指示用户是否有权编辑文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="1235f-128">Indicates whether a user has permission to edit items in a folder.</span></span> <span data-ttu-id="1235f-129">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-130">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="1235f-130">IsFolderContact</span></span>](isfoldercontact.md) <br/> |<span data-ttu-id="1235f-131">指示用户是否为文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="1235f-131">Indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="1235f-132">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-133">IsFolderOwner</span><span class="sxs-lookup"><span data-stu-id="1235f-133">IsFolderOwner</span></span>](isfolderowner.md) <br/> |<span data-ttu-id="1235f-134">指示用户是否为文件夹的所有者。</span><span class="sxs-lookup"><span data-stu-id="1235f-134">Indicates whether a user is the owner of a folder.</span></span> <span data-ttu-id="1235f-135">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-135">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-136">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="1235f-136">IsFolderVisible</span></span>](isfoldervisible.md) <br/> |<span data-ttu-id="1235f-137">指示用户是否可以查看文件夹。</span><span class="sxs-lookup"><span data-stu-id="1235f-137">Indicates whether a user can view a folder.</span></span> <span data-ttu-id="1235f-138">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-139">ReadItems (CalendarPermissionType)</span><span class="sxs-lookup"><span data-stu-id="1235f-139">ReadItems (CalendarPermissionType)</span></span>](readitems-calendarpermissiontype.md) <br/> |<span data-ttu-id="1235f-140">指示用户是否有权读取日历文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="1235f-140">Indicates whether a user has permission to read items within a calendar folder.</span></span> <span data-ttu-id="1235f-141">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-141">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1235f-142">用户 Id</span><span class="sxs-lookup"><span data-stu-id="1235f-142">UserId</span></span>](userid.md) <br/> |<span data-ttu-id="1235f-143">标识委派用户或具有文件夹访问权限的用户。</span><span class="sxs-lookup"><span data-stu-id="1235f-143">Identifies a delegate user or a user who has folder access permissions.</span></span> <span data-ttu-id="1235f-144">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-144">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1235f-145">父元素</span><span class="sxs-lookup"><span data-stu-id="1235f-145">Parent elements</span></span>

|<span data-ttu-id="1235f-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="1235f-146">**Element**</span></span>|<span data-ttu-id="1235f-147">**说明**</span><span class="sxs-lookup"><span data-stu-id="1235f-147">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1235f-148">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="1235f-148">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="1235f-149">包含数组的日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="1235f-149">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="1235f-150">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1235f-150">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1235f-151">备注</span><span class="sxs-lookup"><span data-stu-id="1235f-151">Remarks</span></span>

<span data-ttu-id="1235f-152">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1235f-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1235f-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="1235f-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1235f-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="1235f-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1235f-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="1235f-155">Schema Name</span></span>  <br/> |<span data-ttu-id="1235f-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="1235f-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="1235f-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="1235f-157">Validation File</span></span>  <br/> |<span data-ttu-id="1235f-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1235f-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1235f-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="1235f-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="1235f-160">False</span><span class="sxs-lookup"><span data-stu-id="1235f-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1235f-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1235f-161">See also</span></span>



- [<span data-ttu-id="1235f-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1235f-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1235f-163">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="1235f-163">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

