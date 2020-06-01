---
title: GetOrganizationRelationshipSettingsResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f43b817-92c2-4e04-8095-479d790f768c
description: GetOrganizationRelationshipSettingsResponse 元素包含 GetOrganizationRelationshipSettings 操作（SOAP）响应。 GetOrganizationRelationshipSettingsResponse 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 0f34fbc6577b379dd0ac379564c5e6bbd940d379
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457919"
---
# <a name="getorganizationrelationshipsettingsresponse-soap"></a><span data-ttu-id="5cd8f-105">GetOrganizationRelationshipSettingsResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="5cd8f-105">GetOrganizationRelationshipSettingsResponse (SOAP)</span></span>

<span data-ttu-id="5cd8f-106">**GetOrganizationRelationshipSettingsResponse**元素包含[GETORGANIZATIONRELATIONSHIPSETTINGS 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-106">The **GetOrganizationRelationshipSettingsResponse** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response.</span></span> <span data-ttu-id="5cd8f-107">**GetOrganizationRelationshipSettingsResponse**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-107">The **GetOrganizationRelationshipSettingsResponse** element is for internal use only.</span></span> <span data-ttu-id="5cd8f-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="5cd8f-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cd8f-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5cd8f-110">Attributes and elements</span></span>

<span data-ttu-id="5cd8f-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cd8f-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="5cd8f-112">Attributes</span></span>

<span data-ttu-id="5cd8f-113">无。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cd8f-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5cd8f-114">Child elements</span></span>

|<span data-ttu-id="5cd8f-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-115">**Element**</span></span>|<span data-ttu-id="5cd8f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5cd8f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cd8f-117">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="5cd8f-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="5cd8f-118">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="5cd8f-119">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="5cd8f-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="5cd8f-120">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="5cd8f-121">OrganizationRelationshipSettingsCollection （SOAP）</span><span class="sxs-lookup"><span data-stu-id="5cd8f-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="5cd8f-122">表示与查询匹配的组织关系的集合。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-122">Represents a collection of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5cd8f-123">父元素</span><span class="sxs-lookup"><span data-stu-id="5cd8f-123">Parent elements</span></span>

<span data-ttu-id="5cd8f-124">无。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5cd8f-125">文本值</span><span class="sxs-lookup"><span data-stu-id="5cd8f-125">Text value</span></span>

<span data-ttu-id="5cd8f-126">无。</span><span class="sxs-lookup"><span data-stu-id="5cd8f-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cd8f-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="5cd8f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cd8f-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="5cd8f-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="5cd8f-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="5cd8f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="5cd8f-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="5cd8f-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="5cd8f-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="5cd8f-131">Validation File</span></span>  <br/> |<span data-ttu-id="5cd8f-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5cd8f-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5cd8f-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="5cd8f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="5cd8f-134">True</span><span class="sxs-lookup"><span data-stu-id="5cd8f-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cd8f-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5cd8f-135">See also</span></span>



[<span data-ttu-id="5cd8f-136">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="5cd8f-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

