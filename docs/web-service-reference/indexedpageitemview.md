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
description: IndexedPageItemView 元素描述如何分页的对话或项目 FindItem 操作或 FindConversation 操作请求返回信息。
ms.openlocfilehash: f1743e22087158c1889977f03774fccbc5577390
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825919"
---
# <a name="indexedpageitemview"></a><span data-ttu-id="95205-103">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="95205-103">IndexedPageItemView</span></span>

<span data-ttu-id="95205-104">**IndexedPageItemView**元素描述如何分页的对话或项目[FindItem 操作](finditem-operation.md)或[FindConversation 操作](findconversation-operation.md)请求返回信息。</span><span class="sxs-lookup"><span data-stu-id="95205-104">The **IndexedPageItemView** element describes how paged conversation or item information is returned for a [FindItem operation](finditem-operation.md) or [FindConversation operation](findconversation-operation.md) request.</span></span> 
  
```XML
<IndexedPageViewItemView MaxEntriesReturned="" Offset="" BasePoint=""/>
```

 <span data-ttu-id="95205-105">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="95205-105">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95205-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95205-106">Attributes and elements</span></span>

<span data-ttu-id="95205-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95205-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95205-108">属性</span><span class="sxs-lookup"><span data-stu-id="95205-108">Attributes</span></span>

|<span data-ttu-id="95205-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="95205-109">**Attribute**</span></span>|<span data-ttu-id="95205-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="95205-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95205-111">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="95205-111">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="95205-112">最大个数的项目或在响应中返回的对话。</span><span class="sxs-lookup"><span data-stu-id="95205-112">Describes the maximum number of items or conversations to return in the response.</span></span> <span data-ttu-id="95205-113">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="95205-113">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="95205-114">**Offset**</span><span class="sxs-lookup"><span data-stu-id="95205-114">**Offset**</span></span> <br/> |<span data-ttu-id="95205-115">介绍从**基点**的偏移量。</span><span class="sxs-lookup"><span data-stu-id="95205-115">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="95205-116">如果**基点**等于开头，则偏移量为正数。</span><span class="sxs-lookup"><span data-stu-id="95205-116">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="95205-117">如果**基点**等于结束，则好像它是负数处理偏移量。</span><span class="sxs-lookup"><span data-stu-id="95205-117">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span> <span data-ttu-id="95205-118">这标识哪一项或对话将第一个响应中传送。</span><span class="sxs-lookup"><span data-stu-id="95205-118">This identifies which item or conversation will be the first to be delivered in the response.</span></span> <span data-ttu-id="95205-119">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="95205-119">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="95205-120">**基点**</span><span class="sxs-lookup"><span data-stu-id="95205-120">**BasePoint**</span></span> <br/> |<span data-ttu-id="95205-121">描述是否将从开头或结尾的一项或使用的搜索条件找到的对话的启动项或对话页。</span><span class="sxs-lookup"><span data-stu-id="95205-121">Describes whether the page of items or conversations will start from the beginning or the end of the set of items or conversations that are found by using the search criteria.</span></span> <span data-ttu-id="95205-122">始终从末尾查找往回搜索。</span><span class="sxs-lookup"><span data-stu-id="95205-122">Seeking from the end always searches backward.</span></span> <span data-ttu-id="95205-123">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="95205-123">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="95205-124">基点属性</span><span class="sxs-lookup"><span data-stu-id="95205-124">BasePoint Attribute</span></span>

|<span data-ttu-id="95205-125">**值**</span><span class="sxs-lookup"><span data-stu-id="95205-125">**Value**</span></span>|<span data-ttu-id="95205-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="95205-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95205-127">开始</span><span class="sxs-lookup"><span data-stu-id="95205-127">Beginning</span></span>  <br/> |<span data-ttu-id="95205-128">分页的视图从找到对话或项目集的开头。</span><span class="sxs-lookup"><span data-stu-id="95205-128">The paged view starts at the beginning of the found conversation or item set.</span></span>  <br/> |
|<span data-ttu-id="95205-129">End</span><span class="sxs-lookup"><span data-stu-id="95205-129">End</span></span>  <br/> |<span data-ttu-id="95205-130">找到对话或项目集末尾开始分页的视图。</span><span class="sxs-lookup"><span data-stu-id="95205-130">The paged view starts at the end of the found conversation or item set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95205-131">子元素</span><span class="sxs-lookup"><span data-stu-id="95205-131">Child elements</span></span>

<span data-ttu-id="95205-132">无。</span><span class="sxs-lookup"><span data-stu-id="95205-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95205-133">父元素</span><span class="sxs-lookup"><span data-stu-id="95205-133">Parent elements</span></span>

|<span data-ttu-id="95205-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="95205-134">**Element**</span></span>|<span data-ttu-id="95205-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="95205-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95205-136">FindItem</span><span class="sxs-lookup"><span data-stu-id="95205-136">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="95205-137">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="95205-137">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="95205-138">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="95205-138">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="95205-139">FindConversation</span><span class="sxs-lookup"><span data-stu-id="95205-139">FindConversation</span></span>](findconversation.md) <br/> |<span data-ttu-id="95205-140">定义查找邮箱中的对话的请求。</span><span class="sxs-lookup"><span data-stu-id="95205-140">Defines a request to find conversations in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95205-141">备注</span><span class="sxs-lookup"><span data-stu-id="95205-141">Remarks</span></span>

<span data-ttu-id="95205-142">从末尾查找涉及将移至原点标识的偏移量。</span><span class="sxs-lookup"><span data-stu-id="95205-142">Seeking from the end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="95205-143">此外，将指针向后移动请求的记录数。</span><span class="sxs-lookup"><span data-stu-id="95205-143">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="95205-144">例如，如果有 100 条记录，偏移量为 25 从末尾，从 75 开始搜索。</span><span class="sxs-lookup"><span data-stu-id="95205-144">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="95205-145">如果返回了 10 条记录，10 个附加到 65 记录，并返回记录到 75 65 指针是向后移动。</span><span class="sxs-lookup"><span data-stu-id="95205-145">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="95205-146">下一个索引为 64。</span><span class="sxs-lookup"><span data-stu-id="95205-146">The next index is 64.</span></span> <span data-ttu-id="95205-147">从页面结尾的下一步偏移量为 100 减 64 其等于 36。</span><span class="sxs-lookup"><span data-stu-id="95205-147">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="95205-148">36 是从结束后，若要获取的已编制索引的下一页的下一步偏移量的值。</span><span class="sxs-lookup"><span data-stu-id="95205-148">36 is the value for the next offset from the end to get the next indexed page.</span></span>
  
<span data-ttu-id="95205-149">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95205-149">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="95205-150">示例</span><span class="sxs-lookup"><span data-stu-id="95205-150">Example</span></span>

<span data-ttu-id="95205-151">下面的示例演示一个[FindItem 操作](finditem-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="95205-151">The following example shows a [FindItem operation](finditem-operation.md) request.</span></span> <span data-ttu-id="95205-152">每个项目返回其 ID 和主题。</span><span class="sxs-lookup"><span data-stu-id="95205-152">Each item is returned with its ID and subject.</span></span> <span data-ttu-id="95205-153">在响应中，指定**MaxEntriesReturned**属性返回的六个项目的最大值。</span><span class="sxs-lookup"><span data-stu-id="95205-153">A maximum of six items are returned in the response, as specified by the **MaxEntriesReturned** attribute.</span></span> <span data-ttu-id="95205-154">中按重要性分组的升序排列项目。</span><span class="sxs-lookup"><span data-stu-id="95205-154">The items are listed in ascending order grouped by importance.</span></span> <span data-ttu-id="95205-155">组中的项目进行聚合按主题。</span><span class="sxs-lookup"><span data-stu-id="95205-155">Items in a group are aggregated by subject.</span></span> 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="95205-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="95205-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95205-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="95205-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95205-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="95205-158">Schema Name</span></span>  <br/> |<span data-ttu-id="95205-159">消息架构</span><span class="sxs-lookup"><span data-stu-id="95205-159">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95205-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="95205-160">Validation File</span></span>  <br/> |<span data-ttu-id="95205-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="95205-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95205-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="95205-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="95205-163">False</span><span class="sxs-lookup"><span data-stu-id="95205-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95205-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95205-164">See also</span></span>



[<span data-ttu-id="95205-165">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="95205-165">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="95205-166">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="95205-166">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="95205-167">查找项目</span><span class="sxs-lookup"><span data-stu-id="95205-167">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

