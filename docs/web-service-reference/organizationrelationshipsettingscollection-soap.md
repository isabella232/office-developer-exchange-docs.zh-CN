---
title: OrganizationRelationshipSettingsCollection （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33456abf-a1b6-46da-a864-3ec8af2780de
description: OrganizationRelationshipSettingsCollection 元素表示与查询匹配的组织关系的列表。 OrganizationRelationshipSettingsCollection 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 52f84d932e74393a844f5f55fbd1d09bfb0a5d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462421"
---
# <a name="organizationrelationshipsettingscollection-soap"></a><span data-ttu-id="a672e-105">OrganizationRelationshipSettingsCollection （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a672e-105">OrganizationRelationshipSettingsCollection (SOAP)</span></span>

<span data-ttu-id="a672e-106">**OrganizationRelationshipSettingsCollection**元素表示与查询匹配的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="a672e-106">The **OrganizationRelationshipSettingsCollection** element represents a list of organization relationships that match the query.</span></span> <span data-ttu-id="a672e-107">**OrganizationRelationshipSettingsCollection**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="a672e-107">The **OrganizationRelationshipSettingsCollection** element is for internal use only.</span></span> <span data-ttu-id="a672e-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="a672e-108">This element is not used by clients.</span></span> 
  
```XML
<OrganizationRelationshipSettingsCollection>
   <OrganizationRelationshipSettings/>
</OrganizationRelationshipSettingsCollection>
```

 <span data-ttu-id="a672e-109">**OrganizationRelationshipSettingsCollection**</span><span class="sxs-lookup"><span data-stu-id="a672e-109">**OrganizationRelationshipSettingsCollection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a672e-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a672e-110">Attributes and elements</span></span>

<span data-ttu-id="a672e-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a672e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a672e-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="a672e-112">Attributes</span></span>

<span data-ttu-id="a672e-113">无。</span><span class="sxs-lookup"><span data-stu-id="a672e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a672e-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a672e-114">Child elements</span></span>

|<span data-ttu-id="a672e-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="a672e-115">**Element**</span></span>|<span data-ttu-id="a672e-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="a672e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a672e-117">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a672e-117">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="a672e-118">表示所选组织和 SMTP 地址的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="a672e-118">Represents the list of organization relationships for the selected organization and SMTP addresses.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a672e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a672e-119">Parent elements</span></span>

|<span data-ttu-id="a672e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="a672e-120">**Element**</span></span>|<span data-ttu-id="a672e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a672e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a672e-122">响应（GetOrganizationRelationship）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a672e-122">Response (GetOrganizationRelationship) (SOAP)</span></span>](response-getorganizationrelationshipsoap.md) <br/> |<span data-ttu-id="a672e-123">包含[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)响应信息。</span><span class="sxs-lookup"><span data-stu-id="a672e-123">Contains the [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) response information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a672e-124">文本值</span><span class="sxs-lookup"><span data-stu-id="a672e-124">Text value</span></span>

<span data-ttu-id="a672e-125">无。</span><span class="sxs-lookup"><span data-stu-id="a672e-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a672e-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="a672e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a672e-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="a672e-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a672e-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="a672e-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a672e-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="a672e-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a672e-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="a672e-130">Validation File</span></span>  <br/> |<span data-ttu-id="a672e-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a672e-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a672e-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="a672e-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a672e-133">True</span><span class="sxs-lookup"><span data-stu-id="a672e-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a672e-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a672e-134">See also</span></span>



[<span data-ttu-id="a672e-135">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a672e-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

