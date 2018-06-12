---
title: GlobalUniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueRecipients
api_type:
- schema
ms.assetid: 67379c1c-85d9-4b11-8f17-ad9d24904788
description: GlobalUniqueRecipients元素中包含聚合在一个邮箱之间进行对话的收件人列表。
ms.openlocfilehash: 5eb6e60d3ece8d8369f4603e36ffaaf72a3e459d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825742"
---
# <a name="globaluniquerecipients"></a><span data-ttu-id="944da-103">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="944da-103">GlobalUniqueRecipients</span></span>

<span data-ttu-id="944da-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GlobalUniqueRecipients**元素中包含聚合在一个邮箱之间进行对话的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="944da-104">The **GlobalUniqueRecipients** element contains the recipient list of a conversation aggregated across a mailbox.</span></span> 
  
[<span data-ttu-id="944da-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="944da-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="944da-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="944da-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="944da-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="944da-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="944da-108">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="944da-108">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md)
  
```XML
<GlobalUniqueRecipients>
   <String/>
</GlobalUniqueRecipients>
```

 <span data-ttu-id="944da-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="944da-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="944da-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="944da-110">Attributes and elements</span></span>

<span data-ttu-id="944da-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="944da-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="944da-112">属性</span><span class="sxs-lookup"><span data-stu-id="944da-112">Attributes</span></span>

<span data-ttu-id="944da-113">无。</span><span class="sxs-lookup"><span data-stu-id="944da-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="944da-114">子元素</span><span class="sxs-lookup"><span data-stu-id="944da-114">Child elements</span></span>

|<span data-ttu-id="944da-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="944da-115">**Element**</span></span>|<span data-ttu-id="944da-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="944da-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="944da-117">字符串</span><span class="sxs-lookup"><span data-stu-id="944da-117">String</span></span>](string.md) <br/> |<span data-ttu-id="944da-118">包含单个会话的收件人。</span><span class="sxs-lookup"><span data-stu-id="944da-118">Contains a single conversation recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="944da-119">父元素</span><span class="sxs-lookup"><span data-stu-id="944da-119">Parent elements</span></span>

|<span data-ttu-id="944da-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="944da-120">**Element**</span></span>|<span data-ttu-id="944da-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="944da-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="944da-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="944da-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="944da-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="944da-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="944da-124">文本值</span><span class="sxs-lookup"><span data-stu-id="944da-124">Text value</span></span>

<span data-ttu-id="944da-125">无。</span><span class="sxs-lookup"><span data-stu-id="944da-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="944da-126">备注</span><span class="sxs-lookup"><span data-stu-id="944da-126">Remarks</span></span>

<span data-ttu-id="944da-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="944da-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="944da-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="944da-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="944da-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="944da-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="944da-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="944da-130">Schema name</span></span>  <br/> |<span data-ttu-id="944da-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="944da-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="944da-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="944da-132">Validation file</span></span>  <br/> |<span data-ttu-id="944da-133">types.xsd</span><span class="sxs-lookup"><span data-stu-id="944da-133">types.xsd</span></span>  <br/> |
|<span data-ttu-id="944da-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="944da-134">Can be empty</span></span>  <br/> |<span data-ttu-id="944da-135">False</span><span class="sxs-lookup"><span data-stu-id="944da-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="944da-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="944da-136">See also</span></span>



[<span data-ttu-id="944da-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="944da-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="944da-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="944da-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="944da-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="944da-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

