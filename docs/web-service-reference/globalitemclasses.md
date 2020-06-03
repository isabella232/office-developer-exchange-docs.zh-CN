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
description: GlobalItemClasses 元素包含项类的列表，这些类表示邮箱中会话项目的所有项目类。
ms.openlocfilehash: e4cb8a8886f8262e8cb4a550b054e81ea18a5e11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459431"
---
# <a name="globalitemclasses"></a><span data-ttu-id="c6cd7-103">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="c6cd7-103">GlobalItemClasses</span></span>

<span data-ttu-id="c6cd7-104">**GlobalItemClasses**元素包含项类的列表，这些类表示邮箱中会话项目的所有项目类。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-104">The **GlobalItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="c6cd7-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c6cd7-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c6cd7-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="c6cd7-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c6cd7-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c6cd7-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c6cd7-108">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="c6cd7-108">GlobalItemClasses</span></span>](globalitemclasses.md)
  
```XML
<GlobalItemClasses>
    <String/>
</GlobalItemClasses>
```

 <span data-ttu-id="c6cd7-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="c6cd7-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6cd7-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6cd7-110">Attributes and elements</span></span>

<span data-ttu-id="c6cd7-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6cd7-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="c6cd7-112">Attributes</span></span>

<span data-ttu-id="c6cd7-113">无。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6cd7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c6cd7-114">Child elements</span></span>

|<span data-ttu-id="c6cd7-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6cd7-115">**Element**</span></span>|<span data-ttu-id="c6cd7-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6cd7-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6cd7-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="c6cd7-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="c6cd7-118">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c6cd7-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c6cd7-119">Parent elements</span></span>

|<span data-ttu-id="c6cd7-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6cd7-120">**Element**</span></span>|<span data-ttu-id="c6cd7-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6cd7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6cd7-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c6cd7-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c6cd7-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6cd7-124">文本值</span><span class="sxs-lookup"><span data-stu-id="c6cd7-124">Text value</span></span>

<span data-ttu-id="c6cd7-125">无。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6cd7-126">说明</span><span class="sxs-lookup"><span data-stu-id="c6cd7-126">Remarks</span></span>

<span data-ttu-id="c6cd7-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c6cd7-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6cd7-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6cd7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6cd7-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6cd7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6cd7-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6cd7-130">Schema name</span></span>  <br/> |<span data-ttu-id="c6cd7-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="c6cd7-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6cd7-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6cd7-132">Validation file</span></span>  <br/> |<span data-ttu-id="c6cd7-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c6cd7-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6cd7-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6cd7-134">Can be empty</span></span>  <br/> |<span data-ttu-id="c6cd7-135">False</span><span class="sxs-lookup"><span data-stu-id="c6cd7-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6cd7-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6cd7-136">See also</span></span>



[<span data-ttu-id="c6cd7-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="c6cd7-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c6cd7-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="c6cd7-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c6cd7-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="c6cd7-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

