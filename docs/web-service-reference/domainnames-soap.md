---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: DomainNames 元素均表示域 names 集合。 DomainNames 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 45d256f3d5a57028a04572ad67d4be0786ca39e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753973"
---
# <a name="domainnames-soap"></a><span data-ttu-id="1ce5e-105">DomainNames (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1ce5e-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="1ce5e-106">**DomainNames**元素均表示域 names 集合。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="1ce5e-107">**DomainNames**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="1ce5e-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="1ce5e-109">**DomainNames**</span><span class="sxs-lookup"><span data-stu-id="1ce5e-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ce5e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1ce5e-110">Attributes and elements</span></span>

<span data-ttu-id="1ce5e-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ce5e-112">属性</span><span class="sxs-lookup"><span data-stu-id="1ce5e-112">Attributes</span></span>

<span data-ttu-id="1ce5e-113">无。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ce5e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="1ce5e-114">Child elements</span></span>

|<span data-ttu-id="1ce5e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ce5e-115">**Element**</span></span>|<span data-ttu-id="1ce5e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ce5e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ce5e-117">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1ce5e-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="1ce5e-118">表示从[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)、 [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)或[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)返回的域的集合。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ce5e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1ce5e-119">Parent elements</span></span>

|<span data-ttu-id="1ce5e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="1ce5e-120">**Element**</span></span>|<span data-ttu-id="1ce5e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1ce5e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ce5e-122">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1ce5e-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="1ce5e-123">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ce5e-124">文本值</span><span class="sxs-lookup"><span data-stu-id="1ce5e-124">Text value</span></span>

<span data-ttu-id="1ce5e-125">无。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ce5e-126">注解</span><span class="sxs-lookup"><span data-stu-id="1ce5e-126">Remarks</span></span>

<span data-ttu-id="1ce5e-127">此元素表示的 SMTP 域的外部组织。</span><span class="sxs-lookup"><span data-stu-id="1ce5e-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ce5e-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="1ce5e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ce5e-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="1ce5e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="1ce5e-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="1ce5e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="1ce5e-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="1ce5e-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="1ce5e-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="1ce5e-132">Validation File</span></span>  <br/> |<span data-ttu-id="1ce5e-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1ce5e-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1ce5e-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="1ce5e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ce5e-135">True</span><span class="sxs-lookup"><span data-stu-id="1ce5e-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ce5e-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1ce5e-136">See also</span></span>

- [<span data-ttu-id="1ce5e-137">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="1ce5e-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

