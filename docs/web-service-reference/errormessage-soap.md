---
title: ErrorMessage （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: ErrorMessage 元素表示与自动发现服务返回的错误代码相关联的消息。
ms.openlocfilehash: 4ebaf91fe26083cf241826e1fc16ac184fddf57c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530640"
---
# <a name="errormessage-soap"></a><span data-ttu-id="1003e-103">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-103">ErrorMessage (SOAP)</span></span>

<span data-ttu-id="1003e-104">**ErrorMessage**元素表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="1003e-104">The **ErrorMessage** element represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorMessage/>
```

 <span data-ttu-id="1003e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="1003e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1003e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1003e-106">Attributes and elements</span></span>

<span data-ttu-id="1003e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1003e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1003e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1003e-108">Attributes</span></span>

<span data-ttu-id="1003e-109">无。</span><span class="sxs-lookup"><span data-stu-id="1003e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1003e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1003e-110">Child elements</span></span>

<span data-ttu-id="1003e-111">无。</span><span class="sxs-lookup"><span data-stu-id="1003e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1003e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1003e-112">Parent elements</span></span>

|<span data-ttu-id="1003e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1003e-113">**Element**</span></span>|<span data-ttu-id="1003e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1003e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1003e-115">AutodiscoverResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="1003e-116">表示自动发现服务返回的所有响应的基本类型。</span><span class="sxs-lookup"><span data-stu-id="1003e-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="1003e-117">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="1003e-118">包含指定域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="1003e-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="1003e-119">GetDomainSettingsResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="1003e-120">包含对单个域的[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)调用的响应。</span><span class="sxs-lookup"><span data-stu-id="1003e-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="1003e-121">GetFederationInformationResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="1003e-122">包含对[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1003e-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1003e-123">响应（SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="1003e-124">包含对[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1003e-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1003e-125">UserSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="1003e-126">表示检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="1003e-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="1003e-127">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="1003e-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="1003e-128">表示对单个用户的[GetUserSettings 操作（SOAP）](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1003e-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1003e-129">文本值</span><span class="sxs-lookup"><span data-stu-id="1003e-129">Text value</span></span>

<span data-ttu-id="1003e-130">该文本值表示错误消息。</span><span class="sxs-lookup"><span data-stu-id="1003e-130">The text value represents the error message.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1003e-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="1003e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1003e-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="1003e-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1003e-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="1003e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="1003e-134">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="1003e-134">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1003e-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="1003e-135">Validation File</span></span>  <br/> |<span data-ttu-id="1003e-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1003e-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1003e-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="1003e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="1003e-138">True</span><span class="sxs-lookup"><span data-stu-id="1003e-138">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1003e-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1003e-139">See also</span></span>



[<span data-ttu-id="1003e-140">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1003e-140">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="1003e-141">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1003e-141">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="1003e-142">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1003e-142">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

