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
description: ContextFolderId 元素指示针对使用文件夹的操作的文件夹。 在复制、删除、移动和设置目标文件夹中会话项的读取状态时，必须存在此元素。
ms.openlocfilehash: 60f1eaf3b45eee83632c7da6f453a1d09f54d9fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529257"
---
# <a name="contextfolderid"></a><span data-ttu-id="bd0f1-104">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="bd0f1-104">ContextFolderId</span></span>

<span data-ttu-id="bd0f1-105">**ContextFolderId**元素指示针对使用文件夹的操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-105">The **ContextFolderId** element indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="bd0f1-106">在复制、删除、移动和设置目标文件夹中会话项的读取状态时，必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-106">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span> 
  
- [<span data-ttu-id="bd0f1-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="bd0f1-107">ApplyConversationAction</span></span>](applyconversationaction.md) 
- [<span data-ttu-id="bd0f1-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="bd0f1-108">ConversationActions</span></span>](conversationactions.md)
- [<span data-ttu-id="bd0f1-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="bd0f1-109">ConversationAction</span></span>](conversationaction.md)
- [<span data-ttu-id="bd0f1-110">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="bd0f1-110">ContextFolderId</span></span>](contextfolderid.md)
  
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


<span data-ttu-id="bd0f1-111">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="bd0f1-111">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bd0f1-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd0f1-112">Attributes and elements</span></span>

<span data-ttu-id="bd0f1-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd0f1-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="bd0f1-114">Attributes</span></span>

<span data-ttu-id="bd0f1-115">无。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd0f1-116">子元素</span><span class="sxs-lookup"><span data-stu-id="bd0f1-116">Child elements</span></span>

|<span data-ttu-id="bd0f1-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd0f1-117">**Element**</span></span>|<span data-ttu-id="bd0f1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd0f1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd0f1-119">FolderId</span><span class="sxs-lookup"><span data-stu-id="bd0f1-119">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="bd0f1-120">包含上下文文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-120">Contains the identifier and change key of the context folder.</span></span>  <br/> |
|[<span data-ttu-id="bd0f1-121">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="bd0f1-121">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="bd0f1-122">标识可通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-122">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd0f1-123">父元素</span><span class="sxs-lookup"><span data-stu-id="bd0f1-123">Parent elements</span></span>

|<span data-ttu-id="bd0f1-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd0f1-124">**Element**</span></span>|<span data-ttu-id="bd0f1-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd0f1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd0f1-126">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="bd0f1-126">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="bd0f1-127">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-127">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd0f1-128">文本值</span><span class="sxs-lookup"><span data-stu-id="bd0f1-128">Text value</span></span>

<span data-ttu-id="bd0f1-129">无。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd0f1-130">说明</span><span class="sxs-lookup"><span data-stu-id="bd0f1-130">Remarks</span></span>

<span data-ttu-id="bd0f1-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bd0f1-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd0f1-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="bd0f1-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd0f1-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="bd0f1-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd0f1-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="bd0f1-134">Schema Name</span></span>  <br/> |<span data-ttu-id="bd0f1-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="bd0f1-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd0f1-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="bd0f1-136">Validation File</span></span>  <br/> |<span data-ttu-id="bd0f1-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd0f1-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd0f1-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="bd0f1-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd0f1-139">False</span><span class="sxs-lookup"><span data-stu-id="bd0f1-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd0f1-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd0f1-140">See also</span></span>

- [<span data-ttu-id="bd0f1-141">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="bd0f1-141">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

