---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: DomainResponse 元素包含指定的域的请求的设置。
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753975"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="dc97b-103">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="dc97b-104">**DomainResponse**元素包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="dc97b-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="dc97b-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="dc97b-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc97b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc97b-106">Attributes and elements</span></span>

<span data-ttu-id="dc97b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc97b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc97b-108">属性</span><span class="sxs-lookup"><span data-stu-id="dc97b-108">Attributes</span></span>

<span data-ttu-id="dc97b-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc97b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc97b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc97b-110">Child elements</span></span>

|<span data-ttu-id="dc97b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc97b-111">**Element**</span></span>|<span data-ttu-id="dc97b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc97b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc97b-113">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="dc97b-114">包含错误未能返回的设置的信息。</span><span class="sxs-lookup"><span data-stu-id="dc97b-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="dc97b-115">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="dc97b-116">表示已提交的自动发现请求中或由自动发现响应返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="dc97b-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="dc97b-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="dc97b-118">标识目标的重定向。</span><span class="sxs-lookup"><span data-stu-id="dc97b-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="dc97b-119">URL 或电子邮件地址可以是目标。</span><span class="sxs-lookup"><span data-stu-id="dc97b-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="dc97b-120">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="dc97b-121">指定与特定的请求相关联的错误代码。</span><span class="sxs-lookup"><span data-stu-id="dc97b-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="dc97b-122">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="dc97b-123">指定与特定的请求相关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="dc97b-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc97b-124">父元素</span><span class="sxs-lookup"><span data-stu-id="dc97b-124">Parent elements</span></span>

|<span data-ttu-id="dc97b-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc97b-125">**Element**</span></span>|<span data-ttu-id="dc97b-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc97b-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc97b-127">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="dc97b-128">包含**DomainResponse**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="dc97b-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="dc97b-129">每个**DomainResponse**元素包含指定的用户的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="dc97b-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="dc97b-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="dc97b-131">包含为每个域的响应。</span><span class="sxs-lookup"><span data-stu-id="dc97b-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dc97b-132">文本值</span><span class="sxs-lookup"><span data-stu-id="dc97b-132">Text value</span></span>

<span data-ttu-id="dc97b-133">无。</span><span class="sxs-lookup"><span data-stu-id="dc97b-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc97b-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc97b-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc97b-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc97b-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="dc97b-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc97b-136">Schema Name</span></span>  <br/> |<span data-ttu-id="dc97b-137">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="dc97b-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="dc97b-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc97b-138">Validation File</span></span>  <br/> |<span data-ttu-id="dc97b-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dc97b-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc97b-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc97b-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc97b-141">True</span><span class="sxs-lookup"><span data-stu-id="dc97b-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc97b-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc97b-142">See also</span></span>

- [<span data-ttu-id="dc97b-143">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dc97b-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

