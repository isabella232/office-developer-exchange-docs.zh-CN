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
description: Permissions 元素包含权限的文件夹的集合。
ms.openlocfilehash: 08d015c3b1afb58fce0fb4b99466965cc5c29fc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826727"
---
# <a name="permissions"></a><span data-ttu-id="cbf9b-103">权限</span><span class="sxs-lookup"><span data-stu-id="cbf9b-103">Permissions</span></span>

<span data-ttu-id="cbf9b-104">**Permissions**元素包含权限的文件夹的集合。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-104">The **Permissions** element contains the collection of permissions for a folder.</span></span> 
  
```XML
<Permissions>
   <Permission/>
</Permissions>
```

 <span data-ttu-id="cbf9b-105">**PermissionType**</span><span class="sxs-lookup"><span data-stu-id="cbf9b-105">**PermissionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbf9b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbf9b-106">Attributes and elements</span></span>

<span data-ttu-id="cbf9b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbf9b-108">属性</span><span class="sxs-lookup"><span data-stu-id="cbf9b-108">Attributes</span></span>

<span data-ttu-id="cbf9b-109">无。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbf9b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cbf9b-110">Child elements</span></span>

|<span data-ttu-id="cbf9b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbf9b-111">**Element**</span></span>|<span data-ttu-id="cbf9b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbf9b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbf9b-113">权限</span><span class="sxs-lookup"><span data-stu-id="cbf9b-113">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="cbf9b-114">到文件夹中定义的代理人的访问权限。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-114">Defines the access that a delegate has to a folder.</span></span> <span data-ttu-id="cbf9b-115">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbf9b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="cbf9b-116">Parent elements</span></span>

|<span data-ttu-id="cbf9b-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbf9b-117">**Element**</span></span>|<span data-ttu-id="cbf9b-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbf9b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbf9b-119">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="cbf9b-119">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="cbf9b-120">包含所有配置的文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-120">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="cbf9b-121">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbf9b-122">备注</span><span class="sxs-lookup"><span data-stu-id="cbf9b-122">Remarks</span></span>

<span data-ttu-id="cbf9b-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="cbf9b-124">此元素是在 Exchange Server 2007 Service Pack 1 (SP1) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-124">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="cbf9b-125">版本差异</span><span class="sxs-lookup"><span data-stu-id="cbf9b-125">Version differences</span></span>

<span data-ttu-id="cbf9b-126">应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-126">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="cbf9b-127">若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="cbf9b-127">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cbf9b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbf9b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbf9b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbf9b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cbf9b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbf9b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="cbf9b-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="cbf9b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="cbf9b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbf9b-132">Validation File</span></span>  <br/> |<span data-ttu-id="cbf9b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cbf9b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cbf9b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbf9b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbf9b-135">False</span><span class="sxs-lookup"><span data-stu-id="cbf9b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbf9b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbf9b-136">See also</span></span>



- [<span data-ttu-id="cbf9b-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cbf9b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="cbf9b-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="cbf9b-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

