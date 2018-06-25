---
title: CalendarPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: CalendarPermissionLevel 元素均表示用户对日历文件夹的权限级别。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 646e4df3b70350a16cdd1f3e134260c2984a5161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753422"
---
# <a name="calendarpermissionlevel"></a><span data-ttu-id="ce058-104">CalendarPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ce058-104">CalendarPermissionLevel</span></span>

<span data-ttu-id="ce058-105">**CalendarPermissionLevel**元素均表示用户对日历文件夹的权限级别。</span><span class="sxs-lookup"><span data-stu-id="ce058-105">The **CalendarPermissionLevel** element represents the permission level that a user has on a Calendar folder.</span></span> <span data-ttu-id="ce058-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ce058-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 <span data-ttu-id="ce058-107">**CalendarPermissionLevelType**</span><span class="sxs-lookup"><span data-stu-id="ce058-107">**CalendarPermissionLevelType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce058-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ce058-108">Attributes and elements</span></span>

<span data-ttu-id="ce058-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce058-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce058-110">属性</span><span class="sxs-lookup"><span data-stu-id="ce058-110">Attributes</span></span>

<span data-ttu-id="ce058-111">无。</span><span class="sxs-lookup"><span data-stu-id="ce058-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce058-112">子元素</span><span class="sxs-lookup"><span data-stu-id="ce058-112">Child elements</span></span>

<span data-ttu-id="ce058-113">无。</span><span class="sxs-lookup"><span data-stu-id="ce058-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ce058-114">父元素</span><span class="sxs-lookup"><span data-stu-id="ce058-114">Parent elements</span></span>

|<span data-ttu-id="ce058-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce058-115">**Element**</span></span>|<span data-ttu-id="ce058-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce058-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce058-117">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ce058-117">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ce058-p103">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ce058-p103">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ce058-120">文本值</span><span class="sxs-lookup"><span data-stu-id="ce058-120">Text value</span></span>

<span data-ttu-id="ce058-121">下表列出了**CalendarPermissionLevel**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="ce058-121">The following table lists the possible values for the **CalendarPermissionLevel** element.</span></span> 
  
<span data-ttu-id="ce058-122">**CalendarPermissionLevel 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="ce058-122">**CalendarPermissionLevel element text values**</span></span>

|<span data-ttu-id="ce058-123">**值**</span><span class="sxs-lookup"><span data-stu-id="ce058-123">**Value**</span></span>|<span data-ttu-id="ce058-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce058-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce058-125">无</span><span class="sxs-lookup"><span data-stu-id="ce058-125">None</span></span>  <br/> |<span data-ttu-id="ce058-126">指示用户具有对文件夹没有权限。</span><span class="sxs-lookup"><span data-stu-id="ce058-126">Indicates that the user has no permissions on the folder.</span></span>  <br/> |
|<span data-ttu-id="ce058-127">Owner</span><span class="sxs-lookup"><span data-stu-id="ce058-127">Owner</span></span>  <br/> |<span data-ttu-id="ce058-128">指示，用户可以创建、 读取、 编辑和删除文件夹中的所有项目和创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="ce058-128">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span> <span data-ttu-id="ce058-129">用户是文件夹所有者和文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="ce058-129">The user is both folder owner and folder contact.</span></span>  <br/> |
|<span data-ttu-id="ce058-130">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="ce058-130">PublishingEditor</span></span>  <br/> |<span data-ttu-id="ce058-131">指示，用户可以创建、 读取、 编辑和删除文件夹中的所有项目和创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="ce058-131">Indicates that the user can create, read, edit, and delete all items in the folder, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="ce058-132">Editor</span><span class="sxs-lookup"><span data-stu-id="ce058-132">Editor</span></span>  <br/> |<span data-ttu-id="ce058-133">指示用户可以创建、 读取、 编辑和删除文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="ce058-133">Indicates that the user can create, read, edit and delete all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="ce058-134">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="ce058-134">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="ce058-135">指示用户可以创建和读取所有项的文件夹中，编辑和删除用户创建的项目并创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="ce058-135">Indicates that the user can create and read all items in the folder, edit and delete only items that the user creates, and create subfolders.</span></span>  <br/> |
|<span data-ttu-id="ce058-136">作者</span><span class="sxs-lookup"><span data-stu-id="ce058-136">Author</span></span>  <br/> |<span data-ttu-id="ce058-137">指示用户可以创建和读取所有项的文件夹中，并编辑和删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="ce058-137">Indicates that the user can create and read all items in the folder, and edit and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="ce058-138">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="ce058-138">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="ce058-139">指示用户可以创建和读取所有项的文件夹中，并删除用户创建的项目。</span><span class="sxs-lookup"><span data-stu-id="ce058-139">Indicates that the user can create and read all items in the folder, and delete only items that the user creates.</span></span>  <br/> |
|<span data-ttu-id="ce058-140">Reviewer</span><span class="sxs-lookup"><span data-stu-id="ce058-140">Reviewer</span></span>  <br/> |<span data-ttu-id="ce058-141">指示用户可以读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="ce058-141">Indicates that the user can read all items in the folder.</span></span>  <br/> |
|<span data-ttu-id="ce058-142">参与者</span><span class="sxs-lookup"><span data-stu-id="ce058-142">Contributor</span></span>  <br/> |<span data-ttu-id="ce058-143">指示用户可以创建的文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="ce058-143">Indicates that the user can create items in the folder.</span></span> <span data-ttu-id="ce058-144">不显示该文件夹的内容。</span><span class="sxs-lookup"><span data-stu-id="ce058-144">The contents of the folder do not appear.</span></span>  <br/> |
|<span data-ttu-id="ce058-145">FreeBusyTimeOnly</span><span class="sxs-lookup"><span data-stu-id="ce058-145">FreeBusyTimeOnly</span></span>  <br/> |<span data-ttu-id="ce058-146">指示用户可以查看仅忙/闲时间内的时间的日历。</span><span class="sxs-lookup"><span data-stu-id="ce058-146">Indicates that the user can view only free/busy time within the calendar.</span></span>  <br/> |
|<span data-ttu-id="ce058-147">FreeBusyTimeAndSubjectAndLocation</span><span class="sxs-lookup"><span data-stu-id="ce058-147">FreeBusyTimeAndSubjectAndLocation</span></span>  <br/> |<span data-ttu-id="ce058-148">指示用户可以查看忙/闲时间内日历的主题和位置的约会的时间。</span><span class="sxs-lookup"><span data-stu-id="ce058-148">Indicates that the user can view free/busy time within the calendar and the subject and location of appointments.</span></span>  <br/> |
|<span data-ttu-id="ce058-149">自定义</span><span class="sxs-lookup"><span data-stu-id="ce058-149">Custom</span></span>  <br/> |<span data-ttu-id="ce058-150">指示用户具有自定义访问权限的文件夹。</span><span class="sxs-lookup"><span data-stu-id="ce058-150">Indicates that the user has custom access permissions on the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce058-151">备注</span><span class="sxs-lookup"><span data-stu-id="ce058-151">Remarks</span></span>

<span data-ttu-id="ce058-152">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ce058-152">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce058-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="ce058-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce058-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="ce058-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ce058-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="ce058-155">Schema Name</span></span>  <br/> |<span data-ttu-id="ce058-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="ce058-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="ce058-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="ce058-157">Validation File</span></span>  <br/> |<span data-ttu-id="ce058-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ce058-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ce058-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="ce058-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce058-160">False</span><span class="sxs-lookup"><span data-stu-id="ce058-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce058-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce058-161">See also</span></span>



- [<span data-ttu-id="ce058-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ce058-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ce058-163">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ce058-163">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

