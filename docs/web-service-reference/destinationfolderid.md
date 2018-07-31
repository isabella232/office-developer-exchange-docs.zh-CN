---
title: DestinationFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DestinationFolderId
api_type:
- schema
ms.assetid: 77d2d222-320b-4aab-88e4-934ef177f55c
description: DestinationFolderId 元素指示的副本的目标文件夹，并移动操作。
ms.openlocfilehash: bfbacb9c82a681c7963ab5164c43cbb648e726cd
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353376"
---
# <a name="destinationfolderid"></a><span data-ttu-id="57049-103">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="57049-103">DestinationFolderId</span></span>

<span data-ttu-id="57049-104">**DestinationFolderId**元素指示的副本的目标文件夹，并移动操作。</span><span class="sxs-lookup"><span data-stu-id="57049-104">The **DestinationFolderId** element indicates the destination folder for copy and move actions.</span></span> 
  
- [<span data-ttu-id="57049-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="57049-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="57049-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="57049-106">ConversationActions</span></span>](conversationactions.md) 
- [<span data-ttu-id="57049-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="57049-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="57049-108">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="57049-108">DestinationFolderId</span></span>](destinationfolderid.md)
  
```XML
<DestinationFolderId>
   <FolderId/>
</DestinationFolderId>
```

```XML
<DestinationFolderId>
   <DistinguishedFolderId/>
</DestinationFolderId>
```

<span data-ttu-id="57049-109">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="57049-109">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="57049-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="57049-110">Attributes and elements</span></span>

<span data-ttu-id="57049-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="57049-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57049-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="57049-112">Attributes</span></span>

<span data-ttu-id="57049-113">无。</span><span class="sxs-lookup"><span data-stu-id="57049-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57049-114">子元素</span><span class="sxs-lookup"><span data-stu-id="57049-114">Child elements</span></span>

|<span data-ttu-id="57049-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="57049-115">**Element**</span></span>|<span data-ttu-id="57049-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="57049-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57049-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="57049-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="57049-118">包含目标文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="57049-118">Contains the identifier and change key of the destination folder.</span></span>  <br/> |
|[<span data-ttu-id="57049-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="57049-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="57049-120">标识可以通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="57049-120">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57049-121">父元素</span><span class="sxs-lookup"><span data-stu-id="57049-121">Parent elements</span></span>

|<span data-ttu-id="57049-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="57049-122">**Element**</span></span>|<span data-ttu-id="57049-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="57049-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57049-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="57049-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="57049-125">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="57049-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="57049-126">文本值</span><span class="sxs-lookup"><span data-stu-id="57049-126">Text value</span></span>

<span data-ttu-id="57049-127">无。</span><span class="sxs-lookup"><span data-stu-id="57049-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57049-128">备注</span><span class="sxs-lookup"><span data-stu-id="57049-128">Remarks</span></span>

<span data-ttu-id="57049-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="57049-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57049-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="57049-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57049-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="57049-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="57049-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="57049-132">Schema Name</span></span>  <br/> |<span data-ttu-id="57049-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="57049-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="57049-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="57049-134">Validation File</span></span>  <br/> |<span data-ttu-id="57049-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="57049-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="57049-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="57049-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="57049-137">False</span><span class="sxs-lookup"><span data-stu-id="57049-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57049-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="57049-138">See also</span></span>

- [<span data-ttu-id="57049-139">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="57049-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

