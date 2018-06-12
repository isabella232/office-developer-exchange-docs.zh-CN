---
title: DomainResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: DomainResponses 元素包含数组的每个请求的域设置的响应。
ms.openlocfilehash: 77a3efc1605337ab436f6aea2b61a67f22e4f8ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753981"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="7ee7b-103">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ee7b-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="7ee7b-104">**DomainResponses**元素包含数组的每个请求的域设置的响应。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="7ee7b-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="7ee7b-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ee7b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ee7b-106">Attributes and elements</span></span>

<span data-ttu-id="7ee7b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ee7b-108">属性</span><span class="sxs-lookup"><span data-stu-id="7ee7b-108">Attributes</span></span>

<span data-ttu-id="7ee7b-109">无。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ee7b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7ee7b-110">Child elements</span></span>

|<span data-ttu-id="7ee7b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ee7b-111">**Element**</span></span>|<span data-ttu-id="7ee7b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ee7b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ee7b-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ee7b-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="7ee7b-114">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ee7b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7ee7b-115">Parent elements</span></span>

|<span data-ttu-id="7ee7b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ee7b-116">**Element**</span></span>|<span data-ttu-id="7ee7b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ee7b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ee7b-118">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ee7b-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="7ee7b-119">表示一个域， [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求的响应而返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="7ee7b-120">响应 (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ee7b-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="7ee7b-121">代表对各个域[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)呼叫的响应。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ee7b-122">文本值</span><span class="sxs-lookup"><span data-stu-id="7ee7b-122">Text value</span></span>

<span data-ttu-id="7ee7b-123">无。</span><span class="sxs-lookup"><span data-stu-id="7ee7b-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ee7b-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ee7b-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ee7b-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ee7b-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7ee7b-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ee7b-126">Schema Name</span></span>  <br/> |<span data-ttu-id="7ee7b-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="7ee7b-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7ee7b-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ee7b-128">Validation File</span></span>  <br/> |<span data-ttu-id="7ee7b-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7ee7b-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7ee7b-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ee7b-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ee7b-131">True</span><span class="sxs-lookup"><span data-stu-id="7ee7b-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ee7b-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ee7b-132">See also</span></span>

- [<span data-ttu-id="7ee7b-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ee7b-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

