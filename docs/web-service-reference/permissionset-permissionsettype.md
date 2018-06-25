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
description: PermissionSet 元素包含所有配置的文件夹的权限。
ms.openlocfilehash: 0fa0ac78a0db2bf382ad413cbb8bd072aa88c6fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826732"
---
# <a name="permissionset-permissionsettype"></a><span data-ttu-id="de97f-103">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="de97f-103">PermissionSet (PermissionSetType)</span></span>

<span data-ttu-id="de97f-104">**PermissionSet**元素包含所有配置的文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="de97f-104">The **PermissionSet** element contains all the permissions that are configured for a folder.</span></span> 
  
```XML
<PermissionSet>
   <Permissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="de97f-105">**PermissionSetType**</span><span class="sxs-lookup"><span data-stu-id="de97f-105">**PermissionSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de97f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="de97f-106">Attributes and elements</span></span>

<span data-ttu-id="de97f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="de97f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de97f-108">属性</span><span class="sxs-lookup"><span data-stu-id="de97f-108">Attributes</span></span>

<span data-ttu-id="de97f-109">无。</span><span class="sxs-lookup"><span data-stu-id="de97f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de97f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="de97f-110">Child elements</span></span>

|<span data-ttu-id="de97f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="de97f-111">**Element**</span></span>|<span data-ttu-id="de97f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="de97f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de97f-113">权限</span><span class="sxs-lookup"><span data-stu-id="de97f-113">Permissions</span></span>](permissions.md) <br/> |<span data-ttu-id="de97f-114">包含的文件夹的权限的集合。</span><span class="sxs-lookup"><span data-stu-id="de97f-114">Contains the collection of permissions for a folder.</span></span> <span data-ttu-id="de97f-115">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="de97f-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="de97f-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="de97f-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="de97f-117">包含针对 Active Directory 目录服务无法解析的未知条目的数组。</span><span class="sxs-lookup"><span data-stu-id="de97f-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="de97f-118">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="de97f-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de97f-119">父元素</span><span class="sxs-lookup"><span data-stu-id="de97f-119">Parent elements</span></span>

|<span data-ttu-id="de97f-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="de97f-120">**Element**</span></span>|<span data-ttu-id="de97f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="de97f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de97f-122">Folder</span><span class="sxs-lookup"><span data-stu-id="de97f-122">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="de97f-123">定义一个文件夹，用于创建、 获取、 查找、 同步，或更新。</span><span class="sxs-lookup"><span data-stu-id="de97f-123">Defines a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="de97f-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="de97f-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="de97f-125">表示包含在邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="de97f-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="de97f-126">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="de97f-126">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="de97f-127">表示包含在邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="de97f-127">Represents a contacts folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="de97f-128">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="de97f-128">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="de97f-129">表示包含在邮箱中的任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="de97f-129">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de97f-130">备注</span><span class="sxs-lookup"><span data-stu-id="de97f-130">Remarks</span></span>

<span data-ttu-id="de97f-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="de97f-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="de97f-132">此元素是在 Exchange Server 2007 Service Pack 1 (SP1) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="de97f-132">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="de97f-133">版本差异</span><span class="sxs-lookup"><span data-stu-id="de97f-133">Version differences</span></span>

<span data-ttu-id="de97f-134">应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="de97f-134">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="de97f-135">若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="de97f-135">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="de97f-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="de97f-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de97f-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="de97f-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de97f-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="de97f-138">Schema Name</span></span>  <br/> |<span data-ttu-id="de97f-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="de97f-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="de97f-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="de97f-140">Validation File</span></span>  <br/> |<span data-ttu-id="de97f-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de97f-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de97f-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="de97f-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="de97f-143">False</span><span class="sxs-lookup"><span data-stu-id="de97f-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de97f-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de97f-144">See also</span></span>



- [<span data-ttu-id="de97f-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="de97f-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="de97f-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="de97f-146">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

