---
title: TargetAutodiscoverEpr (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fdb9cc7a-cf0a-431b-9f6f-5f1db1792db7
description: TargetAutodiscoverEpr 元素均表示 TargetAutodiscoverEpr 属性。 TargetAutodiscoverEpr 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 0b28444727e21a98925b6d1062bcbbac62c68981
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838182"
---
# <a name="targetautodiscoverepr-soap"></a><span data-ttu-id="7ba9f-105">TargetAutodiscoverEpr (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ba9f-105">TargetAutodiscoverEpr (SOAP)</span></span>

<span data-ttu-id="7ba9f-106">**TargetAutodiscoverEpr**元素均表示**TargetAutodiscoverEpr**属性。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-106">The **TargetAutodiscoverEpr** element represents the **TargetAutodiscoverEpr** property.</span></span> <span data-ttu-id="7ba9f-107">**TargetAutodiscoverEpr**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-107">The **TargetAutodiscoverEpr** element is for internal use only.</span></span> <span data-ttu-id="7ba9f-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-108">This element is not used by clients.</span></span> 
  
```XML
<TargetAutodiscoverEpr/>
```

 <span data-ttu-id="7ba9f-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="7ba9f-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ba9f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7ba9f-110">Attributes and elements</span></span>

<span data-ttu-id="7ba9f-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ba9f-112">属性</span><span class="sxs-lookup"><span data-stu-id="7ba9f-112">Attributes</span></span>

<span data-ttu-id="7ba9f-113">无。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ba9f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7ba9f-114">Child elements</span></span>

<span data-ttu-id="7ba9f-115">无。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ba9f-116">父元素</span><span class="sxs-lookup"><span data-stu-id="7ba9f-116">Parent elements</span></span>

|<span data-ttu-id="7ba9f-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7ba9f-117">**Element**</span></span>|<span data-ttu-id="7ba9f-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7ba9f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ba9f-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ba9f-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="7ba9f-120">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ba9f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="7ba9f-121">Text value</span></span>

<span data-ttu-id="7ba9f-122">此元素的文本值是组织关系的统一资源标识符 (URI)。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-122">The text value for this element is a uniform resource identifier (URI) for the organization relationship.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ba9f-123">注解</span><span class="sxs-lookup"><span data-stu-id="7ba9f-123">Remarks</span></span>

<span data-ttu-id="7ba9f-124">此元素指定的服务器的外部组织的自动发现 URL。</span><span class="sxs-lookup"><span data-stu-id="7ba9f-124">This element specifies the Autodiscover URL of the server for the external organization.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7ba9f-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="7ba9f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ba9f-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="7ba9f-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7ba9f-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="7ba9f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="7ba9f-128">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="7ba9f-128">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7ba9f-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="7ba9f-129">Validation File</span></span>  <br/> |<span data-ttu-id="7ba9f-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7ba9f-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7ba9f-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="7ba9f-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="7ba9f-132">True</span><span class="sxs-lookup"><span data-stu-id="7ba9f-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ba9f-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7ba9f-133">See also</span></span>



[<span data-ttu-id="7ba9f-134">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7ba9f-134">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

