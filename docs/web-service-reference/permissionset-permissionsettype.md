---
title: PermissionSet (PermissionSetType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermissionSet
api_type:
- schema
ms.assetid: 6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d
description: PermissionSet 元素包含为文件夹配置的所有权限。
ms.openlocfilehash: 5639ee8ba64742f39c0274f4e3aaa76d75bea42b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468129"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="5e608-103">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="5e608-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="5e608-104">**PermissionSet**元素包含为文件夹配置的所有权限。</span><span class="sxs-lookup"><span data-stu-id="5e608-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="5e608-105">**PermissionSetType**</span><span class="sxs-lookup"><span data-stu-id="5e608-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e608-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5e608-106">Attributes and elements</span></span>

<span data-ttu-id="5e608-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5e608-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e608-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5e608-108">Attributes</span></span>

<span data-ttu-id="5e608-109">无。</span><span class="sxs-lookup"><span data-stu-id="5e608-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5e608-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5e608-110">Child elements</span></span>

|<span data-ttu-id="5e608-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e608-111">**Element**</span></span>|<span data-ttu-id="5e608-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e608-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e608-113">权限</span><span class="sxs-lookup"><span data-stu-id="5e608-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="5e608-114">包含文件夹的权限集。</span><span class="sxs-lookup"><span data-stu-id="5e608-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="5e608-115">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5e608-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="5e608-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="5e608-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="5e608-117">包含无法针对 Active Directory 目录服务解析的未知条目数组。</span><span class="sxs-lookup"><span data-stu-id="5e608-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="5e608-118">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5e608-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5e608-119">父元素</span><span class="sxs-lookup"><span data-stu-id="5e608-119">Parent elements</span></span>

|<span data-ttu-id="5e608-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="5e608-120">**Element**</span></span>|<span data-ttu-id="5e608-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="5e608-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e608-122">Folder</span><span class="sxs-lookup"><span data-stu-id="5e608-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="5e608-123">定义要创建、获取、查找、同步或更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5e608-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="5e608-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5e608-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="5e608-125">表示邮箱中包含的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5e608-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5e608-126">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="5e608-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="5e608-127">表示邮箱中包含的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5e608-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5e608-128">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="5e608-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="5e608-129">表示邮箱中包含的 "任务" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5e608-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e608-130">说明</span><span class="sxs-lookup"><span data-stu-id="5e608-130">Remarks</span></span>

<span data-ttu-id="5e608-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5e608-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="5e608-132">此元素是在 Exchange Server 2007 Service Pack 1 （SP1）中引入的。</span><span class="sxs-lookup"><span data-stu-id="5e608-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="5e608-133">版本差异</span><span class="sxs-lookup"><span data-stu-id="5e608-133">Version differences</span></span>

<span data-ttu-id="5e608-134">对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="5e608-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="5e608-135">若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5e608-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5e608-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="5e608-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e608-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="5e608-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5e608-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="5e608-138">Schema Name</span></span>  <br/> |<span data-ttu-id="5e608-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="5e608-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="5e608-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="5e608-140">Validation File</span></span>  <br/> |<span data-ttu-id="5e608-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5e608-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5e608-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="5e608-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e608-143">False</span><span class="sxs-lookup"><span data-stu-id="5e608-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e608-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5e608-144">See also</span></span>



- [<span data-ttu-id="5e608-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5e608-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5e608-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="5e608-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

