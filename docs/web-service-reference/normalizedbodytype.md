---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: NormalizedBodyType 元素指定是否以文本或 HTML 格式返回规范化的正文。
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826554"
---
# <a name="normalizedbodytype"></a><span data-ttu-id="22a10-103">NormalizedBodyType</span><span class="sxs-lookup"><span data-stu-id="22a10-103">NormalizedBodyType</span></span>

<span data-ttu-id="22a10-104">**NormalizedBodyType**元素指定是否以文本或 HTML 格式返回规范化的正文。</span><span class="sxs-lookup"><span data-stu-id="22a10-104">The **NormalizedBodyType** element specifies whether the normalized body is returned in text or HTML format.</span></span> 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
```

 <span data-ttu-id="22a10-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="22a10-105">**BodyTypeResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22a10-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22a10-106">Attributes and elements</span></span>

<span data-ttu-id="22a10-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22a10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22a10-108">属性</span><span class="sxs-lookup"><span data-stu-id="22a10-108">Attributes</span></span>

<span data-ttu-id="22a10-109">无。</span><span class="sxs-lookup"><span data-stu-id="22a10-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22a10-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22a10-110">Child elements</span></span>

<span data-ttu-id="22a10-111">无。</span><span class="sxs-lookup"><span data-stu-id="22a10-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22a10-112">父元素</span><span class="sxs-lookup"><span data-stu-id="22a10-112">Parent elements</span></span>

[<span data-ttu-id="22a10-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="22a10-113">ItemShape</span></span>](itemshape.md)
  
## <a name="text-value"></a><span data-ttu-id="22a10-114">文本值</span><span class="sxs-lookup"><span data-stu-id="22a10-114">Text value</span></span>

<span data-ttu-id="22a10-115">**NormalizedBodyType**元素的文本值指示规范化的正文格式返回中。</span><span class="sxs-lookup"><span data-stu-id="22a10-115">The text value of the **NormalizedBodyType** element indicates format the normalized body is returned in.</span></span> <span data-ttu-id="22a10-116">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="22a10-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="22a10-117">**值**</span><span class="sxs-lookup"><span data-stu-id="22a10-117">**Value**</span></span>|<span data-ttu-id="22a10-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="22a10-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22a10-119">最佳</span><span class="sxs-lookup"><span data-stu-id="22a10-119">Best</span></span>  <br/> |<span data-ttu-id="22a10-120">响应将返回正文文本的丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="22a10-120">The response will return the richest available content of body text.</span></span> <span data-ttu-id="22a10-121">这很有用，如果不知道的内容是否是文本或 HTML。</span><span class="sxs-lookup"><span data-stu-id="22a10-121">This is useful if it is unknown whether the content is text or HTML.</span></span>  <br/> <span data-ttu-id="22a10-122">返回的正文将文本，如果存储的正文采用纯文本。</span><span class="sxs-lookup"><span data-stu-id="22a10-122">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="22a10-123">否则，如果存储的正文采用 HTML 或 RTF 格式响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="22a10-123">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span>  <br/> <span data-ttu-id="22a10-124">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="22a10-124">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="22a10-125">HTML</span><span class="sxs-lookup"><span data-stu-id="22a10-125">HTML</span></span>  <br/> |<span data-ttu-id="22a10-126">响应将以 HTML 形式返回规范化的正文。</span><span class="sxs-lookup"><span data-stu-id="22a10-126">The response will return a normalized body as HTML.</span></span>  <br/> |
|<span data-ttu-id="22a10-127">Text</span><span class="sxs-lookup"><span data-stu-id="22a10-127">Text</span></span>  <br/> |<span data-ttu-id="22a10-128">响应将以纯文本形式返回规范化的正文。</span><span class="sxs-lookup"><span data-stu-id="22a10-128">The response will return a normalized body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22a10-129">备注</span><span class="sxs-lookup"><span data-stu-id="22a10-129">Remarks</span></span>

<span data-ttu-id="22a10-130">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="22a10-130">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="22a10-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22a10-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22a10-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="22a10-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22a10-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="22a10-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22a10-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="22a10-134">Schema Name</span></span>  <br/> |<span data-ttu-id="22a10-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="22a10-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="22a10-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="22a10-136">Validation File</span></span>  <br/> |<span data-ttu-id="22a10-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22a10-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22a10-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="22a10-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="22a10-139">True</span><span class="sxs-lookup"><span data-stu-id="22a10-139">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22a10-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22a10-140">See also</span></span>



[<span data-ttu-id="22a10-141">ItemShape</span><span class="sxs-lookup"><span data-stu-id="22a10-141">ItemShape</span></span>](itemshape.md)


- [<span data-ttu-id="22a10-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="22a10-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

