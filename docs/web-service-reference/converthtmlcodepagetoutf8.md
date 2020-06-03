---
title: ConvertHtmlCodePageToUTF8
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f02c8331-0a4e-4d01-adc2-2b93ed838a42
description: ConvertHtmlCodePageToUTF8 元素指示是否将项目 HTML 正文转换为 UTF8。
ms.openlocfilehash: a714eacd8cc105146a1471f062ec35dc16730d61
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457590"
---
# <a name="converthtmlcodepagetoutf8"></a><span data-ttu-id="1557d-103">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="1557d-103">ConvertHtmlCodePageToUTF8</span></span>

<span data-ttu-id="1557d-104">**ConvertHtmlCodePageToUTF8**元素指示是否将项目 HTML 正文转换为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="1557d-104">The **ConvertHtmlCodePageToUTF8** element indicates whether the item HTML body is converted to UTF8.</span></span> 
  
```XML
<ConvertHtmlCodePageToUTF8/>
```

 <span data-ttu-id="1557d-105">**xs： boolean**</span><span class="sxs-lookup"><span data-stu-id="1557d-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1557d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1557d-106">Attributes and elements</span></span>

<span data-ttu-id="1557d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1557d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1557d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1557d-108">Attributes</span></span>

<span data-ttu-id="1557d-109">无。</span><span class="sxs-lookup"><span data-stu-id="1557d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1557d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1557d-110">Child elements</span></span>

<span data-ttu-id="1557d-111">无。</span><span class="sxs-lookup"><span data-stu-id="1557d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1557d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1557d-112">Parent elements</span></span>

|<span data-ttu-id="1557d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1557d-113">**Element**</span></span>|<span data-ttu-id="1557d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1557d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1557d-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="1557d-115">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="1557d-116">标识要在响应中返回的一组属性。</span><span class="sxs-lookup"><span data-stu-id="1557d-116">Identifies a set of properties to return in a response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1557d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1557d-117">Text value</span></span>

<span data-ttu-id="1557d-118">如果**ConvertHtmlCodePageToUTF8**元素的文本值为**true** ，则指示 HTML 正文将转换为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="1557d-118">A text value of **true** for the **ConvertHtmlCodePageToUTF8** element indicates that the HTML body is converted to UTF8.</span></span> <span data-ttu-id="1557d-119">如果文本值为**false** ，则表示 HTML 正文不转换为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="1557d-119">A text value of **false** indicates that the HTML body is not converted to UTF8.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1557d-120">备注</span><span class="sxs-lookup"><span data-stu-id="1557d-120">Remarks</span></span>

<span data-ttu-id="1557d-121">如果请求中未指定**ConvertHtmlCodePageToUTF8**元素，则使用默认值**true** 。</span><span class="sxs-lookup"><span data-stu-id="1557d-121">The default value of **true** is used if the **ConvertHtmlCodePageToUTF8** element is not specified in a request.</span></span> 
  
<span data-ttu-id="1557d-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1557d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1557d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1557d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1557d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1557d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1557d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1557d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1557d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="1557d-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1557d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1557d-127">Validation File</span></span>  <br/> |<span data-ttu-id="1557d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1557d-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1557d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1557d-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="1557d-130">False</span><span class="sxs-lookup"><span data-stu-id="1557d-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1557d-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1557d-131">See also</span></span>



- [<span data-ttu-id="1557d-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1557d-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

