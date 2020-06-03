---
title: 响应（GetFederationInformation）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Response 元素包含 GetFederationInformation 操作（SOAP）响应信息。
ms.openlocfilehash: 0b9a2c518b968faa6ef86b7c1f544eac40f8e5c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530584"
---
# <a name="response-getfederationinformation-soap"></a><span data-ttu-id="4d0db-103">响应（GetFederationInformation）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-103">Response (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="4d0db-104">**Response**元素包含[GETFEDERATIONINFORMATION 操作（SOAP）](getfederationinformation-operation-soap.md)响应信息。</span><span class="sxs-lookup"><span data-stu-id="4d0db-104">The **Response** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span> 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 <span data-ttu-id="4d0db-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="4d0db-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d0db-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d0db-106">Attributes and elements</span></span>

<span data-ttu-id="4d0db-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d0db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d0db-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4d0db-108">Attributes</span></span>

<span data-ttu-id="4d0db-109">无。</span><span class="sxs-lookup"><span data-stu-id="4d0db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d0db-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4d0db-110">Child elements</span></span>

|<span data-ttu-id="4d0db-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d0db-111">**Element**</span></span>|<span data-ttu-id="4d0db-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d0db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d0db-113">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="4d0db-114">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="4d0db-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="4d0db-115">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="4d0db-116">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="4d0db-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="4d0db-117">ApplicationUri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="4d0db-118">定义应用程序的位置。</span><span class="sxs-lookup"><span data-stu-id="4d0db-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="4d0db-119">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-119">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="4d0db-120">代表域集合在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)中返回的配置，或组织在[GETFEDERATIONINFORMATION 操作（soap）](getfederationinformation-operation-soap.md)中联合的域。</span><span class="sxs-lookup"><span data-stu-id="4d0db-120">Represents the domain collection the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), or the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4d0db-121">父元素</span><span class="sxs-lookup"><span data-stu-id="4d0db-121">Parent elements</span></span>

|<span data-ttu-id="4d0db-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d0db-122">**Element**</span></span>|<span data-ttu-id="4d0db-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d0db-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d0db-124">GetFederationInformationResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="4d0db-124">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md) <br/> |<span data-ttu-id="4d0db-125">定义对[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="4d0db-125">Defines a response to a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4d0db-126">文本值</span><span class="sxs-lookup"><span data-stu-id="4d0db-126">Text value</span></span>

<span data-ttu-id="4d0db-127">无。</span><span class="sxs-lookup"><span data-stu-id="4d0db-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d0db-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d0db-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d0db-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d0db-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4d0db-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d0db-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4d0db-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="4d0db-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4d0db-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d0db-132">Validation File</span></span>  <br/> |<span data-ttu-id="4d0db-133">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="4d0db-133">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4d0db-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d0db-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d0db-135">True</span><span class="sxs-lookup"><span data-stu-id="4d0db-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d0db-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d0db-136">See also</span></span>



[<span data-ttu-id="4d0db-137">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4d0db-137">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

