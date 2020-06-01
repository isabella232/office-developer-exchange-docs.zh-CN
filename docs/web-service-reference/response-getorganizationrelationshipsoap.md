---
title: 响应（GetOrganizationRelationship）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e6bbe800-3cbc-48b2-87b3-2043f575e88b
description: Response 元素包含 GetOrganizationRelationshipSettings 操作（SOAP）响应信息。 Response 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 55f8cd549f40b780b2e7438634a851a2c3854f40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467940"
---
# <a name="response-getorganizationrelationship-soap"></a><span data-ttu-id="60300-105">响应（GetOrganizationRelationship）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="60300-105">Response (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="60300-106">**Response**元素包含[GETORGANIZATIONRELATIONSHIPSETTINGS 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)响应信息。</span><span class="sxs-lookup"><span data-stu-id="60300-106">The **Response** element contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span> <span data-ttu-id="60300-107">**Response**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="60300-107">The **Response** element is for internal use only.</span></span> <span data-ttu-id="60300-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="60300-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <OrganizationRelationshipSettingsCollection/>
</GetOrganizationRelationshipSettingResponse>
```

 <span data-ttu-id="60300-109">**GetOrganizationRelationshipSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="60300-109">**GetOrganizationRelationshipSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60300-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="60300-110">Attributes and elements</span></span>

<span data-ttu-id="60300-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="60300-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60300-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="60300-112">Attributes</span></span>

<span data-ttu-id="60300-113">无。</span><span class="sxs-lookup"><span data-stu-id="60300-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60300-114">子元素</span><span class="sxs-lookup"><span data-stu-id="60300-114">Child elements</span></span>

|<span data-ttu-id="60300-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="60300-115">**Element**</span></span>|<span data-ttu-id="60300-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="60300-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60300-117">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="60300-117">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="60300-118">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="60300-118">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="60300-119">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="60300-119">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="60300-120">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="60300-120">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="60300-121">OrganizationRelationshipSettingsCollection （SOAP）</span><span class="sxs-lookup"><span data-stu-id="60300-121">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="60300-122">表示与查询匹配的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="60300-122">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="60300-123">父元素</span><span class="sxs-lookup"><span data-stu-id="60300-123">Parent elements</span></span>

<span data-ttu-id="60300-124">无。</span><span class="sxs-lookup"><span data-stu-id="60300-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="60300-125">文本值</span><span class="sxs-lookup"><span data-stu-id="60300-125">Text value</span></span>

<span data-ttu-id="60300-126">无。</span><span class="sxs-lookup"><span data-stu-id="60300-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60300-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="60300-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60300-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="60300-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="60300-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="60300-129">Schema Name</span></span>  <br/> |<span data-ttu-id="60300-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="60300-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="60300-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="60300-131">Validation File</span></span>  <br/> |<span data-ttu-id="60300-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="60300-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="60300-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="60300-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="60300-134">True</span><span class="sxs-lookup"><span data-stu-id="60300-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60300-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="60300-135">See also</span></span>



[<span data-ttu-id="60300-136">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="60300-136">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

