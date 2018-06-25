---
title: GlobalHasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalHasAttachments
api_type:
- schema
ms.assetid: 3d075e93-14bc-479d-957f-9b7873d1db39
description: GlobalHasAttachments元素中包含一个值，指示是否至少一个对话邮箱中的邮件带有附件。
ms.openlocfilehash: 85443c45f611a2f4bff392ffecb26029564d7558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825715"
---
# <a name="globalhasattachments"></a><span data-ttu-id="9ef45-103">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="9ef45-103">GlobalHasAttachments</span></span>

<span data-ttu-id="9ef45-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GlobalHasAttachments**元素中包含一个值，指示是否至少一个对话邮箱中的邮件带有附件。</span><span class="sxs-lookup"><span data-stu-id="9ef45-104">The **GlobalHasAttachments** element contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span> 
  
[<span data-ttu-id="9ef45-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="9ef45-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="9ef45-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="9ef45-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="9ef45-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="9ef45-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="9ef45-108">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="9ef45-108">GlobalHasAttachments</span></span>](globalhasattachments.md)
  
```XML
<GlobalHasAttachments/>
```

 <span data-ttu-id="9ef45-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9ef45-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ef45-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ef45-110">Attributes and elements</span></span>

<span data-ttu-id="9ef45-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ef45-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ef45-112">属性</span><span class="sxs-lookup"><span data-stu-id="9ef45-112">Attributes</span></span>

<span data-ttu-id="9ef45-113">无。</span><span class="sxs-lookup"><span data-stu-id="9ef45-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ef45-114">子元素</span><span class="sxs-lookup"><span data-stu-id="9ef45-114">Child elements</span></span>

<span data-ttu-id="9ef45-115">无。</span><span class="sxs-lookup"><span data-stu-id="9ef45-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9ef45-116">父元素</span><span class="sxs-lookup"><span data-stu-id="9ef45-116">Parent elements</span></span>

|<span data-ttu-id="9ef45-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="9ef45-117">**Element**</span></span>|<span data-ttu-id="9ef45-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="9ef45-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ef45-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="9ef45-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="9ef45-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="9ef45-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9ef45-121">文本值</span><span class="sxs-lookup"><span data-stu-id="9ef45-121">Text value</span></span>

<span data-ttu-id="9ef45-p101">**GlobalHasAttachments**元素的值指示是否至少一个对话邮箱中的邮件带有附件。表示一个布尔值的文本值是必需的。 **true**的值表示该对话有至少一个可见附件。 **false**的值表示对话既没有附件或仅包含隐藏的附件。</span><span class="sxs-lookup"><span data-stu-id="9ef45-p101">The value of the **GlobalHasAttachments** element indicates whether at least one conversation item in a mailbox has an attachment. A text value that represents a Boolean value is required. A value of **true** means that the conversation has at least one visible attachment. A value of **false** means that the conversation either has no attachments or has only hidden attachments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9ef45-126">备注</span><span class="sxs-lookup"><span data-stu-id="9ef45-126">Remarks</span></span>

<span data-ttu-id="9ef45-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9ef45-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ef45-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ef45-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ef45-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ef45-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ef45-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ef45-130">Schema name</span></span>  <br/> |<span data-ttu-id="9ef45-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="9ef45-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ef45-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ef45-132">Validation file</span></span>  <br/> |<span data-ttu-id="9ef45-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ef45-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ef45-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ef45-134">Can be empty</span></span>  <br/> |<span data-ttu-id="9ef45-135">False</span><span class="sxs-lookup"><span data-stu-id="9ef45-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ef45-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9ef45-136">See also</span></span>



[<span data-ttu-id="9ef45-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="9ef45-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="9ef45-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="9ef45-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="9ef45-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="9ef45-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

