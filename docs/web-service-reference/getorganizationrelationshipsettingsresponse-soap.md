---
title: GetOrganizationRelationshipSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: GetOrganizationRelationshipSettingsResponse 元素包含 GetOrganizationRelationshipSettings 操作 (SOAP) 响应。 GetOrganizationRelationshipSettingsResponse 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 907113df2186a93345c6e0bc7dd470909508bd38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754634"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a><span data-ttu-id="cf5a2-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf5a2-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span></span>

<span data-ttu-id="cf5a2-106">**GetOrganizationRelationshipSettingsResponse**元素包含[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-106">The **GetOrganizationRelationshipSettingsResponse** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response.</span></span> <span data-ttu-id="cf5a2-107">**GetOrganizationRelationshipSettingsResponse**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-107">The **GetOrganizationRelationshipSettingsResponse** element is for internal use only.</span></span> <span data-ttu-id="cf5a2-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="cf5a2-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="cf5a2-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf5a2-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf5a2-110">Attributes and elements</span></span>

<span data-ttu-id="cf5a2-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf5a2-112">属性</span><span class="sxs-lookup"><span data-stu-id="cf5a2-112">Attributes</span></span>

<span data-ttu-id="cf5a2-113">无。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf5a2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="cf5a2-114">Child elements</span></span>

|<span data-ttu-id="cf5a2-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf5a2-115">**Element**</span></span>|<span data-ttu-id="cf5a2-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf5a2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf5a2-117">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf5a2-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="cf5a2-118">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="cf5a2-119">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf5a2-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="cf5a2-120">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="cf5a2-121">OrganizationRelationshipSettingsCollection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf5a2-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="cf5a2-122">表示与查询匹配的组织关系的集合。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-122">Represents a collection of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf5a2-123">父元素</span><span class="sxs-lookup"><span data-stu-id="cf5a2-123">Parent elements</span></span>

<span data-ttu-id="cf5a2-124">无。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cf5a2-125">文本值</span><span class="sxs-lookup"><span data-stu-id="cf5a2-125">Text value</span></span>

<span data-ttu-id="cf5a2-126">无。</span><span class="sxs-lookup"><span data-stu-id="cf5a2-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf5a2-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf5a2-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf5a2-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf5a2-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cf5a2-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf5a2-129">Schema Name</span></span>  <br/> |<span data-ttu-id="cf5a2-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="cf5a2-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cf5a2-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf5a2-131">Validation File</span></span>  <br/> |<span data-ttu-id="cf5a2-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf5a2-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf5a2-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf5a2-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf5a2-134">True</span><span class="sxs-lookup"><span data-stu-id="cf5a2-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf5a2-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf5a2-135">See also</span></span>



[<span data-ttu-id="cf5a2-136">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf5a2-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

