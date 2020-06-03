---
title: GlobalUnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUnreadCount
api_type:
- schema
ms.assetid: 5e5ccf3e-2f95-4bf9-b915-8b7e59e807a5
description: GlobalUnreadCount 元素包含邮箱中所有未读对话项的计数。
ms.openlocfilehash: 976067078908523936769b2856712e3e6908f0c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530111"
---
# <a name="globalunreadcount"></a><span data-ttu-id="d0755-103">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="d0755-103">GlobalUnreadCount</span></span>

<span data-ttu-id="d0755-104">**GlobalUnreadCount**元素包含邮箱中所有未读对话项的计数。</span><span class="sxs-lookup"><span data-stu-id="d0755-104">The **GlobalUnreadCount** element contains a count of all the unread conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="d0755-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="d0755-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="d0755-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="d0755-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="d0755-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d0755-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="d0755-108">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="d0755-108">GlobalUnreadCount</span></span>](globalunreadcount.md)
  
```XML
<GlobalUnreadCount/>
```

 <span data-ttu-id="d0755-109">**xs： int**</span><span class="sxs-lookup"><span data-stu-id="d0755-109">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0755-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0755-110">Attributes and elements</span></span>

<span data-ttu-id="d0755-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0755-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0755-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="d0755-112">Attributes</span></span>

<span data-ttu-id="d0755-113">无。</span><span class="sxs-lookup"><span data-stu-id="d0755-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0755-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d0755-114">Child elements</span></span>

<span data-ttu-id="d0755-115">无。</span><span class="sxs-lookup"><span data-stu-id="d0755-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0755-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d0755-116">Parent elements</span></span>

|<span data-ttu-id="d0755-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0755-117">**Element**</span></span>|<span data-ttu-id="d0755-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0755-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0755-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="d0755-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="d0755-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="d0755-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0755-121">文本值</span><span class="sxs-lookup"><span data-stu-id="d0755-121">Text value</span></span>

<span data-ttu-id="d0755-122">**GlobalUnreadCount**元素的文本值是一个整数值，表示邮箱中的所有未读对话项的计数。</span><span class="sxs-lookup"><span data-stu-id="d0755-122">The text value of the **GlobalUnreadCount** element is an integer value that represents a count of all the unread conversation items in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0755-123">备注</span><span class="sxs-lookup"><span data-stu-id="d0755-123">Remarks</span></span>

<span data-ttu-id="d0755-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d0755-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0755-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0755-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0755-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0755-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0755-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0755-127">Schema name</span></span>  <br/> |<span data-ttu-id="d0755-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="d0755-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0755-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0755-129">Validation file</span></span>  <br/> |<span data-ttu-id="d0755-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0755-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0755-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0755-131">Can be empty</span></span>  <br/> |<span data-ttu-id="d0755-132">False</span><span class="sxs-lookup"><span data-stu-id="d0755-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0755-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0755-133">See also</span></span>



[<span data-ttu-id="d0755-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="d0755-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="d0755-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="d0755-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="d0755-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="d0755-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

