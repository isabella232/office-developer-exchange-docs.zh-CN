---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: ItemChange 元素包含项标识符和更新应用到的项。
ms.openlocfilehash: 42484c8deecb106e05023215342af3c7d996d852
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353509"
---
# <a name="itemchange"></a><span data-ttu-id="b9553-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="b9553-103">ItemChange</span></span>

<span data-ttu-id="b9553-104">**ItemChange**元素包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="b9553-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
- [<span data-ttu-id="b9553-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b9553-105">UpdateItem</span></span>](updateitem.md) 
- [<span data-ttu-id="b9553-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="b9553-106">ItemChanges</span></span>](itemchanges.md)
- [<span data-ttu-id="b9553-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="b9553-107">ItemChange</span></span>](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

<span data-ttu-id="b9553-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="b9553-108">**ItemChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b9553-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b9553-109">Attributes and elements</span></span>

<span data-ttu-id="b9553-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b9553-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9553-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="b9553-111">Attributes</span></span>

<span data-ttu-id="b9553-112">无。</span><span class="sxs-lookup"><span data-stu-id="b9553-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9553-113">子元素</span><span class="sxs-lookup"><span data-stu-id="b9553-113">Child elements</span></span>

|<span data-ttu-id="b9553-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="b9553-114">**Element**</span></span>|<span data-ttu-id="b9553-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="b9553-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9553-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="b9553-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b9553-117">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="b9553-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="b9553-118">如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="b9553-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="b9553-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="b9553-120">标识定期项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="b9553-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="b9553-121">如果使用此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-121">This element is required if used.</span></span> <span data-ttu-id="b9553-122">如果未使用的[RecurringMasterItemId](recurringmasteritemid.md)或[ItemId](itemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="b9553-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="b9553-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="b9553-124">标识通过其相关的匹配项的标识符之一确定定期主项目。</span><span class="sxs-lookup"><span data-stu-id="b9553-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="b9553-125">如果使用此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-125">This element is required if used.</span></span> <span data-ttu-id="b9553-126">如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[ItemId](itemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="b9553-127">Updates (Item)</span><span class="sxs-lookup"><span data-stu-id="b9553-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="b9553-128">包含定义的数组的 append、 设置和删除项目属性更改。</span><span class="sxs-lookup"><span data-stu-id="b9553-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="b9553-129">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b9553-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b9553-130">父元素</span><span class="sxs-lookup"><span data-stu-id="b9553-130">Parent elements</span></span>

|<span data-ttu-id="b9553-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="b9553-131">**Element**</span></span>|<span data-ttu-id="b9553-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="b9553-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9553-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="b9553-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="b9553-134">包含确定项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="b9553-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="b9553-135">下面是此元素的 XPath 表达式:  </span><span class="sxs-lookup"><span data-stu-id="b9553-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9553-136">说明</span><span class="sxs-lookup"><span data-stu-id="b9553-136">Remarks</span></span>

<span data-ttu-id="b9553-137">可在**ItemChange**元素只能包含单个[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="b9553-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="b9553-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b9553-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9553-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="b9553-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9553-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="b9553-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9553-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="b9553-141">Schema Name</span></span>  <br/> |<span data-ttu-id="b9553-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="b9553-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9553-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="b9553-143">Validation File</span></span>  <br/> |<span data-ttu-id="b9553-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9553-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9553-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="b9553-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9553-146">False</span><span class="sxs-lookup"><span data-stu-id="b9553-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9553-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9553-147">See also</span></span>

- [<span data-ttu-id="b9553-148">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="b9553-148">UpdateItem operation</span></span>](updateitem-operation.md)

