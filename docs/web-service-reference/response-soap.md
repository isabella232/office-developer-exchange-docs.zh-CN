---
title: 响应（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Response 元素包含对 GetUserSettings 操作（SOAP）、GetDomainSettings 操作（SOAP）或 GetFederationInformation 操作（SOAP）请求的响应。
ms.openlocfilehash: 90cb29dd4ce4026211a5b592f149c8190dc81d29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456414"
---
# <a name="response-soap"></a><span data-ttu-id="41ee4-103">响应（SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-103">Response (SOAP)</span></span>

<span data-ttu-id="41ee4-104">**Response**元素包含对[GETUSERSETTINGS 操作（soap）](getusersettings-operation-soap.md)、 [GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)或[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="41ee4-104">The **Response** element contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md), [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 <span data-ttu-id="41ee4-105">**GetUserSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="41ee4-105">**GetUserSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41ee4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41ee4-106">Attributes and elements</span></span>

<span data-ttu-id="41ee4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41ee4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41ee4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="41ee4-108">Attributes</span></span>

<span data-ttu-id="41ee4-109">无。</span><span class="sxs-lookup"><span data-stu-id="41ee4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41ee4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="41ee4-110">Child elements</span></span>

|<span data-ttu-id="41ee4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="41ee4-111">**Element**</span></span>|<span data-ttu-id="41ee4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="41ee4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41ee4-113">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="41ee4-114">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="41ee4-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="41ee4-115">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="41ee4-116">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="41ee4-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="41ee4-117">UserResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-117">UserResponses (SOAP)</span></span>](userresponses-soap.md) <br/> |<span data-ttu-id="41ee4-118">包含每个请求的用户的配置设置。</span><span class="sxs-lookup"><span data-stu-id="41ee4-118">Contains the configuration settings for each requested user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41ee4-119">父元素</span><span class="sxs-lookup"><span data-stu-id="41ee4-119">Parent elements</span></span>

|<span data-ttu-id="41ee4-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="41ee4-120">**Element**</span></span>|<span data-ttu-id="41ee4-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="41ee4-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41ee4-122">GetUserSettingsResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-122">GetUserSettingsResponseMessage (SOAP)</span></span>](getusersettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="41ee4-123">定义对[GetUserSettingsRequest （SOAP）](getusersettingsrequest-soap.md)的响应</span><span class="sxs-lookup"><span data-stu-id="41ee4-123">Defines a response to a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)</span></span> <br/> |
|[<span data-ttu-id="41ee4-124">GetDomainSettingsResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-124">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="41ee4-125">定义对[GetDomainSettingsRequest （SOAP）](getdomainsettingsrequest-soap.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="41ee4-125">Defines a response to a [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="41ee4-126">GetFederationInformationResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41ee4-126">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="41ee4-127">定义对[GetFederationInformationRequest （SOAP）](getfederationinformationrequest-soap.md)的响应。</span><span class="sxs-lookup"><span data-stu-id="41ee4-127">Defines a response to a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41ee4-128">文本值</span><span class="sxs-lookup"><span data-stu-id="41ee4-128">Text value</span></span>

<span data-ttu-id="41ee4-129">无。</span><span class="sxs-lookup"><span data-stu-id="41ee4-129">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41ee4-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="41ee4-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41ee4-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="41ee4-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41ee4-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="41ee4-132">Schema Name</span></span>  <br/> |<span data-ttu-id="41ee4-133">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="41ee4-133">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41ee4-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="41ee4-134">Validation File</span></span>  <br/> |<span data-ttu-id="41ee4-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41ee4-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41ee4-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="41ee4-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="41ee4-137">True</span><span class="sxs-lookup"><span data-stu-id="41ee4-137">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41ee4-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41ee4-138">See also</span></span>



[<span data-ttu-id="41ee4-139">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="41ee4-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="41ee4-140">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="41ee4-140">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="41ee4-141">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="41ee4-141">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

