---
title: Delete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: aa45f0c1-a80d-4b6c-8a85-375b6de515f4
description: Delete 元素指示客户端是否可以删除文件夹或项目。
ms.openlocfilehash: 5460f9e49b126ca6b039c6f11aaa3c6eb4a40544
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457352"
---
# <a name="delete"></a><span data-ttu-id="2ea60-103">Delete</span><span class="sxs-lookup"><span data-stu-id="2ea60-103">Delete</span></span>

<span data-ttu-id="2ea60-104">**Delete**元素指示客户端是否可以删除文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="2ea60-104">The **Delete** element indicates whether a client can delete a folder or item.</span></span> 
  
```XML
<Delete>true or false</Delete>
```

<span data-ttu-id="2ea60-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="2ea60-105">**boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2ea60-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ea60-106">Attributes and elements</span></span>

<span data-ttu-id="2ea60-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ea60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ea60-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2ea60-108">Attributes</span></span>

<span data-ttu-id="2ea60-109">无。</span><span class="sxs-lookup"><span data-stu-id="2ea60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ea60-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2ea60-110">Child elements</span></span>

<span data-ttu-id="2ea60-111">无。</span><span class="sxs-lookup"><span data-stu-id="2ea60-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ea60-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2ea60-112">Parent elements</span></span>

|<span data-ttu-id="2ea60-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ea60-113">**Element**</span></span>|<span data-ttu-id="2ea60-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ea60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ea60-115">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="2ea60-115">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="2ea60-116">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="2ea60-116">Contains the rights of the client based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="2ea60-117">操作</span><span class="sxs-lookup"><span data-stu-id="2ea60-117">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="2ea60-118">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="2ea60-118">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ea60-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2ea60-119">Text value</span></span>

<span data-ttu-id="2ea60-120">如果文本值为**true，则**表示客户端可以删除项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="2ea60-120">A text value of **true** indicates that a client can delete an item or folder.</span></span> <span data-ttu-id="2ea60-121">**如果值为 false** ，则表示客户端无法删除项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="2ea60-121">A value of **false** indicates that a client cannot delete an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ea60-122">说明</span><span class="sxs-lookup"><span data-stu-id="2ea60-122">Remarks</span></span>

<span data-ttu-id="2ea60-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ea60-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ea60-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ea60-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ea60-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ea60-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ea60-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ea60-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2ea60-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="2ea60-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="2ea60-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ea60-128">Validation File</span></span>  <br/> |<span data-ttu-id="2ea60-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ea60-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ea60-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ea60-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="2ea60-131">False</span><span class="sxs-lookup"><span data-stu-id="2ea60-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ea60-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ea60-132">See also</span></span>

- [<span data-ttu-id="2ea60-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2ea60-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2ea60-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="2ea60-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

