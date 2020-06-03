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
description: DeleteType 元素指示如何删除对话中的项目。
ms.openlocfilehash: 199f7afc29fe866865509d2fb90d24944113d5c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442631"
---
# <a name="deletetype"></a><span data-ttu-id="af59e-103">DeleteType</span><span class="sxs-lookup"><span data-stu-id="af59e-103">DeleteType</span></span>

<span data-ttu-id="af59e-104">**DeleteType**元素指示如何删除对话中的项目。</span><span class="sxs-lookup"><span data-stu-id="af59e-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="af59e-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="af59e-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="af59e-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="af59e-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="af59e-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="af59e-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="af59e-108">DeleteType</span><span class="sxs-lookup"><span data-stu-id="af59e-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="af59e-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="af59e-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af59e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af59e-110">Attributes and elements</span></span>

<span data-ttu-id="af59e-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af59e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af59e-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="af59e-112">Attributes</span></span>

<span data-ttu-id="af59e-113">无。</span><span class="sxs-lookup"><span data-stu-id="af59e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af59e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="af59e-114">Child elements</span></span>

<span data-ttu-id="af59e-115">无。</span><span class="sxs-lookup"><span data-stu-id="af59e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af59e-116">父元素</span><span class="sxs-lookup"><span data-stu-id="af59e-116">Parent elements</span></span>

|<span data-ttu-id="af59e-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="af59e-117">**Element**</span></span>|<span data-ttu-id="af59e-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="af59e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af59e-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="af59e-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="af59e-120">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="af59e-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af59e-121">文本值</span><span class="sxs-lookup"><span data-stu-id="af59e-121">Text value</span></span>

<span data-ttu-id="af59e-122">**DeleteType**元素的文本值指示如何删除对话中的项目。</span><span class="sxs-lookup"><span data-stu-id="af59e-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="af59e-123">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="af59e-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="af59e-124">HardDelete-表示会话中的项目从邮箱数据库中永久删除。</span><span class="sxs-lookup"><span data-stu-id="af59e-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="af59e-125">MoveToDeleteItems-指示将会话中的项目移动到 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="af59e-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="af59e-126">SoftDelete-指示如果转储程序已启用，则会将会话中的项目移至转储程序。</span><span class="sxs-lookup"><span data-stu-id="af59e-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af59e-127">备注</span><span class="sxs-lookup"><span data-stu-id="af59e-127">Remarks</span></span>

<span data-ttu-id="af59e-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="af59e-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af59e-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="af59e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af59e-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="af59e-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af59e-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="af59e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="af59e-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="af59e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="af59e-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="af59e-133">Validation File</span></span>  <br/> |<span data-ttu-id="af59e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af59e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af59e-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="af59e-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="af59e-136">False</span><span class="sxs-lookup"><span data-stu-id="af59e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af59e-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af59e-137">See also</span></span>

- [<span data-ttu-id="af59e-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="af59e-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="af59e-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af59e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

