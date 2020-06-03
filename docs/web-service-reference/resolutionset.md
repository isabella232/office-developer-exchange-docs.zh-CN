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
description: ResolutionSet 元素包含一个不明确名称的分辨率数组。
ms.openlocfilehash: 483a096a7fcedbabe25758ebcaa31c83405a0ad4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467170"
---
# <a name="resolutionset"></a><span data-ttu-id="1c90e-103">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="1c90e-103">ResolutionSet</span></span>

<span data-ttu-id="1c90e-104">**ResolutionSet**元素包含一个不明确名称的分辨率数组。</span><span class="sxs-lookup"><span data-stu-id="1c90e-104">The **ResolutionSet** element contains an array of resolutions for an ambiguous name.</span></span> 
  
[<span data-ttu-id="1c90e-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="1c90e-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="1c90e-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1c90e-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="1c90e-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1c90e-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="1c90e-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="1c90e-108">ResolutionSet</span></span>](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 <span data-ttu-id="1c90e-109">**ArrayOfResolutionType**</span><span class="sxs-lookup"><span data-stu-id="1c90e-109">**ArrayOfResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c90e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1c90e-110">Attributes and elements</span></span>

<span data-ttu-id="1c90e-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1c90e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c90e-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="1c90e-112">Attributes</span></span>

|<span data-ttu-id="1c90e-113">**属性**</span><span class="sxs-lookup"><span data-stu-id="1c90e-113">**Attribute**</span></span>|<span data-ttu-id="1c90e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1c90e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c90e-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="1c90e-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="1c90e-116">表示在使用索引页视图时应用于下一个请求的下一个索引。</span><span class="sxs-lookup"><span data-stu-id="1c90e-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="1c90e-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="1c90e-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="1c90e-118">表示在使用分数页面视图时用于下一个请求的新的分子值。</span><span class="sxs-lookup"><span data-stu-id="1c90e-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="1c90e-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="1c90e-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="1c90e-120">表示使用分数页面视图时用于下一个请求的下一个分母。</span><span class="sxs-lookup"><span data-stu-id="1c90e-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="1c90e-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="1c90e-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="1c90e-122">如果当前结果包含查询中的最后一项，因此不需要进行其他分页，则此属性为 true。</span><span class="sxs-lookup"><span data-stu-id="1c90e-122">This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="1c90e-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="1c90e-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="1c90e-124">表示视图中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="1c90e-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1c90e-125">子元素</span><span class="sxs-lookup"><span data-stu-id="1c90e-125">Child elements</span></span>

|<span data-ttu-id="1c90e-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="1c90e-126">**Element**</span></span>|<span data-ttu-id="1c90e-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="1c90e-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c90e-128">解决方法</span><span class="sxs-lookup"><span data-stu-id="1c90e-128">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="1c90e-129">包含单个已解析的实体。</span><span class="sxs-lookup"><span data-stu-id="1c90e-129">Contains a single resolved entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1c90e-130">父元素</span><span class="sxs-lookup"><span data-stu-id="1c90e-130">Parent elements</span></span>

|<span data-ttu-id="1c90e-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="1c90e-131">**Element**</span></span>|<span data-ttu-id="1c90e-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="1c90e-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c90e-133">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1c90e-133">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md) <br/> |<span data-ttu-id="1c90e-134">包含 ResolveNames 请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="1c90e-134">Contains the status and result of a ResolveNames request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c90e-135">备注</span><span class="sxs-lookup"><span data-stu-id="1c90e-135">Remarks</span></span>

<span data-ttu-id="1c90e-136">**ResolutionSet**元素最多可包含100个已解析实体。</span><span class="sxs-lookup"><span data-stu-id="1c90e-136">A **ResolutionSet** element can contain a maximum of 100 resolved entities.</span></span> 
  
<span data-ttu-id="1c90e-137">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1c90e-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c90e-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="1c90e-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c90e-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="1c90e-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1c90e-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="1c90e-140">Schema Name</span></span>  <br/> |<span data-ttu-id="1c90e-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="1c90e-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1c90e-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="1c90e-142">Validation File</span></span>  <br/> |<span data-ttu-id="1c90e-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1c90e-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1c90e-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="1c90e-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="1c90e-145">False</span><span class="sxs-lookup"><span data-stu-id="1c90e-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c90e-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1c90e-146">See also</span></span>



[<span data-ttu-id="1c90e-147">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="1c90e-147">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="1c90e-148">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="1c90e-148">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="1c90e-149">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="1c90e-149">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="1c90e-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1c90e-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

