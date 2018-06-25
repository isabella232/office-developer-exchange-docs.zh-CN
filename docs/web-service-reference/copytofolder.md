---
title: CopyToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyToFolder
api_type:
- schema
ms.assetid: 6fd8a6b8-d813-43ff-991b-0e9e782fe00e
description: CopyToFolder元素指定文件夹的标识符可将项目复制到该电子邮件。
ms.openlocfilehash: b641c23b7aed11ae85157e2ed01cfa9d61d07e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753612"
---
# <a name="copytofolder"></a><span data-ttu-id="f35e9-103">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="f35e9-103">CopyToFolder</span></span>

<span data-ttu-id="f35e9-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CopyToFolder**元素指定文件夹的标识符可将项目复制到该电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f35e9-104">The **CopyToFolder** element specifies the identifier of the folder that email items can be copied to.</span></span> 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
```

 <span data-ttu-id="f35e9-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="f35e9-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f35e9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f35e9-106">Attributes and elements</span></span>

<span data-ttu-id="f35e9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f35e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f35e9-108">属性</span><span class="sxs-lookup"><span data-stu-id="f35e9-108">Attributes</span></span>

<span data-ttu-id="f35e9-109">无。</span><span class="sxs-lookup"><span data-stu-id="f35e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f35e9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f35e9-110">Child elements</span></span>

|<span data-ttu-id="f35e9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f35e9-111">**Element**</span></span>|<span data-ttu-id="f35e9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f35e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f35e9-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="f35e9-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="f35e9-114">包含用于复制或移动的项或文件夹的目标文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f35e9-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="f35e9-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="f35e9-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="f35e9-116">标识命名的目标文件夹复制或移动的项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="f35e9-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f35e9-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f35e9-117">Parent elements</span></span>

|<span data-ttu-id="f35e9-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="f35e9-118">**Element**</span></span>|<span data-ttu-id="f35e9-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="f35e9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f35e9-120">操作</span><span class="sxs-lookup"><span data-stu-id="f35e9-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f35e9-121">表示可在满足条件时要采取对邮件的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="f35e9-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f35e9-122">文本值</span><span class="sxs-lookup"><span data-stu-id="f35e9-122">Text value</span></span>

<span data-ttu-id="f35e9-123">无。</span><span class="sxs-lookup"><span data-stu-id="f35e9-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f35e9-124">备注</span><span class="sxs-lookup"><span data-stu-id="f35e9-124">Remarks</span></span>

<span data-ttu-id="f35e9-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f35e9-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f35e9-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="f35e9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f35e9-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="f35e9-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f35e9-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="f35e9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f35e9-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="f35e9-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f35e9-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="f35e9-130">Validation File</span></span>  <br/> |<span data-ttu-id="f35e9-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f35e9-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f35e9-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="f35e9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="f35e9-133">True</span><span class="sxs-lookup"><span data-stu-id="f35e9-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f35e9-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f35e9-134">See also</span></span>



[<span data-ttu-id="f35e9-135">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="f35e9-135">MoveToFolder</span></span>](movetofolder.md)


- [<span data-ttu-id="f35e9-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f35e9-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

