---
title: GlobalSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalSize
api_type:
- schema
ms.assetid: 23c24437-8dab-4c86-888d-471d23af675a
description: GlobalSize 元素包含从邮箱中所有会话项目的大小计算出的对话的大小。
ms.openlocfilehash: d23ab080dadb006cd5eff9d712d081fe7d94a2a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462449"
---
# <a name="globalsize"></a><span data-ttu-id="16954-103">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="16954-103">GlobalSize</span></span>

<span data-ttu-id="16954-104">**GlobalSize**元素包含从邮箱中所有会话项目的大小计算出的对话的大小。</span><span class="sxs-lookup"><span data-stu-id="16954-104">The **GlobalSize** element contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="16954-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="16954-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="16954-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="16954-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="16954-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="16954-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="16954-108">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="16954-108">GlobalSize</span></span>](globalsize.md)
  
```XML
<GlobalSize/>
```

 <span data-ttu-id="16954-109">**xs： int**</span><span class="sxs-lookup"><span data-stu-id="16954-109">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16954-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="16954-110">Attributes and elements</span></span>

<span data-ttu-id="16954-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="16954-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16954-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="16954-112">Attributes</span></span>

<span data-ttu-id="16954-113">无。</span><span class="sxs-lookup"><span data-stu-id="16954-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="16954-114">子元素</span><span class="sxs-lookup"><span data-stu-id="16954-114">Child elements</span></span>

<span data-ttu-id="16954-115">无。</span><span class="sxs-lookup"><span data-stu-id="16954-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="16954-116">父元素</span><span class="sxs-lookup"><span data-stu-id="16954-116">Parent elements</span></span>

|<span data-ttu-id="16954-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="16954-117">**Element**</span></span>|<span data-ttu-id="16954-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="16954-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16954-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="16954-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="16954-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="16954-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="16954-121">文本值</span><span class="sxs-lookup"><span data-stu-id="16954-121">Text value</span></span>

<span data-ttu-id="16954-122">**GlobalSize**元素的文本值是从邮箱中所有会话项目的大小计算出的对话的大小。</span><span class="sxs-lookup"><span data-stu-id="16954-122">The text value of the **GlobalSize** element is the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="16954-123">备注</span><span class="sxs-lookup"><span data-stu-id="16954-123">Remarks</span></span>

<span data-ttu-id="16954-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="16954-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16954-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="16954-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16954-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="16954-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16954-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="16954-127">Schema name</span></span>  <br/> |<span data-ttu-id="16954-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="16954-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="16954-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="16954-129">Validation file</span></span>  <br/> |<span data-ttu-id="16954-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="16954-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="16954-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="16954-131">Can be empty</span></span>  <br/> |<span data-ttu-id="16954-132">False</span><span class="sxs-lookup"><span data-stu-id="16954-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16954-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16954-133">See also</span></span>



[<span data-ttu-id="16954-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="16954-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="16954-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="16954-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="16954-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="16954-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

