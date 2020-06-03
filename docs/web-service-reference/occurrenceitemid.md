---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: OccurrenceItemId 元素标识定期项目的单个事件。
ms.openlocfilehash: 37c3a2442afb3302bca88ef0301e98013ff0319b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468374"
---
# <a name="occurrenceitemid"></a><span data-ttu-id="d59f5-103">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="d59f5-103">OccurrenceItemId</span></span>

<span data-ttu-id="d59f5-104">**OccurrenceItemId**元素标识定期项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="d59f5-104">The **OccurrenceItemId** element identifies a single occurrence of a recurring item.</span></span> 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

<span data-ttu-id="d59f5-105">**OccurrenceItemIdType**</span><span class="sxs-lookup"><span data-stu-id="d59f5-105">**OccurrenceItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d59f5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d59f5-106">Attributes and elements</span></span>

<span data-ttu-id="d59f5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d59f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d59f5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d59f5-108">Attributes</span></span>

|<span data-ttu-id="d59f5-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d59f5-109">**Attribute**</span></span>|<span data-ttu-id="d59f5-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d59f5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d59f5-111">**RecurringMasterId**</span><span class="sxs-lookup"><span data-stu-id="d59f5-111">**RecurringMasterId**</span></span> <br/> |<span data-ttu-id="d59f5-112">标识定期项目的定期母版。</span><span class="sxs-lookup"><span data-stu-id="d59f5-112">Identifies the recurring master of a recurring item.</span></span> <span data-ttu-id="d59f5-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d59f5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="d59f5-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="d59f5-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="d59f5-115">标识定期母版或项目发生的特定版本。</span><span class="sxs-lookup"><span data-stu-id="d59f5-115">Identifies a specific version of the recurring master or an item occurrence.</span></span> <span data-ttu-id="d59f5-116">如果定期主数据或其任何发生发生更改，则**ChangeKey**会发生更改。</span><span class="sxs-lookup"><span data-stu-id="d59f5-116">If either the recurring master or any of its occurrences change, the **ChangeKey** changes.</span></span> <span data-ttu-id="d59f5-117">对于定期母版和所有事件， **ChangeKey**是相同的。</span><span class="sxs-lookup"><span data-stu-id="d59f5-117">The **ChangeKey** is the same for the recurring master and all occurrences.</span></span>  <br/> |
|<span data-ttu-id="d59f5-118">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="d59f5-118">**InstanceIndex**</span></span> <br/> |<span data-ttu-id="d59f5-119">标识项目发生的索引。</span><span class="sxs-lookup"><span data-stu-id="d59f5-119">Identifies the index of the item occurrence.</span></span> <span data-ttu-id="d59f5-120">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d59f5-120">This attribute is required.</span></span> <span data-ttu-id="d59f5-121">此值表示一个整数。</span><span class="sxs-lookup"><span data-stu-id="d59f5-121">This value represents an integer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d59f5-122">子元素</span><span class="sxs-lookup"><span data-stu-id="d59f5-122">Child elements</span></span>

<span data-ttu-id="d59f5-123">无。</span><span class="sxs-lookup"><span data-stu-id="d59f5-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d59f5-124">父元素</span><span class="sxs-lookup"><span data-stu-id="d59f5-124">Parent elements</span></span>

|<span data-ttu-id="d59f5-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="d59f5-125">**Element**</span></span>|<span data-ttu-id="d59f5-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="d59f5-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d59f5-127">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="d59f5-127">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="d59f5-128">包含邮箱中所有会话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="d59f5-128">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d59f5-129">ItemIds</span><span class="sxs-lookup"><span data-stu-id="d59f5-129">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="d59f5-130">包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="d59f5-130">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/><br/><span data-ttu-id="d59f5-131">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="d59f5-131">The following are the XPath expressions to this element:</span></span> <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/><span data-ttu-id="d59f5-132">**注意**： [MoveItem 操作](moveitem-operation.md)和[CopyItem 操作](copyitem-operation.md)仅适用于单个日历项目和定期的主项目。</span><span class="sxs-lookup"><span data-stu-id="d59f5-132">**NOTE**: [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items.</span></span> <span data-ttu-id="d59f5-133">通过这些操作，项目发生次数无效。</span><span class="sxs-lookup"><span data-stu-id="d59f5-133">Item occurrences are invalid with these operations.</span></span>           |
|[<span data-ttu-id="d59f5-134">ItemChange</span><span class="sxs-lookup"><span data-stu-id="d59f5-134">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="d59f5-135">包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="d59f5-135">Contains an item identifier and the updates to apply to the item.</span></span><br/><br/> <span data-ttu-id="d59f5-136">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="d59f5-136">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d59f5-137">文本值</span><span class="sxs-lookup"><span data-stu-id="d59f5-137">Text value</span></span>

<span data-ttu-id="d59f5-138">无。</span><span class="sxs-lookup"><span data-stu-id="d59f5-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d59f5-139">说明</span><span class="sxs-lookup"><span data-stu-id="d59f5-139">Remarks</span></span>

<span data-ttu-id="d59f5-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d59f5-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="d59f5-141">示例</span><span class="sxs-lookup"><span data-stu-id="d59f5-141">Example</span></span>

<span data-ttu-id="d59f5-142">下面的示例确定具有标识34vswe4 的定期项的第四次发生。</span><span class="sxs-lookup"><span data-stu-id="d59f5-142">The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.</span></span>
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a><span data-ttu-id="d59f5-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="d59f5-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d59f5-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="d59f5-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d59f5-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="d59f5-145">Schema Name</span></span>  <br/> |<span data-ttu-id="d59f5-146">类型架构</span><span class="sxs-lookup"><span data-stu-id="d59f5-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="d59f5-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="d59f5-147">Validation File</span></span>  <br/> |<span data-ttu-id="d59f5-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d59f5-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d59f5-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="d59f5-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="d59f5-150">False</span><span class="sxs-lookup"><span data-stu-id="d59f5-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d59f5-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d59f5-151">See also</span></span>

- [<span data-ttu-id="d59f5-152">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="d59f5-152">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
- [<span data-ttu-id="d59f5-153">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="d59f5-153">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="d59f5-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d59f5-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

