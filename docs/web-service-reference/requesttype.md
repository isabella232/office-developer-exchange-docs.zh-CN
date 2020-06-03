---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: RequestType 元素标识代理请求是否为跨网站或跨林请求。
ms.openlocfilehash: 278a65a1f2ce4cb433ae8099703d70d0a2cafa3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455966"
---
# <a name="requesttype"></a><span data-ttu-id="a8d2a-103">RequestType</span><span class="sxs-lookup"><span data-stu-id="a8d2a-103">RequestType</span></span>

<span data-ttu-id="a8d2a-104">**RequestType**元素标识代理请求是否为跨网站或跨林请求。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-104">The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request.</span></span> 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 <span data-ttu-id="a8d2a-105">**AvailabilityProxyRequestType**</span><span class="sxs-lookup"><span data-stu-id="a8d2a-105">**AvailabilityProxyRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8d2a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a8d2a-106">Attributes and elements</span></span>

<span data-ttu-id="a8d2a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8d2a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a8d2a-108">Attributes</span></span>

<span data-ttu-id="a8d2a-109">无。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8d2a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a8d2a-110">Child elements</span></span>

<span data-ttu-id="a8d2a-111">无。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8d2a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a8d2a-112">Parent elements</span></span>

<span data-ttu-id="a8d2a-113">此元素在架构中没有父级。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-113">This element does not have a parent in the schema.</span></span> <span data-ttu-id="a8d2a-114">此元素在 SOAP 标头中使用。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-114">This element is used in the SOAP header.</span></span> <span data-ttu-id="a8d2a-115">有关如何使用此元素的详细信息，请参阅 WSDL 文件。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-115">For more information about how this element is used, see the WSDL file.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a8d2a-116">文本值</span><span class="sxs-lookup"><span data-stu-id="a8d2a-116">Text value</span></span>

<span data-ttu-id="a8d2a-117">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="a8d2a-117">A text value is required for this element.</span></span> <span data-ttu-id="a8d2a-118">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="a8d2a-118">The following are the possible values:</span></span>
  
- <span data-ttu-id="a8d2a-119">CrossSite</span><span class="sxs-lookup"><span data-stu-id="a8d2a-119">CrossSite</span></span>
    
- <span data-ttu-id="a8d2a-120">CrossForest</span><span class="sxs-lookup"><span data-stu-id="a8d2a-120">CrossForest</span></span>
    
## <a name="element-information"></a><span data-ttu-id="a8d2a-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="a8d2a-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8d2a-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="a8d2a-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8d2a-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="a8d2a-123">Schema name</span></span>  <br/> |<span data-ttu-id="a8d2a-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="a8d2a-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8d2a-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="a8d2a-125">Validation file</span></span>  <br/> |<span data-ttu-id="a8d2a-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8d2a-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8d2a-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="a8d2a-127">Can be empty</span></span>  <br/> |<span data-ttu-id="a8d2a-128">False</span><span class="sxs-lookup"><span data-stu-id="a8d2a-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8d2a-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8d2a-129">See also</span></span>



- [<span data-ttu-id="a8d2a-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a8d2a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

