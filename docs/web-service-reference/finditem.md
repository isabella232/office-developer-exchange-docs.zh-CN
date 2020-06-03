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
description: FindItem 元素定义一个请求，以查找邮箱中的项目。
ms.openlocfilehash: 3aeda1cffc03292734a91bc3fff3289d51c9b445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460993"
---
# <a name="finditem"></a><span data-ttu-id="00efa-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="00efa-103">FindItem</span></span>

<span data-ttu-id="00efa-104">**FindItem**元素定义一个请求，以查找邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="00efa-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
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

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


<span data-ttu-id="00efa-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="00efa-105">**FindItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="00efa-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="00efa-106">Attributes and elements</span></span>

<span data-ttu-id="00efa-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="00efa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00efa-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="00efa-108">Attributes</span></span>

|<span data-ttu-id="00efa-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="00efa-109">**Attribute**</span></span>|<span data-ttu-id="00efa-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="00efa-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00efa-111">**遍历**</span><span class="sxs-lookup"><span data-stu-id="00efa-111">**Traversal**</span></span> <br/> |<span data-ttu-id="00efa-112">定义搜索是查找文件夹中的项目还是文件夹的 dumpsters。</span><span class="sxs-lookup"><span data-stu-id="00efa-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="00efa-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="00efa-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="00efa-114">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="00efa-114">Traversal attribute values</span></span>

|<span data-ttu-id="00efa-115">**值**</span><span class="sxs-lookup"><span data-stu-id="00efa-115">**Value**</span></span>|<span data-ttu-id="00efa-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="00efa-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00efa-117">浅</span><span class="sxs-lookup"><span data-stu-id="00efa-117">Shallow</span></span>  <br/> |<span data-ttu-id="00efa-118">仅返回文件夹中项的标识。</span><span class="sxs-lookup"><span data-stu-id="00efa-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="00efa-119">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="00efa-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="00efa-120">仅返回文件夹的转储程序中项的标识。</span><span class="sxs-lookup"><span data-stu-id="00efa-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="00efa-121">请注意，与搜索限制组合在一起的软删除的遍历将导致返回零个项目，即使存在与搜索条件匹配的项目也是如此。</span><span class="sxs-lookup"><span data-stu-id="00efa-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="00efa-122">相应</span><span class="sxs-lookup"><span data-stu-id="00efa-122">Associated</span></span>  <br/> |<span data-ttu-id="00efa-123">仅返回文件夹中关联项的标识。</span><span class="sxs-lookup"><span data-stu-id="00efa-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="00efa-124">子元素</span><span class="sxs-lookup"><span data-stu-id="00efa-124">Child elements</span></span>

|<span data-ttu-id="00efa-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="00efa-125">**Element**</span></span>|<span data-ttu-id="00efa-126">**描述**</span><span class="sxs-lookup"><span data-stu-id="00efa-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00efa-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="00efa-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="00efa-128">标识要包括在[FindItem 操作](finditem-operation.md)响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="00efa-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="00efa-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="00efa-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="00efa-130">介绍如何为**FindItem**请求返回分页项目信息。</span><span class="sxs-lookup"><span data-stu-id="00efa-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="00efa-131">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="00efa-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="00efa-133">介绍分页视图的起始位置和**FindItem**请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="00efa-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="00efa-134">从一组找到的项目开始的分页视图偏移量按分数进行描述。</span><span class="sxs-lookup"><span data-stu-id="00efa-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="00efa-135">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="00efa-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="00efa-137">提供用于定义对日历项目的搜索的时间跨度限制。</span><span class="sxs-lookup"><span data-stu-id="00efa-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="00efa-138">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="00efa-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="00efa-140">根据字母显示名称定义对联系人项目的搜索。</span><span class="sxs-lookup"><span data-stu-id="00efa-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="00efa-141">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="00efa-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="00efa-143">指定**FindItem**查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="00efa-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="00efa-144">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="00efa-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="00efa-146">提供**FindItem**查询的标准分组。</span><span class="sxs-lookup"><span data-stu-id="00efa-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="00efa-147">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-148">限制</span><span class="sxs-lookup"><span data-stu-id="00efa-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="00efa-149">定义用于筛选**FindItem** /  **FindFolder**和 search folder 操作中的项或文件夹的限制或查询。</span><span class="sxs-lookup"><span data-stu-id="00efa-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="00efa-150">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="00efa-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="00efa-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="00efa-152">定义如何在 FindItem 请求中对项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="00efa-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="00efa-153">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="00efa-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="00efa-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="00efa-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="00efa-155">标识用于搜索 FindItem 和 FindFolder 操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="00efa-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="00efa-156">QueryString （QueryStringType）</span><span class="sxs-lookup"><span data-stu-id="00efa-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="00efa-157">包含基于高级查询语法（AQS）的邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="00efa-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00efa-158">父元素</span><span class="sxs-lookup"><span data-stu-id="00efa-158">Parent elements</span></span>

<span data-ttu-id="00efa-159">无。</span><span class="sxs-lookup"><span data-stu-id="00efa-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00efa-160">说明</span><span class="sxs-lookup"><span data-stu-id="00efa-160">Remarks</span></span>

<span data-ttu-id="00efa-161">**FindItem**请求中只能包含[IndexedPageItemView](indexedpageitemview.md)、 [FractionalPageItemView](fractionalpageitemview.md)、 [CalendarView](calendarview.md)或[ContactsView](contactsview.md)元素中的一个。</span><span class="sxs-lookup"><span data-stu-id="00efa-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="00efa-162">只有一个[GroupBy](groupby.md)或[DistinguishedGroupBy](distinguishedgroupby.md)元素可以包含在**FindItem**请求中。</span><span class="sxs-lookup"><span data-stu-id="00efa-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="00efa-163">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="00efa-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00efa-164">元素信息</span><span class="sxs-lookup"><span data-stu-id="00efa-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00efa-165">命名空间</span><span class="sxs-lookup"><span data-stu-id="00efa-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="00efa-166">架构名称</span><span class="sxs-lookup"><span data-stu-id="00efa-166">Schema Name</span></span>  <br/> |<span data-ttu-id="00efa-167">消息架构</span><span class="sxs-lookup"><span data-stu-id="00efa-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="00efa-168">验证文件</span><span class="sxs-lookup"><span data-stu-id="00efa-168">Validation File</span></span>  <br/> |<span data-ttu-id="00efa-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="00efa-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="00efa-170">可以为空</span><span class="sxs-lookup"><span data-stu-id="00efa-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="00efa-171">False</span><span class="sxs-lookup"><span data-stu-id="00efa-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00efa-172">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00efa-172">See also</span></span>

- [<span data-ttu-id="00efa-173">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="00efa-173">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="00efa-174">查找项目</span><span class="sxs-lookup"><span data-stu-id="00efa-174">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

