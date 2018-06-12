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
description: RecurringMasterItemId 元素标识定期主项目通过标识之一的及其相关的匹配项的标识符。
ms.openlocfilehash: ae59e33ece55d85435ece4c9030ccda32eb62eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827015"
---
# <a name="recurringmasteritemid"></a><span data-ttu-id="bb4a5-103">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="bb4a5-103">RecurringMasterItemId</span></span>

<span data-ttu-id="bb4a5-104">**RecurringMasterItemId**元素标识定期主项目通过标识之一的及其相关的匹配项的标识符。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-104">The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 <span data-ttu-id="bb4a5-105">**RecurringMasterItemIdType**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-105">**RecurringMasterItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb4a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bb4a5-106">Attributes and elements</span></span>

<span data-ttu-id="bb4a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb4a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="bb4a5-108">Attributes</span></span>

|<span data-ttu-id="bb4a5-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-109">**Attribute**</span></span>|<span data-ttu-id="bb4a5-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb4a5-111">**OccurrenceId**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-111">**OccurrenceId**</span></span> <br/> |<span data-ttu-id="bb4a5-112">标识定期主项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="bb4a5-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="bb4a5-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="bb4a5-115">标识定期主项目的一个匹配项的特定版本。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="bb4a5-116">此外，因为它和一次将包含相同的更改键，也被标识定期主项目。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="bb4a5-117">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bb4a5-118">子元素</span><span class="sxs-lookup"><span data-stu-id="bb4a5-118">Child elements</span></span>

<span data-ttu-id="bb4a5-119">无。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb4a5-120">父元素</span><span class="sxs-lookup"><span data-stu-id="bb4a5-120">Parent elements</span></span>

|<span data-ttu-id="bb4a5-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-121">**Element**</span></span>|<span data-ttu-id="bb4a5-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="bb4a5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb4a5-123">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="bb4a5-123">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="bb4a5-124">包含的项标识符的邮箱中的所有对话项的集合。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-124">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="bb4a5-125">ItemChange</span><span class="sxs-lookup"><span data-stu-id="bb4a5-125">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="bb4a5-126">包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-126">Contains an item identifier and the updates to apply to the item.</span></span> <br/> <br/> <span data-ttu-id="bb4a5-127">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="bb4a5-127">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="bb4a5-128">ItemIds</span><span class="sxs-lookup"><span data-stu-id="bb4a5-128">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="bb4a5-129">包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-129">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="bb4a5-130">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="bb4a5-130">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bb4a5-131">文本值</span><span class="sxs-lookup"><span data-stu-id="bb4a5-131">Text value</span></span>

<span data-ttu-id="bb4a5-132">无。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb4a5-133">备注</span><span class="sxs-lookup"><span data-stu-id="bb4a5-133">Remarks</span></span>

<span data-ttu-id="bb4a5-134">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="bb4a5-135">示例</span><span class="sxs-lookup"><span data-stu-id="bb4a5-135">Example</span></span>

<span data-ttu-id="bb4a5-136">下面的示例通过识别与标识符 56lkjh6 其情况之一标识定期主项目。</span><span class="sxs-lookup"><span data-stu-id="bb4a5-136">The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.</span></span>
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a><span data-ttu-id="bb4a5-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="bb4a5-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb4a5-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="bb4a5-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bb4a5-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="bb4a5-139">Schema Name</span></span>  <br/> |<span data-ttu-id="bb4a5-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="bb4a5-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bb4a5-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="bb4a5-141">Validation File</span></span>  <br/> |<span data-ttu-id="bb4a5-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bb4a5-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bb4a5-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="bb4a5-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb4a5-144">False</span><span class="sxs-lookup"><span data-stu-id="bb4a5-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb4a5-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb4a5-145">See also</span></span>

- [<span data-ttu-id="bb4a5-146">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="bb4a5-146">OccurrenceItemId</span></span>](occurrenceitemid.md)
- [<span data-ttu-id="bb4a5-147">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="bb4a5-147">FindConversation operation</span></span>](findconversation-operation.md)

