---
title: ContextFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: ContextFolderId 元素指示使用文件夹的操作的目标文件夹。 此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。
ms.openlocfilehash: 94428a079be6da8873c777556771579a7110fb62
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354279"
---
# <a name="contextfolderid"></a><span data-ttu-id="264f5-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="264f5-104">ContextFolderId</span></span>

<span data-ttu-id="264f5-105">**ContextFolderId**元素指示使用文件夹的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="264f5-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="264f5-106">此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。</span><span class="sxs-lookup"><span data-stu-id="264f5-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
- [<span data-ttu-id="264f5-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="264f5-107">ApplyConversationAction</span></span>](applyconversationaction.md) 
- [<span data-ttu-id="264f5-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="264f5-108">ConversationActions</span></span>](conversationactions.md)
- [<span data-ttu-id="264f5-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="264f5-109">ConversationAction</span></span>](conversationaction.md)
- [<span data-ttu-id="264f5-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="264f5-110">ContextFolderId</span></span>](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


<span data-ttu-id="264f5-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="264f5-111">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="264f5-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="264f5-112">Attributes and elements</span></span>

<span data-ttu-id="264f5-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="264f5-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="264f5-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="264f5-114">Attributes</span></span>

<span data-ttu-id="264f5-115">无。</span><span class="sxs-lookup"><span data-stu-id="264f5-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="264f5-116">子元素</span><span class="sxs-lookup"><span data-stu-id="264f5-116">Child elements</span></span>

|<span data-ttu-id="264f5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="264f5-117">**Element**</span></span>|<span data-ttu-id="264f5-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="264f5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="264f5-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="264f5-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="264f5-120">包含，上下文文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="264f5-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="264f5-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="264f5-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="264f5-122">标识可以通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="264f5-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="264f5-123">父元素</span><span class="sxs-lookup"><span data-stu-id="264f5-123">Parent elements</span></span>

|<span data-ttu-id="264f5-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="264f5-124">**Element**</span></span>|<span data-ttu-id="264f5-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="264f5-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="264f5-126">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="264f5-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="264f5-127">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="264f5-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="264f5-128">文本值</span><span class="sxs-lookup"><span data-stu-id="264f5-128">Text value</span></span>

<span data-ttu-id="264f5-129">无。</span><span class="sxs-lookup"><span data-stu-id="264f5-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="264f5-130">备注</span><span class="sxs-lookup"><span data-stu-id="264f5-130">Remarks</span></span>

<span data-ttu-id="264f5-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="264f5-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="264f5-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="264f5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="264f5-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="264f5-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="264f5-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="264f5-134">Schema Name</span></span>  <br/> |<span data-ttu-id="264f5-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="264f5-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="264f5-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="264f5-136">Validation File</span></span>  <br/> |<span data-ttu-id="264f5-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="264f5-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="264f5-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="264f5-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="264f5-139">False</span><span class="sxs-lookup"><span data-stu-id="264f5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="264f5-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="264f5-140">See also</span></span>

- [<span data-ttu-id="264f5-141">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="264f5-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

