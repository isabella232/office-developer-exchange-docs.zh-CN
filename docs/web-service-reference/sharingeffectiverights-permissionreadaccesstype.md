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
description: SharingEffectiveRights 元素指示用户拥有的联系人数据的共享的权限。
ms.openlocfilehash: 19e67827dd2dbff6fb70423980d670da5cc257a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827486"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a><span data-ttu-id="4266f-103">SharingEffectiveRights (PermissionReadAccessType)</span><span class="sxs-lookup"><span data-stu-id="4266f-103">SharingEffectiveRights (PermissionReadAccessType)</span></span>

<span data-ttu-id="4266f-104">**SharingEffectiveRights**元素指示用户拥有的联系人数据的共享的权限。</span><span class="sxs-lookup"><span data-stu-id="4266f-104">The **SharingEffectiveRights** element indicates the permissions that the user has for the contact data that is being shared.</span></span> 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 <span data-ttu-id="4266f-105">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="4266f-105">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4266f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4266f-106">Attributes and elements</span></span>

<span data-ttu-id="4266f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4266f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4266f-108">属性</span><span class="sxs-lookup"><span data-stu-id="4266f-108">Attributes</span></span>

<span data-ttu-id="4266f-109">无。</span><span class="sxs-lookup"><span data-stu-id="4266f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4266f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4266f-110">Child elements</span></span>

<span data-ttu-id="4266f-111">无。</span><span class="sxs-lookup"><span data-stu-id="4266f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4266f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4266f-112">Parent elements</span></span>

|<span data-ttu-id="4266f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4266f-113">**Element**</span></span>|<span data-ttu-id="4266f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4266f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4266f-115">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="4266f-115">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="4266f-116">表示包含在邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="4266f-116">Represents a Contacts folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4266f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="4266f-117">Text value</span></span>

<span data-ttu-id="4266f-118">下表列出了**SharingEffectiveRights**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="4266f-118">The following table lists the possible values for the **SharingEffectiveRights** element.</span></span> 
  
<span data-ttu-id="4266f-119">**SharingEffectiveRights 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="4266f-119">**SharingEffectiveRights element text values**</span></span>

|<span data-ttu-id="4266f-120">**值**</span><span class="sxs-lookup"><span data-stu-id="4266f-120">**Value**</span></span>|<span data-ttu-id="4266f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="4266f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4266f-122">无</span><span class="sxs-lookup"><span data-stu-id="4266f-122">None</span></span>  <br/> |<span data-ttu-id="4266f-123">指示用户没有读取文件夹中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="4266f-123">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="4266f-124">FullDetails</span><span class="sxs-lookup"><span data-stu-id="4266f-124">FullDetails</span></span>  <br/> |<span data-ttu-id="4266f-125">指示用户有权读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="4266f-125">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4266f-126">备注</span><span class="sxs-lookup"><span data-stu-id="4266f-126">Remarks</span></span>

<span data-ttu-id="4266f-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4266f-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4266f-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="4266f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4266f-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="4266f-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4266f-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="4266f-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4266f-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="4266f-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="4266f-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="4266f-132">Validation File</span></span>  <br/> |<span data-ttu-id="4266f-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4266f-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4266f-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="4266f-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4266f-135">False</span><span class="sxs-lookup"><span data-stu-id="4266f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4266f-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4266f-136">See also</span></span>



- [<span data-ttu-id="4266f-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4266f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

