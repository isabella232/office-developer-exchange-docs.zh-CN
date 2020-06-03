---
title: ReadItems （PermissionType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadItems
api_type:
- schema
ms.assetid: 0a11a802-28e2-436b-b5a9-30fd064675a6
description: ReadItems 元素指示用户是否有权读取文件夹中的项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: af6ef5107b5e4f2b3071c0bc9b4b528efea6dcca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468269"
---
# <a name="readitems-permissiontype"></a><span data-ttu-id="295a6-104">ReadItems （PermissionType）</span><span class="sxs-lookup"><span data-stu-id="295a6-104">ReadItems (PermissionType)</span></span>

<span data-ttu-id="295a6-105">**ReadItems**元素指示用户是否有权读取文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="295a6-105">The **ReadItems** element indicates whether a user has permission to read items within a folder.</span></span> <span data-ttu-id="295a6-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="295a6-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReadItems>None or FullDetails</ReadItems>
```

 <span data-ttu-id="295a6-107">**PermissionReadAccessType**</span><span class="sxs-lookup"><span data-stu-id="295a6-107">**PermissionReadAccessType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="295a6-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="295a6-108">Attributes and elements</span></span>

<span data-ttu-id="295a6-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="295a6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="295a6-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="295a6-110">Attributes</span></span>

<span data-ttu-id="295a6-111">无。</span><span class="sxs-lookup"><span data-stu-id="295a6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="295a6-112">子元素</span><span class="sxs-lookup"><span data-stu-id="295a6-112">Child elements</span></span>

<span data-ttu-id="295a6-113">无。</span><span class="sxs-lookup"><span data-stu-id="295a6-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="295a6-114">父元素</span><span class="sxs-lookup"><span data-stu-id="295a6-114">Parent elements</span></span>

|<span data-ttu-id="295a6-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="295a6-115">**Element**</span></span>|<span data-ttu-id="295a6-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="295a6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="295a6-117">权限</span><span class="sxs-lookup"><span data-stu-id="295a6-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="295a6-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="295a6-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="295a6-120">文本值</span><span class="sxs-lookup"><span data-stu-id="295a6-120">Text value</span></span>

<span data-ttu-id="295a6-121">下表列出了**ReadItems**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="295a6-121">The following table lists the possible values for the **ReadItems** element.</span></span> 
  
<span data-ttu-id="295a6-122">**ReadItems 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="295a6-122">**ReadItems element text values**</span></span>

|<span data-ttu-id="295a6-123">**值**</span><span class="sxs-lookup"><span data-stu-id="295a6-123">**Value**</span></span>|<span data-ttu-id="295a6-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="295a6-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="295a6-125">无</span><span class="sxs-lookup"><span data-stu-id="295a6-125">None</span></span>  <br/> |<span data-ttu-id="295a6-126">指示用户没有读取文件夹中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="295a6-126">Indicates that the user does not have permission to read items in the folder.</span></span>  <br/> |
|<span data-ttu-id="295a6-127">FullDetails</span><span class="sxs-lookup"><span data-stu-id="295a6-127">FullDetails</span></span>  <br/> |<span data-ttu-id="295a6-128">指示用户有权读取文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="295a6-128">Indicates that the user has permission to read all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="295a6-129">说明</span><span class="sxs-lookup"><span data-stu-id="295a6-129">Remarks</span></span>

<span data-ttu-id="295a6-130">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="295a6-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="295a6-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="295a6-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="295a6-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="295a6-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="295a6-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="295a6-133">Schema Name</span></span>  <br/> |<span data-ttu-id="295a6-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="295a6-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="295a6-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="295a6-135">Validation File</span></span>  <br/> |<span data-ttu-id="295a6-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="295a6-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="295a6-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="295a6-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="295a6-138">False</span><span class="sxs-lookup"><span data-stu-id="295a6-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="295a6-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="295a6-139">See also</span></span>



- [<span data-ttu-id="295a6-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="295a6-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="295a6-141">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="295a6-141">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

