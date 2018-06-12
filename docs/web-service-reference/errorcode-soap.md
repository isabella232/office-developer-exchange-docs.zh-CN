---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: ErrorCode 元素均表示由自动发现服务返回的错误代码。
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754146"
---
# <a name="errorcode-soap"></a><span data-ttu-id="7951a-103">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-103">ErrorCode (SOAP)</span></span>

<span data-ttu-id="7951a-104">**ErrorCode**元素均表示由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="7951a-104">The **ErrorCode** element represents an error code that is returned by the Autodiscover service.</span></span> 
  
```XML
<ErrorCode/>
```

 <span data-ttu-id="7951a-105">**string**</span><span class="sxs-lookup"><span data-stu-id="7951a-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7951a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7951a-106">Attributes and elements</span></span>

<span data-ttu-id="7951a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7951a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7951a-108">属性</span><span class="sxs-lookup"><span data-stu-id="7951a-108">Attributes</span></span>

<span data-ttu-id="7951a-109">无。</span><span class="sxs-lookup"><span data-stu-id="7951a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7951a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7951a-110">Child elements</span></span>

<span data-ttu-id="7951a-111">无。</span><span class="sxs-lookup"><span data-stu-id="7951a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7951a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7951a-112">Parent elements</span></span>

|<span data-ttu-id="7951a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7951a-113">**Element**</span></span>|<span data-ttu-id="7951a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7951a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7951a-115">AutodiscoverResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-115">AutodiscoverResponse (SOAP)</span></span>](autodiscoverresponse-soap.md) <br/> |<span data-ttu-id="7951a-116">代表由自动发现服务返回的所有响应的基类型。</span><span class="sxs-lookup"><span data-stu-id="7951a-116">Represents the base type for all responses that are returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7951a-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="7951a-118">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="7951a-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
|[<span data-ttu-id="7951a-119">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-119">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="7951a-120">包含对各个域[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)呼叫的响应。</span><span class="sxs-lookup"><span data-stu-id="7951a-120">Contains the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
|[<span data-ttu-id="7951a-121">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-121">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="7951a-122">包含对[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7951a-122">Contains the response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7951a-123">响应 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-123">Response (SOAP)</span></span>](response-soap.md) <br/> |<span data-ttu-id="7951a-124">包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7951a-124">Contains the response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md)request.</span></span>  <br/> |
|[<span data-ttu-id="7951a-125">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-125">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="7951a-126">代表在检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="7951a-126">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="7951a-127">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-127">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="7951a-128">代表对单个用户[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7951a-128">Represents a response to a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7951a-129">文本值</span><span class="sxs-lookup"><span data-stu-id="7951a-129">Text value</span></span>

<span data-ttu-id="7951a-130">文本值表示的错误代码为自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="7951a-130">The text value represents the error code for an Autodiscover error response.</span></span> <span data-ttu-id="7951a-131">下表列出了**ErrorCode**元素的可能的文本值。</span><span class="sxs-lookup"><span data-stu-id="7951a-131">The following table lists the possible text values for the **ErrorCode** element.</span></span> 
  
|<span data-ttu-id="7951a-132">**错误代码的文本值**</span><span class="sxs-lookup"><span data-stu-id="7951a-132">**Error code text value**</span></span>|<span data-ttu-id="7951a-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="7951a-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7951a-134">NoError</span><span class="sxs-lookup"><span data-stu-id="7951a-134">NoError</span></span>  <br/> |<span data-ttu-id="7951a-135">没有错误。</span><span class="sxs-lookup"><span data-stu-id="7951a-135">There was no error.</span></span>  <br/> |
|<span data-ttu-id="7951a-136">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="7951a-136">RedirectAddress</span></span>  <br/> |<span data-ttu-id="7951a-137">呼叫者必须遵循的电子邮件地址重定向返回的自动发现。</span><span class="sxs-lookup"><span data-stu-id="7951a-137">The caller must follow the e-mail address redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="7951a-138">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="7951a-138">RedirectUrl</span></span>  <br/> |<span data-ttu-id="7951a-139">呼叫者必须遵循返回的自动发现 URL 重定向。</span><span class="sxs-lookup"><span data-stu-id="7951a-139">The caller must follow the URL redirection that was returned by Autodiscover.</span></span>  <br/> |
|<span data-ttu-id="7951a-140">InvalidUser</span><span class="sxs-lookup"><span data-stu-id="7951a-140">InvalidUser</span></span>  <br/> |<span data-ttu-id="7951a-141">无效的用户的请求中传递。</span><span class="sxs-lookup"><span data-stu-id="7951a-141">The user that was passed in the request is invalid.</span></span>  <br/> |
|<span data-ttu-id="7951a-142">InvalidRequest</span><span class="sxs-lookup"><span data-stu-id="7951a-142">InvalidRequest</span></span>  <br/> |<span data-ttu-id="7951a-143">请求无效。</span><span class="sxs-lookup"><span data-stu-id="7951a-143">The request is invalid.</span></span>  <br/> |
|<span data-ttu-id="7951a-144">InvalidSetting</span><span class="sxs-lookup"><span data-stu-id="7951a-144">InvalidSetting</span></span>  <br/> |<span data-ttu-id="7951a-145">指定的设置无效。</span><span class="sxs-lookup"><span data-stu-id="7951a-145">A specified setting is invalid.</span></span>  <br/> |
|<span data-ttu-id="7951a-146">SettingIsNotAvailable</span><span class="sxs-lookup"><span data-stu-id="7951a-146">SettingIsNotAvailable</span></span>  <br/> |<span data-ttu-id="7951a-147">指定的设置不可用。</span><span class="sxs-lookup"><span data-stu-id="7951a-147">A specified setting is not available.</span></span>  <br/> |
|<span data-ttu-id="7951a-148">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="7951a-148">ServerBusy</span></span>  <br/> |<span data-ttu-id="7951a-149">服务器太忙而无法处理请求。</span><span class="sxs-lookup"><span data-stu-id="7951a-149">The server is too busy to process the request.</span></span>  <br/> |
|<span data-ttu-id="7951a-150">InvalidDomain</span><span class="sxs-lookup"><span data-stu-id="7951a-150">InvalidDomain</span></span>  <br/> |<span data-ttu-id="7951a-151">所请求的域无效。</span><span class="sxs-lookup"><span data-stu-id="7951a-151">The requested domain is not valid.</span></span>  <br/> |
|<span data-ttu-id="7951a-152">NotFederated</span><span class="sxs-lookup"><span data-stu-id="7951a-152">NotFederated</span></span>  <br/> |<span data-ttu-id="7951a-153">非联盟组织。</span><span class="sxs-lookup"><span data-stu-id="7951a-153">The organization is not federated.</span></span>  <br/> |
|<span data-ttu-id="7951a-154">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="7951a-154">InternalServerError</span></span>  <br/> |<span data-ttu-id="7951a-155">没有内部服务器错误。</span><span class="sxs-lookup"><span data-stu-id="7951a-155">There is an internal server error.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="7951a-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="7951a-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7951a-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="7951a-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7951a-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="7951a-158">Schema Name</span></span>  <br/> |<span data-ttu-id="7951a-159">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="7951a-159">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7951a-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="7951a-160">Validation File</span></span>  <br/> |<span data-ttu-id="7951a-161">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7951a-161">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7951a-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="7951a-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="7951a-163">True</span><span class="sxs-lookup"><span data-stu-id="7951a-163">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7951a-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7951a-164">See also</span></span>



[<span data-ttu-id="7951a-165">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-165">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="7951a-166">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-166">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
  
[<span data-ttu-id="7951a-167">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7951a-167">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

