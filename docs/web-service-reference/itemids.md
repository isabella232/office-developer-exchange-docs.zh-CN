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
description: ItemIds 元素包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。
ms.openlocfilehash: bbd594ce2610bd625b0e16a0383fda552ee9eb19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460601"
---
# <a name="itemids"></a><span data-ttu-id="51196-103">ItemIds</span><span class="sxs-lookup"><span data-stu-id="51196-103">ItemIds</span></span>
  
<span data-ttu-id="51196-104">**ItemIds**元素包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="51196-104">The **ItemIds** element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

<span data-ttu-id="51196-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="51196-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="51196-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="51196-106">Attributes and elements</span></span>

<span data-ttu-id="51196-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="51196-107">The following sections describe attributes, child elements, and parent elements.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="51196-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="51196-108">Attributes</span></span>

<span data-ttu-id="51196-109">无。</span><span class="sxs-lookup"><span data-stu-id="51196-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51196-110">子元素</span><span class="sxs-lookup"><span data-stu-id="51196-110">Child elements</span></span>

|<span data-ttu-id="51196-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="51196-111">**Element**</span></span>|<span data-ttu-id="51196-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="51196-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51196-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="51196-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="51196-114">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="51196-114">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="51196-115">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="51196-115">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="51196-116">标识定期项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="51196-116">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="51196-117">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="51196-117">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="51196-118">通过标识一个 "定期" 主项目的 "标识符" 标识该项目。</span><span class="sxs-lookup"><span data-stu-id="51196-118">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51196-119">父元素</span><span class="sxs-lookup"><span data-stu-id="51196-119">Parent elements</span></span>

|<span data-ttu-id="51196-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="51196-120">**Element**</span></span>|<span data-ttu-id="51196-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="51196-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51196-122">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="51196-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="51196-123">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="51196-123">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="51196-124">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="51196-124">DeleteItem</span></span>](deleteitem.md) <br/> |<span data-ttu-id="51196-125">定义在 Exchange 存储中删除项目的请求。</span><span class="sxs-lookup"><span data-stu-id="51196-125">Defines a request to delete items in the Exchange store.</span></span>  <br/> <span data-ttu-id="51196-126">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="51196-126">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteItem` <br/> |
|[<span data-ttu-id="51196-127">SendItem</span><span class="sxs-lookup"><span data-stu-id="51196-127">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="51196-128">定义在 Exchange 存储中发送邮件的请求的根元素。</span><span class="sxs-lookup"><span data-stu-id="51196-128">The root element that defines a request to send items in the Exchange store.</span></span>  <br/> <span data-ttu-id="51196-129">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="51196-129">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
|[<span data-ttu-id="51196-130">GetItem</span><span class="sxs-lookup"><span data-stu-id="51196-130">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="51196-131">定义从 Exchange 存储中获取项目的请求。</span><span class="sxs-lookup"><span data-stu-id="51196-131">Defines a request to get items from the Exchange store.</span></span>  <br/> <span data-ttu-id="51196-132">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="51196-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="51196-133">MoveItem</span><span class="sxs-lookup"><span data-stu-id="51196-133">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="51196-134">定义在 Exchange 存储中移动项目的请求。</span><span class="sxs-lookup"><span data-stu-id="51196-134">Defines a request to move items in the Exchange store.</span></span>  <br/> <span data-ttu-id="51196-135">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="51196-135">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="51196-136">CopyItem</span><span class="sxs-lookup"><span data-stu-id="51196-136">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="51196-137">定义在 Exchange 存储中复制项目的请求。</span><span class="sxs-lookup"><span data-stu-id="51196-137">Defines a request to copy items in the Exchange store.</span></span>  <br/> <span data-ttu-id="51196-138">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="51196-138">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51196-139">说明</span><span class="sxs-lookup"><span data-stu-id="51196-139">Remarks</span></span>

<span data-ttu-id="51196-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="51196-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51196-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="51196-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51196-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="51196-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="51196-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="51196-143">Schema Name</span></span>  <br/> |<span data-ttu-id="51196-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="51196-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="51196-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="51196-145">Validation File</span></span>  <br/> |<span data-ttu-id="51196-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="51196-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="51196-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="51196-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="51196-148">False</span><span class="sxs-lookup"><span data-stu-id="51196-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51196-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="51196-149">See also</span></span>

- [<span data-ttu-id="51196-150">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="51196-150">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="51196-151">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="51196-151">SendItem operation</span></span>](senditem-operation.md) 
- [<span data-ttu-id="51196-152">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="51196-152">GetItem operation</span></span>](getitem-operation.md)
- [<span data-ttu-id="51196-153">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="51196-153">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="51196-154">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="51196-154">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="51196-155">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="51196-155">FindConversation operation</span></span>](findconversation-operation.md)

