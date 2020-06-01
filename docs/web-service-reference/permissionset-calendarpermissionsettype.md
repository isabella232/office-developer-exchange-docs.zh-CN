---
title: PermissionSet （CalendarPermissionSetType）
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
ms.assetid: 75f20033-85eb-4627-b4f8-be85e4889e96
description: PermissionSet 元素包含为 "日历" 文件夹配置的所有权限。
ms.openlocfilehash: 9564608397ac8a5ab0ddd4508eacd8cad665d76e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458031"
---
# <a name="permissionset-calendarpermissionsettype"></a><span data-ttu-id="d176e-103">PermissionSet （CalendarPermissionSetType）</span><span class="sxs-lookup"><span data-stu-id="d176e-103">PermissionSet (CalendarPermissionSetType)</span></span>

<span data-ttu-id="d176e-104">**PermissionSet**元素包含为 "日历" 文件夹配置的所有权限。</span><span class="sxs-lookup"><span data-stu-id="d176e-104">The **PermissionSet** element contains all the permissions that are configured for a calendar folder.</span></span> 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="d176e-105">**CalendarPermissonSetType**</span><span class="sxs-lookup"><span data-stu-id="d176e-105">**CalendarPermissonSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d176e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d176e-106">Attributes and elements</span></span>

<span data-ttu-id="d176e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d176e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d176e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d176e-108">Attributes</span></span>

<span data-ttu-id="d176e-109">无。</span><span class="sxs-lookup"><span data-stu-id="d176e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d176e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d176e-110">Child elements</span></span>

|<span data-ttu-id="d176e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d176e-111">**Element**</span></span>|<span data-ttu-id="d176e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d176e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d176e-113">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="d176e-113">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="d176e-114">包含文件夹的日历权限数组。</span><span class="sxs-lookup"><span data-stu-id="d176e-114">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="d176e-115">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d176e-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d176e-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="d176e-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="d176e-117">包含无法针对 Active Directory 目录服务解析的未知条目数组。</span><span class="sxs-lookup"><span data-stu-id="d176e-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="d176e-118">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d176e-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d176e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d176e-119">Parent elements</span></span>

|<span data-ttu-id="d176e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="d176e-120">**Element**</span></span>|<span data-ttu-id="d176e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="d176e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d176e-122">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="d176e-122">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="d176e-123">代表主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d176e-123">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d176e-124">说明</span><span class="sxs-lookup"><span data-stu-id="d176e-124">Remarks</span></span>

<span data-ttu-id="d176e-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d176e-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d176e-126">此元素是在 Exchange Server 2007 Service Pack 1 （SP1）中引入的。</span><span class="sxs-lookup"><span data-stu-id="d176e-126">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="d176e-127">版本差异</span><span class="sxs-lookup"><span data-stu-id="d176e-127">Version differences</span></span>

<span data-ttu-id="d176e-128">对于面向 Exchange Online 的应用程序，Exchange Online 作为 Office 365 的一部分，或从 Exchange 2013 开始的 Exchange 内部部署版本，当[BaseShape](baseshape.md)元素的[GetFolder](getfolder-operation.md)操作请求中的值为**AllProperties**时，不会返回文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="d176e-128">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="d176e-129">若要检索文件夹权限，请将[PermissionSet （PermissionSetType）](permissionset-permissionsettype.md)元素添加到**GetFolder**请求中的[AdditionalProperties](additionalproperties.md)元素。</span><span class="sxs-lookup"><span data-stu-id="d176e-129">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d176e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="d176e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d176e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="d176e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d176e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="d176e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d176e-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="d176e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d176e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="d176e-134">Validation File</span></span>  <br/> |<span data-ttu-id="d176e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d176e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d176e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="d176e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d176e-137">False</span><span class="sxs-lookup"><span data-stu-id="d176e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d176e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d176e-138">See also</span></span>



- [<span data-ttu-id="d176e-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d176e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d176e-140">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="d176e-140">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

