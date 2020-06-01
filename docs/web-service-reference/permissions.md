---
title: 权限
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Permissions
api_type:
- schema
ms.assetid: 2ba50bd9-819f-4e5f-a3bb-85a0a87d8a86
description: 权限元素包含文件夹权限的集合。
ms.openlocfilehash: b8616cefdb8c453106753fb0788a6c7d6a0ded79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459214"
---
# <a name="permissions"></a><span data-ttu-id="25dd3-103">权限</span><span class="sxs-lookup"><span data-stu-id="25dd3-103">Permissions</span></span>

<span data-ttu-id="25dd3-104">**权限**元素包含文件夹权限的集合。</span><span class="sxs-lookup"><span data-stu-id="25dd3-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="25dd3-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="25dd3-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25dd3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="25dd3-106">Attributes and elements</span></span>

<span data-ttu-id="25dd3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="25dd3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25dd3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="25dd3-108">Attributes</span></span>

<span data-ttu-id="25dd3-109">无。</span><span class="sxs-lookup"><span data-stu-id="25dd3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25dd3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="25dd3-110">Child elements</span></span>

|<span data-ttu-id="25dd3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="25dd3-111">**Element**</span></span>|<span data-ttu-id="25dd3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="25dd3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25dd3-113">权限</span><span class="sxs-lookup"><span data-stu-id="25dd3-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="25dd3-114">定义代理对文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="25dd3-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="25dd3-115">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="25dd3-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25dd3-116">父元素</span><span class="sxs-lookup"><span data-stu-id="25dd3-116">Parent elements</span></span>

|<span data-ttu-id="25dd3-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="25dd3-117">**Element**</span></span>|<span data-ttu-id="25dd3-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="25dd3-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25dd3-119">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="25dd3-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="25dd3-120">包含为文件夹配置的所有权限。</span><span class="sxs-lookup"><span data-stu-id="25dd3-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="25dd3-121">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="25dd3-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25dd3-122">说明</span><span class="sxs-lookup"><span data-stu-id="25dd3-122">Remarks</span></span>

<span data-ttu-id="25dd3-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="25dd3-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="25dd3-124">此元素是在 Exchange Server 2007 Service Pack 1 （SP1）中引入的。</span><span class="sxs-lookup"><span data-stu-id="25dd3-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="25dd3-125">版本差异</span><span class="sxs-lookup"><span data-stu-id="25dd3-125">Version differences</span></span>

<span data-ttu-id="25dd3-126">对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="25dd3-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="25dd3-127">若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="25dd3-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="25dd3-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="25dd3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25dd3-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="25dd3-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25dd3-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="25dd3-130">Schema Name</span></span>  <br/> |<span data-ttu-id="25dd3-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="25dd3-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="25dd3-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="25dd3-132">Validation File</span></span>  <br/> |<span data-ttu-id="25dd3-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25dd3-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25dd3-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="25dd3-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="25dd3-135">False</span><span class="sxs-lookup"><span data-stu-id="25dd3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25dd3-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="25dd3-136">See also</span></span>



- [<span data-ttu-id="25dd3-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="25dd3-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="25dd3-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="25dd3-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

