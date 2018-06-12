---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: ErrorMessage 元素均表示一条消息，与错误代码返回的自动发现服务相关联。
ms.openlocfilehash: 888eedc9c7cbbd1aad5cba21e76d999699c7ed02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754156"
---
# <a name="errormessage-soap"></a><span data-ttu-id="c8947-103">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="c8947-104">**ErrorMessage**元素均表示一条消息，与错误代码返回的自动发现服务相关联。</span><span class="sxs-lookup"><span data-stu-id="c8947-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="c8947-105">**string**</span><span class="sxs-lookup"><span data-stu-id="c8947-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8947-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c8947-106">Attributes and elements</span></span>

<span data-ttu-id="c8947-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8947-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8947-108">属性</span><span class="sxs-lookup"><span data-stu-id="c8947-108">Attributes</span></span>

<span data-ttu-id="c8947-109">无。</span><span class="sxs-lookup"><span data-stu-id="c8947-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8947-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c8947-110">Child elements</span></span>

<span data-ttu-id="c8947-111">无。</span><span class="sxs-lookup"><span data-stu-id="c8947-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c8947-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c8947-112">Parent elements</span></span>

|<span data-ttu-id="c8947-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8947-113">**Element**</span></span>|<span data-ttu-id="c8947-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8947-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8947-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="c8947-116">代表由自动发现服务返回的所有响应的基类型。</span><span class="sxs-lookup"><span data-stu-id="c8947-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="c8947-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="c8947-118">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="c8947-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="c8947-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="c8947-120">包含对各个域[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)呼叫的响应。</span><span class="sxs-lookup"><span data-stu-id="c8947-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="c8947-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="c8947-122">包含对[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c8947-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c8947-123">响应 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="c8947-124">包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c8947-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c8947-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="c8947-126">代表在检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="c8947-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="c8947-127">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="c8947-128">代表对单个用户[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c8947-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c8947-129">文本值</span><span class="sxs-lookup"><span data-stu-id="c8947-129">Text value</span></span>

<span data-ttu-id="c8947-130">文本值表示的错误消息。</span><span class="sxs-lookup"><span data-stu-id="c8947-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8947-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="c8947-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8947-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="c8947-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c8947-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="c8947-133">Schema Name</span></span>  <br/> |<span data-ttu-id="c8947-134">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="c8947-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c8947-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="c8947-135">Validation File</span></span>  <br/> |<span data-ttu-id="c8947-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c8947-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c8947-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="c8947-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8947-138">True</span><span class="sxs-lookup"><span data-stu-id="c8947-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8947-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8947-139">See also</span></span>



[<span data-ttu-id="c8947-140">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="c8947-141">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="c8947-142">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c8947-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

