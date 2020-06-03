---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: GroupBy 元素指定 FindItem 查询的任意分组。
ms.openlocfilehash: 0d681e5376e4dd71921cc97f270211e49179db85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530097"
---
# <a name="groupby"></a><span data-ttu-id="2726a-103">GroupBy</span><span class="sxs-lookup"><span data-stu-id="2726a-103">GroupBy</span></span>

<span data-ttu-id="2726a-104">**GroupBy**元素指定 FindItem 查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="2726a-104">The **GroupBy** element specifies an arbitrary grouping for FindItem queries.</span></span> 
  
- [<span data-ttu-id="2726a-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="2726a-105">FindItem</span></span>](finditem.md)
- [<span data-ttu-id="2726a-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="2726a-106">GroupBy</span></span>](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

<span data-ttu-id="2726a-107">**GroupByType**</span><span class="sxs-lookup"><span data-stu-id="2726a-107">**GroupByType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2726a-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2726a-108">Attributes and elements</span></span>

<span data-ttu-id="2726a-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2726a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2726a-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="2726a-110">Attributes</span></span>

|<span data-ttu-id="2726a-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="2726a-111">**Attribute**</span></span>|<span data-ttu-id="2726a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2726a-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2726a-113">**Order**</span><span class="sxs-lookup"><span data-stu-id="2726a-113">**Order**</span></span> <br/> | <span data-ttu-id="2726a-114">确定在响应中返回的分组项数组中组的顺序。</span><span class="sxs-lookup"><span data-stu-id="2726a-114">Determines the order of the groups in the grouped item array that is returned in the response.</span></span> <span data-ttu-id="2726a-115">此属性的类型为 SortDirectionType。</span><span class="sxs-lookup"><span data-stu-id="2726a-115">This attribute is of type SortDirectionType.</span></span>  <br/> |
   
#### <a name="order-attribute-values"></a><span data-ttu-id="2726a-116">顺序属性值</span><span class="sxs-lookup"><span data-stu-id="2726a-116">Order attribute values</span></span>

|<span data-ttu-id="2726a-117">**值**</span><span class="sxs-lookup"><span data-stu-id="2726a-117">**Value**</span></span>|<span data-ttu-id="2726a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2726a-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2726a-119">升序</span><span class="sxs-lookup"><span data-stu-id="2726a-119">Ascending</span></span>  <br/> |<span data-ttu-id="2726a-120">组按升序排列。</span><span class="sxs-lookup"><span data-stu-id="2726a-120">The groups are ordered in ascending order.</span></span>  <br/> |
|<span data-ttu-id="2726a-121">降序</span><span class="sxs-lookup"><span data-stu-id="2726a-121">Descending</span></span>  <br/> |<span data-ttu-id="2726a-122">组按降序排列。</span><span class="sxs-lookup"><span data-stu-id="2726a-122">The groups are ordered in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2726a-123">子元素</span><span class="sxs-lookup"><span data-stu-id="2726a-123">Child elements</span></span>

|<span data-ttu-id="2726a-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="2726a-124">**Element**</span></span>|<span data-ttu-id="2726a-125">**描述**</span><span class="sxs-lookup"><span data-stu-id="2726a-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2726a-126">FieldURI</span><span class="sxs-lookup"><span data-stu-id="2726a-126">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="2726a-127">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="2726a-127">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="2726a-128">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2726a-128">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="2726a-129">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="2726a-129">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="2726a-130">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="2726a-130">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="2726a-131">标识要获取、设置或创建的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="2726a-131">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="2726a-132">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="2726a-132">AggregateOn</span></span>](aggregateon.md) <br/> |<span data-ttu-id="2726a-133">表示用于确定响应中的组顺序的字段。</span><span class="sxs-lookup"><span data-stu-id="2726a-133">Represents the field that is used to determine the order of groups in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2726a-134">父元素</span><span class="sxs-lookup"><span data-stu-id="2726a-134">Parent elements</span></span>

|<span data-ttu-id="2726a-135">**元素**</span><span class="sxs-lookup"><span data-stu-id="2726a-135">**Element**</span></span>|<span data-ttu-id="2726a-136">**描述**</span><span class="sxs-lookup"><span data-stu-id="2726a-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2726a-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="2726a-137">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="2726a-138">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="2726a-138">Defines a request to find items in a mailbox.</span></span>  <br/><br/> <span data-ttu-id="2726a-139">下面是此元素的 XPath 表达式:  `/FindItem`</span><span class="sxs-lookup"><span data-stu-id="2726a-139">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2726a-140">备注</span><span class="sxs-lookup"><span data-stu-id="2726a-140">Remarks</span></span>

<span data-ttu-id="2726a-141">FindItem 响应将包含组的集合。</span><span class="sxs-lookup"><span data-stu-id="2726a-141">The FindItem response will contain a collection of groups.</span></span> <span data-ttu-id="2726a-142">每个组将包含具有**GroupBy**属性的匹配值的所有项目。</span><span class="sxs-lookup"><span data-stu-id="2726a-142">Each group will contain all items that had matching values for the **GroupBy** property.</span></span> <span data-ttu-id="2726a-143">确定分组的属性在[FieldURI](fielduri.md)、 [IndexedFieldURI](indexedfielduri.md)或[ExtendedFieldURI](extendedfielduri.md)元素中进行标识。</span><span class="sxs-lookup"><span data-stu-id="2726a-143">The property that determines the grouping is identified in the [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md), or [ExtendedFieldURI](extendedfielduri.md) element.</span></span> 
  
<span data-ttu-id="2726a-144">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2726a-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2726a-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="2726a-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2726a-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="2726a-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2726a-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="2726a-147">Schema Name</span></span>  <br/> |<span data-ttu-id="2726a-148">消息架构</span><span class="sxs-lookup"><span data-stu-id="2726a-148">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2726a-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="2726a-149">Validation File</span></span>  <br/> |<span data-ttu-id="2726a-150">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2726a-150">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2726a-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="2726a-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="2726a-152">False</span><span class="sxs-lookup"><span data-stu-id="2726a-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2726a-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2726a-153">See also</span></span>

- [<span data-ttu-id="2726a-154">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="2726a-154">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="2726a-155">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2726a-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="2726a-156">查找项目</span><span class="sxs-lookup"><span data-stu-id="2726a-156">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

