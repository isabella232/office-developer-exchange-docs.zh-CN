---
title: GetOrganizationRelationshipSettingsResponseMessage （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb087ac9-bac7-4635-a54f-3b115d9f5dc4
description: GetOrganizationRelationshipSettingsResponseMessage 元素定义对 GetOrganizationRelationshipSettings 操作（SOAP）请求的响应。 GetOrganizationRelationshipSettingsResponseMessage 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 806f062824e7e8d937f54cd3d38000aba42acf1e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466169"
---
# <a name="getorganizationrelationshipsettingsresponsemessage-soap"></a><span data-ttu-id="db9c8-105">GetOrganizationRelationshipSettingsResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="db9c8-105">GetOrganizationRelationshipSettingsResponseMessage (SOAP)</span></span>

<span data-ttu-id="db9c8-106">**GetOrganizationRelationshipSettingsResponseMessage**元素定义对[GETORGANIZATIONRELATIONSHIPSETTINGS 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="db9c8-106">The **GetOrganizationRelationshipSettingsResponseMessage** element defines a response to a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span> <span data-ttu-id="db9c8-107">**GetOrganizationRelationshipSettingsResponseMessage**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="db9c8-107">The **GetOrganizationRelationshipSettingsResponseMessage** element is for internal use only.</span></span> <span data-ttu-id="db9c8-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="db9c8-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponseMessage>
   <Response/>
</GetOrganizationRelationshipSettingsResponseMessage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="db9c8-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db9c8-109">Attributes and elements</span></span>

<span data-ttu-id="db9c8-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db9c8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db9c8-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="db9c8-111">Attributes</span></span>

<span data-ttu-id="db9c8-112">无。</span><span class="sxs-lookup"><span data-stu-id="db9c8-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db9c8-113">子元素</span><span class="sxs-lookup"><span data-stu-id="db9c8-113">Child elements</span></span>

|<span data-ttu-id="db9c8-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="db9c8-114">**Element**</span></span>|<span data-ttu-id="db9c8-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="db9c8-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db9c8-116">响应（GetOrganizationRelationship）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="db9c8-116">Response (GetOrganizationRelationship) (SOAP)</span></span>](response-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="db9c8-117">包含[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)响应信息。</span><span class="sxs-lookup"><span data-stu-id="db9c8-117">Contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db9c8-118">父元素</span><span class="sxs-lookup"><span data-stu-id="db9c8-118">Parent elements</span></span>

<span data-ttu-id="db9c8-119">无。</span><span class="sxs-lookup"><span data-stu-id="db9c8-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db9c8-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="db9c8-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db9c8-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="db9c8-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="db9c8-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="db9c8-122">Schema Name</span></span>  <br/> |<span data-ttu-id="db9c8-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="db9c8-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="db9c8-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="db9c8-124">Validation File</span></span>  <br/> |<span data-ttu-id="db9c8-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="db9c8-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="db9c8-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="db9c8-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="db9c8-127">True</span><span class="sxs-lookup"><span data-stu-id="db9c8-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db9c8-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db9c8-128">See also</span></span>



[<span data-ttu-id="db9c8-129">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="db9c8-129">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

