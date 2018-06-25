---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: UniqueBodyType 元素指定唯一的正文是否以文本或 HTML 格式返回。
ms.openlocfilehash: c6eb4ec4e39a0c5355775a635db4c63efc666820
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838332"
---
# <a name="uniquebodytype"></a><span data-ttu-id="b9aa1-103">UniqueBodyType</span><span class="sxs-lookup"><span data-stu-id="b9aa1-103">UniqueBodyType</span></span>

<span data-ttu-id="b9aa1-104">**UniqueBodyType**元素指定唯一的正文是否以文本或 HTML 格式返回。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-104">The **UniqueBodyType** element specifies whether the unique body is returned in text or HTML format.</span></span> 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 <span data-ttu-id="b9aa1-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="b9aa1-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9aa1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b9aa1-106">Attributes and elements</span></span>

<span data-ttu-id="b9aa1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9aa1-108">属性</span><span class="sxs-lookup"><span data-stu-id="b9aa1-108">Attributes</span></span>

<span data-ttu-id="b9aa1-109">无。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9aa1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b9aa1-110">Child elements</span></span>

<span data-ttu-id="b9aa1-111">无。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9aa1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b9aa1-112">Parent elements</span></span>

[<span data-ttu-id="b9aa1-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b9aa1-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="b9aa1-114">文本值</span><span class="sxs-lookup"><span data-stu-id="b9aa1-114">Text value</span></span>

<span data-ttu-id="b9aa1-115">**UniqueBodyType**元素的文本值指示返回的唯一的正文格式。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-115">The text value of the **UniqueBodyType** element indicates format the unique body is returned in.</span></span> <span data-ttu-id="b9aa1-116">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="b9aa1-117">**值**</span><span class="sxs-lookup"><span data-stu-id="b9aa1-117">**Value**</span></span>|<span data-ttu-id="b9aa1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b9aa1-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9aa1-119">最佳</span><span class="sxs-lookup"><span data-stu-id="b9aa1-119">Best</span></span>  <br/> |<span data-ttu-id="b9aa1-120">响应将返回正文文本的丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="b9aa1-121">这很有用，如果不知道的内容是否是文本或 HTML。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="b9aa1-122">返回的正文将文本，如果存储的正文采用纯文本。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="b9aa1-123">否则，如果存储的正文采用 HTML 或 RTF 格式响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="b9aa1-124">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="b9aa1-125">HTML</span><span class="sxs-lookup"><span data-stu-id="b9aa1-125">HTML</span></span>  <br/> |<span data-ttu-id="b9aa1-126">响应将以 HTML 形式返回唯一的正文。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-126">The response will return a unique body as HTML.</span></span>  <br/> |
|<span data-ttu-id="b9aa1-127">Text</span><span class="sxs-lookup"><span data-stu-id="b9aa1-127">Text</span></span>  <br/> |<span data-ttu-id="b9aa1-128">响应将以纯文本形式返回唯一的正文。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-128">The response will return a unique body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9aa1-129">备注</span><span class="sxs-lookup"><span data-stu-id="b9aa1-129">Remarks</span></span>

<span data-ttu-id="b9aa1-130">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="b9aa1-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b9aa1-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9aa1-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="b9aa1-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9aa1-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="b9aa1-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9aa1-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="b9aa1-134">Schema Name</span></span>  <br/> |<span data-ttu-id="b9aa1-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="b9aa1-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9aa1-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="b9aa1-136">Validation File</span></span>  <br/> |<span data-ttu-id="b9aa1-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9aa1-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9aa1-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="b9aa1-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9aa1-139">True</span><span class="sxs-lookup"><span data-stu-id="b9aa1-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9aa1-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9aa1-140">See also</span></span>



[<span data-ttu-id="b9aa1-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="b9aa1-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="b9aa1-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b9aa1-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

