---
title: 响应 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Response 元素包含对 GetUserSettings 操作 (SOAP)、 GetDomainSettings 操作 (SOAP) 或 GetFederationInformation 操作 (SOAP) 请求的响应。
ms.openlocfilehash: 240c8e1f904ad685b51c1f657b2bc18e14fd985e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827179"
---
# <a name="response-soap"></a><span data-ttu-id="3ff59-103">响应 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-103">Response (SOAP)</span></span>

<span data-ttu-id="3ff59-104">**Response**元素包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)、 [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)或[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="3ff59-104">The **Response** element contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 <span data-ttu-id="3ff59-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="3ff59-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ff59-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3ff59-106">Attributes and elements</span></span>

<span data-ttu-id="3ff59-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3ff59-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ff59-108">属性</span><span class="sxs-lookup"><span data-stu-id="3ff59-108">Attributes</span></span>

<span data-ttu-id="3ff59-109">无。</span><span class="sxs-lookup"><span data-stu-id="3ff59-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ff59-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3ff59-110">Child elements</span></span>

|<span data-ttu-id="3ff59-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3ff59-111">**Element**</span></span>|<span data-ttu-id="3ff59-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3ff59-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ff59-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="3ff59-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="3ff59-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="3ff59-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="3ff59-116">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="3ff59-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="3ff59-117">UserResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="3ff59-118">包含为每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="3ff59-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ff59-119">父元素</span><span class="sxs-lookup"><span data-stu-id="3ff59-119">Parent elements</span></span>

|<span data-ttu-id="3ff59-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="3ff59-120">**Element**</span></span>|<span data-ttu-id="3ff59-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="3ff59-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ff59-122">GetUserSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-122">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="3ff59-123">定义对[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)的响应</span><span class="sxs-lookup"><span data-stu-id="3ff59-123">Defines a response to a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span></span> <br/> |
|[<span data-ttu-id="3ff59-124">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-124">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="3ff59-125">定义对[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="3ff59-125">Defines a response to a [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="3ff59-126">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-126">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="3ff59-127">定义对[GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="3ff59-127">Defines a response to a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ff59-128">文本值</span><span class="sxs-lookup"><span data-stu-id="3ff59-128">Text value</span></span>

<span data-ttu-id="3ff59-129">无。</span><span class="sxs-lookup"><span data-stu-id="3ff59-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ff59-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="3ff59-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ff59-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="3ff59-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3ff59-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="3ff59-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3ff59-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="3ff59-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3ff59-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="3ff59-134">Validation File</span></span>  <br/> |<span data-ttu-id="3ff59-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3ff59-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ff59-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="3ff59-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ff59-137">True</span><span class="sxs-lookup"><span data-stu-id="3ff59-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ff59-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3ff59-138">See also</span></span>



[<span data-ttu-id="3ff59-139">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3ff59-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="3ff59-140">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="3ff59-140">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="3ff59-141">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="3ff59-141">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

