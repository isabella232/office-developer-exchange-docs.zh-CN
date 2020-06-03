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
ms.openlocfilehash: d7f6b0aa01aceb6a251fb0c46d89b34cad260acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530724"
---
# <a name="uniquerecipients"></a><span data-ttu-id="299fd-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="299fd-104">UniqueRecipients</span></span>

<span data-ttu-id="299fd-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UniqueRecipients**元素中包含的收件人列表的特定文件夹中的对话。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="299fd-p102">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder. This element is read-only.</span></span> 
  
[<span data-ttu-id="299fd-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="299fd-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="299fd-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="299fd-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="299fd-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="299fd-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="299fd-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="299fd-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="299fd-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="299fd-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="299fd-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="299fd-112">Attributes and elements</span></span>

<span data-ttu-id="299fd-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="299fd-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="299fd-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="299fd-114">Attributes</span></span>

<span data-ttu-id="299fd-115">无。</span><span class="sxs-lookup"><span data-stu-id="299fd-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="299fd-116">子元素</span><span class="sxs-lookup"><span data-stu-id="299fd-116">Child elements</span></span>

|<span data-ttu-id="299fd-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="299fd-117">**Element**</span></span>|<span data-ttu-id="299fd-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="299fd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="299fd-119">字符串</span><span class="sxs-lookup"><span data-stu-id="299fd-119">String</span></span>](string.md) <br/> |<span data-ttu-id="299fd-p103">表示唯一收件人的对话。此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="299fd-p103">Represents a unique recipient of a conversation. This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="299fd-122">父元素</span><span class="sxs-lookup"><span data-stu-id="299fd-122">Parent elements</span></span>

|<span data-ttu-id="299fd-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="299fd-123">**Element**</span></span>|<span data-ttu-id="299fd-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="299fd-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="299fd-125">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="299fd-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="299fd-126">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="299fd-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="299fd-127">文本值</span><span class="sxs-lookup"><span data-stu-id="299fd-127">Text value</span></span>

<span data-ttu-id="299fd-128">无。</span><span class="sxs-lookup"><span data-stu-id="299fd-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="299fd-129">说明</span><span class="sxs-lookup"><span data-stu-id="299fd-129">Remarks</span></span>

<span data-ttu-id="299fd-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="299fd-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="299fd-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="299fd-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="299fd-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="299fd-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="299fd-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="299fd-133">Schema name</span></span>  <br/> |<span data-ttu-id="299fd-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="299fd-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="299fd-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="299fd-135">Validation file</span></span>  <br/> |<span data-ttu-id="299fd-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="299fd-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="299fd-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="299fd-137">Can be empty</span></span>  <br/> |<span data-ttu-id="299fd-138">False</span><span class="sxs-lookup"><span data-stu-id="299fd-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="299fd-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="299fd-139">See also</span></span>



[<span data-ttu-id="299fd-140">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="299fd-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="299fd-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="299fd-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

