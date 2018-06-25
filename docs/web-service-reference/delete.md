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
description: 删除元素指示客户端是否可以删除文件夹或项目。
ms.openlocfilehash: 8a00a24ea63fa564ecefb96a5caed3a9199690eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753785"
---
# <a name="delete"></a><span data-ttu-id="384a1-103">Delete</span><span class="sxs-lookup"><span data-stu-id="384a1-103">Delete</span></span>

<span data-ttu-id="384a1-104">**删除**元素指示客户端是否可以删除文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="384a1-104">The **Delete** element indicates whether a client can delete a folder or item.</span></span> 
  
```XML
<Delete>true or false</Delete>
```

<span data-ttu-id="384a1-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="384a1-105">**boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="384a1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="384a1-106">Attributes and elements</span></span>

<span data-ttu-id="384a1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="384a1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="384a1-108">属性</span><span class="sxs-lookup"><span data-stu-id="384a1-108">Attributes</span></span>

<span data-ttu-id="384a1-109">无。</span><span class="sxs-lookup"><span data-stu-id="384a1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="384a1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="384a1-110">Child elements</span></span>

<span data-ttu-id="384a1-111">无。</span><span class="sxs-lookup"><span data-stu-id="384a1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="384a1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="384a1-112">Parent elements</span></span>

|<span data-ttu-id="384a1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="384a1-113">**Element**</span></span>|<span data-ttu-id="384a1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="384a1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="384a1-115">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="384a1-115">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="384a1-116">包含客户端基于的项目或文件夹的权限设置的权限。</span><span class="sxs-lookup"><span data-stu-id="384a1-116">Contains the rights of the client based on the permission settings for the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="384a1-117">操作</span><span class="sxs-lookup"><span data-stu-id="384a1-117">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="384a1-118">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="384a1-118">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="384a1-119">文本值</span><span class="sxs-lookup"><span data-stu-id="384a1-119">Text value</span></span>

<span data-ttu-id="384a1-120">文本值为**true**指示客户端可以删除项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="384a1-120">A text value of **true** indicates that a client can delete an item or folder.</span></span> <span data-ttu-id="384a1-121">如果值为**false**指示客户端无法删除项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="384a1-121">A value of **false** indicates that a client cannot delete an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="384a1-122">备注</span><span class="sxs-lookup"><span data-stu-id="384a1-122">Remarks</span></span>

<span data-ttu-id="384a1-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="384a1-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="384a1-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="384a1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="384a1-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="384a1-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="384a1-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="384a1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="384a1-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="384a1-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="384a1-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="384a1-128">Validation File</span></span>  <br/> |<span data-ttu-id="384a1-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="384a1-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="384a1-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="384a1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="384a1-131">False</span><span class="sxs-lookup"><span data-stu-id="384a1-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="384a1-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="384a1-132">See also</span></span>

- [<span data-ttu-id="384a1-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="384a1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="384a1-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="384a1-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

