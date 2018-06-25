---
title: GetOrganizationRelationshipSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: GetOrganizationRelationshipSettingsRequest 元素均表示调用 GetOrganizationRelationshipSettings 操作 (SOAP) 操作的参数。 GetOrganizationRelationshipSettingsRequest 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 451506d53212ddca416f5b797624688f511988d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754631"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="df403-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="df403-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="df403-106">**GetOrganizationRelationshipSettingsRequest**元素均表示调用[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)操作的参数。</span><span class="sxs-lookup"><span data-stu-id="df403-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="df403-107">**GetOrganizationRelationshipSettingsRequest**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="df403-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="df403-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="df403-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="df403-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="df403-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df403-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="df403-110">Attributes and elements</span></span>

<span data-ttu-id="df403-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="df403-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df403-112">属性</span><span class="sxs-lookup"><span data-stu-id="df403-112">Attributes</span></span>

<span data-ttu-id="df403-113">无。</span><span class="sxs-lookup"><span data-stu-id="df403-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df403-114">子元素</span><span class="sxs-lookup"><span data-stu-id="df403-114">Child elements</span></span>

|<span data-ttu-id="df403-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="df403-115">**Element**</span></span>|<span data-ttu-id="df403-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="df403-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df403-117">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="df403-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="df403-118">表示域标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="df403-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="df403-119">父元素</span><span class="sxs-lookup"><span data-stu-id="df403-119">Parent elements</span></span>

<span data-ttu-id="df403-120">无。</span><span class="sxs-lookup"><span data-stu-id="df403-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df403-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="df403-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df403-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="df403-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="df403-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="df403-123">Schema Name</span></span>  <br/> |<span data-ttu-id="df403-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="df403-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="df403-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="df403-125">Validation File</span></span>  <br/> |<span data-ttu-id="df403-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="df403-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="df403-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="df403-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="df403-128">True</span><span class="sxs-lookup"><span data-stu-id="df403-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df403-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df403-129">See also</span></span>



[<span data-ttu-id="df403-130">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="df403-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

