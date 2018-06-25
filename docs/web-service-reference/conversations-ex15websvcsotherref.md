---
title: 对话
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversations
api_type:
- schema
ms.assetid: 1d18f98c-6457-45e9-a934-32da20885ac6
description: 对话元素包含一个数组 FindConversation 响应中返回的对话。
ms.openlocfilehash: cd36364bd975d1464af9a1114c64c29543b4ec47
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753595"
---
# <a name="conversations"></a><span data-ttu-id="b6635-103">对话</span><span class="sxs-lookup"><span data-stu-id="b6635-103">Conversations</span></span>

<span data-ttu-id="b6635-104">**对话**元素包含一个数组**FindConversation**响应中返回的对话。</span><span class="sxs-lookup"><span data-stu-id="b6635-104">The **Conversations** element contains an array of conversations that are returned in the **FindConversation** response.</span></span> 
  
[<span data-ttu-id="b6635-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="b6635-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="b6635-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="b6635-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
```xml
<Conversations>
   <Conversation/>
</Conversations>
```

 <span data-ttu-id="b6635-107">**ArrayOfConversationsType**</span><span class="sxs-lookup"><span data-stu-id="b6635-107">**ArrayOfConversationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6635-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b6635-108">Attributes and elements</span></span>

<span data-ttu-id="b6635-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b6635-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6635-110">属性</span><span class="sxs-lookup"><span data-stu-id="b6635-110">Attributes</span></span>

<span data-ttu-id="b6635-111">无。</span><span class="sxs-lookup"><span data-stu-id="b6635-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6635-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b6635-112">Child elements</span></span>

|<span data-ttu-id="b6635-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6635-113">**Element**</span></span>|<span data-ttu-id="b6635-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6635-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6635-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b6635-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="b6635-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="b6635-116">Represents a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6635-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b6635-117">Parent elements</span></span>

|<span data-ttu-id="b6635-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6635-118">**Element**</span></span>|<span data-ttu-id="b6635-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6635-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6635-120">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="b6635-120">FindConversationResponse</span></span>](findconversationresponse.md) <br/> |<span data-ttu-id="b6635-121">定义**FindConversation**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="b6635-121">Defines a response to a **FindConversation** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6635-122">文本值</span><span class="sxs-lookup"><span data-stu-id="b6635-122">Text value</span></span>

<span data-ttu-id="b6635-123">无。</span><span class="sxs-lookup"><span data-stu-id="b6635-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6635-124">备注</span><span class="sxs-lookup"><span data-stu-id="b6635-124">Remarks</span></span>

<span data-ttu-id="b6635-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b6635-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6635-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b6635-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6635-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b6635-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6635-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b6635-128">Schema name</span></span>  <br/> |<span data-ttu-id="b6635-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="b6635-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6635-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b6635-130">Validation file</span></span>  <br/> |<span data-ttu-id="b6635-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6635-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6635-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b6635-132">Can be empty</span></span>  <br/> |<span data-ttu-id="b6635-133">False</span><span class="sxs-lookup"><span data-stu-id="b6635-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6635-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6635-134">See also</span></span>



[<span data-ttu-id="b6635-135">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="b6635-135">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="b6635-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="b6635-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

