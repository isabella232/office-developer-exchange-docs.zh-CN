---
title: FreeBusyAccessLevel (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: FreeBusyAccessLevel 元素均表示 FreeBusyAccessLevel 属性。 FreeBusyAccessLevel 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: c978608982a2795af1683b4b2121435a02149935
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754424"
---
# <a name="freebusyaccesslevel-soap"></a><span data-ttu-id="f2830-105">FreeBusyAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2830-105">FreeBusyAccessLevel (SOAP)</span></span>

<span data-ttu-id="f2830-106">**FreeBusyAccessLevel**元素均表示**FreeBusyAccessLevel**属性。</span><span class="sxs-lookup"><span data-stu-id="f2830-106">The **FreeBusyAccessLevel** element represents the **FreeBusyAccessLevel** property.</span></span> <span data-ttu-id="f2830-107">**FreeBusyAccessLevel**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="f2830-107">The **FreeBusyAccessLevel** element is for internal use only.</span></span> <span data-ttu-id="f2830-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="f2830-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessLevel/>
```

 <span data-ttu-id="f2830-109">**string**</span><span class="sxs-lookup"><span data-stu-id="f2830-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2830-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2830-110">Attributes and elements</span></span>

<span data-ttu-id="f2830-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2830-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2830-112">属性</span><span class="sxs-lookup"><span data-stu-id="f2830-112">Attributes</span></span>

<span data-ttu-id="f2830-113">无。</span><span class="sxs-lookup"><span data-stu-id="f2830-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2830-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f2830-114">Child elements</span></span>

<span data-ttu-id="f2830-115">无。</span><span class="sxs-lookup"><span data-stu-id="f2830-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2830-116">父元素</span><span class="sxs-lookup"><span data-stu-id="f2830-116">Parent elements</span></span>

|<span data-ttu-id="f2830-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2830-117">**Element**</span></span>|<span data-ttu-id="f2830-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2830-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2830-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2830-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="f2830-120">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="f2830-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2830-121">注解</span><span class="sxs-lookup"><span data-stu-id="f2830-121">Remarks</span></span>

<span data-ttu-id="f2830-122">此元素指定的忙/闲信息的详细信息，将在响应中返回的最大，并指示外部共享的忙/闲数据的级别。</span><span class="sxs-lookup"><span data-stu-id="f2830-122">This element specifies the maximum amount of free/busy detail that will be returned in the response and indicates the level of free/busy data that is externally shared.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f2830-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2830-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2830-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2830-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f2830-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2830-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f2830-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f2830-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f2830-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2830-127">Validation File</span></span>  <br/> |<span data-ttu-id="f2830-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2830-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2830-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2830-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2830-130">True</span><span class="sxs-lookup"><span data-stu-id="f2830-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2830-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2830-131">See also</span></span>



[<span data-ttu-id="f2830-132">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2830-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

