---
title: UniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueSenders
api_type:
- schema
ms.assetid: 1f55f2fe-b2f2-4169-83c1-fa5c752bd695
description: UniqueSenders 元素包含当前文件夹中的会话项目的所有发件人的列表。 此元素是只读的。
ms.openlocfilehash: b75846534141e23e6d8158bc36f0ef60bcb1d7ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838337"
---
# <a name="uniquesenders"></a><span data-ttu-id="1db53-104">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="1db53-104">UniqueSenders</span></span>

<span data-ttu-id="1db53-105">**UniqueSenders**元素包含当前文件夹中的会话项目的所有发件人的列表。</span><span class="sxs-lookup"><span data-stu-id="1db53-105">The **UniqueSenders** element contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="1db53-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="1db53-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="1db53-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="1db53-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="1db53-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="1db53-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="1db53-109">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="1db53-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="1db53-110">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="1db53-110">UniqueSenders</span></span>](uniquesenders.md)
  
```XML
<UniqueSenders>
   <String/>
</UniqueSenders>
```

 <span data-ttu-id="1db53-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="1db53-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1db53-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1db53-112">Attributes and elements</span></span>

<span data-ttu-id="1db53-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1db53-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1db53-114">属性</span><span class="sxs-lookup"><span data-stu-id="1db53-114">Attributes</span></span>

<span data-ttu-id="1db53-115">无。</span><span class="sxs-lookup"><span data-stu-id="1db53-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1db53-116">子元素</span><span class="sxs-lookup"><span data-stu-id="1db53-116">Child elements</span></span>

|<span data-ttu-id="1db53-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="1db53-117">**Element**</span></span>|<span data-ttu-id="1db53-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="1db53-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1db53-119">字符串</span><span class="sxs-lookup"><span data-stu-id="1db53-119">String</span></span>](string.md) <br/> |<span data-ttu-id="1db53-120">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="1db53-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1db53-121">父元素</span><span class="sxs-lookup"><span data-stu-id="1db53-121">Parent elements</span></span>

|<span data-ttu-id="1db53-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="1db53-122">**Element**</span></span>|<span data-ttu-id="1db53-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="1db53-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1db53-124">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="1db53-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="1db53-125">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="1db53-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1db53-126">文本值</span><span class="sxs-lookup"><span data-stu-id="1db53-126">Text value</span></span>

<span data-ttu-id="1db53-127">无。</span><span class="sxs-lookup"><span data-stu-id="1db53-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1db53-128">备注</span><span class="sxs-lookup"><span data-stu-id="1db53-128">Remarks</span></span>

<span data-ttu-id="1db53-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1db53-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1db53-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="1db53-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1db53-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="1db53-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1db53-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="1db53-132">Schema name</span></span>  <br/> |<span data-ttu-id="1db53-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="1db53-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="1db53-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="1db53-134">Validation file</span></span>  <br/> |<span data-ttu-id="1db53-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1db53-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1db53-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="1db53-136">Can be empty</span></span>  <br/> |<span data-ttu-id="1db53-137">False</span><span class="sxs-lookup"><span data-stu-id="1db53-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1db53-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1db53-138">See also</span></span>



[<span data-ttu-id="1db53-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="1db53-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="1db53-140">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="1db53-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="1db53-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="1db53-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

