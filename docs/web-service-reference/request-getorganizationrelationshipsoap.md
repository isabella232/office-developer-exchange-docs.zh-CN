---
title: 请求 (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: 请求元素均表示一个 GetOrganizationRelationshipSettingsRequest (SOAP) 请求。 请求元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: d3ae48ca403398288b8399ede82b98322a1b3260
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827122"
---
# <a name="request-getorganizationrelationship-soap"></a><span data-ttu-id="d1601-105">请求 (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d1601-105">Request (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="d1601-106">**请求**元素均表示一个[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="d1601-106">The **Request** element represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span> <span data-ttu-id="d1601-107">仅供内部使用的**请求**的元素。</span><span class="sxs-lookup"><span data-stu-id="d1601-107">The **Request** element is for internal use only.</span></span> <span data-ttu-id="d1601-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="d1601-108">This element is not used by clients.</span></span> 
  
```XML
<Request>
   <Domains/>
</Request>
```

 <span data-ttu-id="d1601-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="d1601-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1601-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1601-110">Attributes and elements</span></span>

<span data-ttu-id="d1601-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1601-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1601-112">属性</span><span class="sxs-lookup"><span data-stu-id="d1601-112">Attributes</span></span>

<span data-ttu-id="d1601-113">无。</span><span class="sxs-lookup"><span data-stu-id="d1601-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1601-114">子元素</span><span class="sxs-lookup"><span data-stu-id="d1601-114">Child elements</span></span>

|<span data-ttu-id="d1601-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1601-115">**Element**</span></span>|<span data-ttu-id="d1601-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1601-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1601-117">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d1601-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="d1601-118">表示域的自动发现是运行以及要在查询中使用。</span><span class="sxs-lookup"><span data-stu-id="d1601-118">Represents the domains for which Autodiscover is to be run and that are to be used in a query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1601-119">父元素</span><span class="sxs-lookup"><span data-stu-id="d1601-119">Parent elements</span></span>

|<span data-ttu-id="d1601-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="d1601-120">**Element**</span></span>|<span data-ttu-id="d1601-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="d1601-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1601-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d1601-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="d1601-123">代表[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="d1601-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1601-124">文本值</span><span class="sxs-lookup"><span data-stu-id="d1601-124">Text value</span></span>

<span data-ttu-id="d1601-125">无。</span><span class="sxs-lookup"><span data-stu-id="d1601-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1601-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1601-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1601-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1601-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d1601-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1601-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d1601-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="d1601-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d1601-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1601-130">Validation File</span></span>  <br/> |<span data-ttu-id="d1601-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d1601-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1601-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1601-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1601-133">True</span><span class="sxs-lookup"><span data-stu-id="d1601-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1601-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1601-134">See also</span></span>



[<span data-ttu-id="d1601-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d1601-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md)


[<span data-ttu-id="d1601-136">使用自动发现</span><span class="sxs-lookup"><span data-stu-id="d1601-136">Working with Autodiscover</span></span>](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

