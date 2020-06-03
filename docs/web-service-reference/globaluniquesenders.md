---
title: GlobalUniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueSenders
api_type:
- schema
ms.assetid: 6bd9e9cb-19c8-45af-b211-dfb8a6003b1b
description: GlobalUniqueSender 元素包含邮箱中对话项目的所有发件人的列表。
ms.openlocfilehash: 0e85e201017e175a9ffc6b923976020d4157d5b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459061"
---
# <a name="globaluniquesenders"></a><span data-ttu-id="dfe9a-103">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="dfe9a-103">GlobalUniqueSenders</span></span>

<span data-ttu-id="dfe9a-104">**GlobalUniqueSender**元素包含邮箱中对话项目的所有发件人的列表。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-104">The **GlobalUniqueSender** element contains a list of all the senders of conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="dfe9a-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="dfe9a-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="dfe9a-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="dfe9a-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="dfe9a-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="dfe9a-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="dfe9a-108">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="dfe9a-108">GlobalUniqueSenders</span></span>](globaluniquesenders.md)
  
```XML
<GlobalUniqueSender>
   <String/>
</GlobalUniqueSender>
```

 <span data-ttu-id="dfe9a-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dfe9a-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dfe9a-110">Attributes and elements</span></span>

<span data-ttu-id="dfe9a-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dfe9a-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="dfe9a-112">Attributes</span></span>

<span data-ttu-id="dfe9a-113">无。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dfe9a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="dfe9a-114">Child elements</span></span>

|<span data-ttu-id="dfe9a-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-115">**Element**</span></span>|<span data-ttu-id="dfe9a-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfe9a-117">字符串</span><span class="sxs-lookup"><span data-stu-id="dfe9a-117">String</span></span>](string.md) <br/> |<span data-ttu-id="dfe9a-118">包含单个对话发件人。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dfe9a-119">父元素</span><span class="sxs-lookup"><span data-stu-id="dfe9a-119">Parent elements</span></span>

|<span data-ttu-id="dfe9a-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-120">**Element**</span></span>|<span data-ttu-id="dfe9a-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="dfe9a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dfe9a-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="dfe9a-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="dfe9a-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dfe9a-124">文本值</span><span class="sxs-lookup"><span data-stu-id="dfe9a-124">Text value</span></span>

<span data-ttu-id="dfe9a-125">无。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfe9a-126">说明</span><span class="sxs-lookup"><span data-stu-id="dfe9a-126">Remarks</span></span>

<span data-ttu-id="dfe9a-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dfe9a-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dfe9a-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="dfe9a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dfe9a-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="dfe9a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dfe9a-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="dfe9a-130">Schema name</span></span>  <br/> |<span data-ttu-id="dfe9a-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="dfe9a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="dfe9a-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="dfe9a-132">Validation file</span></span>  <br/> |<span data-ttu-id="dfe9a-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dfe9a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dfe9a-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="dfe9a-134">Can be empty</span></span>  <br/> |<span data-ttu-id="dfe9a-135">False</span><span class="sxs-lookup"><span data-stu-id="dfe9a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dfe9a-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dfe9a-136">See also</span></span>



[<span data-ttu-id="dfe9a-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="dfe9a-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="dfe9a-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="dfe9a-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="dfe9a-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="dfe9a-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

