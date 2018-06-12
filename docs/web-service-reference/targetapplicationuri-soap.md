---
title: TargetApplicationUri (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e13c0edd-2ab1-49bb-a993-54a8db2dfbb9
description: TargetApplicationUri 元素定义的目标应用程序 URI。 TargetApplicationUri 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: fa401d4c1e8c1460804f116d840fe21129957852
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838181"
---
# <a name="targetapplicationuri-soap"></a><span data-ttu-id="14b5c-105">TargetApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="14b5c-105">TargetApplicationUri (SOAP)</span></span>

<span data-ttu-id="14b5c-106">**TargetApplicationUri**元素定义的目标应用程序 URI。</span><span class="sxs-lookup"><span data-stu-id="14b5c-106">The **TargetApplicationUri** element defines the target application URI.</span></span> <span data-ttu-id="14b5c-107">**TargetApplicationUri**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="14b5c-107">The **TargetApplicationUri** element is for internal use only.</span></span> <span data-ttu-id="14b5c-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="14b5c-108">This element is not used by clients.</span></span> 
  
```XML
<TargetApplicationUri/>
```

 <span data-ttu-id="14b5c-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="14b5c-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14b5c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14b5c-110">Attributes and elements</span></span>

<span data-ttu-id="14b5c-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14b5c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14b5c-112">属性</span><span class="sxs-lookup"><span data-stu-id="14b5c-112">Attributes</span></span>

<span data-ttu-id="14b5c-113">无。</span><span class="sxs-lookup"><span data-stu-id="14b5c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14b5c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="14b5c-114">Child elements</span></span>

<span data-ttu-id="14b5c-115">无。</span><span class="sxs-lookup"><span data-stu-id="14b5c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="14b5c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="14b5c-116">Parent elements</span></span>

|<span data-ttu-id="14b5c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="14b5c-117">**Element**</span></span>|<span data-ttu-id="14b5c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="14b5c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14b5c-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="14b5c-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="14b5c-120">代表单个组织的组织关系的列表</span><span class="sxs-lookup"><span data-stu-id="14b5c-120">Represents a list of organization relationships for a single organization</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14b5c-121">备注</span><span class="sxs-lookup"><span data-stu-id="14b5c-121">Remarks</span></span>

<span data-ttu-id="14b5c-122">此元素定义的目标外部组织的 URI。</span><span class="sxs-lookup"><span data-stu-id="14b5c-122">This element defines the target URI of the external organization.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14b5c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="14b5c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14b5c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="14b5c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="14b5c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="14b5c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="14b5c-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="14b5c-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="14b5c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="14b5c-127">Validation File</span></span>  <br/> |<span data-ttu-id="14b5c-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="14b5c-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14b5c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="14b5c-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="14b5c-130">True</span><span class="sxs-lookup"><span data-stu-id="14b5c-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14b5c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14b5c-131">See also</span></span>



[<span data-ttu-id="14b5c-132">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="14b5c-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

