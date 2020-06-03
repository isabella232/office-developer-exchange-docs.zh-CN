---
title: DomainResponses （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: DomainResponses 元素包含每个请求的域的设置的响应数组。
ms.openlocfilehash: 2c76b9691fe88657a65130ef6829e5af64380d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526317"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="ff2a4-103">DomainResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ff2a4-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="ff2a4-104">**DomainResponses**元素包含每个请求的域的设置的响应数组。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="ff2a4-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="ff2a4-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff2a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ff2a4-106">Attributes and elements</span></span>

<span data-ttu-id="ff2a4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff2a4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ff2a4-108">Attributes</span></span>

<span data-ttu-id="ff2a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff2a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ff2a4-110">Child elements</span></span>

|<span data-ttu-id="ff2a4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff2a4-111">**Element**</span></span>|<span data-ttu-id="ff2a4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff2a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff2a4-113">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ff2a4-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="ff2a4-114">包含指定域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ff2a4-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ff2a4-115">Parent elements</span></span>

|<span data-ttu-id="ff2a4-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff2a4-116">**Element**</span></span>|<span data-ttu-id="ff2a4-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff2a4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff2a4-118">GetDomainSettingsResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ff2a4-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="ff2a4-119">表示对域的[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求的响应，并返回域设置。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="ff2a4-120">响应（GetDomainSettings）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="ff2a4-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="ff2a4-121">表示对单个域的[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)调用的响应。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff2a4-122">文本值</span><span class="sxs-lookup"><span data-stu-id="ff2a4-122">Text value</span></span>

<span data-ttu-id="ff2a4-123">无。</span><span class="sxs-lookup"><span data-stu-id="ff2a4-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff2a4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="ff2a4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff2a4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="ff2a4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ff2a4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="ff2a4-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ff2a4-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ff2a4-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ff2a4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="ff2a4-128">Validation File</span></span>  <br/> |<span data-ttu-id="ff2a4-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ff2a4-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ff2a4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="ff2a4-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff2a4-131">True</span><span class="sxs-lookup"><span data-stu-id="ff2a4-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff2a4-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff2a4-132">See also</span></span>

- [<span data-ttu-id="ff2a4-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ff2a4-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

