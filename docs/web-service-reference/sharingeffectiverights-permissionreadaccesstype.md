---
title: SharingEffectiveRights (PermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: SharingEffectiveRights 元素指示用户对要共享的联系人数据所具有的权限。
ms.openlocfilehash: 64b1e6d831068e9699e9cd47693e74919e0416a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526660"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="a808e-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="a808e-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="a808e-104">**SharingEffectiveRights**元素指示用户对要共享的联系人数据所具有的权限。</span><span class="sxs-lookup"><span data-stu-id="a808e-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="a808e-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="a808e-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a808e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a808e-106">Attributes and elements</span></span>

<span data-ttu-id="a808e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a808e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a808e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a808e-108">Attributes</span></span>

<span data-ttu-id="a808e-109">无。</span><span class="sxs-lookup"><span data-stu-id="a808e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a808e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a808e-110">Child elements</span></span>

<span data-ttu-id="a808e-111">无。</span><span class="sxs-lookup"><span data-stu-id="a808e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a808e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a808e-112">Parent elements</span></span>

|<span data-ttu-id="a808e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a808e-113">**Element**</span></span>|<span data-ttu-id="a808e-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="a808e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a808e-115">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="a808e-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="a808e-116">表示邮箱中包含的 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="a808e-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a808e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a808e-117">Text value</span></span>

<span data-ttu-id="a808e-118">下表列出了**SharingEffectiveRights**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="a808e-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="a808e-119">**SharingEffectiveRights 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="a808e-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="a808e-120">**值**</span><span class="sxs-lookup"><span data-stu-id="a808e-120">**Value**</span></span>|<span data-ttu-id="a808e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a808e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a808e-122">无</span><span class="sxs-lookup"><span data-stu-id="a808e-122">None</span></span>  <br/> |<span data-ttu-id="a808e-123">指示用户没有读取文件夹中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="a808e-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="a808e-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="a808e-124">FullDetails</span></span>  <br/> |<span data-ttu-id="a808e-125">指示用户有权读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="a808e-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a808e-126">说明</span><span class="sxs-lookup"><span data-stu-id="a808e-126">Remarks</span></span>

<span data-ttu-id="a808e-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a808e-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a808e-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="a808e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a808e-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="a808e-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a808e-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="a808e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a808e-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="a808e-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a808e-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="a808e-132">Validation File</span></span>  <br/> |<span data-ttu-id="a808e-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a808e-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a808e-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="a808e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a808e-135">False</span><span class="sxs-lookup"><span data-stu-id="a808e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a808e-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a808e-136">See also</span></span>



- [<span data-ttu-id="a808e-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a808e-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

