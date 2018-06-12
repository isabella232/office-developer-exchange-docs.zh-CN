---
title: GetOrganizationRelationshipSettingsResponseMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fb087ac9-bac7-4635-a54f-3b115d9f5dc4
description: GetOrganizationRelationshipSettingsResponseMessage 元素定义 GetOrganizationRelationshipSettings 操作 (SOAP) 请求的响应。 GetOrganizationRelationshipSettingsResponseMessage 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 40a61616acba70d870d0f2ad32de8b828ea64c63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754641"
---
# <a name="getorganizationrelationshipsettingsresponsemessage-soap"></a><span data-ttu-id="0b561-105">GetOrganizationRelationshipSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0b561-105">GetOrganizationRelationshipSettingsResponseMessage (SOAP)</span></span>

<span data-ttu-id="0b561-106">**GetOrganizationRelationshipSettingsResponseMessage**元素定义[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0b561-106">The **GetOrganizationRelationshipSettingsResponseMessage** element defines a response to a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) request.</span></span> <span data-ttu-id="0b561-107">**GetOrganizationRelationshipSettingsResponseMessage**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="0b561-107">The **GetOrganizationRelationshipSettingsResponseMessage** element is for internal use only.</span></span> <span data-ttu-id="0b561-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="0b561-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsResponseMessage>
   <Response/>
</GetOrganizationRelationshipSettingsResponseMessage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0b561-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0b561-109">Attributes and elements</span></span>

<span data-ttu-id="0b561-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0b561-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b561-111">属性</span><span class="sxs-lookup"><span data-stu-id="0b561-111">Attributes</span></span>

<span data-ttu-id="0b561-112">无。</span><span class="sxs-lookup"><span data-stu-id="0b561-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b561-113">子元素</span><span class="sxs-lookup"><span data-stu-id="0b561-113">Child elements</span></span>

|<span data-ttu-id="0b561-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="0b561-114">**Element**</span></span>|<span data-ttu-id="0b561-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="0b561-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b561-116">响应 (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0b561-116">Response (GetOrganizationRelationship) (SOAP)</span></span>](response-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="0b561-117">包含[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)响应的信息。</span><span class="sxs-lookup"><span data-stu-id="0b561-117">Contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0b561-118">父元素</span><span class="sxs-lookup"><span data-stu-id="0b561-118">Parent elements</span></span>

<span data-ttu-id="0b561-119">无。</span><span class="sxs-lookup"><span data-stu-id="0b561-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b561-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="0b561-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b561-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="0b561-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0b561-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="0b561-122">Schema Name</span></span>  <br/> |<span data-ttu-id="0b561-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="0b561-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0b561-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="0b561-124">Validation File</span></span>  <br/> |<span data-ttu-id="0b561-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0b561-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0b561-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="0b561-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="0b561-127">True</span><span class="sxs-lookup"><span data-stu-id="0b561-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b561-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0b561-128">See also</span></span>



[<span data-ttu-id="0b561-129">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0b561-129">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

