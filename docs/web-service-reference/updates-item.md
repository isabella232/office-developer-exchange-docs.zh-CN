---
title: 更新（项目）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: Updates 元素包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。
ms.openlocfilehash: 6902ea4d3d3d9adc074745d5642cdfa6d91a9163
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456351"
---
# <a name="updates-item"></a><span data-ttu-id="92703-103">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="92703-103">Updates (Item)</span></span>

<span data-ttu-id="92703-104">**Updates**元素包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="92703-104">The **Updates** element contains a set of elements that define append, set, and delete changes to item properties.</span></span> 
  
- [<span data-ttu-id="92703-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="92703-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="92703-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="92703-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="92703-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="92703-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="92703-108">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="92703-108">Updates (Item)</span></span>](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

<span data-ttu-id="92703-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="92703-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="92703-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92703-110">Attributes and elements</span></span>

<span data-ttu-id="92703-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92703-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92703-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="92703-112">Attributes</span></span>

<span data-ttu-id="92703-113">无。</span><span class="sxs-lookup"><span data-stu-id="92703-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92703-114">子元素</span><span class="sxs-lookup"><span data-stu-id="92703-114">Child elements</span></span>

|<span data-ttu-id="92703-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="92703-115">**Element**</span></span>|<span data-ttu-id="92703-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="92703-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92703-117">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="92703-117">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="92703-118">表示在[UpdateItem 操作](updateitem-operation.md)过程中追加到项的单个属性的数据。</span><span class="sxs-lookup"><span data-stu-id="92703-118">Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="92703-119">SetItemField</span><span class="sxs-lookup"><span data-stu-id="92703-119">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="92703-120">表示对[UpdateItem 操作](updateitem-operation.md)中项的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="92703-120">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="92703-121">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="92703-121">DeleteItemField</span></span>](deleteitemfield.md) <br/> |<span data-ttu-id="92703-122">表示在[UpdateItem 操作](updateitem-operation.md)过程中从项中删除给定属性的操作。</span><span class="sxs-lookup"><span data-stu-id="92703-122">Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92703-123">父元素</span><span class="sxs-lookup"><span data-stu-id="92703-123">Parent elements</span></span>

|<span data-ttu-id="92703-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="92703-124">**Element**</span></span>|<span data-ttu-id="92703-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="92703-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92703-126">ItemChange</span><span class="sxs-lookup"><span data-stu-id="92703-126">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="92703-127">包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="92703-127">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> <span data-ttu-id="92703-128">下面是此元素的 XPath 表达式:  `/UpdateItem/ItemChanges/ItemChange[i]`</span><span class="sxs-lookup"><span data-stu-id="92703-128">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92703-129">备注</span><span class="sxs-lookup"><span data-stu-id="92703-129">Remarks</span></span>

<span data-ttu-id="92703-130">此元素定义的更新将对由[ItemId](itemid.md)、 [OccurrenceItemId](occurrenceitemid.md)或[RecurringMasterItemId](recurringmasteritemid.md)元素标识的项目执行。</span><span class="sxs-lookup"><span data-stu-id="92703-130">The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements.</span></span> 
  
<span data-ttu-id="92703-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="92703-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92703-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="92703-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92703-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="92703-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92703-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="92703-134">Schema Name</span></span>  <br/> |<span data-ttu-id="92703-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="92703-135">types schema</span></span>  <br/> |
|<span data-ttu-id="92703-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="92703-136">Validation File</span></span>  <br/> |<span data-ttu-id="92703-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92703-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92703-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="92703-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="92703-139">False</span><span class="sxs-lookup"><span data-stu-id="92703-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92703-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92703-140">See also</span></span>

- [<span data-ttu-id="92703-141">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="92703-141">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="92703-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="92703-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

