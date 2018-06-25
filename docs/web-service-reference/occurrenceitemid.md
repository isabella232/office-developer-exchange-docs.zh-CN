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
description: OccurrenceItemId 元素标识定期项目的一个匹配项。
ms.openlocfilehash: e3d7b6efc49775f54219ce0dc0ec39a34a95f8fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826639"
---
# <a name="occurrenceitemid"></a><span data-ttu-id="5b741-103">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="5b741-103">OccurrenceItemId</span></span>

<span data-ttu-id="5b741-104">**OccurrenceItemId**元素标识定期项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="5b741-104">The **OccurrenceItemId** element identifies a single occurrence of a recurring item.</span></span> 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

<span data-ttu-id="5b741-105">**OccurrenceItemIdType**</span><span class="sxs-lookup"><span data-stu-id="5b741-105">**OccurrenceItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5b741-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5b741-106">Attributes and elements</span></span>

<span data-ttu-id="5b741-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b741-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b741-108">属性</span><span class="sxs-lookup"><span data-stu-id="5b741-108">Attributes</span></span>

|<span data-ttu-id="5b741-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5b741-109">**Attribute**</span></span>|<span data-ttu-id="5b741-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b741-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b741-111">**RecurringMasterId**</span><span class="sxs-lookup"><span data-stu-id="5b741-111">**RecurringMasterId**</span></span> <br/> |<span data-ttu-id="5b741-112">标识定期项目的定期母的版。</span><span class="sxs-lookup"><span data-stu-id="5b741-112">Identifies the recurring master of a recurring item.</span></span> <span data-ttu-id="5b741-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="5b741-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="5b741-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="5b741-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="5b741-115">标识定期主控形状或项匹配项的特定版本。</span><span class="sxs-lookup"><span data-stu-id="5b741-115">Identifies a specific version of the recurring master or an item occurrence.</span></span> <span data-ttu-id="5b741-116">如果定期主控形状或其出现的任何更改，**更改密钥**更改。</span><span class="sxs-lookup"><span data-stu-id="5b741-116">If either the recurring master or any of its occurrences change, the **ChangeKey** changes.</span></span> <span data-ttu-id="5b741-117">**更改密钥**是相同的定期主控形状和所有匹配项。</span><span class="sxs-lookup"><span data-stu-id="5b741-117">The **ChangeKey** is the same for the recurring master and all occurrences.</span></span>  <br/> |
|<span data-ttu-id="5b741-118">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="5b741-118">**InstanceIndex**</span></span> <br/> |<span data-ttu-id="5b741-119">标识项目匹配项的索引。</span><span class="sxs-lookup"><span data-stu-id="5b741-119">Identifies the index of the item occurrence.</span></span> <span data-ttu-id="5b741-120">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="5b741-120">This attribute is required.</span></span> <span data-ttu-id="5b741-121">此值表示的整数。</span><span class="sxs-lookup"><span data-stu-id="5b741-121">This value represents an integer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5b741-122">子元素</span><span class="sxs-lookup"><span data-stu-id="5b741-122">Child elements</span></span>

<span data-ttu-id="5b741-123">无。</span><span class="sxs-lookup"><span data-stu-id="5b741-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5b741-124">父元素</span><span class="sxs-lookup"><span data-stu-id="5b741-124">Parent elements</span></span>

|<span data-ttu-id="5b741-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="5b741-125">**Element**</span></span>|<span data-ttu-id="5b741-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b741-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b741-127">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="5b741-127">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="5b741-128">包含的项标识符的邮箱中的所有对话项的集合。</span><span class="sxs-lookup"><span data-stu-id="5b741-128">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5b741-129">ItemIds</span><span class="sxs-lookup"><span data-stu-id="5b741-129">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="5b741-130">包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="5b741-130">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/><br/><span data-ttu-id="5b741-131">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="5b741-131">The following are the XPath expressions to this element:</span></span> <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/><span data-ttu-id="5b741-132">**注意**： [MoveItem 操作](moveitem-operation.md)和[CopyItem 操作](copyitem-operation.md)仅使用单个日历项和定期主项目。</span><span class="sxs-lookup"><span data-stu-id="5b741-132">**Note**:  [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items.</span></span> <span data-ttu-id="5b741-133">项目出现，则使用这些操作无效。</span><span class="sxs-lookup"><span data-stu-id="5b741-133">Item occurrences are invalid with these operations.</span></span>           |
|[<span data-ttu-id="5b741-134">ItemChange</span><span class="sxs-lookup"><span data-stu-id="5b741-134">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="5b741-135">包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="5b741-135">Contains an item identifier and the updates to apply to the item.</span></span><br/><br/> <span data-ttu-id="5b741-136">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="5b741-136">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5b741-137">文本值</span><span class="sxs-lookup"><span data-stu-id="5b741-137">Text value</span></span>

<span data-ttu-id="5b741-138">无。</span><span class="sxs-lookup"><span data-stu-id="5b741-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b741-139">备注</span><span class="sxs-lookup"><span data-stu-id="5b741-139">Remarks</span></span>

<span data-ttu-id="5b741-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5b741-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="5b741-141">示例</span><span class="sxs-lookup"><span data-stu-id="5b741-141">Example</span></span>

<span data-ttu-id="5b741-142">以下示例标识具有标识 34vswe4 定期项目的第四个匹配项。</span><span class="sxs-lookup"><span data-stu-id="5b741-142">The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.</span></span>
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a><span data-ttu-id="5b741-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="5b741-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b741-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="5b741-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5b741-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="5b741-145">Schema Name</span></span>  <br/> |<span data-ttu-id="5b741-146">类型架构</span><span class="sxs-lookup"><span data-stu-id="5b741-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="5b741-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="5b741-147">Validation File</span></span>  <br/> |<span data-ttu-id="5b741-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5b741-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5b741-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="5b741-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b741-150">False</span><span class="sxs-lookup"><span data-stu-id="5b741-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b741-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b741-151">See also</span></span>

- [<span data-ttu-id="5b741-152">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="5b741-152">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
- [<span data-ttu-id="5b741-153">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="5b741-153">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="5b741-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5b741-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

