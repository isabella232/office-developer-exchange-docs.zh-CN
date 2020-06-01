---
title: IndexedPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageItemView
api_type:
- schema
ms.assetid: 6d1b0b04-cc35-4a57-bd7a-824136d14fda
description: IndexedPageItemView 元素介绍如何为 FindItem 操作或 FindConversation 操作请求返回分页对话或项目信息。
ms.openlocfilehash: 0a66f17855fd425082e3651886d3eeec4f217ac4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456911"
---
# <a name="indexedpageitemview"></a><span data-ttu-id="ed067-103">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="ed067-103">IndexedPageItemView</span></span>

<span data-ttu-id="ed067-104">**IndexedPageItemView**元素介绍如何为[FindItem 操作](finditem-operation.md)或[FindConversation 操作](findconversation-operation.md)请求返回分页对话或项目信息。</span><span class="sxs-lookup"><span data-stu-id="ed067-104">The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 <span data-ttu-id="ed067-105">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="ed067-105">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed067-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ed067-106">Attributes and elements</span></span>

<span data-ttu-id="ed067-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed067-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed067-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ed067-108">Attributes</span></span>

|<span data-ttu-id="ed067-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ed067-109">**Attribute**</span></span>|<span data-ttu-id="ed067-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed067-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed067-111">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="ed067-111">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="ed067-112">描述要在响应中返回的项目或对话的最大数量。</span><span class="sxs-lookup"><span data-stu-id="ed067-112">Describes the maximum number of items or conversations to return in the response.</span></span> <span data-ttu-id="ed067-113">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="ed067-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="ed067-114">**Offset**</span><span class="sxs-lookup"><span data-stu-id="ed067-114">**Offset**</span></span> <br/> |<span data-ttu-id="ed067-115">描述**BasePoint**中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="ed067-115">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="ed067-116">如果**BasePoint**等于开头，则偏移量为正值。</span><span class="sxs-lookup"><span data-stu-id="ed067-116">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="ed067-117">如果**BasePoint**等于 End，则处理的是负的偏移量。</span><span class="sxs-lookup"><span data-stu-id="ed067-117">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span> <span data-ttu-id="ed067-118">这标识在响应中将首先传递哪个项目或对话。</span><span class="sxs-lookup"><span data-stu-id="ed067-118">This identifies which item or conversation will be the first to be delivered in the response.</span></span> <span data-ttu-id="ed067-119">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="ed067-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ed067-120">**BasePoint**</span><span class="sxs-lookup"><span data-stu-id="ed067-120">**BasePoint**</span></span> <br/> |<span data-ttu-id="ed067-121">描述项目或对话的页面是从使用搜索条件找到的项目或对话集的开头还是结尾开始。</span><span class="sxs-lookup"><span data-stu-id="ed067-121">Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria.</span></span> <span data-ttu-id="ed067-122">从末尾进行的查找始终向后搜索。</span><span class="sxs-lookup"><span data-stu-id="ed067-122">Seeking from the end always searches backward.</span></span> <span data-ttu-id="ed067-123">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="ed067-123">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="ed067-124">BasePoint 属性</span><span class="sxs-lookup"><span data-stu-id="ed067-124">BasePoint Attribute</span></span>

|<span data-ttu-id="ed067-125">**值**</span><span class="sxs-lookup"><span data-stu-id="ed067-125">**Value**</span></span>|<span data-ttu-id="ed067-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="ed067-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed067-127">始</span><span class="sxs-lookup"><span data-stu-id="ed067-127">Beginning</span></span>  <br/> |<span data-ttu-id="ed067-128">分页视图从找到的对话或项目集的开头开始。</span><span class="sxs-lookup"><span data-stu-id="ed067-128">The paged view starts at the beginning of the found conversation or item set.</span></span>  <br/> |
|<span data-ttu-id="ed067-129">End</span><span class="sxs-lookup"><span data-stu-id="ed067-129">End</span></span>  <br/> |<span data-ttu-id="ed067-130">分页视图从找到的对话或项目集的末尾开始。</span><span class="sxs-lookup"><span data-stu-id="ed067-130">The paged view starts at the end of the found conversation or item set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ed067-131">子元素</span><span class="sxs-lookup"><span data-stu-id="ed067-131">Child elements</span></span>

<span data-ttu-id="ed067-132">无。</span><span class="sxs-lookup"><span data-stu-id="ed067-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed067-133">父元素</span><span class="sxs-lookup"><span data-stu-id="ed067-133">Parent elements</span></span>

|<span data-ttu-id="ed067-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="ed067-134">**Element**</span></span>|<span data-ttu-id="ed067-135">**描述**</span><span class="sxs-lookup"><span data-stu-id="ed067-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed067-136">FindItem</span><span class="sxs-lookup"><span data-stu-id="ed067-136">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="ed067-137">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="ed067-137">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="ed067-138">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ed067-138">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="ed067-139">FindConversation</span><span class="sxs-lookup"><span data-stu-id="ed067-139">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="ed067-140">定义在邮箱中查找对话的请求。</span><span class="sxs-lookup"><span data-stu-id="ed067-140">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed067-141">备注</span><span class="sxs-lookup"><span data-stu-id="ed067-141">Remarks</span></span>

<span data-ttu-id="ed067-142">从末尾进行查找包括移到由偏移量标识的源。</span><span class="sxs-lookup"><span data-stu-id="ed067-142">Seeking from the end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="ed067-143">此外，还会按请求的记录数向后移动指针。</span><span class="sxs-lookup"><span data-stu-id="ed067-143">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="ed067-144">例如，如果有100条记录，偏移量是从末尾到25，则搜索从75开始。</span><span class="sxs-lookup"><span data-stu-id="ed067-144">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="ed067-145">如果返回10个记录，指针将向后移动10条记录到65，并返回记录65至75。</span><span class="sxs-lookup"><span data-stu-id="ed067-145">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="ed067-146">下一个索引为64。</span><span class="sxs-lookup"><span data-stu-id="ed067-146">The next index is 64.</span></span> <span data-ttu-id="ed067-147">距页面末尾的下一个偏移量是100减去64，等于36。</span><span class="sxs-lookup"><span data-stu-id="ed067-147">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="ed067-148">36是来自 end 的下一个偏移量的值，以获取下一个索引页。</span><span class="sxs-lookup"><span data-stu-id="ed067-148">36 is the value for the next offset from the end to get the next indexed page.</span></span>
  
<span data-ttu-id="ed067-149">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ed067-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="ed067-150">示例</span><span class="sxs-lookup"><span data-stu-id="ed067-150">Example</span></span>

<span data-ttu-id="ed067-151">下面的示例展示了一个[FindItem 操作](finditem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="ed067-151">The following example shows a [FindItem operation](finditem-operation.md) request.</span></span> <span data-ttu-id="ed067-152">每个项目都返回其 ID 和主题。</span><span class="sxs-lookup"><span data-stu-id="ed067-152">Each item is returned with its ID and subject.</span></span> <span data-ttu-id="ed067-153">响应中最多可返回6个项目，如**MaxEntriesReturned**属性指定。</span><span class="sxs-lookup"><span data-stu-id="ed067-153">A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute.</span></span> <span data-ttu-id="ed067-154">项目按重要性分组按升序排列。</span><span class="sxs-lookup"><span data-stu-id="ed067-154">The items are listed in ascending order grouped by importance.</span></span> <span data-ttu-id="ed067-155">组中的项目按主题进行聚合。</span><span class="sxs-lookup"><span data-stu-id="ed067-155">Items in a group are aggregated by subject.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <IndexedPageItemView MaxEntriesReturned="6" BasePoint="Beginning" Offset="0" />
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="item:Importance"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="ed067-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="ed067-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed067-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="ed067-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed067-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="ed067-158">Schema Name</span></span>  <br/> |<span data-ttu-id="ed067-159">消息架构</span><span class="sxs-lookup"><span data-stu-id="ed067-159">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed067-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="ed067-160">Validation File</span></span>  <br/> |<span data-ttu-id="ed067-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed067-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed067-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="ed067-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed067-163">False</span><span class="sxs-lookup"><span data-stu-id="ed067-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed067-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed067-164">See also</span></span>



[<span data-ttu-id="ed067-165">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="ed067-165">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="ed067-166">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="ed067-166">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="ed067-167">查找项目</span><span class="sxs-lookup"><span data-stu-id="ed067-167">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

