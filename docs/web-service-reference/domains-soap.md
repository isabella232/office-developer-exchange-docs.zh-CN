---
title: 域 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: 域元素均表示返回 GetDomainSettings 操作 (SOAP)、 组织具有联合 GetFederationInformation 操作 (SOAP) 中的域或与组织关系作为域中的域集合返回由 GetOrganizationRelationshipSettings 操作 (SOAP)。
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753982"
---
# <a name="domains-soap"></a><span data-ttu-id="83f26-103">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-103">Domains (SOAP)</span></span>

<span data-ttu-id="83f26-104">**域**元素均表示返回[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)、 组织已在[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中，联合域或域中的域集合返回由[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)的组织关系。</span><span class="sxs-lookup"><span data-stu-id="83f26-104">The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 <span data-ttu-id="83f26-105">**域**</span><span class="sxs-lookup"><span data-stu-id="83f26-105">**Domains**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83f26-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="83f26-106">Attributes and elements</span></span>

<span data-ttu-id="83f26-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="83f26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83f26-108">属性</span><span class="sxs-lookup"><span data-stu-id="83f26-108">Attributes</span></span>

<span data-ttu-id="83f26-109">无。</span><span class="sxs-lookup"><span data-stu-id="83f26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83f26-110">子元素</span><span class="sxs-lookup"><span data-stu-id="83f26-110">Child elements</span></span>

|<span data-ttu-id="83f26-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="83f26-111">**Element**</span></span>|<span data-ttu-id="83f26-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="83f26-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83f26-113">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-113">Domain (SOAP)</span></span>](domain-soap.md) <br/> |<span data-ttu-id="83f26-114">代表单个域。</span><span class="sxs-lookup"><span data-stu-id="83f26-114">Represents a single domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83f26-115">父元素</span><span class="sxs-lookup"><span data-stu-id="83f26-115">Parent elements</span></span>

|<span data-ttu-id="83f26-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="83f26-116">**Element**</span></span>|<span data-ttu-id="83f26-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="83f26-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83f26-118">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-118">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="83f26-119">代表[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="83f26-119">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="83f26-120">响应 (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-120">Response (GetFederationInformation) (SOAP)</span></span>](response-getfederationinformationsoap.md) <br/> |<span data-ttu-id="83f26-121">包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应的信息。</span><span class="sxs-lookup"><span data-stu-id="83f26-121">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span>  <br/> |
|[<span data-ttu-id="83f26-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md) <br/> |<span data-ttu-id="83f26-123">代表[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="83f26-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="83f26-124">文本值</span><span class="sxs-lookup"><span data-stu-id="83f26-124">Text value</span></span>

<span data-ttu-id="83f26-125">无。</span><span class="sxs-lookup"><span data-stu-id="83f26-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83f26-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="83f26-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83f26-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="83f26-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="83f26-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="83f26-128">Schema Name</span></span>  <br/> |<span data-ttu-id="83f26-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="83f26-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="83f26-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="83f26-130">Validation File</span></span>  <br/> |<span data-ttu-id="83f26-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="83f26-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="83f26-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="83f26-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="83f26-133">True</span><span class="sxs-lookup"><span data-stu-id="83f26-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83f26-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83f26-134">See also</span></span>

- [<span data-ttu-id="83f26-135">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-135">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md)  
- [<span data-ttu-id="83f26-136">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="83f26-136">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md)

