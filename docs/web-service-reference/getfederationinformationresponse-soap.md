---
title: GetFederationInformationResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: GetFederationInformationResponse 元素包含 GetFederationInformation 操作（SOAP）响应。
ms.openlocfilehash: c9e65a2b1759946b8493b3c730f08df6fe353fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460041"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="a4839-103">GetFederationInformationResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="a4839-104">**GetFederationInformationResponse**元素包含[GETFEDERATIONINFORMATION 操作（SOAP）](getfederationinformation-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="a4839-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="a4839-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="a4839-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4839-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a4839-106">Attributes and elements</span></span>

<span data-ttu-id="a4839-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a4839-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4839-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a4839-108">Attributes</span></span>

<span data-ttu-id="a4839-109">无。</span><span class="sxs-lookup"><span data-stu-id="a4839-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4839-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a4839-110">Child elements</span></span>

|<span data-ttu-id="a4839-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a4839-111">**Element**</span></span>|<span data-ttu-id="a4839-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a4839-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4839-113">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="a4839-114">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a4839-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a4839-115">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="a4839-116">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="a4839-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a4839-117">ApplicationUri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="a4839-118">定义应用程序的位置。</span><span class="sxs-lookup"><span data-stu-id="a4839-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="a4839-119">TokenIssuers （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="a4839-120">表示安全令牌的集合，其中包含安全令牌服务标识符和终结点。</span><span class="sxs-lookup"><span data-stu-id="a4839-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="a4839-121">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a4839-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="a4839-122">代表域在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md) **GetDomainSettings**操作中返回的配置或组织在[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md) **GetFederationInformation**操作中进行了联合的域。</span><span class="sxs-lookup"><span data-stu-id="a4839-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a4839-123">父元素</span><span class="sxs-lookup"><span data-stu-id="a4839-123">Parent elements</span></span>

<span data-ttu-id="a4839-124">无。</span><span class="sxs-lookup"><span data-stu-id="a4839-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a4839-125">文本值</span><span class="sxs-lookup"><span data-stu-id="a4839-125">Text value</span></span>

<span data-ttu-id="a4839-126">无。</span><span class="sxs-lookup"><span data-stu-id="a4839-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4839-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="a4839-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4839-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="a4839-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a4839-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="a4839-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a4839-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="a4839-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a4839-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="a4839-131">Validation File</span></span>  <br/> |<span data-ttu-id="a4839-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a4839-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a4839-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="a4839-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4839-134">True</span><span class="sxs-lookup"><span data-stu-id="a4839-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4839-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a4839-135">See also</span></span>



[<span data-ttu-id="a4839-136">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a4839-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

