---
title: FractionalPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageItemView
api_type:
- schema
ms.assetid: 4111afec-35e7-4c6f-b291-9bbba603f633
description: FractionalPageItemView 元素介绍其中分页的视图启动和 FindItem 请求中返回的最大项目数。
ms.openlocfilehash: 38c35d2b68dabfca1a43ab034deaf72c47b0ea66
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754418"
---
# <a name="fractionalpageitemview"></a><span data-ttu-id="271c9-103">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="271c9-103">FractionalPageItemView</span></span>

<span data-ttu-id="271c9-104">**FractionalPageItemView**元素介绍其中分页的视图启动和[FindItem](finditem.md)请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="271c9-104">The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request.</span></span> 
  
[<span data-ttu-id="271c9-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="271c9-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="271c9-106">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="271c9-106">FractionalPageItemView</span></span>](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="271c9-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="271c9-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="271c9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="271c9-108">Attributes and elements</span></span>

<span data-ttu-id="271c9-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="271c9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="271c9-110">属性</span><span class="sxs-lookup"><span data-stu-id="271c9-110">Attributes</span></span>

|<span data-ttu-id="271c9-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="271c9-111">**Attribute**</span></span>|<span data-ttu-id="271c9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="271c9-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="271c9-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="271c9-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="271c9-114">标识要[FindItem](finditem.md)响应中返回结果的最大数量。</span><span class="sxs-lookup"><span data-stu-id="271c9-114">Identifies the maximum number of results to return in the [FindItem](finditem.md) response.</span></span> <span data-ttu-id="271c9-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="271c9-115">This attribute is optional.</span></span> <span data-ttu-id="271c9-116">如果未指定此属性，则呼叫将返回所有可用的项。</span><span class="sxs-lookup"><span data-stu-id="271c9-116">If this attribute is not specified, the call will return all available items.</span></span>  <br/> |
|<span data-ttu-id="271c9-117">**分子**</span><span class="sxs-lookup"><span data-stu-id="271c9-117">**Numerator**</span></span> <br/> |<span data-ttu-id="271c9-118">从结果集中的开始表示分数偏移量的分子。</span><span class="sxs-lookup"><span data-stu-id="271c9-118">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="271c9-119">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="271c9-119">This attribute is required.</span></span> <span data-ttu-id="271c9-120">分子必须等于或小于分母。</span><span class="sxs-lookup"><span data-stu-id="271c9-120">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="271c9-121">此属性必须表示等于或大于零的整数值。</span><span class="sxs-lookup"><span data-stu-id="271c9-121">This attribute must represent an integral value that is equal to or greater than zero.</span></span>  <br/> <span data-ttu-id="271c9-122">有关详细信息，请参阅本主题后面的备注。</span><span class="sxs-lookup"><span data-stu-id="271c9-122">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="271c9-123">**分母**</span><span class="sxs-lookup"><span data-stu-id="271c9-123">**Denominator**</span></span> <br/> |<span data-ttu-id="271c9-124">从结果集中的项目总数开始代表分数偏移量的分母，为。</span><span class="sxs-lookup"><span data-stu-id="271c9-124">Represents the denominator of the fractional offset from the start of the total number of items in the result set.</span></span> <span data-ttu-id="271c9-125">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="271c9-125">This attribute is required.</span></span> <span data-ttu-id="271c9-126">此属性必须表示大于 1 的整数值。</span><span class="sxs-lookup"><span data-stu-id="271c9-126">This attribute must represent an integral value that is greater than one.</span></span>  <br/> <span data-ttu-id="271c9-127">有关详细信息，请参阅本主题后面的备注。</span><span class="sxs-lookup"><span data-stu-id="271c9-127">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="271c9-128">子元素</span><span class="sxs-lookup"><span data-stu-id="271c9-128">Child elements</span></span>

<span data-ttu-id="271c9-129">无。</span><span class="sxs-lookup"><span data-stu-id="271c9-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="271c9-130">父元素</span><span class="sxs-lookup"><span data-stu-id="271c9-130">Parent elements</span></span>

|<span data-ttu-id="271c9-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="271c9-131">**Element**</span></span>|<span data-ttu-id="271c9-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="271c9-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="271c9-133">FindItem</span><span class="sxs-lookup"><span data-stu-id="271c9-133">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="271c9-134">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="271c9-134">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="271c9-135">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="271c9-135">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="271c9-136">备注</span><span class="sxs-lookup"><span data-stu-id="271c9-136">Remarks</span></span>

<span data-ttu-id="271c9-137">通过一小部分介绍了从找到项集开始的分页的视图偏移量。</span><span class="sxs-lookup"><span data-stu-id="271c9-137">The paged view offset from the start of the set of found items is described by a fraction.</span></span> <span data-ttu-id="271c9-138">分数，由**分子**和**分母**属性定义，介绍的信息页的起始位置。</span><span class="sxs-lookup"><span data-stu-id="271c9-138">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="271c9-139">例如，如果**分子**等于四**分母**等于 5，返回的信息开始的项的页面位于五分之四中到结果集中的方式。</span><span class="sxs-lookup"><span data-stu-id="271c9-139">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="271c9-140">如果 fraction 计算结果为零，用于指示结果集的开头。</span><span class="sxs-lookup"><span data-stu-id="271c9-140">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="271c9-141">如果 fraction 计算结果为一个，表明结果集的末尾。</span><span class="sxs-lookup"><span data-stu-id="271c9-141">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="271c9-142">分数表示的页面的起始点，则将返回结果集内的结果不数量。</span><span class="sxs-lookup"><span data-stu-id="271c9-142">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="271c9-143">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="271c9-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="271c9-144">示例</span><span class="sxs-lookup"><span data-stu-id="271c9-144">Example</span></span>

<span data-ttu-id="271c9-145">下面的示例演示一个[FindItem](finditem.md)请求。</span><span class="sxs-lookup"><span data-stu-id="271c9-145">The following example shows a [FindItem](finditem.md) request.</span></span> <span data-ttu-id="271c9-146">请求后启动第二个第三的所有项目在结果集中在搜索结果中返回的项目。</span><span class="sxs-lookup"><span data-stu-id="271c9-146">The request returns items from the search results that start after the second third of all the items in the result set.</span></span> 
  
```
<?xml version="1.0" encoding="utf-8"?>
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
      <FractionalPageItemView MaxEntriesReturned="12" Numerator="2" Denominator="3"/>
      <GroupBy Order="Descending">
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

<span data-ttu-id="271c9-147">例如，如果在结果集中包含九个项目，分页的视图将返回达 12 个项，从开始到结果集中的方式中找到项三分之二。</span><span class="sxs-lookup"><span data-stu-id="271c9-147">For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set.</span></span> <span data-ttu-id="271c9-148">在这种情况下，页上启动在第七个项目。</span><span class="sxs-lookup"><span data-stu-id="271c9-148">In this case, the page starts at the seventh item.</span></span> <span data-ttu-id="271c9-149">页将包含的第七个，第八个和第九个项目。</span><span class="sxs-lookup"><span data-stu-id="271c9-149">The page will contain the seventh, eighth, and ninth items.</span></span> <span data-ttu-id="271c9-150">如果分子设置为零，将页面视图将在结果集中，只要数小于**MaxEntriesReturned**属性返回的所有项目。</span><span class="sxs-lookup"><span data-stu-id="271c9-150">If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="271c9-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="271c9-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="271c9-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="271c9-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="271c9-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="271c9-153">Schema Name</span></span>  <br/> |<span data-ttu-id="271c9-154">消息架构</span><span class="sxs-lookup"><span data-stu-id="271c9-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="271c9-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="271c9-155">Validation File</span></span>  <br/> |<span data-ttu-id="271c9-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="271c9-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="271c9-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="271c9-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="271c9-158">False</span><span class="sxs-lookup"><span data-stu-id="271c9-158">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="271c9-159">另请参阅</span><span class="sxs-lookup"><span data-stu-id="271c9-159">See also</span></span>



[<span data-ttu-id="271c9-160">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="271c9-160">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="271c9-161">查找项目</span><span class="sxs-lookup"><span data-stu-id="271c9-161">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

