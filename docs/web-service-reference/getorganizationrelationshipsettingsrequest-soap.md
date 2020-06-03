---
title: GetOrganizationRelationshipSettingsRequest （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e8aa3b3-4bfc-40c3-b96b-9f7062b09309
description: GetOrganizationRelationshipSettingsRequest 元素表示对 GetOrganizationRelationshipSettings 操作（SOAP）操作的调用的参数。 GetOrganizationRelationshipSettingsRequest 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 053bbb8cbe2ccdcf6d544ab1fc92bb81765997e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452732"
---
# <a name="getorganizationrelationshipsettingsrequest-soap"></a><span data-ttu-id="3a8cd-105">GetOrganizationRelationshipSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3a8cd-105">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>

<span data-ttu-id="3a8cd-106">**GetOrganizationRelationshipSettingsRequest**元素表示对[GETORGANIZATIONRELATIONSHIPSETTINGS 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)操作的调用的参数。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-106">The **GetOrganizationRelationshipSettingsRequest** element represents the parameters of a call to the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation.</span></span> <span data-ttu-id="3a8cd-107">**GetOrganizationRelationshipSettingsRequest**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-107">The **GetOrganizationRelationshipSettingsRequest** element is for internal use only.</span></span> <span data-ttu-id="3a8cd-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-108">This element is not used by clients.</span></span> 
  
```XML
<GetOrganizationRelationshipSettingsRequest>
   <Domains/>
</GetOrganizationRelationshipSettingsRequest>
```

 <span data-ttu-id="3a8cd-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="3a8cd-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a8cd-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3a8cd-110">Attributes and elements</span></span>

<span data-ttu-id="3a8cd-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a8cd-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="3a8cd-112">Attributes</span></span>

<span data-ttu-id="3a8cd-113">无。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a8cd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="3a8cd-114">Child elements</span></span>

|<span data-ttu-id="3a8cd-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a8cd-115">**Element**</span></span>|<span data-ttu-id="3a8cd-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a8cd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a8cd-117">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="3a8cd-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="3a8cd-118">代表域标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-118">Represents a collection of domain identifiers.</span></span>  <br/> |
|||
   
### <a name="parent-elements"></a><span data-ttu-id="3a8cd-119">父元素</span><span class="sxs-lookup"><span data-stu-id="3a8cd-119">Parent elements</span></span>

<span data-ttu-id="3a8cd-120">无。</span><span class="sxs-lookup"><span data-stu-id="3a8cd-120">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a8cd-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="3a8cd-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a8cd-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a8cd-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3a8cd-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="3a8cd-123">Schema Name</span></span>  <br/> |<span data-ttu-id="3a8cd-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="3a8cd-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3a8cd-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="3a8cd-125">Validation File</span></span>  <br/> |<span data-ttu-id="3a8cd-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3a8cd-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a8cd-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="3a8cd-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a8cd-128">True</span><span class="sxs-lookup"><span data-stu-id="3a8cd-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a8cd-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a8cd-129">See also</span></span>



[<span data-ttu-id="3a8cd-130">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="3a8cd-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

