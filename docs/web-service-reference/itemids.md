---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: ItemIds 元素包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。
ms.openlocfilehash: 1bd4d6f4593a7c3b418561269d8b29707cc6030c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826155"
---
# <a name="itemids"></a><span data-ttu-id="ac73b-103">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ac73b-103">ItemIds</span></span>
  
<span data-ttu-id="ac73b-104">**ItemIds**元素包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="ac73b-104">The **ItemIds** element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

<span data-ttu-id="ac73b-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="ac73b-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ac73b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ac73b-106">Attributes and elements</span></span>

<span data-ttu-id="ac73b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ac73b-107">The following sections describe attributes, child elements, and parent elements.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="ac73b-108">属性</span><span class="sxs-lookup"><span data-stu-id="ac73b-108">Attributes</span></span>

<span data-ttu-id="ac73b-109">无。</span><span class="sxs-lookup"><span data-stu-id="ac73b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ac73b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ac73b-110">Child elements</span></span>

|<span data-ttu-id="ac73b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ac73b-111">**Element**</span></span>|<span data-ttu-id="ac73b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ac73b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac73b-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="ac73b-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="ac73b-114">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="ac73b-114">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ac73b-115">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="ac73b-115">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="ac73b-116">标识定期项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="ac73b-116">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="ac73b-117">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="ac73b-117">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="ac73b-118">标识通过其相关的匹配项的标识符之一确定定期主项目。</span><span class="sxs-lookup"><span data-stu-id="ac73b-118">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac73b-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ac73b-119">Parent elements</span></span>

|<span data-ttu-id="ac73b-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ac73b-120">**Element**</span></span>|<span data-ttu-id="ac73b-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ac73b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac73b-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ac73b-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ac73b-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="ac73b-123">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="ac73b-124">删除项</span><span class="sxs-lookup"><span data-stu-id="ac73b-124">DeleteItem</span></span>](deleteitem.md) <br/> |<span data-ttu-id="ac73b-125">定义删除 Exchange 存储中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="ac73b-125">Defines a request to delete items in the Exchange store.</span></span>  <br/> <span data-ttu-id="ac73b-126">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ac73b-126">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteItem` <br/> |
|[<span data-ttu-id="ac73b-127">SendItem</span><span class="sxs-lookup"><span data-stu-id="ac73b-127">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="ac73b-128">定义发送 Exchange 存储中的项目的请求的根元素。</span><span class="sxs-lookup"><span data-stu-id="ac73b-128">The root element that defines a request to send items in the Exchange store.</span></span>  <br/> <span data-ttu-id="ac73b-129">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ac73b-129">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
|[<span data-ttu-id="ac73b-130">GetItem</span><span class="sxs-lookup"><span data-stu-id="ac73b-130">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="ac73b-131">定义从 Exchange 存储中获取项的请求。</span><span class="sxs-lookup"><span data-stu-id="ac73b-131">Defines a request to get items from the Exchange store.</span></span>  <br/> <span data-ttu-id="ac73b-132">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ac73b-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="ac73b-133">MoveItem</span><span class="sxs-lookup"><span data-stu-id="ac73b-133">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="ac73b-134">定义将项目移 Exchange 存储中的请求。</span><span class="sxs-lookup"><span data-stu-id="ac73b-134">Defines a request to move items in the Exchange store.</span></span>  <br/> <span data-ttu-id="ac73b-135">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ac73b-135">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="ac73b-136">CopyItem</span><span class="sxs-lookup"><span data-stu-id="ac73b-136">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="ac73b-137">定义在 Exchange 存储中复制项的请求。</span><span class="sxs-lookup"><span data-stu-id="ac73b-137">Defines a request to copy items in the Exchange store.</span></span>  <br/> <span data-ttu-id="ac73b-138">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ac73b-138">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac73b-139">备注</span><span class="sxs-lookup"><span data-stu-id="ac73b-139">Remarks</span></span>

<span data-ttu-id="ac73b-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ac73b-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac73b-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="ac73b-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac73b-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="ac73b-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ac73b-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="ac73b-143">Schema Name</span></span>  <br/> |<span data-ttu-id="ac73b-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="ac73b-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ac73b-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="ac73b-145">Validation File</span></span>  <br/> |<span data-ttu-id="ac73b-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ac73b-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ac73b-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="ac73b-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac73b-148">False</span><span class="sxs-lookup"><span data-stu-id="ac73b-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac73b-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ac73b-149">See also</span></span>

- [<span data-ttu-id="ac73b-150">删除项操作</span><span class="sxs-lookup"><span data-stu-id="ac73b-150">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="ac73b-151">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="ac73b-151">SendItem operation</span></span>](senditem-operation.md) 
- [<span data-ttu-id="ac73b-152">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="ac73b-152">GetItem operation</span></span>](getitem-operation.md)
- [<span data-ttu-id="ac73b-153">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="ac73b-153">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="ac73b-154">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="ac73b-154">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="ac73b-155">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ac73b-155">FindConversation operation</span></span>](findconversation-operation.md)

