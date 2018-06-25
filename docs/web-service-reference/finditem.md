---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: FindItem 元素定义查找邮箱中的项目的请求。
ms.openlocfilehash: 9831b034be7deb0cf6e756bb585bdbe34b370afd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754345"
---
# <a name="finditem"></a><span data-ttu-id="64f07-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="64f07-103">FindItem</span></span>

<span data-ttu-id="64f07-104">**FindItem**元素定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="64f07-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

 <span data-ttu-id="64f07-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="64f07-105">**FindItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64f07-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64f07-106">Attributes and elements</span></span>

<span data-ttu-id="64f07-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64f07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64f07-108">属性</span><span class="sxs-lookup"><span data-stu-id="64f07-108">Attributes</span></span>

|<span data-ttu-id="64f07-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="64f07-109">**Attribute**</span></span>|<span data-ttu-id="64f07-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="64f07-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64f07-111">**遍历**</span><span class="sxs-lookup"><span data-stu-id="64f07-111">**Traversal**</span></span> <br/> |<span data-ttu-id="64f07-112">定义搜索是否查找文件夹或文件夹的垃圾站中的项目。</span><span class="sxs-lookup"><span data-stu-id="64f07-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="64f07-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="64f07-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="64f07-114">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="64f07-114">Traversal attribute values</span></span>

|<span data-ttu-id="64f07-115">**值**</span><span class="sxs-lookup"><span data-stu-id="64f07-115">**Value**</span></span>|<span data-ttu-id="64f07-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="64f07-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="64f07-117">浅</span><span class="sxs-lookup"><span data-stu-id="64f07-117">Shallow</span></span>  <br/> |<span data-ttu-id="64f07-118">返回文件夹中的项的标识。</span><span class="sxs-lookup"><span data-stu-id="64f07-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="64f07-119">带有 SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="64f07-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="64f07-120">返回仅的文件夹中的项的标识转储程序。</span><span class="sxs-lookup"><span data-stu-id="64f07-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="64f07-121">注意与搜索限制组合软删除遍历将导致返回零项即使有与搜索条件匹配项。</span><span class="sxs-lookup"><span data-stu-id="64f07-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="64f07-122">关联</span><span class="sxs-lookup"><span data-stu-id="64f07-122">Associated</span></span>  <br/> |<span data-ttu-id="64f07-123">返回文件夹中仅的相关联的项的标识。</span><span class="sxs-lookup"><span data-stu-id="64f07-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="64f07-124">子元素</span><span class="sxs-lookup"><span data-stu-id="64f07-124">Child elements</span></span>

|<span data-ttu-id="64f07-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="64f07-125">**Element**</span></span>|<span data-ttu-id="64f07-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="64f07-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64f07-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="64f07-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="64f07-128">标识项目属性和[FindItem 操作](finditem-operation.md)响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="64f07-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="64f07-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="64f07-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="64f07-130">介绍如何分页的项信息**FindItem**请求返回。</span><span class="sxs-lookup"><span data-stu-id="64f07-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="64f07-131">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="64f07-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="64f07-133">介绍其中分页的视图启动和**FindItem**请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="64f07-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="64f07-134">通过一小部分介绍了从找到项集开头的分页的视图偏移量。</span><span class="sxs-lookup"><span data-stu-id="64f07-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="64f07-135">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="64f07-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="64f07-137">提供时间跨越限制以定义搜索的日历项目。</span><span class="sxs-lookup"><span data-stu-id="64f07-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="64f07-138">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="64f07-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="64f07-140">定义搜索联系人项目基于按字母顺序排列的显示名称。</span><span class="sxs-lookup"><span data-stu-id="64f07-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="64f07-141">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="64f07-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="64f07-143">指定**FindItem**查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="64f07-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="64f07-144">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="64f07-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="64f07-146">提供用于**FindItem**查询标准分组。</span><span class="sxs-lookup"><span data-stu-id="64f07-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="64f07-147">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-148">限制</span><span class="sxs-lookup"><span data-stu-id="64f07-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="64f07-149">定义的限制或用于筛选项目或**FindItem**中的文件夹的查询/ **FindFolder**和搜索文件夹的操作。</span><span class="sxs-lookup"><span data-stu-id="64f07-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="64f07-150">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="64f07-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="64f07-152">定义项 FindItem 请求中的排序方式。</span><span class="sxs-lookup"><span data-stu-id="64f07-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="64f07-153">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="64f07-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="64f07-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="64f07-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="64f07-155">标识要搜索的 FindItem 和 FindFolder 操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="64f07-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="64f07-156">查询字符串 (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="64f07-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="64f07-157">包含基于上高级查询语法 (AQS) 邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="64f07-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64f07-158">父元素</span><span class="sxs-lookup"><span data-stu-id="64f07-158">Parent elements</span></span>

<span data-ttu-id="64f07-159">无。</span><span class="sxs-lookup"><span data-stu-id="64f07-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64f07-160">注解</span><span class="sxs-lookup"><span data-stu-id="64f07-160">Remarks</span></span>

<span data-ttu-id="64f07-161">只有一个[IndexedPageItemView](indexedpageitemview.md)、 [FractionalPageItemView](fractionalpageitemview.md)、 [CalendarView](calendarview.md)，或[ContactsView](contactsview.md)元素可以包含在**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="64f07-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="64f07-162">只有一个[GroupBy](groupby.md)或[DistinguishedGroupBy](distinguishedgroupby.md)元素可以包含在**FindItem**请求。</span><span class="sxs-lookup"><span data-stu-id="64f07-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="64f07-163">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="64f07-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64f07-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="64f07-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64f07-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="64f07-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="64f07-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="64f07-166">Schema Name</span></span>  <br/> |<span data-ttu-id="64f07-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="64f07-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="64f07-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="64f07-168">Validation File</span></span>  <br/> |<span data-ttu-id="64f07-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="64f07-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="64f07-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="64f07-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="64f07-171">False</span><span class="sxs-lookup"><span data-stu-id="64f07-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64f07-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64f07-172">See also</span></span>



[<span data-ttu-id="64f07-173">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="64f07-173">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="64f07-174">查找项目</span><span class="sxs-lookup"><span data-stu-id="64f07-174">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

