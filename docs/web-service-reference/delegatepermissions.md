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
description: DelegatePermissions 元素包含用户的委派权限级别设置。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 2cf8c9a8d3c5db8e13d43c207df173c12fca5acb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457408"
---
# <a name="delegatepermissions"></a><span data-ttu-id="ab251-104">DelegatePermissions</span><span class="sxs-lookup"><span data-stu-id="ab251-104">DelegatePermissions</span></span>

<span data-ttu-id="ab251-105">**DelegatePermissions**元素包含用户的委派权限级别设置。</span><span class="sxs-lookup"><span data-stu-id="ab251-105">The **DelegatePermissions** element contains the delegate permission-level settings for a user.</span></span> <span data-ttu-id="ab251-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
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

<span data-ttu-id="ab251-107">**DelegatePermissionsType**</span><span class="sxs-lookup"><span data-stu-id="ab251-107">**DelegatePermissionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ab251-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ab251-108">Attributes and elements</span></span>

<span data-ttu-id="ab251-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab251-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="ab251-110">Attributes</span></span>

<span data-ttu-id="ab251-111">无。</span><span class="sxs-lookup"><span data-stu-id="ab251-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab251-112">子元素</span><span class="sxs-lookup"><span data-stu-id="ab251-112">Child elements</span></span>

|<span data-ttu-id="ab251-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ab251-113">**Element**</span></span>|<span data-ttu-id="ab251-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ab251-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab251-115">CalendarFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-115">CalendarFolderPermissionLevel</span></span>](calendarfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-116">包含默认 "日历" 文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-116">Contains the permissions for the default Calendar folder.</span></span> <span data-ttu-id="ab251-117">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ab251-118">TasksFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-118">TasksFolderPermissionLevel</span></span>](tasksfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-119">包含默认的任务文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-119">Contains the permissions for the default Task folder.</span></span> <span data-ttu-id="ab251-120">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ab251-121">InboxFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-121">InboxFolderPermissionLevel</span></span>](inboxfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-122">包含默认 "收件箱" 文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-122">Contains the permissions for the default Inbox folder.</span></span> <span data-ttu-id="ab251-123">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ab251-124">ContactsFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-124">ContactsFolderPermissionLevel</span></span>](contactsfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-125">包含默认 "联系人" 文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-125">Contains the permissions for the default Contacts folder.</span></span> <span data-ttu-id="ab251-126">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ab251-127">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-127">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-128">包含默认 "便笺" 文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-128">Contains the permissions for the default Notes folder.</span></span> <span data-ttu-id="ab251-129">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-129">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ab251-130">JournalFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="ab251-130">JournalFolderPermissionLevel</span></span>](journalfolderpermissionlevel.md) <br/> |<span data-ttu-id="ab251-131">包含默认日记文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ab251-131">Contains the permissions for the default Journal folder.</span></span> <span data-ttu-id="ab251-132">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-132">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab251-133">父元素</span><span class="sxs-lookup"><span data-stu-id="ab251-133">Parent elements</span></span>

|<span data-ttu-id="ab251-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="ab251-134">**Element**</span></span>|<span data-ttu-id="ab251-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="ab251-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab251-136">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="ab251-136">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="ab251-137">标识要在邮箱中添加或更新的单个代理。</span><span class="sxs-lookup"><span data-stu-id="ab251-137">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="ab251-138">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ab251-138">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab251-139">说明</span><span class="sxs-lookup"><span data-stu-id="ab251-139">Remarks</span></span>

<span data-ttu-id="ab251-140">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ab251-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab251-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="ab251-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab251-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="ab251-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab251-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="ab251-143">Schema Name</span></span>  <br/> |<span data-ttu-id="ab251-144">类型架构</span><span class="sxs-lookup"><span data-stu-id="ab251-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab251-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="ab251-145">Validation File</span></span>  <br/> |<span data-ttu-id="ab251-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ab251-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab251-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="ab251-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab251-148">False</span><span class="sxs-lookup"><span data-stu-id="ab251-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab251-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ab251-149">See also</span></span>

- [<span data-ttu-id="ab251-150">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ab251-150">AddDelegate operation</span></span>](adddelegate-operation.md) 
- [<span data-ttu-id="ab251-151">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="ab251-151">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
- [<span data-ttu-id="ab251-152">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ab251-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="ab251-153">添加委派</span><span class="sxs-lookup"><span data-stu-id="ab251-153">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

