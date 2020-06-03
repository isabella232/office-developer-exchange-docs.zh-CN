---
title: DomainNames （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: DomainNames 元素表示域名集合。 DomainNames 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 0b425b3cd4c0e7cb2427920d61feb04010a3b123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458416"
---
# <a name="domainnames-soap"></a><span data-ttu-id="75aa5-105">DomainNames （SOAP）</span><span class="sxs-lookup"><span data-stu-id="75aa5-105">DomainNames (SOAP)</span></span>

<span data-ttu-id="75aa5-106">**DomainNames**元素表示域名集合。</span><span class="sxs-lookup"><span data-stu-id="75aa5-106">The **DomainNames** element represents the domain names collection.</span></span> <span data-ttu-id="75aa5-107">**DomainNames**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="75aa5-107">The **DomainNames** element is for internal use only.</span></span> <span data-ttu-id="75aa5-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="75aa5-108">This element is not used by clients.</span></span> 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 <span data-ttu-id="75aa5-109">**DomainNames**</span><span class="sxs-lookup"><span data-stu-id="75aa5-109">**DomainNames**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75aa5-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="75aa5-110">Attributes and elements</span></span>

<span data-ttu-id="75aa5-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="75aa5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75aa5-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="75aa5-112">Attributes</span></span>

<span data-ttu-id="75aa5-113">无。</span><span class="sxs-lookup"><span data-stu-id="75aa5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75aa5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="75aa5-114">Child elements</span></span>

|<span data-ttu-id="75aa5-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="75aa5-115">**Element**</span></span>|<span data-ttu-id="75aa5-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="75aa5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75aa5-117">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="75aa5-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="75aa5-118">表示从[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)、 [GETFEDERATIONINFORMATION 操作（Soap）](getfederationinformation-operation-soap.md)或[GetOrganizationRelationshipSettings 操作（soap）](getorganizationrelationshipsettings-operation-soap.md)返回的域的集合。</span><span class="sxs-lookup"><span data-stu-id="75aa5-118">Represents a collection of domains that are returned from the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md), or the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75aa5-119">父元素</span><span class="sxs-lookup"><span data-stu-id="75aa5-119">Parent elements</span></span>

|<span data-ttu-id="75aa5-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="75aa5-120">**Element**</span></span>|<span data-ttu-id="75aa5-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="75aa5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75aa5-122">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="75aa5-122">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="75aa5-123">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="75aa5-123">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="75aa5-124">文本值</span><span class="sxs-lookup"><span data-stu-id="75aa5-124">Text value</span></span>

<span data-ttu-id="75aa5-125">无。</span><span class="sxs-lookup"><span data-stu-id="75aa5-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75aa5-126">说明</span><span class="sxs-lookup"><span data-stu-id="75aa5-126">Remarks</span></span>

<span data-ttu-id="75aa5-127">此元素表示外部组织的 SMTP 域。</span><span class="sxs-lookup"><span data-stu-id="75aa5-127">This element represents the SMTP domains of the external organizations.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75aa5-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="75aa5-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75aa5-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="75aa5-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="75aa5-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="75aa5-130">Schema Name</span></span>  <br/> |<span data-ttu-id="75aa5-131">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="75aa5-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="75aa5-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="75aa5-132">Validation File</span></span>  <br/> |<span data-ttu-id="75aa5-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="75aa5-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="75aa5-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="75aa5-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="75aa5-135">True</span><span class="sxs-lookup"><span data-stu-id="75aa5-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75aa5-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75aa5-136">See also</span></span>

- [<span data-ttu-id="75aa5-137">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="75aa5-137">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

