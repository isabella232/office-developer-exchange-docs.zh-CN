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
description: FractionalPageItemView 元素说明分页视图的起始位置以及在 FindItem 请求中返回的最大项目数。
ms.openlocfilehash: cbf45838558873dc5846823c2d1b26cf2c8af514
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461308"
---
# <a name="fractionalpageitemview"></a><span data-ttu-id="d2ea1-103">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="d2ea1-103">FractionalPageItemView</span></span>

<span data-ttu-id="d2ea1-104">**FractionalPageItemView**元素说明分页视图的起始位置以及在[FindItem](finditem.md)请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-104">The **FractionalPageItemView** element describes where the paged view starts and the maximum number of items returned in a [FindItem](finditem.md) request.</span></span> 
  
[<span data-ttu-id="d2ea1-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="d2ea1-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="d2ea1-106">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="d2ea1-106">FractionalPageItemView</span></span>](fractionalpageitemview.md)
  
```xml
<FractionalPageItemView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="d2ea1-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2ea1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2ea1-108">Attributes and elements</span></span>

<span data-ttu-id="d2ea1-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2ea1-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2ea1-110">Attributes</span></span>

|<span data-ttu-id="d2ea1-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-111">**Attribute**</span></span>|<span data-ttu-id="d2ea1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d2ea1-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="d2ea1-114">标识要在[FindItem](finditem.md)响应中返回的最大结果数。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-114">Identifies the maximum number of results to return in the [FindItem](finditem.md) response.</span></span> <span data-ttu-id="d2ea1-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-115">This attribute is optional.</span></span> <span data-ttu-id="d2ea1-116">如果未指定此属性，则该调用将返回所有可用项目。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-116">If this attribute is not specified, the call will return all available items.</span></span>  <br/> |
|<span data-ttu-id="d2ea1-117">**分子**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-117">**Numerator**</span></span> <br/> |<span data-ttu-id="d2ea1-118">表示从结果集的开头的小数偏移量的分子。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-118">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="d2ea1-119">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-119">This attribute is required.</span></span> <span data-ttu-id="d2ea1-120">分子必须等于或小于分母。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-120">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="d2ea1-121">此属性必须代表等于或大于零的整数值。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-121">This attribute must represent an integral value that is equal to or greater than zero.</span></span>  <br/> <span data-ttu-id="d2ea1-122">有关详细信息，请参阅本主题后面的 "备注"。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-122">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="d2ea1-123">**母**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-123">**Denominator**</span></span> <br/> |<span data-ttu-id="d2ea1-124">表示从结果集内的项目总数开始的小数偏移量的分母。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-124">Represents the denominator of the fractional offset from the start of the total number of items in the result set.</span></span> <span data-ttu-id="d2ea1-125">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-125">This attribute is required.</span></span> <span data-ttu-id="d2ea1-126">此属性必须代表大于1的整数值。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-126">This attribute must represent an integral value that is greater than one.</span></span>  <br/> <span data-ttu-id="d2ea1-127">有关详细信息，请参阅本主题后面的 "备注"。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-127">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d2ea1-128">子元素</span><span class="sxs-lookup"><span data-stu-id="d2ea1-128">Child elements</span></span>

<span data-ttu-id="d2ea1-129">无。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-129">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2ea1-130">父元素</span><span class="sxs-lookup"><span data-stu-id="d2ea1-130">Parent elements</span></span>

|<span data-ttu-id="d2ea1-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-131">**Element**</span></span>|<span data-ttu-id="d2ea1-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2ea1-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2ea1-133">FindItem</span><span class="sxs-lookup"><span data-stu-id="d2ea1-133">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="d2ea1-134">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-134">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="d2ea1-135">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="d2ea1-135">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2ea1-136">备注</span><span class="sxs-lookup"><span data-stu-id="d2ea1-136">Remarks</span></span>

<span data-ttu-id="d2ea1-137">从一组找到的项目开始的分页视图偏移量按分数进行描述。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-137">The paged view offset from the start of the set of found items is described by a fraction.</span></span> <span data-ttu-id="d2ea1-138">由**分子**和**分母**属性定义的小数描述了信息页面的起始位置。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-138">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="d2ea1-139">例如，如果**分子**等于四，**分母**等于5，则返回的信息的页面从 fifths 中的一个条目开始，该条目位于结果集内。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-139">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="d2ea1-140">如果分式的计算结果为零，则指示结果集的开头。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-140">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="d2ea1-141">如果该分数的计算结果为1，则指示结果集的结尾。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-141">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2ea1-142">分数表示页面的起始点，而不是返回结果集中的结果数。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-142">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="d2ea1-143">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="d2ea1-144">示例</span><span class="sxs-lookup"><span data-stu-id="d2ea1-144">Example</span></span>

<span data-ttu-id="d2ea1-145">下面的示例展示了一个[FindItem](finditem.md)请求。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-145">The following example shows a [FindItem](finditem.md) request.</span></span> <span data-ttu-id="d2ea1-146">请求返回搜索结果中的项目，这些项目在结果集内的所有项目的第二个第二个之后开始。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-146">The request returns items from the search results that start after the second third of all the items in the result set.</span></span> 
  
```
<?xml version="1.0" encoding="utf-8"?>
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

<span data-ttu-id="d2ea1-147">例如，如果结果集包含九个项目，分页视图将返回最长12个项目，从项目中的第一到结果集中找到了三分之二。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-147">For example, if the result set contains nine items, the paged view will return up to 12 items, starting at the item found two-thirds of the way in to the result set.</span></span> <span data-ttu-id="d2ea1-148">在这种情况下，页面从第七个项目开始。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-148">In this case, the page starts at the seventh item.</span></span> <span data-ttu-id="d2ea1-149">页面将包含第七个、第八个和第九个项目。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-149">The page will contain the seventh, eighth, and ninth items.</span></span> <span data-ttu-id="d2ea1-150">如果分子设置为零，则页面视图将返回结果集中的所有项，前提是该数字小于**MaxEntriesReturned**属性。</span><span class="sxs-lookup"><span data-stu-id="d2ea1-150">If the numerator is set to zero, the page view will return all the items in the result set as long as the number is less than the **MaxEntriesReturned** attribute.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d2ea1-151">元素信息</span><span class="sxs-lookup"><span data-stu-id="d2ea1-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2ea1-152">命名空间</span><span class="sxs-lookup"><span data-stu-id="d2ea1-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d2ea1-153">架构名称</span><span class="sxs-lookup"><span data-stu-id="d2ea1-153">Schema Name</span></span>  <br/> |<span data-ttu-id="d2ea1-154">消息架构</span><span class="sxs-lookup"><span data-stu-id="d2ea1-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d2ea1-155">验证文件</span><span class="sxs-lookup"><span data-stu-id="d2ea1-155">Validation File</span></span>  <br/> |<span data-ttu-id="d2ea1-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d2ea1-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d2ea1-157">可以为空</span><span class="sxs-lookup"><span data-stu-id="d2ea1-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2ea1-158">False</span><span class="sxs-lookup"><span data-stu-id="d2ea1-158">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2ea1-159">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2ea1-159">See also</span></span>



[<span data-ttu-id="d2ea1-160">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="d2ea1-160">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="d2ea1-161">查找项目</span><span class="sxs-lookup"><span data-stu-id="d2ea1-161">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

