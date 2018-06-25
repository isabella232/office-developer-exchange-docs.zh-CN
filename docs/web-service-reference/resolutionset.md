---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: ResolutionSet 元素包含的不明确名称解析的数组。
ms.openlocfilehash: ad7bd31c85051e8c80aea25aa9e6f2914cf0ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827160"
---
# <a name="resolutionset"></a><span data-ttu-id="c9b24-103">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="c9b24-103">ResolutionSet</span></span>

<span data-ttu-id="c9b24-104">**ResolutionSet**元素包含的不明确名称解析的数组。</span><span class="sxs-lookup"><span data-stu-id="c9b24-104">The **ResolutionSet** element contains an array of resolutions for an ambiguous name.</span></span> 
  
[<span data-ttu-id="c9b24-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="c9b24-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="c9b24-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c9b24-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="c9b24-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c9b24-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="c9b24-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="c9b24-108">ResolutionSet</span></span>](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 <span data-ttu-id="c9b24-109">**ArrayOfResolutionType**</span><span class="sxs-lookup"><span data-stu-id="c9b24-109">**ArrayOfResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9b24-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c9b24-110">Attributes and elements</span></span>

<span data-ttu-id="c9b24-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c9b24-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9b24-112">属性</span><span class="sxs-lookup"><span data-stu-id="c9b24-112">Attributes</span></span>

|<span data-ttu-id="c9b24-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="c9b24-113">**Attribute**</span></span>|<span data-ttu-id="c9b24-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c9b24-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c9b24-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="c9b24-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="c9b24-116">表示使用索引的页面视图时，则在下一个请求时应使用的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="c9b24-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="c9b24-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="c9b24-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="c9b24-118">代表要使用分数页面视图时使用的下一个请求的新分子值。</span><span class="sxs-lookup"><span data-stu-id="c9b24-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="c9b24-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="c9b24-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="c9b24-120">代表下一个分母使用分数页面视图时用于下一个请求。</span><span class="sxs-lookup"><span data-stu-id="c9b24-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="c9b24-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="c9b24-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="c9b24-122">此属性将当前结果包含的最后一项在查询中，如果为 true，以便不需要其他分页。</span><span class="sxs-lookup"><span data-stu-id="c9b24-122">This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="c9b24-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="c9b24-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="c9b24-124">代表视图中的项目的总数。</span><span class="sxs-lookup"><span data-stu-id="c9b24-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c9b24-125">子元素</span><span class="sxs-lookup"><span data-stu-id="c9b24-125">Child elements</span></span>

|<span data-ttu-id="c9b24-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="c9b24-126">**Element**</span></span>|<span data-ttu-id="c9b24-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="c9b24-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9b24-128">解决方法</span><span class="sxs-lookup"><span data-stu-id="c9b24-128">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="c9b24-129">包含单个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="c9b24-129">Contains a single resolved entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9b24-130">父元素</span><span class="sxs-lookup"><span data-stu-id="c9b24-130">Parent elements</span></span>

|<span data-ttu-id="c9b24-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="c9b24-131">**Element**</span></span>|<span data-ttu-id="c9b24-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="c9b24-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9b24-133">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c9b24-133">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md) <br/> |<span data-ttu-id="c9b24-134">包含状态和 ResolveNames 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="c9b24-134">Contains the status and result of a ResolveNames request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9b24-135">注解</span><span class="sxs-lookup"><span data-stu-id="c9b24-135">Remarks</span></span>

<span data-ttu-id="c9b24-136">**ResolutionSet**元素可以包含最多 100 解析实体。</span><span class="sxs-lookup"><span data-stu-id="c9b24-136">A **ResolutionSet** element can contain a maximum of 100 resolved entities.</span></span> 
  
<span data-ttu-id="c9b24-137">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c9b24-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9b24-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="c9b24-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9b24-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="c9b24-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c9b24-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="c9b24-140">Schema Name</span></span>  <br/> |<span data-ttu-id="c9b24-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="c9b24-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c9b24-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="c9b24-142">Validation File</span></span>  <br/> |<span data-ttu-id="c9b24-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c9b24-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c9b24-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="c9b24-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="c9b24-145">False</span><span class="sxs-lookup"><span data-stu-id="c9b24-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9b24-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c9b24-146">See also</span></span>



[<span data-ttu-id="c9b24-147">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c9b24-147">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="c9b24-148">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="c9b24-148">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="c9b24-149">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="c9b24-149">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="c9b24-150">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c9b24-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

