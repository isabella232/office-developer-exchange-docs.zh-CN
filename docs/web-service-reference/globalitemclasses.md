---
title: GlobalItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemClasses
api_type:
- schema
ms.assetid: 72634700-6d75-44c0-80b7-8c31743c04d6
description: GlobalItemClasses 元素包含列表项类的值，该值代表的邮箱中的会话项目的所有项类。
ms.openlocfilehash: a8f947d37c1335f1eaba5550a2b3a0aece0246ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825735"
---
# <a name="globalitemclasses"></a><span data-ttu-id="49c71-103">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="49c71-103">GlobalItemClasses</span></span>

<span data-ttu-id="49c71-104">**GlobalItemClasses**元素包含列表项类的值，该值代表的邮箱中的会话项目的所有项类。</span><span class="sxs-lookup"><span data-stu-id="49c71-104">The **GlobalItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="49c71-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="49c71-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="49c71-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="49c71-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="49c71-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="49c71-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="49c71-108">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="49c71-108">GlobalItemClasses</span></span>](globalitemclasses.md)
  
```XML
<GlobalItemClasses>
    <String/>
</GlobalItemClasses>
```

 <span data-ttu-id="49c71-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="49c71-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49c71-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49c71-110">Attributes and elements</span></span>

<span data-ttu-id="49c71-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49c71-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49c71-112">属性</span><span class="sxs-lookup"><span data-stu-id="49c71-112">Attributes</span></span>

<span data-ttu-id="49c71-113">无。</span><span class="sxs-lookup"><span data-stu-id="49c71-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49c71-114">子元素</span><span class="sxs-lookup"><span data-stu-id="49c71-114">Child elements</span></span>

|<span data-ttu-id="49c71-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="49c71-115">**Element**</span></span>|<span data-ttu-id="49c71-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="49c71-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49c71-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="49c71-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="49c71-118">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="49c71-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="49c71-119">父元素</span><span class="sxs-lookup"><span data-stu-id="49c71-119">Parent elements</span></span>

|<span data-ttu-id="49c71-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="49c71-120">**Element**</span></span>|<span data-ttu-id="49c71-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="49c71-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49c71-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="49c71-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="49c71-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="49c71-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49c71-124">文本值</span><span class="sxs-lookup"><span data-stu-id="49c71-124">Text value</span></span>

<span data-ttu-id="49c71-125">无。</span><span class="sxs-lookup"><span data-stu-id="49c71-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="49c71-126">备注</span><span class="sxs-lookup"><span data-stu-id="49c71-126">Remarks</span></span>

<span data-ttu-id="49c71-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="49c71-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49c71-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="49c71-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49c71-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="49c71-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49c71-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="49c71-130">Schema name</span></span>  <br/> |<span data-ttu-id="49c71-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="49c71-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="49c71-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="49c71-132">Validation file</span></span>  <br/> |<span data-ttu-id="49c71-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49c71-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49c71-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="49c71-134">Can be empty</span></span>  <br/> |<span data-ttu-id="49c71-135">False</span><span class="sxs-lookup"><span data-stu-id="49c71-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49c71-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49c71-136">See also</span></span>



[<span data-ttu-id="49c71-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="49c71-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="49c71-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="49c71-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="49c71-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="49c71-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)
