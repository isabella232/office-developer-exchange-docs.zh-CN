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
description: ItemChange 元素包含项目标识符和要应用于项目的更新。
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459915"
---
# <a name="itemchange"></a><span data-ttu-id="47894-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="47894-103">ItemChange</span></span>

<span data-ttu-id="47894-104">**ItemChange**元素包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="47894-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
- [<span data-ttu-id="47894-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="47894-105">UpdateItem</span></span>](updateitem.md) 
- [<span data-ttu-id="47894-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="47894-106">ItemChanges</span></span>](itemchanges.md)
- [<span data-ttu-id="47894-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="47894-107">ItemChange</span></span>](itemchange.md)
  
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

<span data-ttu-id="47894-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="47894-108">**ItemChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="47894-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="47894-109">Attributes and elements</span></span>

<span data-ttu-id="47894-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="47894-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47894-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="47894-111">Attributes</span></span>

<span data-ttu-id="47894-112">无。</span><span class="sxs-lookup"><span data-stu-id="47894-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47894-113">子元素</span><span class="sxs-lookup"><span data-stu-id="47894-113">Child elements</span></span>

|<span data-ttu-id="47894-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="47894-114">**Element**</span></span>|<span data-ttu-id="47894-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="47894-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47894-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="47894-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="47894-117">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="47894-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="47894-118">如果未使用[OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="47894-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="47894-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="47894-120">标识定期项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="47894-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="47894-121">如果使用此元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-121">This element is required if used.</span></span> <span data-ttu-id="47894-122">如果未使用[RecurringMasterItemId](recurringmasteritemid.md)或[ItemId](itemid.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="47894-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="47894-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="47894-124">通过标识一个 "定期" 主项目的 "标识符" 标识该项目。</span><span class="sxs-lookup"><span data-stu-id="47894-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="47894-125">如果使用此元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-125">This element is required if used.</span></span> <span data-ttu-id="47894-126">如果未使用[OccurrenceItemId](occurrenceitemid.md)或[ItemId](itemid.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="47894-127">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="47894-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="47894-128">包含定义追加、设置和删除对项属性所做的更改的数组。</span><span class="sxs-lookup"><span data-stu-id="47894-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="47894-129">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="47894-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="47894-130">父元素</span><span class="sxs-lookup"><span data-stu-id="47894-130">Parent elements</span></span>

|<span data-ttu-id="47894-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="47894-131">**Element**</span></span>|<span data-ttu-id="47894-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="47894-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47894-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="47894-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="47894-134">包含标识项目和要应用于项目的更新的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="47894-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="47894-135">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="47894-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="47894-136">备注</span><span class="sxs-lookup"><span data-stu-id="47894-136">Remarks</span></span>

<span data-ttu-id="47894-137">只有一个[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素可以在**ItemChange**元素中使用。</span><span class="sxs-lookup"><span data-stu-id="47894-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="47894-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="47894-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47894-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="47894-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47894-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="47894-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="47894-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="47894-141">Schema Name</span></span>  <br/> |<span data-ttu-id="47894-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="47894-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="47894-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="47894-143">Validation File</span></span>  <br/> |<span data-ttu-id="47894-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="47894-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="47894-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="47894-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="47894-146">False</span><span class="sxs-lookup"><span data-stu-id="47894-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47894-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47894-147">See also</span></span>

- [<span data-ttu-id="47894-148">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="47894-148">UpdateItem operation</span></span>](updateitem-operation.md)

