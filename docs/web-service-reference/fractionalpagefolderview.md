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
description: FractionalPageFolderView 元素说明分页视图的起始位置以及在 FindFolder 请求中返回的最大文件夹数。
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463067"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="ae196-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="ae196-103">FractionalPageFolderView</span></span>

<span data-ttu-id="ae196-104">**FractionalPageFolderView**元素说明分页视图的起始位置以及在[FindFolder](findfolder.md)请求中返回的最大文件夹数。</span><span class="sxs-lookup"><span data-stu-id="ae196-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="ae196-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="ae196-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="ae196-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="ae196-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="ae196-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="ae196-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae196-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae196-108">Attributes and elements</span></span>

<span data-ttu-id="ae196-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae196-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae196-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="ae196-110">Attributes</span></span>

|<span data-ttu-id="ae196-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="ae196-111">**Attribute**</span></span>|<span data-ttu-id="ae196-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae196-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae196-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="ae196-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="ae196-114">标识要在[FindFolder](findfolder.md)响应中返回的最大结果数。</span><span class="sxs-lookup"><span data-stu-id="ae196-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="ae196-115">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="ae196-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="ae196-116">**分子**</span><span class="sxs-lookup"><span data-stu-id="ae196-116">**Numerator**</span></span> <br/> |<span data-ttu-id="ae196-117">表示从结果集的开头的小数偏移量的分子。</span><span class="sxs-lookup"><span data-stu-id="ae196-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="ae196-118">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="ae196-118">This attribute is required.</span></span> <span data-ttu-id="ae196-119">分子必须等于或小于分母。</span><span class="sxs-lookup"><span data-stu-id="ae196-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="ae196-120">此属性必须代表等于或大于零的整数值。</span><span class="sxs-lookup"><span data-stu-id="ae196-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="ae196-121">有关详细信息，请参阅本主题后面的 "备注"。</span><span class="sxs-lookup"><span data-stu-id="ae196-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="ae196-122">**母**</span><span class="sxs-lookup"><span data-stu-id="ae196-122">**Denominator**</span></span> <br/> |<span data-ttu-id="ae196-123">表示从结果集内的文件夹总数开始的小数偏移量的分母。</span><span class="sxs-lookup"><span data-stu-id="ae196-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="ae196-124">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="ae196-124">This attribute is required.</span></span> <span data-ttu-id="ae196-125">此属性必须代表大于1的整数值。</span><span class="sxs-lookup"><span data-stu-id="ae196-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="ae196-126">有关详细信息，请参阅本主题后面的 "备注"。</span><span class="sxs-lookup"><span data-stu-id="ae196-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae196-127">子元素</span><span class="sxs-lookup"><span data-stu-id="ae196-127">Child elements</span></span>

<span data-ttu-id="ae196-128">无。</span><span class="sxs-lookup"><span data-stu-id="ae196-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae196-129">父元素</span><span class="sxs-lookup"><span data-stu-id="ae196-129">Parent elements</span></span>

|<span data-ttu-id="ae196-130">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae196-130">**Element**</span></span>|<span data-ttu-id="ae196-131">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae196-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae196-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="ae196-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="ae196-133">定义用于标识邮箱中的文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="ae196-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="ae196-134">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ae196-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae196-135">备注</span><span class="sxs-lookup"><span data-stu-id="ae196-135">Remarks</span></span>

<span data-ttu-id="ae196-136">从找到的文件夹集开始的分页视图偏移量按分数进行描述。</span><span class="sxs-lookup"><span data-stu-id="ae196-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="ae196-137">由**分子**和**分母**属性定义的小数描述了信息页面的起始位置。</span><span class="sxs-lookup"><span data-stu-id="ae196-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="ae196-138">例如，如果**分子**等于四，**分母**等于5，则返回的信息的页面从 fifths 中的一个条目开始，该条目位于结果集内。</span><span class="sxs-lookup"><span data-stu-id="ae196-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="ae196-139">如果分式的计算结果为零，则指示结果集的开头。</span><span class="sxs-lookup"><span data-stu-id="ae196-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="ae196-140">如果该分数的计算结果为1，则指示结果集的结尾。</span><span class="sxs-lookup"><span data-stu-id="ae196-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae196-141">分数表示页面的起始点，而不是返回结果集中的结果数。</span><span class="sxs-lookup"><span data-stu-id="ae196-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="ae196-142">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae196-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae196-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae196-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae196-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae196-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae196-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae196-145">Schema Name</span></span>  <br/> |<span data-ttu-id="ae196-146">消息架构</span><span class="sxs-lookup"><span data-stu-id="ae196-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae196-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae196-147">Validation File</span></span>  <br/> |<span data-ttu-id="ae196-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae196-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae196-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae196-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae196-150">False</span><span class="sxs-lookup"><span data-stu-id="ae196-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae196-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae196-151">See also</span></span>



[<span data-ttu-id="ae196-152">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="ae196-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="ae196-153">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="ae196-153">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

