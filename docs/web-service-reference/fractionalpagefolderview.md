---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: FractionalPageFolderView 元素描述其中分页的视图启动并返回 FindFolder 请求中的文件夹的最大数目。
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754415"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="82dbb-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="82dbb-103">FractionalPageFolderView</span></span>

<span data-ttu-id="82dbb-104">**FractionalPageFolderView**元素描述其中分页的视图启动并返回[FindFolder](findfolder.md)请求中的文件夹的最大数目。</span><span class="sxs-lookup"><span data-stu-id="82dbb-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="82dbb-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="82dbb-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="82dbb-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="82dbb-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="82dbb-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="82dbb-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82dbb-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82dbb-108">Attributes and elements</span></span>

<span data-ttu-id="82dbb-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82dbb-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82dbb-110">属性</span><span class="sxs-lookup"><span data-stu-id="82dbb-110">Attributes</span></span>

|<span data-ttu-id="82dbb-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="82dbb-111">**Attribute**</span></span>|<span data-ttu-id="82dbb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="82dbb-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82dbb-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="82dbb-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="82dbb-114">标识要[FindFolder](findfolder.md)响应中返回结果的最大数量。</span><span class="sxs-lookup"><span data-stu-id="82dbb-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="82dbb-115">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="82dbb-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="82dbb-116">**分子**</span><span class="sxs-lookup"><span data-stu-id="82dbb-116">**Numerator**</span></span> <br/> |<span data-ttu-id="82dbb-117">从结果集中的开始表示分数偏移量的分子。</span><span class="sxs-lookup"><span data-stu-id="82dbb-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="82dbb-118">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="82dbb-118">This attribute is required.</span></span> <span data-ttu-id="82dbb-119">分子必须等于或小于分母。</span><span class="sxs-lookup"><span data-stu-id="82dbb-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="82dbb-120">此属性必须表示等于或大于零的整数值。</span><span class="sxs-lookup"><span data-stu-id="82dbb-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="82dbb-121">有关详细信息，请参阅本主题后面的备注。</span><span class="sxs-lookup"><span data-stu-id="82dbb-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="82dbb-122">**分母**</span><span class="sxs-lookup"><span data-stu-id="82dbb-122">**Denominator**</span></span> <br/> |<span data-ttu-id="82dbb-123">代表分数偏移量的分母，为从的开始处的结果集内的文件夹的总数。</span><span class="sxs-lookup"><span data-stu-id="82dbb-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="82dbb-124">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="82dbb-124">This attribute is required.</span></span> <span data-ttu-id="82dbb-125">此属性必须表示大于 1 的整数值。</span><span class="sxs-lookup"><span data-stu-id="82dbb-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="82dbb-126">有关详细信息，请参阅本主题后面的备注。</span><span class="sxs-lookup"><span data-stu-id="82dbb-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="82dbb-127">子元素</span><span class="sxs-lookup"><span data-stu-id="82dbb-127">Child elements</span></span>

<span data-ttu-id="82dbb-128">无。</span><span class="sxs-lookup"><span data-stu-id="82dbb-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82dbb-129">父元素</span><span class="sxs-lookup"><span data-stu-id="82dbb-129">Parent elements</span></span>

|<span data-ttu-id="82dbb-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="82dbb-130">**Element**</span></span>|<span data-ttu-id="82dbb-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="82dbb-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82dbb-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="82dbb-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="82dbb-133">定义一个请求，以确定邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="82dbb-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="82dbb-134">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="82dbb-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82dbb-135">备注</span><span class="sxs-lookup"><span data-stu-id="82dbb-135">Remarks</span></span>

<span data-ttu-id="82dbb-136">通过一小部分介绍了从开始的一组找到文件夹的分页的视图偏移量。</span><span class="sxs-lookup"><span data-stu-id="82dbb-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="82dbb-137">分数，由**分子**和**分母**属性定义，介绍的信息页的起始位置。</span><span class="sxs-lookup"><span data-stu-id="82dbb-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="82dbb-138">例如，如果**分子**等于四**分母**等于 5，返回的信息开始的项的页面位于五分之四中到结果集中的方式。</span><span class="sxs-lookup"><span data-stu-id="82dbb-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="82dbb-139">如果 fraction 计算结果为零，用于指示结果集的开头。</span><span class="sxs-lookup"><span data-stu-id="82dbb-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="82dbb-140">如果 fraction 计算结果为一个，表明结果集的末尾。</span><span class="sxs-lookup"><span data-stu-id="82dbb-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82dbb-141">分数表示的页面的起始点，则将返回结果集内的结果不数量。</span><span class="sxs-lookup"><span data-stu-id="82dbb-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="82dbb-142">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82dbb-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82dbb-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="82dbb-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82dbb-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="82dbb-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="82dbb-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="82dbb-145">Schema Name</span></span>  <br/> |<span data-ttu-id="82dbb-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="82dbb-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="82dbb-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="82dbb-147">Validation File</span></span>  <br/> |<span data-ttu-id="82dbb-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82dbb-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82dbb-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="82dbb-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="82dbb-150">False</span><span class="sxs-lookup"><span data-stu-id="82dbb-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82dbb-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82dbb-151">See also</span></span>



[<span data-ttu-id="82dbb-152">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="82dbb-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="82dbb-153">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="82dbb-153">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

