---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: RecurringMasterItemId 元素通过标识一个定期的主项目来标识该项目的相关发生项的标识符。
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529880"
---
# <a name="recurringmasteritemid"></a><span data-ttu-id="a7711-103">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="a7711-103">RecurringMasterItemId</span></span>

<span data-ttu-id="a7711-104">**RecurringMasterItemId**元素通过标识一个定期的主项目来标识该项目的相关发生项的标识符。</span><span class="sxs-lookup"><span data-stu-id="a7711-104">The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 <span data-ttu-id="a7711-105">**RecurringMasterItemIdType**</span><span class="sxs-lookup"><span data-stu-id="a7711-105">**RecurringMasterItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7711-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a7711-106">Attributes and elements</span></span>

<span data-ttu-id="a7711-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7711-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7711-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a7711-108">Attributes</span></span>

|<span data-ttu-id="a7711-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="a7711-109">**Attribute**</span></span>|<span data-ttu-id="a7711-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7711-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7711-111">**OccurrenceId**</span><span class="sxs-lookup"><span data-stu-id="a7711-111">**OccurrenceId**</span></span> <br/> |<span data-ttu-id="a7711-112">标识定期主项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="a7711-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="a7711-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="a7711-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a7711-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="a7711-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="a7711-115">标识定期主项目的单个事件的特定版本。</span><span class="sxs-lookup"><span data-stu-id="a7711-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="a7711-116">此外，还会标识定期主项目，因为它和单个事件将包含相同的更改密钥。</span><span class="sxs-lookup"><span data-stu-id="a7711-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="a7711-117">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="a7711-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a7711-118">子元素</span><span class="sxs-lookup"><span data-stu-id="a7711-118">Child elements</span></span>

<span data-ttu-id="a7711-119">无。</span><span class="sxs-lookup"><span data-stu-id="a7711-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a7711-120">父元素</span><span class="sxs-lookup"><span data-stu-id="a7711-120">Parent elements</span></span>

|<span data-ttu-id="a7711-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7711-121">**Element**</span></span>|<span data-ttu-id="a7711-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7711-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7711-123">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="a7711-123">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="a7711-124">包含邮箱中所有会话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="a7711-124">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a7711-125">ItemChange</span><span class="sxs-lookup"><span data-stu-id="a7711-125">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="a7711-126">包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="a7711-126">Contains an item identifier and the updates to apply to the item.</span></span> <br/> <br/> <span data-ttu-id="a7711-127">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a7711-127">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="a7711-128">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a7711-128">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="a7711-129">包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="a7711-129">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="a7711-130">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a7711-130">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a7711-131">文本值</span><span class="sxs-lookup"><span data-stu-id="a7711-131">Text value</span></span>

<span data-ttu-id="a7711-132">无。</span><span class="sxs-lookup"><span data-stu-id="a7711-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7711-133">说明</span><span class="sxs-lookup"><span data-stu-id="a7711-133">Remarks</span></span>

<span data-ttu-id="a7711-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a7711-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="a7711-135">示例</span><span class="sxs-lookup"><span data-stu-id="a7711-135">Example</span></span>

<span data-ttu-id="a7711-136">下面的示例通过使用标识符56lkjh6 标识其匹配项之一来标识定期主项目。</span><span class="sxs-lookup"><span data-stu-id="a7711-136">The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.</span></span>
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a><span data-ttu-id="a7711-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="a7711-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7711-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="a7711-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7711-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="a7711-139">Schema Name</span></span>  <br/> |<span data-ttu-id="a7711-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="a7711-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7711-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="a7711-141">Validation File</span></span>  <br/> |<span data-ttu-id="a7711-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7711-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7711-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="a7711-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7711-144">False</span><span class="sxs-lookup"><span data-stu-id="a7711-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7711-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7711-145">See also</span></span>

- [<span data-ttu-id="a7711-146">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="a7711-146">OccurrenceItemId</span></span>](occurrenceitemid.md)
- [<span data-ttu-id="a7711-147">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="a7711-147">FindConversation operation</span></span>](findconversation-operation.md)

