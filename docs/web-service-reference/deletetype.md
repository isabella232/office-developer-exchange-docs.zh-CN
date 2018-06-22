---
title: DeleteType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: DeleteType 元素指示如何删除会话中的项目。
ms.openlocfilehash: abaa0c3d8b7001b2f42a38d1c82475edba32d2c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753814"
---
# <a name="deletetype"></a><span data-ttu-id="d11e7-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="d11e7-103">DeleteType</span></span>

<span data-ttu-id="d11e7-104">**DeleteType**元素指示如何删除会话中的项目。</span><span class="sxs-lookup"><span data-stu-id="d11e7-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="d11e7-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="d11e7-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="d11e7-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="d11e7-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="d11e7-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="d11e7-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="d11e7-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="d11e7-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="d11e7-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="d11e7-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d11e7-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d11e7-110">Attributes and elements</span></span>

<span data-ttu-id="d11e7-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d11e7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d11e7-112">属性</span><span class="sxs-lookup"><span data-stu-id="d11e7-112">Attributes</span></span>

<span data-ttu-id="d11e7-113">无。</span><span class="sxs-lookup"><span data-stu-id="d11e7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d11e7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d11e7-114">Child elements</span></span>

<span data-ttu-id="d11e7-115">无。</span><span class="sxs-lookup"><span data-stu-id="d11e7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d11e7-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d11e7-116">Parent elements</span></span>

|<span data-ttu-id="d11e7-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d11e7-117">**Element**</span></span>|<span data-ttu-id="d11e7-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d11e7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d11e7-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="d11e7-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="d11e7-120">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="d11e7-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d11e7-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d11e7-121">Text value</span></span>

<span data-ttu-id="d11e7-122">**DeleteType**元素的文本值指示如何删除会话中的项目。</span><span class="sxs-lookup"><span data-stu-id="d11e7-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="d11e7-123">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="d11e7-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="d11e7-124">HardDelete-指示邮箱数据库从对话中的项目被永久删除。</span><span class="sxs-lookup"><span data-stu-id="d11e7-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="d11e7-125">MoveToDeleteItems-指示对话中的项目已移动到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="d11e7-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="d11e7-126">SoftDelete-指示对话中的项目是否已移动到转储程序如果转储程序已启用。</span><span class="sxs-lookup"><span data-stu-id="d11e7-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d11e7-127">备注</span><span class="sxs-lookup"><span data-stu-id="d11e7-127">Remarks</span></span>

<span data-ttu-id="d11e7-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d11e7-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d11e7-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="d11e7-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d11e7-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="d11e7-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d11e7-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="d11e7-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d11e7-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="d11e7-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="d11e7-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="d11e7-133">Validation File</span></span>  <br/> |<span data-ttu-id="d11e7-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d11e7-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d11e7-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="d11e7-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="d11e7-136">False</span><span class="sxs-lookup"><span data-stu-id="d11e7-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d11e7-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d11e7-137">See also</span></span>

- [<span data-ttu-id="d11e7-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="d11e7-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="d11e7-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d11e7-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

