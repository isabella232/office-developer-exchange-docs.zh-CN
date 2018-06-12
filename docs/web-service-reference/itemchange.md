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
ms.openlocfilehash: d10ce96cacb0be7411c4e8230ebc9b2803b7a5b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826145"
---
# <a name="itemchange"></a><span data-ttu-id="eaa54-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="eaa54-103">ItemChange</span></span>

<span data-ttu-id="eaa54-104">**ItemChange**元素包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="eaa54-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
[<span data-ttu-id="eaa54-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="eaa54-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="eaa54-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="eaa54-106">ItemChanges</span></span>](itemchanges.md)
  
[<span data-ttu-id="eaa54-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="eaa54-107">ItemChange</span></span>](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

 <span data-ttu-id="eaa54-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="eaa54-108">**ItemChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eaa54-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eaa54-109">Attributes and elements</span></span>

<span data-ttu-id="eaa54-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eaa54-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eaa54-111">属性</span><span class="sxs-lookup"><span data-stu-id="eaa54-111">Attributes</span></span>

<span data-ttu-id="eaa54-112">无。</span><span class="sxs-lookup"><span data-stu-id="eaa54-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eaa54-113">子元素</span><span class="sxs-lookup"><span data-stu-id="eaa54-113">Child elements</span></span>

|<span data-ttu-id="eaa54-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="eaa54-114">**Element**</span></span>|<span data-ttu-id="eaa54-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="eaa54-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eaa54-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="eaa54-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="eaa54-117">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="eaa54-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="eaa54-118">如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="eaa54-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="eaa54-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="eaa54-120">标识定期项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="eaa54-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="eaa54-121">如果使用此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-121">This element is required if used.</span></span> <span data-ttu-id="eaa54-122">如果未使用的[RecurringMasterItemId](recurringmasteritemid.md)或[ItemId](itemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="eaa54-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="eaa54-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="eaa54-124">标识通过其相关的匹配项的标识符之一确定定期主项目。</span><span class="sxs-lookup"><span data-stu-id="eaa54-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="eaa54-125">如果使用此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-125">This element is required if used.</span></span> <span data-ttu-id="eaa54-126">如果未使用的[OccurrenceItemId](occurrenceitemid.md)或[ItemId](itemid.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="eaa54-127">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="eaa54-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="eaa54-128">包含定义的数组的 append、 设置和删除项目属性更改。</span><span class="sxs-lookup"><span data-stu-id="eaa54-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="eaa54-129">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="eaa54-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eaa54-130">父元素</span><span class="sxs-lookup"><span data-stu-id="eaa54-130">Parent elements</span></span>

|<span data-ttu-id="eaa54-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="eaa54-131">**Element**</span></span>|<span data-ttu-id="eaa54-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="eaa54-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eaa54-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="eaa54-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="eaa54-134">包含确定项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="eaa54-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="eaa54-135">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="eaa54-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eaa54-136">备注</span><span class="sxs-lookup"><span data-stu-id="eaa54-136">Remarks</span></span>

<span data-ttu-id="eaa54-137">可在**ItemChange**元素只能包含单个[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="eaa54-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="eaa54-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eaa54-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eaa54-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="eaa54-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eaa54-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="eaa54-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eaa54-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="eaa54-141">Schema Name</span></span>  <br/> |<span data-ttu-id="eaa54-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="eaa54-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="eaa54-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="eaa54-143">Validation File</span></span>  <br/> |<span data-ttu-id="eaa54-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eaa54-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eaa54-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="eaa54-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="eaa54-146">False</span><span class="sxs-lookup"><span data-stu-id="eaa54-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eaa54-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eaa54-147">See also</span></span>



[<span data-ttu-id="eaa54-148">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="eaa54-148">UpdateItem operation</span></span>](updateitem-operation.md)

