---
title: GlobalCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalCategories
api_type:
- schema
ms.assetid: 7a1d3f04-4ada-4a31-845e-f1f1ff6e136f
description: GlobalCategories 元素包含邮箱中的所有对话项目类别列表。
ms.openlocfilehash: 5cedea821b14264f15026c2d297c3017534ca354
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825711"
---
# <a name="globalcategories"></a><span data-ttu-id="a6f3c-103">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="a6f3c-103">GlobalCategories</span></span>

<span data-ttu-id="a6f3c-104">**GlobalCategories**元素包含邮箱中的所有对话项目类别列表。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-104">The **GlobalCategories** element contains the category list for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="a6f3c-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a6f3c-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a6f3c-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="a6f3c-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a6f3c-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a6f3c-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="a6f3c-108">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="a6f3c-108">GlobalCategories</span></span>](globalcategories.md)
  
```XML
<GlobalCategories>
   <String/>
</GlobalCategories>
```

 <span data-ttu-id="a6f3c-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="a6f3c-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6f3c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6f3c-110">Attributes and elements</span></span>

<span data-ttu-id="a6f3c-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6f3c-112">属性</span><span class="sxs-lookup"><span data-stu-id="a6f3c-112">Attributes</span></span>

<span data-ttu-id="a6f3c-113">无。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6f3c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a6f3c-114">Child elements</span></span>

|<span data-ttu-id="a6f3c-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6f3c-115">**Element**</span></span>|<span data-ttu-id="a6f3c-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6f3c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6f3c-117">字符串</span><span class="sxs-lookup"><span data-stu-id="a6f3c-117">String</span></span>](string.md) <br/> |<span data-ttu-id="a6f3c-118">包含单个类别。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-118">Contains a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6f3c-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a6f3c-119">Parent elements</span></span>

|<span data-ttu-id="a6f3c-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6f3c-120">**Element**</span></span>|<span data-ttu-id="a6f3c-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6f3c-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6f3c-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a6f3c-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a6f3c-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6f3c-124">文本值</span><span class="sxs-lookup"><span data-stu-id="a6f3c-124">Text value</span></span>

<span data-ttu-id="a6f3c-125">无。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6f3c-126">备注</span><span class="sxs-lookup"><span data-stu-id="a6f3c-126">Remarks</span></span>

<span data-ttu-id="a6f3c-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a6f3c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6f3c-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6f3c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6f3c-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6f3c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6f3c-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6f3c-130">Schema name</span></span>  <br/> |<span data-ttu-id="a6f3c-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="a6f3c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6f3c-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6f3c-132">Validation file</span></span>  <br/> |<span data-ttu-id="a6f3c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6f3c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6f3c-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6f3c-134">Can be empty</span></span>  <br/> |<span data-ttu-id="a6f3c-135">False</span><span class="sxs-lookup"><span data-stu-id="a6f3c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6f3c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6f3c-136">See also</span></span>



[<span data-ttu-id="a6f3c-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="a6f3c-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a6f3c-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="a6f3c-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a6f3c-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="a6f3c-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

