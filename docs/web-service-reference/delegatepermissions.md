---
title: DelegatePermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DelegatePermissions
api_type:
- schema
ms.assetid: 292badc7-bab3-4368-9d7c-9a8b7edb279b
description: DelegatePermissions 元素包含用户的委派权限级别设置。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 319592b6c3386a07b3094115c335c7fb8ffe1130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753776"
---
# <a name="delegatepermissions"></a><span data-ttu-id="12ca4-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="12ca4-104">DelegatePermissions</span></span>

<span data-ttu-id="12ca4-105">**DelegatePermissions**元素包含用户的委派权限级别设置。</span><span class="sxs-lookup"><span data-stu-id="12ca4-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="12ca4-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<DelegatePermissions>
   <CalendarFolderPermissionLevel/>
   <TasksFolderPermissionLevel/>
   <InboxFolderPermissionLevel/>
   <ContactsFolderPermissionLevel/>
   <NotesFolderPermissionLevel/>
   <JournalFolderPermissionLevel/>
</DelegatePermissions>
```

<span data-ttu-id="12ca4-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="12ca4-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="12ca4-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="12ca4-108">Attributes and elements</span></span>

<span data-ttu-id="12ca4-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12ca4-110">属性</span><span class="sxs-lookup"><span data-stu-id="12ca4-110">Attributes</span></span>

<span data-ttu-id="12ca4-111">无。</span><span class="sxs-lookup"><span data-stu-id="12ca4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12ca4-112">子元素</span><span class="sxs-lookup"><span data-stu-id="12ca4-112">Child elements</span></span>

|<span data-ttu-id="12ca4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="12ca4-113">**Element**</span></span>|<span data-ttu-id="12ca4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="12ca4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12ca4-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-116">包含默认日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="12ca4-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="12ca4-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-119">包含的默认任务文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="12ca4-120">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="12ca4-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-122">包含默认收件箱文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="12ca4-123">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="12ca4-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-125">包含默认联系人文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="12ca4-126">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="12ca4-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-128">包含默认便笺文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="12ca4-129">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="12ca4-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="12ca4-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="12ca4-131">包含默认的日记文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="12ca4-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="12ca4-132">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12ca4-133">父元素</span><span class="sxs-lookup"><span data-stu-id="12ca4-133">Parent elements</span></span>

|<span data-ttu-id="12ca4-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="12ca4-134">**Element**</span></span>|<span data-ttu-id="12ca4-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="12ca4-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12ca4-136">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="12ca4-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="12ca4-137">标识要添加或更新的邮箱中的单个委托。</span><span class="sxs-lookup"><span data-stu-id="12ca4-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="12ca4-138">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12ca4-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12ca4-139">备注</span><span class="sxs-lookup"><span data-stu-id="12ca4-139">Remarks</span></span>

<span data-ttu-id="12ca4-140">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="12ca4-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12ca4-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="12ca4-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12ca4-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="12ca4-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12ca4-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="12ca4-143">Schema Name</span></span>  <br/> |<span data-ttu-id="12ca4-144">类型架构</span><span class="sxs-lookup"><span data-stu-id="12ca4-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="12ca4-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="12ca4-145">Validation File</span></span>  <br/> |<span data-ttu-id="12ca4-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="12ca4-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="12ca4-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="12ca4-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="12ca4-148">False</span><span class="sxs-lookup"><span data-stu-id="12ca4-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12ca4-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12ca4-149">See also</span></span>

- [<span data-ttu-id="12ca4-150">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="12ca4-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="12ca4-151">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="12ca4-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="12ca4-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="12ca4-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="12ca4-153">添加代理人</span><span class="sxs-lookup"><span data-stu-id="12ca4-153">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

