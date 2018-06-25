---
title: 响应 (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Response 元素包含 GetFederationInformation 操作 (SOAP) 响应的信息。
ms.openlocfilehash: 946cba56d7503a0e20ec59640f4f1258c00a844e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827171"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="f168b-103">响应 (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="f168b-104">**Response**元素包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应的信息。</span><span class="sxs-lookup"><span data-stu-id="f168b-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="f168b-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="f168b-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f168b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f168b-106">Attributes and elements</span></span>

<span data-ttu-id="f168b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f168b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f168b-108">属性</span><span class="sxs-lookup"><span data-stu-id="f168b-108">Attributes</span></span>

<span data-ttu-id="f168b-109">无。</span><span class="sxs-lookup"><span data-stu-id="f168b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f168b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f168b-110">Child elements</span></span>

|<span data-ttu-id="f168b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f168b-111">**Element**</span></span>|<span data-ttu-id="f168b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f168b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f168b-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="f168b-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f168b-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="f168b-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="f168b-116">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="f168b-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="f168b-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="f168b-118">定义应用程序的位置。</span><span class="sxs-lookup"><span data-stu-id="f168b-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="f168b-119">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="f168b-120">代表为其配置返回在[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)或组织具有联合[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中的域的域集合。</span><span class="sxs-lookup"><span data-stu-id="f168b-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f168b-121">父元素</span><span class="sxs-lookup"><span data-stu-id="f168b-121">Parent elements</span></span>

|<span data-ttu-id="f168b-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="f168b-122">**Element**</span></span>|<span data-ttu-id="f168b-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="f168b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f168b-124">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="f168b-125">定义[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f168b-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f168b-126">文本值</span><span class="sxs-lookup"><span data-stu-id="f168b-126">Text value</span></span>

<span data-ttu-id="f168b-127">无。</span><span class="sxs-lookup"><span data-stu-id="f168b-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f168b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="f168b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f168b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="f168b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f168b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="f168b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f168b-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f168b-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f168b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="f168b-132">Validation File</span></span>  <br/> |<span data-ttu-id="f168b-133">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f168b-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f168b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="f168b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f168b-135">True</span><span class="sxs-lookup"><span data-stu-id="f168b-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f168b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f168b-136">See also</span></span>



[<span data-ttu-id="f168b-137">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f168b-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

