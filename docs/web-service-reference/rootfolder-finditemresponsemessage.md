---
title: RootFolder (FindItemResponseMessage)
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
description: RootFolder 元素包含 FindItem 操作过程中的单个根文件夹的搜索结果。
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827254"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="41770-103">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="41770-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="41770-104">**RootFolder**元素包含[FindItem 操作](finditem-operation.md)期间的单个根文件夹的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="41770-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="41770-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="41770-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41770-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41770-106">Attributes and elements</span></span>

<span data-ttu-id="41770-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41770-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41770-108">属性</span><span class="sxs-lookup"><span data-stu-id="41770-108">Attributes</span></span>

|<span data-ttu-id="41770-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="41770-109">**Attribute**</span></span>|<span data-ttu-id="41770-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="41770-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41770-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="41770-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="41770-112">表示使用索引的分页视图时，则在下一个请求时应使用的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="41770-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="41770-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="41770-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="41770-114">代表要用于下一个请求时使用分数页面视图的新分子值。</span><span class="sxs-lookup"><span data-stu-id="41770-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="41770-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="41770-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="41770-116">代表下一步分母执行分数分页时用于下一个请求。</span><span class="sxs-lookup"><span data-stu-id="41770-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="41770-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="41770-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="41770-118">指示当前结果是否包含在查询中，最后一项，因此不需要进一步分页。</span><span class="sxs-lookup"><span data-stu-id="41770-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="41770-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="41770-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="41770-120">表示超出限制的项目总数。</span><span class="sxs-lookup"><span data-stu-id="41770-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="41770-121">在组合[FindItem 操作](finditem-operation.md)， **TotalItemsInView**属性返回的视图中的项目总数以及组的总数。</span><span class="sxs-lookup"><span data-stu-id="41770-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="41770-122">子元素</span><span class="sxs-lookup"><span data-stu-id="41770-122">Child elements</span></span>

|<span data-ttu-id="41770-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="41770-123">**Element**</span></span>|<span data-ttu-id="41770-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="41770-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41770-125">Items</span><span class="sxs-lookup"><span data-stu-id="41770-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="41770-126">包含数组中找到的项目的已标识[FindItem 操作](finditem-operation.md)请求中的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="41770-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="41770-127">组</span><span class="sxs-lookup"><span data-stu-id="41770-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="41770-128">包含一组具有[FindItem 操作](finditem-operation.md)请求中标识的搜索和聚合条件。</span><span class="sxs-lookup"><span data-stu-id="41770-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41770-129">父元素</span><span class="sxs-lookup"><span data-stu-id="41770-129">Parent elements</span></span>

|<span data-ttu-id="41770-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="41770-130">**Element**</span></span>|<span data-ttu-id="41770-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="41770-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41770-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="41770-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="41770-133">包含状态和[FindItem 操作](finditem-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="41770-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41770-134">注解</span><span class="sxs-lookup"><span data-stu-id="41770-134">Remarks</span></span>

<span data-ttu-id="41770-135">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41770-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41770-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="41770-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41770-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="41770-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="41770-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="41770-138">Schema name</span></span>  <br/> |<span data-ttu-id="41770-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="41770-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="41770-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="41770-140">Validation file</span></span>  <br/> |<span data-ttu-id="41770-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41770-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41770-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="41770-142">Can be empty</span></span>  <br/> |<span data-ttu-id="41770-143">False</span><span class="sxs-lookup"><span data-stu-id="41770-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41770-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41770-144">See also</span></span>



[<span data-ttu-id="41770-145">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="41770-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="41770-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="41770-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="41770-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="41770-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="41770-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="41770-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="41770-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="41770-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="41770-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="41770-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="41770-151">查找项目</span><span class="sxs-lookup"><span data-stu-id="41770-151">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

