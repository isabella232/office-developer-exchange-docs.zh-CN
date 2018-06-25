---
title: 响应 (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e6bbe800-3cbc-48b2-87b3-2043f575e88b
description: Response 元素包含 GetOrganizationRelationshipSettings 操作 (SOAP) 响应的信息。 响应元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 97bef9ab9f0b860e62646703c35d539b7922a65a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827174"
---
# <a name="response-getorganizationrelationship-soap"></a><span data-ttu-id="bd9e9-105">响应 (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd9e9-105">Response (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="bd9e9-106">**Response**元素包含[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)响应的信息。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-106">The **Response** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span> <span data-ttu-id="bd9e9-107">**响应**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-107">The **Response** element is for internal use only.</span></span> <span data-ttu-id="bd9e9-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="bd9e9-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="bd9e9-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd9e9-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd9e9-110">Attributes and elements</span></span>

<span data-ttu-id="bd9e9-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd9e9-112">属性</span><span class="sxs-lookup"><span data-stu-id="bd9e9-112">Attributes</span></span>

<span data-ttu-id="bd9e9-113">无。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd9e9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="bd9e9-114">Child elements</span></span>

|<span data-ttu-id="bd9e9-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd9e9-115">**Element**</span></span>|<span data-ttu-id="bd9e9-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd9e9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd9e9-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd9e9-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="bd9e9-118">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="bd9e9-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd9e9-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="bd9e9-120">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="bd9e9-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd9e9-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="bd9e9-122">代表一个与查询匹配的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-122">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd9e9-123">父元素</span><span class="sxs-lookup"><span data-stu-id="bd9e9-123">Parent elements</span></span>

<span data-ttu-id="bd9e9-124">无。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="bd9e9-125">文本值</span><span class="sxs-lookup"><span data-stu-id="bd9e9-125">Text value</span></span>

<span data-ttu-id="bd9e9-126">无。</span><span class="sxs-lookup"><span data-stu-id="bd9e9-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd9e9-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="bd9e9-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd9e9-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="bd9e9-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bd9e9-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="bd9e9-129">Schema Name</span></span>  <br/> |<span data-ttu-id="bd9e9-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="bd9e9-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bd9e9-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="bd9e9-131">Validation File</span></span>  <br/> |<span data-ttu-id="bd9e9-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bd9e9-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bd9e9-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="bd9e9-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd9e9-134">True</span><span class="sxs-lookup"><span data-stu-id="bd9e9-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd9e9-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd9e9-135">See also</span></span>



[<span data-ttu-id="bd9e9-136">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd9e9-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

