---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: UniqueBodyType 元素指定是否以文本或 HTML 格式返回唯一正文。
ms.openlocfilehash: 7e6c4631ef589555ce4d5da747c200ffe956f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459438"
---
# <a name="uniquebodytype"></a><span data-ttu-id="18e5f-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="18e5f-103">UniqueBodyType</span></span>

<span data-ttu-id="18e5f-104">**UniqueBodyType**元素指定是否以文本或 HTML 格式返回唯一正文。</span><span class="sxs-lookup"><span data-stu-id="18e5f-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="18e5f-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="18e5f-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18e5f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18e5f-106">Attributes and elements</span></span>

<span data-ttu-id="18e5f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18e5f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18e5f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="18e5f-108">Attributes</span></span>

<span data-ttu-id="18e5f-109">无。</span><span class="sxs-lookup"><span data-stu-id="18e5f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18e5f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="18e5f-110">Child elements</span></span>

<span data-ttu-id="18e5f-111">无。</span><span class="sxs-lookup"><span data-stu-id="18e5f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18e5f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="18e5f-112">Parent elements</span></span>

[<span data-ttu-id="18e5f-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="18e5f-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="18e5f-114">文本值</span><span class="sxs-lookup"><span data-stu-id="18e5f-114">Text value</span></span>

<span data-ttu-id="18e5f-115">**UniqueBodyType**元素的文本值指示中返回的唯一正文的格式。</span><span class="sxs-lookup"><span data-stu-id="18e5f-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="18e5f-116">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="18e5f-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="18e5f-117">**值**</span><span class="sxs-lookup"><span data-stu-id="18e5f-117">**Value**</span></span>|<span data-ttu-id="18e5f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="18e5f-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18e5f-119">最好</span><span class="sxs-lookup"><span data-stu-id="18e5f-119">Best</span></span>  <br/> |<span data-ttu-id="18e5f-120">响应将返回正文文本的最丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="18e5f-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="18e5f-121">如果不知道内容是文本还是 HTML，这将非常有用。</span><span class="sxs-lookup"><span data-stu-id="18e5f-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="18e5f-122">如果存储的正文为纯文本，则返回的正文将为文本。</span><span class="sxs-lookup"><span data-stu-id="18e5f-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="18e5f-123">否则，如果存储的正文是 HTML 格式或 RTF 格式，则响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="18e5f-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="18e5f-124">此值为默认值。</span><span class="sxs-lookup"><span data-stu-id="18e5f-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="18e5f-125">HTML</span><span class="sxs-lookup"><span data-stu-id="18e5f-125">HTML</span></span>  <br/> |<span data-ttu-id="18e5f-126">响应将以 HTML 形式返回唯一正文。</span><span class="sxs-lookup"><span data-stu-id="18e5f-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="18e5f-127">文本</span><span class="sxs-lookup"><span data-stu-id="18e5f-127">Text</span></span>  <br/> |<span data-ttu-id="18e5f-128">响应将以纯文本形式返回唯一正文。</span><span class="sxs-lookup"><span data-stu-id="18e5f-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18e5f-129">说明</span><span class="sxs-lookup"><span data-stu-id="18e5f-129">Remarks</span></span>

<span data-ttu-id="18e5f-130">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="18e5f-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="18e5f-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18e5f-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18e5f-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="18e5f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18e5f-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="18e5f-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18e5f-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="18e5f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="18e5f-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="18e5f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="18e5f-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="18e5f-136">Validation File</span></span>  <br/> |<span data-ttu-id="18e5f-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18e5f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18e5f-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="18e5f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="18e5f-139">True</span><span class="sxs-lookup"><span data-stu-id="18e5f-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18e5f-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18e5f-140">See also</span></span>



[<span data-ttu-id="18e5f-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="18e5f-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="18e5f-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18e5f-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

