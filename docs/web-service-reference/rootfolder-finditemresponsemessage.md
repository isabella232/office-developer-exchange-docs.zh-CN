---
title: RootFolder （FindItemResponseMessage）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: RootFolder 元素包含在 FindItem 操作过程中搜索单个根文件夹的结果。
ms.openlocfilehash: 3bbab325dff26139739c50ef519b215aea620a0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457128"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="fc837-103">RootFolder （FindItemResponseMessage）</span><span class="sxs-lookup"><span data-stu-id="fc837-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="fc837-104">**RootFolder**元素包含在[FindItem 操作](finditem-operation.md)过程中搜索单个根文件夹的结果。</span><span class="sxs-lookup"><span data-stu-id="fc837-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="fc837-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="fc837-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc837-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fc837-106">Attributes and elements</span></span>

<span data-ttu-id="fc837-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc837-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc837-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fc837-108">Attributes</span></span>

|<span data-ttu-id="fc837-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fc837-109">**Attribute**</span></span>|<span data-ttu-id="fc837-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc837-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc837-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="fc837-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="fc837-112">表示在使用索引分页视图时应用于下一个请求的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="fc837-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="fc837-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="fc837-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="fc837-114">表示使用分数页面视图时用于下一个请求的新的分子值。</span><span class="sxs-lookup"><span data-stu-id="fc837-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="fc837-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="fc837-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="fc837-116">表示执行分数分页时用于下一个请求的下一个分母。</span><span class="sxs-lookup"><span data-stu-id="fc837-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="fc837-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="fc837-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="fc837-118">指示当前结果是否包含查询中的最后一项，以便不需要进一步分页。</span><span class="sxs-lookup"><span data-stu-id="fc837-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="fc837-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="fc837-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="fc837-120">表示传递限制的项目总数。</span><span class="sxs-lookup"><span data-stu-id="fc837-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="fc837-121">在分组的[FindItem 操作](finditem-operation.md)中， **TotalItemsInView**属性返回视图中的项目总数加上总组数。</span><span class="sxs-lookup"><span data-stu-id="fc837-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fc837-122">子元素</span><span class="sxs-lookup"><span data-stu-id="fc837-122">Child elements</span></span>

|<span data-ttu-id="fc837-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc837-123">**Element**</span></span>|<span data-ttu-id="fc837-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc837-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc837-125">Items</span><span class="sxs-lookup"><span data-stu-id="fc837-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="fc837-126">包含找到的项的数组，这些项具有在[FindItem 操作](finditem-operation.md)请求中标识的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="fc837-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="fc837-127">组</span><span class="sxs-lookup"><span data-stu-id="fc837-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="fc837-128">包含找到的组的集合，这些组具有在[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件。</span><span class="sxs-lookup"><span data-stu-id="fc837-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc837-129">父元素</span><span class="sxs-lookup"><span data-stu-id="fc837-129">Parent elements</span></span>

|<span data-ttu-id="fc837-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc837-130">**Element**</span></span>|<span data-ttu-id="fc837-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc837-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc837-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fc837-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="fc837-133">包含[FindItem 操作](finditem-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="fc837-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc837-134">备注</span><span class="sxs-lookup"><span data-stu-id="fc837-134">Remarks</span></span>

<span data-ttu-id="fc837-135">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fc837-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc837-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="fc837-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc837-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="fc837-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fc837-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="fc837-138">Schema name</span></span>  <br/> |<span data-ttu-id="fc837-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="fc837-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fc837-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="fc837-140">Validation file</span></span>  <br/> |<span data-ttu-id="fc837-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fc837-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fc837-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="fc837-142">Can be empty</span></span>  <br/> |<span data-ttu-id="fc837-143">False</span><span class="sxs-lookup"><span data-stu-id="fc837-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc837-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc837-144">See also</span></span>



[<span data-ttu-id="fc837-145">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="fc837-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="fc837-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="fc837-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="fc837-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="fc837-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="fc837-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="fc837-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="fc837-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="fc837-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="fc837-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="fc837-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="fc837-151">查找项目</span><span class="sxs-lookup"><span data-stu-id="fc837-151">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

