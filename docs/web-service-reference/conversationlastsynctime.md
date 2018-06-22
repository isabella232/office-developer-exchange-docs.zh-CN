---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: ConversationLastSyncTime 元素包含的日期和对话上次同步的时间。 此元素必须存在时尝试删除接收到指定的时间过去的对话中的所有项目。
ms.openlocfilehash: 3b086d69ac0ef307059df4902e65f796c63733d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753587"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="a215d-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="a215d-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="a215d-105">**ConversationLastSyncTime**元素包含的日期和对话上次同步的时间。</span><span class="sxs-lookup"><span data-stu-id="a215d-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="a215d-106">此元素必须存在时尝试删除接收到指定的时间过去的对话中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="a215d-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="a215d-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a215d-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="a215d-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="a215d-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="a215d-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="a215d-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="a215d-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="a215d-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="a215d-111">**xs:dateTime**</span><span class="sxs-lookup"><span data-stu-id="a215d-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a215d-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a215d-112">Attributes and elements</span></span>

<span data-ttu-id="a215d-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a215d-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a215d-114">属性</span><span class="sxs-lookup"><span data-stu-id="a215d-114">Attributes</span></span>

<span data-ttu-id="a215d-115">无。</span><span class="sxs-lookup"><span data-stu-id="a215d-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a215d-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a215d-116">Child elements</span></span>

<span data-ttu-id="a215d-117">无。</span><span class="sxs-lookup"><span data-stu-id="a215d-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a215d-118">父元素</span><span class="sxs-lookup"><span data-stu-id="a215d-118">Parent elements</span></span>

|<span data-ttu-id="a215d-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="a215d-119">**Element**</span></span>|<span data-ttu-id="a215d-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="a215d-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a215d-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="a215d-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="a215d-122">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="a215d-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a215d-123">文本值</span><span class="sxs-lookup"><span data-stu-id="a215d-123">Text value</span></span>

<span data-ttu-id="a215d-124">**ConversationLastSyncTime**的文本值指示的上次对话已同步。</span><span class="sxs-lookup"><span data-stu-id="a215d-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a215d-125">备注</span><span class="sxs-lookup"><span data-stu-id="a215d-125">Remarks</span></span>

<span data-ttu-id="a215d-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a215d-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a215d-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="a215d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a215d-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="a215d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a215d-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="a215d-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a215d-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="a215d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a215d-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="a215d-131">Validation File</span></span>  <br/> |<span data-ttu-id="a215d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a215d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a215d-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="a215d-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a215d-134">False</span><span class="sxs-lookup"><span data-stu-id="a215d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a215d-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a215d-135">See also</span></span>



[<span data-ttu-id="a215d-136">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="a215d-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="a215d-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a215d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

