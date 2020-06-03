---
title: 响应（GetDomainSettings）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: Response 元素表示对单个域的 GetDomainSettings 调用的响应。
ms.openlocfilehash: 67fe7aea4533058fa0df972e49a2069749dc258b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455581"
---
# <a name="response-getdomainsettings-soap"></a><span data-ttu-id="04d8b-103">响应（GetDomainSettings）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="04d8b-103">Response (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="04d8b-104">**Response**元素表示对单个域的**GetDomainSettings**调用的响应。</span><span class="sxs-lookup"><span data-stu-id="04d8b-104">The **Response** element represents the response to a **GetDomainSettings** call for an individual domain.</span></span> 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 <span data-ttu-id="04d8b-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="04d8b-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04d8b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="04d8b-106">Attributes and elements</span></span>

<span data-ttu-id="04d8b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="04d8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04d8b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="04d8b-108">Attributes</span></span>

<span data-ttu-id="04d8b-109">无。</span><span class="sxs-lookup"><span data-stu-id="04d8b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04d8b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="04d8b-110">Child elements</span></span>

|<span data-ttu-id="04d8b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="04d8b-111">**Element**</span></span>|<span data-ttu-id="04d8b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="04d8b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04d8b-113">DomainResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="04d8b-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="04d8b-114">包含对**GetDomainSettings**请求中请求的每个域的响应。</span><span class="sxs-lookup"><span data-stu-id="04d8b-114">Contains the response for each domain requested in a **GetDomainSettings** request.</span></span>  <br/> |
|[<span data-ttu-id="04d8b-115">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="04d8b-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="04d8b-116">包含与响应关联的错误代码（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="04d8b-116">Contains the error code that is associated with the response, if applicable.</span></span>  <br/> |
|[<span data-ttu-id="04d8b-117">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="04d8b-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="04d8b-118">包含与响应关联的错误消息（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="04d8b-118">Contains the error message that is associated with the response, if applicable.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04d8b-119">父元素</span><span class="sxs-lookup"><span data-stu-id="04d8b-119">Parent elements</span></span>

|<span data-ttu-id="04d8b-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="04d8b-120">**Element**</span></span>|<span data-ttu-id="04d8b-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="04d8b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04d8b-122">GetDomainSettingsResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="04d8b-122">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="04d8b-123">返回到调用方的域配置设置。</span><span class="sxs-lookup"><span data-stu-id="04d8b-123">Returns to the caller the domain configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="04d8b-124">文本值</span><span class="sxs-lookup"><span data-stu-id="04d8b-124">Text value</span></span>

<span data-ttu-id="04d8b-125">无。</span><span class="sxs-lookup"><span data-stu-id="04d8b-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04d8b-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="04d8b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04d8b-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="04d8b-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="04d8b-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="04d8b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="04d8b-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="04d8b-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="04d8b-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="04d8b-130">Validation File</span></span>  <br/> |<span data-ttu-id="04d8b-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="04d8b-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04d8b-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="04d8b-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="04d8b-133">True</span><span class="sxs-lookup"><span data-stu-id="04d8b-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04d8b-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04d8b-134">See also</span></span>



[<span data-ttu-id="04d8b-135">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04d8b-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

