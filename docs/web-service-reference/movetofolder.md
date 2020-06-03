---
title: MoveToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveToFolder
api_type:
- schema
ms.assetid: 991673b9-b627-4848-bfba-59a187b8575f
description: MoveToFolder元素指定电子邮件项可以移动到的文件夹的标识符。
ms.openlocfilehash: e323b2ac5390855b3db0b5495af667cdf2da5596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530004"
---
# <a name="movetofolder"></a><span data-ttu-id="da177-103">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="da177-103">MoveToFolder</span></span>

<span data-ttu-id="da177-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MoveToFolder**元素指定电子邮件项可以移动到的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="da177-104">The **MoveToFolder** element specifies the identifier of the folder to which email items can be moved.</span></span> 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 <span data-ttu-id="da177-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="da177-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="da177-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="da177-106">Attributes and elements</span></span>

<span data-ttu-id="da177-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="da177-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da177-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="da177-108">Attributes</span></span>

<span data-ttu-id="da177-109">无。</span><span class="sxs-lookup"><span data-stu-id="da177-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da177-110">子元素</span><span class="sxs-lookup"><span data-stu-id="da177-110">Child elements</span></span>

|<span data-ttu-id="da177-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="da177-111">**Element**</span></span>|<span data-ttu-id="da177-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="da177-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da177-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="da177-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="da177-114">包含用于复制或移动的项或文件夹的目标文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="da177-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="da177-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="da177-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="da177-116">标识命名的目标文件夹复制或移动的项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="da177-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da177-117">父元素</span><span class="sxs-lookup"><span data-stu-id="da177-117">Parent elements</span></span>

|<span data-ttu-id="da177-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="da177-118">**Element**</span></span>|<span data-ttu-id="da177-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="da177-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da177-120">操作</span><span class="sxs-lookup"><span data-stu-id="da177-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="da177-121">表示可在满足条件时要采取对邮件的操作的集合.</span><span class="sxs-lookup"><span data-stu-id="da177-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled..</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="da177-122">文本值</span><span class="sxs-lookup"><span data-stu-id="da177-122">Text value</span></span>

<span data-ttu-id="da177-123">无。</span><span class="sxs-lookup"><span data-stu-id="da177-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="da177-124">说明</span><span class="sxs-lookup"><span data-stu-id="da177-124">Remarks</span></span>

<span data-ttu-id="da177-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="da177-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da177-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="da177-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da177-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="da177-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="da177-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="da177-128">Schema Name</span></span>  <br/> |<span data-ttu-id="da177-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="da177-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="da177-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="da177-130">Validation File</span></span>  <br/> |<span data-ttu-id="da177-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="da177-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="da177-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="da177-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="da177-133">True</span><span class="sxs-lookup"><span data-stu-id="da177-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da177-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="da177-134">See also</span></span>



[<span data-ttu-id="da177-135">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="da177-135">CopyToFolder</span></span>](copytofolder.md)


- [<span data-ttu-id="da177-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="da177-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

