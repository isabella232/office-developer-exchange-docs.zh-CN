---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: UnknownEntries 元素包含无法针对 Active Directory 目录服务解析的未知权限条目数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 68cb2518b895ca0a74e6b9ed649ee92b7502ab05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459417"
---
# <a name="unknownentries"></a><span data-ttu-id="599a6-104">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="599a6-104">UnknownEntries</span></span>

<span data-ttu-id="599a6-105">**UnknownEntries**元素包含无法针对 Active directory 目录服务解析的未知权限条目数组。</span><span class="sxs-lookup"><span data-stu-id="599a6-105">The **UnknownEntries** element contains an array of unknown permission entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="599a6-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="599a6-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 <span data-ttu-id="599a6-107">**ArrayOfUnknownEntriesType**</span><span class="sxs-lookup"><span data-stu-id="599a6-107">**ArrayOfUnknownEntriesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="599a6-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="599a6-108">Attributes and elements</span></span>

<span data-ttu-id="599a6-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="599a6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="599a6-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="599a6-110">Attributes</span></span>

<span data-ttu-id="599a6-111">无。</span><span class="sxs-lookup"><span data-stu-id="599a6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="599a6-112">子元素</span><span class="sxs-lookup"><span data-stu-id="599a6-112">Child elements</span></span>

|<span data-ttu-id="599a6-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="599a6-113">**Element**</span></span>|<span data-ttu-id="599a6-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="599a6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599a6-115">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="599a6-115">UnknownEntry</span></span>](unknownentry.md) <br/> |<span data-ttu-id="599a6-116">代表单个无法对 Active Directory 进行解析的未知权限条目。</span><span class="sxs-lookup"><span data-stu-id="599a6-116">Represents a single unknown permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="599a6-117">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="599a6-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="599a6-118">父元素</span><span class="sxs-lookup"><span data-stu-id="599a6-118">Parent elements</span></span>

|<span data-ttu-id="599a6-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="599a6-119">**Element**</span></span>|<span data-ttu-id="599a6-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="599a6-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599a6-121">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="599a6-121">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="599a6-122">包含为文件夹配置的所有权限。</span><span class="sxs-lookup"><span data-stu-id="599a6-122">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="599a6-123">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="599a6-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="599a6-124">PermissionSet （CalendarPermissionSetType）</span><span class="sxs-lookup"><span data-stu-id="599a6-124">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="599a6-125">包含为 "日历" 文件夹配置的所有权限。</span><span class="sxs-lookup"><span data-stu-id="599a6-125">Contains all the permissions that are configured for a calendar folder.</span></span> <span data-ttu-id="599a6-126">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="599a6-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="599a6-127">备注</span><span class="sxs-lookup"><span data-stu-id="599a6-127">Remarks</span></span>

<span data-ttu-id="599a6-128">您可以通过将 UpdateFolder 操作与[SetFolderField](setfolderfield.md)元素一起使用，从文件夹中删除未知条目。</span><span class="sxs-lookup"><span data-stu-id="599a6-128">You can delete unknown entries from a folder by using the UpdateFolder operation with the [SetFolderField](setfolderfield.md) element.</span></span> <span data-ttu-id="599a6-129">使用 UpdateFolder 操作的 SetFolderField 选项重置 PermissionSet 时，将删除未知的条目。</span><span class="sxs-lookup"><span data-stu-id="599a6-129">The unknown entries are deleted when you reset the PermissionSet by using the SetFolderField option of the UpdateFolder operation.</span></span> <span data-ttu-id="599a6-130">Exchange Web 服务不支持删除单个条目。</span><span class="sxs-lookup"><span data-stu-id="599a6-130">Exchange Web Services does not support the deletion of individual entries.</span></span> 
  
<span data-ttu-id="599a6-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="599a6-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="599a6-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="599a6-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="599a6-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="599a6-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="599a6-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="599a6-134">Schema Name</span></span>  <br/> |<span data-ttu-id="599a6-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="599a6-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="599a6-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="599a6-136">Validation File</span></span>  <br/> |<span data-ttu-id="599a6-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="599a6-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="599a6-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="599a6-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="599a6-139">False</span><span class="sxs-lookup"><span data-stu-id="599a6-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="599a6-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="599a6-140">See also</span></span>



[<span data-ttu-id="599a6-141">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="599a6-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="599a6-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="599a6-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="599a6-143">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="599a6-143">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

