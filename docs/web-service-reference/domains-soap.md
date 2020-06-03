---
title: 域（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Domain 元素表示在 GetDomainSettings 操作（SOAP）中返回的域集合、组织在 GetFederationInformation 操作（SOAP）中进行了联合的域，或者由 GetOrganizationRelationshipSettings 操作（SOAP）返回的具有组织关系关系的域。
ms.openlocfilehash: c56fb72841776c0060c1300b52b2f6a06b1ec0ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526303"
---
# <a name="domains-soap"></a><span data-ttu-id="ba5a9-103">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-103">Domains (SOAP)</span></span>

<span data-ttu-id="ba5a9-104">Domain**元素表示**在[GETDOMAINSETTINGS 操作（soap）](getdomainsettings-operation-soap.md)中返回的域集合、组织在[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md)中进行了联合的域，或者由[GetOrganizationRelationshipSettings 操作（soap）](getorganizationrelationshipsettings-operation-soap.md)返回的具有组织关系关系的域。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-104">The **Domains** element represents the domain collection that is returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), the domains that the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the domains with an organization relationship as returned by [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 <span data-ttu-id="ba5a9-105">**域**</span><span class="sxs-lookup"><span data-stu-id="ba5a9-105">**Domains**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba5a9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba5a9-106">Attributes and elements</span></span>

<span data-ttu-id="ba5a9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba5a9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ba5a9-108">Attributes</span></span>

<span data-ttu-id="ba5a9-109">无。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba5a9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ba5a9-110">Child elements</span></span>

|<span data-ttu-id="ba5a9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba5a9-111">**Element**</span></span>|<span data-ttu-id="ba5a9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba5a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba5a9-113">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-113">Domain (SOAP)</span></span>](domain-soap.md) <br/> |<span data-ttu-id="ba5a9-114">代表单个域。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-114">Represents a single domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba5a9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ba5a9-115">Parent elements</span></span>

|<span data-ttu-id="ba5a9-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba5a9-116">**Element**</span></span>|<span data-ttu-id="ba5a9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba5a9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba5a9-118">GetDomainSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-118">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="ba5a9-119">表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-119">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
|[<span data-ttu-id="ba5a9-120">响应（GetFederationInformation）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-120">Response (GetFederationInformation) (SOAP)</span></span>](response-getfederationinformationsoap.md) <br/> |<span data-ttu-id="ba5a9-121">包含[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)响应信息。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-121">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response information.</span></span>  <br/> |
|[<span data-ttu-id="ba5a9-122">GetOrganizationRelationshipSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-122">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md) <br/> |<span data-ttu-id="ba5a9-123">表示[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba5a9-124">文本值</span><span class="sxs-lookup"><span data-stu-id="ba5a9-124">Text value</span></span>

<span data-ttu-id="ba5a9-125">无。</span><span class="sxs-lookup"><span data-stu-id="ba5a9-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba5a9-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba5a9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba5a9-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba5a9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ba5a9-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba5a9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ba5a9-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ba5a9-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ba5a9-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba5a9-130">Validation File</span></span>  <br/> |<span data-ttu-id="ba5a9-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba5a9-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba5a9-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba5a9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba5a9-133">True</span><span class="sxs-lookup"><span data-stu-id="ba5a9-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba5a9-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba5a9-134">See also</span></span>

- [<span data-ttu-id="ba5a9-135">GetDomainSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-135">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md)  
- [<span data-ttu-id="ba5a9-136">GetFederationInformationResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ba5a9-136">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md)

