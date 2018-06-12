---
title: GetOrganizationRelationshipSettingsRequestMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec9ad6a0-1a3c-405b-a6ea-b8dd4323c22a
description: GetOrganizationRelationshipSettingRequestMessage 元素均表示一个 GetOrganizationRelationshipSettings 操作 (SOAP) 操作请求。 GetOrganizationRelationshipSettingRequestMessage 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 357f6c75ff81fdf6b31bab15f4662d0f17fbbec0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754635"
---
# <a name="getorganizationrelationshipsettingsrequestmessage-soap"></a><span data-ttu-id="c1091-105">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1091-105">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>

<span data-ttu-id="c1091-106">**GetOrganizationRelationshipSettingRequestMessage**元素均表示一个[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="c1091-106">The **GetOrganizationRelationshipSettingRequestMessage** element represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span> <span data-ttu-id="c1091-107">**GetOrganizationRelationshipSettingRequestMessage**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="c1091-107">The **GetOrganizationRelationshipSettingRequestMessage** element is for internal use only.</span></span> <span data-ttu-id="c1091-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="c1091-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingRequestMessage>
   <Request/>
</GetOrganizationRelationshipSettingRequestMessage>
```

 <span data-ttu-id="c1091-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="c1091-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1091-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1091-110">Attributes and elements</span></span>

<span data-ttu-id="c1091-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1091-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1091-112">属性</span><span class="sxs-lookup"><span data-stu-id="c1091-112">Attributes</span></span>

<span data-ttu-id="c1091-113">无。</span><span class="sxs-lookup"><span data-stu-id="c1091-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1091-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c1091-114">Child elements</span></span>

|<span data-ttu-id="c1091-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1091-115">**Element**</span></span>|<span data-ttu-id="c1091-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1091-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1091-117">请求 (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1091-117">Request (GetOrganizationRelationship) (SOAP)</span></span>](request-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="c1091-118">代表[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="c1091-118">Represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1091-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c1091-119">Parent elements</span></span>

<span data-ttu-id="c1091-120">无。</span><span class="sxs-lookup"><span data-stu-id="c1091-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1091-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1091-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1091-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1091-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="c1091-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1091-123">Schema Name</span></span>  <br/> |<span data-ttu-id="c1091-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="c1091-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="c1091-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1091-125">Validation File</span></span>  <br/> |<span data-ttu-id="c1091-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1091-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1091-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1091-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1091-128">True</span><span class="sxs-lookup"><span data-stu-id="c1091-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1091-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1091-129">See also</span></span>



[<span data-ttu-id="c1091-130">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="c1091-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
