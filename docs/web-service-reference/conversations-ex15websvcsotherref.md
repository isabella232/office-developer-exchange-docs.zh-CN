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
description: 对话元素包含在 FindConversation 响应中返回的一组对话。
ms.openlocfilehash: 8af1023db51dd955c544422520ec5565f09f5372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463795"
---
# <a name="conversations"></a><span data-ttu-id="01d5c-103">对话</span><span class="sxs-lookup"><span data-stu-id="01d5c-103">Conversations</span></span>

<span data-ttu-id="01d5c-104">**对话**元素包含在**FindConversation**响应中返回的一组对话。</span><span class="sxs-lookup"><span data-stu-id="01d5c-104">The **Conversations** element contains an array of conversations that are returned in the **FindConversation** response.</span></span> 
  
[<span data-ttu-id="01d5c-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="01d5c-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="01d5c-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="01d5c-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
```xml
<Conversations>
   <Conversation/>
</Conversations>
```

 <span data-ttu-id="01d5c-107">**ArrayOfConversationsType**</span><span class="sxs-lookup"><span data-stu-id="01d5c-107">**ArrayOfConversationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01d5c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01d5c-108">Attributes and elements</span></span>

<span data-ttu-id="01d5c-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01d5c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01d5c-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="01d5c-110">Attributes</span></span>

<span data-ttu-id="01d5c-111">无。</span><span class="sxs-lookup"><span data-stu-id="01d5c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01d5c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="01d5c-112">Child elements</span></span>

|<span data-ttu-id="01d5c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="01d5c-113">**Element**</span></span>|<span data-ttu-id="01d5c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="01d5c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01d5c-115">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="01d5c-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="01d5c-116">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="01d5c-116">Represents a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="01d5c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="01d5c-117">Parent elements</span></span>

|<span data-ttu-id="01d5c-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="01d5c-118">**Element**</span></span>|<span data-ttu-id="01d5c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="01d5c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01d5c-120">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="01d5c-120">FindConversationResponse</span></span>](findconversationresponse.md) <br/> |<span data-ttu-id="01d5c-121">定义对**FindConversation**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="01d5c-121">Defines a response to a **FindConversation** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01d5c-122">文本值</span><span class="sxs-lookup"><span data-stu-id="01d5c-122">Text value</span></span>

<span data-ttu-id="01d5c-123">无。</span><span class="sxs-lookup"><span data-stu-id="01d5c-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01d5c-124">说明</span><span class="sxs-lookup"><span data-stu-id="01d5c-124">Remarks</span></span>

<span data-ttu-id="01d5c-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="01d5c-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01d5c-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="01d5c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01d5c-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="01d5c-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="01d5c-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="01d5c-128">Schema name</span></span>  <br/> |<span data-ttu-id="01d5c-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="01d5c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="01d5c-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="01d5c-130">Validation file</span></span>  <br/> |<span data-ttu-id="01d5c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="01d5c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="01d5c-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="01d5c-132">Can be empty</span></span>  <br/> |<span data-ttu-id="01d5c-133">False</span><span class="sxs-lookup"><span data-stu-id="01d5c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01d5c-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01d5c-134">See also</span></span>



[<span data-ttu-id="01d5c-135">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="01d5c-135">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="01d5c-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="01d5c-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

