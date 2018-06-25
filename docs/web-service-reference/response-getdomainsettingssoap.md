---
title: 响应 (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: 响应元素均表示各个域 GetDomainSettings 呼叫的响应。
ms.openlocfilehash: 316d77104894cf5ed9121e7dab1c38646765c948
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827169"
---
# <a name="response-getdomainsettings-soap"></a><span data-ttu-id="ae0d9-103">响应 (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-103">Response (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="ae0d9-104">**响应**元素均表示各个域**GetDomainSettings**呼叫的响应。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-104">The **Response** element represents the response to a **GetDomainSettings** call for an individual domain.</span></span> 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 <span data-ttu-id="ae0d9-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="ae0d9-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae0d9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae0d9-106">Attributes and elements</span></span>

<span data-ttu-id="ae0d9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae0d9-108">属性</span><span class="sxs-lookup"><span data-stu-id="ae0d9-108">Attributes</span></span>

<span data-ttu-id="ae0d9-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae0d9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae0d9-110">Child elements</span></span>

|<span data-ttu-id="ae0d9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae0d9-111">**Element**</span></span>|<span data-ttu-id="ae0d9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae0d9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae0d9-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="ae0d9-114">包含为每个域**GetDomainSettings**请求中请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-114">Contains the response for each domain requested in a **GetDomainSettings** request.</span></span>  <br/> |
|[<span data-ttu-id="ae0d9-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="ae0d9-116">如果适用，则包含响应中，与相关联的错误代码。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-116">Contains the error code that is associated with the response, if applicable.</span></span>  <br/> |
|[<span data-ttu-id="ae0d9-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="ae0d9-118">如果适用，则包含响应中，与相关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-118">Contains the error message that is associated with the response, if applicable.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae0d9-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ae0d9-119">Parent elements</span></span>

|<span data-ttu-id="ae0d9-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae0d9-120">**Element**</span></span>|<span data-ttu-id="ae0d9-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae0d9-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae0d9-122">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-122">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="ae0d9-123">返回给调用方域配置设置。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-123">Returns to the caller the domain configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae0d9-124">文本值</span><span class="sxs-lookup"><span data-stu-id="ae0d9-124">Text value</span></span>

<span data-ttu-id="ae0d9-125">无。</span><span class="sxs-lookup"><span data-stu-id="ae0d9-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae0d9-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae0d9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae0d9-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae0d9-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ae0d9-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae0d9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ae0d9-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ae0d9-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ae0d9-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae0d9-130">Validation File</span></span>  <br/> |<span data-ttu-id="ae0d9-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae0d9-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae0d9-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae0d9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae0d9-133">True</span><span class="sxs-lookup"><span data-stu-id="ae0d9-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae0d9-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae0d9-134">See also</span></span>



[<span data-ttu-id="ae0d9-135">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ae0d9-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

