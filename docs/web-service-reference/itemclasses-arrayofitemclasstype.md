---
title: ItemClasses (ArrayOfItemClassType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 971784d1-6860-4833-bb26-0e930fa11c21
description: ItemClasses 元素包含项类的列表，这些类表示当前文件夹中的会话项目的所有项目类。
ms.openlocfilehash: 39118bf845429bb198874ae4e6b424c6339b1964
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467296"
---
# <a name="itemclasses-arrayofitemclasstype"></a><span data-ttu-id="ae146-103">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="ae146-103">ItemClasses (ArrayOfItemClassType)</span></span>

<span data-ttu-id="ae146-104">**ItemClasses**元素包含项类的列表，这些类表示当前文件夹中的会话项目的所有项目类。</span><span class="sxs-lookup"><span data-stu-id="ae146-104">The **ItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="ae146-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ae146-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ae146-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="ae146-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="ae146-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ae146-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="ae146-108">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="ae146-108">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md)
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="ae146-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="ae146-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae146-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae146-110">Attributes and elements</span></span>

<span data-ttu-id="ae146-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae146-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae146-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="ae146-112">Attributes</span></span>

<span data-ttu-id="ae146-113">无。</span><span class="sxs-lookup"><span data-stu-id="ae146-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae146-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ae146-114">Child elements</span></span>

|<span data-ttu-id="ae146-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae146-115">**Element**</span></span>|<span data-ttu-id="ae146-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae146-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae146-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="ae146-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="ae146-118">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="ae146-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae146-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ae146-119">Parent elements</span></span>

|<span data-ttu-id="ae146-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae146-120">**Element**</span></span>|<span data-ttu-id="ae146-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae146-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae146-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ae146-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ae146-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="ae146-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae146-124">文本值</span><span class="sxs-lookup"><span data-stu-id="ae146-124">Text value</span></span>

<span data-ttu-id="ae146-125">无。</span><span class="sxs-lookup"><span data-stu-id="ae146-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae146-126">说明</span><span class="sxs-lookup"><span data-stu-id="ae146-126">Remarks</span></span>

<span data-ttu-id="ae146-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ae146-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae146-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae146-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae146-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae146-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae146-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae146-130">Schema name</span></span>  <br/> |<span data-ttu-id="ae146-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="ae146-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae146-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae146-132">Validation file</span></span>  <br/> |<span data-ttu-id="ae146-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae146-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae146-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae146-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae146-135">False</span><span class="sxs-lookup"><span data-stu-id="ae146-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae146-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae146-136">See also</span></span>



[<span data-ttu-id="ae146-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ae146-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="ae146-138">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="ae146-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="ae146-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ae146-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

