---
title: UniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueRecipients
api_type:
- schema
ms.assetid: 9f46ed05-5370-46ee-80f5-83f97224c76e
description: UniqueRecipients元素中包含的收件人列表的特定文件夹中的对话。此元素是只读的。
ms.openlocfilehash: 710559e599c6cec1db371165f01187f8960024f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838342"
---
# <a name="uniquerecipients"></a><span data-ttu-id="c7033-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="c7033-104">UniqueRecipients</span></span>

<span data-ttu-id="c7033-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UniqueRecipients**元素中包含的收件人列表的特定文件夹中的对话。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="c7033-p102">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder. This element is read-only.</span></span> 
  
[<span data-ttu-id="c7033-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c7033-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c7033-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="c7033-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c7033-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c7033-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c7033-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="c7033-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="c7033-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="c7033-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7033-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7033-112">Attributes and elements</span></span>

<span data-ttu-id="c7033-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7033-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7033-114">属性</span><span class="sxs-lookup"><span data-stu-id="c7033-114">Attributes</span></span>

<span data-ttu-id="c7033-115">无。</span><span class="sxs-lookup"><span data-stu-id="c7033-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7033-116">子元素</span><span class="sxs-lookup"><span data-stu-id="c7033-116">Child elements</span></span>

|<span data-ttu-id="c7033-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7033-117">**Element**</span></span>|<span data-ttu-id="c7033-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7033-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7033-119">字符串</span><span class="sxs-lookup"><span data-stu-id="c7033-119">String</span></span>](string.md) <br/> |<span data-ttu-id="c7033-p103">表示唯一收件人的对话。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="c7033-p103">Represents a unique recipient of a conversation. This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7033-122">父元素</span><span class="sxs-lookup"><span data-stu-id="c7033-122">Parent elements</span></span>

|<span data-ttu-id="c7033-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7033-123">**Element**</span></span>|<span data-ttu-id="c7033-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7033-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7033-125">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c7033-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c7033-126">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="c7033-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7033-127">文本值</span><span class="sxs-lookup"><span data-stu-id="c7033-127">Text value</span></span>

<span data-ttu-id="c7033-128">无。</span><span class="sxs-lookup"><span data-stu-id="c7033-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7033-129">备注</span><span class="sxs-lookup"><span data-stu-id="c7033-129">Remarks</span></span>

<span data-ttu-id="c7033-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c7033-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7033-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="c7033-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7033-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="c7033-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7033-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="c7033-133">Schema name</span></span>  <br/> |<span data-ttu-id="c7033-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="c7033-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7033-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="c7033-135">Validation file</span></span>  <br/> |<span data-ttu-id="c7033-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c7033-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7033-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="c7033-137">Can be empty</span></span>  <br/> |<span data-ttu-id="c7033-138">False</span><span class="sxs-lookup"><span data-stu-id="c7033-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7033-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7033-139">See also</span></span>



[<span data-ttu-id="c7033-140">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="c7033-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="c7033-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="c7033-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

