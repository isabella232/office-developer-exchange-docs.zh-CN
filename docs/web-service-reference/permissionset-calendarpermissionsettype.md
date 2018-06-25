---
title: PermissionSet (CalendarPermissionSetType)
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
description: PermissionSet 元素包含所有配置的日历文件夹的权限。
ms.openlocfilehash: b2e642fd2ee8ded4d0d4c67509a5587f7b1efa8a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826728"
---
# <a name="permissionset-calendarpermissionsettype"></a><span data-ttu-id="1fbe3-103">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="1fbe3-103">PermissionSet (CalendarPermissionSetType)</span></span>

<span data-ttu-id="1fbe3-104">**PermissionSet**元素包含所有配置的日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-104">The **PermissionSet** element contains all the permissions that are configured for a calendar folder.</span></span> 
  
```XML
<PermissionSet>
   <CalendarPermissions/>
   <UnknownEntries/>
</PermissionSet>
```

 <span data-ttu-id="1fbe3-105">**CalendarPermissonSetType**</span><span class="sxs-lookup"><span data-stu-id="1fbe3-105">**CalendarPermissonSetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1fbe3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1fbe3-106">Attributes and elements</span></span>

<span data-ttu-id="1fbe3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1fbe3-108">属性</span><span class="sxs-lookup"><span data-stu-id="1fbe3-108">Attributes</span></span>

<span data-ttu-id="1fbe3-109">无。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1fbe3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1fbe3-110">Child elements</span></span>

|<span data-ttu-id="1fbe3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1fbe3-111">**Element**</span></span>|<span data-ttu-id="1fbe3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1fbe3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fbe3-113">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="1fbe3-113">CalendarPermissions</span></span>](calendarpermissions.md) <br/> |<span data-ttu-id="1fbe3-114">包含数组的日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-114">Contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="1fbe3-115">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-115">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="1fbe3-116">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="1fbe3-116">UnknownEntries</span></span>](unknownentries.md) <br/> |<span data-ttu-id="1fbe3-117">包含针对 Active Directory 目录服务无法解析的未知条目的数组。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-117">Contains an array of unknown entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="1fbe3-118">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-118">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1fbe3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1fbe3-119">Parent elements</span></span>

|<span data-ttu-id="1fbe3-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="1fbe3-120">**Element**</span></span>|<span data-ttu-id="1fbe3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1fbe3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fbe3-122">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="1fbe3-122">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="1fbe3-123">表示主要包含日历项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-123">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fbe3-124">备注</span><span class="sxs-lookup"><span data-stu-id="1fbe3-124">Remarks</span></span>

<span data-ttu-id="1fbe3-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="1fbe3-126">此元素是在 Exchange Server 2007 Service Pack 1 (SP1) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-126">This element was introduced in Exchange Server 2007 Service Pack 1 (SP1).</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="1fbe3-127">版本差异</span><span class="sxs-lookup"><span data-stu-id="1fbe3-127">Version differences</span></span>

<span data-ttu-id="1fbe3-128">应用程序面向 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 开头 Exchange 2013 的本地版本文件夹权限不返回时[BaseShape](baseshape.md)元素的值为**AllProperties**在[GetFolder](getfolder-operation.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-128">For applications that target Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013, folder permissions are not returned when the [BaseShape](baseshape.md) element has a value of **AllProperties** in the [GetFolder](getfolder-operation.md) operation request.</span></span> <span data-ttu-id="1fbe3-129">若要检索文件夹权限，请向**GetFolder**请求中[AdditionalProperties](additionalproperties.md) element 中添加[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="1fbe3-129">To retrieve folder permissions, add the [PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) element to the [AdditionalProperties](additionalproperties.md) element in the **GetFolder** request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1fbe3-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="1fbe3-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fbe3-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="1fbe3-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1fbe3-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="1fbe3-132">Schema Name</span></span>  <br/> |<span data-ttu-id="1fbe3-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="1fbe3-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1fbe3-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="1fbe3-134">Validation File</span></span>  <br/> |<span data-ttu-id="1fbe3-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1fbe3-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1fbe3-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="1fbe3-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="1fbe3-137">False</span><span class="sxs-lookup"><span data-stu-id="1fbe3-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fbe3-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1fbe3-138">See also</span></span>



- [<span data-ttu-id="1fbe3-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1fbe3-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1fbe3-140">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="1fbe3-140">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

