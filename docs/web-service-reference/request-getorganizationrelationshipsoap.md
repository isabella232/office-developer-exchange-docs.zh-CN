---
title: 请求（GetOrganizationRelationship）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: Request 元素表示 GetOrganizationRelationshipSettingsRequest （SOAP）请求。 Request 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 90ccd3579c91c916ea645e6a3b466c9de4706421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459558"
---
# <a name="request-getorganizationrelationship-soap"></a><span data-ttu-id="52745-105">请求（GetOrganizationRelationship）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="52745-105">Request (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="52745-106">**Request**元素表示[GetOrganizationRelationshipSettingsRequest （SOAP）](getorganizationrelationshipsettingsrequest-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="52745-106">The **Request** element represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span> <span data-ttu-id="52745-107">**Request**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="52745-107">The **Request** element is for internal use only.</span></span> <span data-ttu-id="52745-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="52745-108">This element is not used by clients.</span></span> 
  
```XML
<Request>
   <Domains/>
</Request>
```

 <span data-ttu-id="52745-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="52745-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52745-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52745-110">Attributes and elements</span></span>

<span data-ttu-id="52745-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52745-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52745-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="52745-112">Attributes</span></span>

<span data-ttu-id="52745-113">无。</span><span class="sxs-lookup"><span data-stu-id="52745-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52745-114">子元素</span><span class="sxs-lookup"><span data-stu-id="52745-114">Child elements</span></span>

|<span data-ttu-id="52745-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="52745-115">**Element**</span></span>|<span data-ttu-id="52745-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="52745-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52745-117">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="52745-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="52745-118">表示要在其中运行自动发现并在查询中使用的域。</span><span class="sxs-lookup"><span data-stu-id="52745-118">Represents the domains for which Autodiscover is to be run and that are to be used in a query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52745-119">父元素</span><span class="sxs-lookup"><span data-stu-id="52745-119">Parent elements</span></span>

|<span data-ttu-id="52745-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="52745-120">**Element**</span></span>|<span data-ttu-id="52745-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="52745-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52745-122">GetOrganizationRelationshipSettingsRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="52745-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="52745-123">表示[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)操作请求。</span><span class="sxs-lookup"><span data-stu-id="52745-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52745-124">文本值</span><span class="sxs-lookup"><span data-stu-id="52745-124">Text value</span></span>

<span data-ttu-id="52745-125">无。</span><span class="sxs-lookup"><span data-stu-id="52745-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52745-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="52745-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52745-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="52745-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="52745-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="52745-128">Schema Name</span></span>  <br/> |<span data-ttu-id="52745-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="52745-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="52745-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="52745-130">Validation File</span></span>  <br/> |<span data-ttu-id="52745-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52745-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52745-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="52745-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="52745-133">True</span><span class="sxs-lookup"><span data-stu-id="52745-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52745-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52745-134">See also</span></span>



[<span data-ttu-id="52745-135">GetOrganizationRelationshipSettingsRequest （SOAP）</span><span class="sxs-lookup"><span data-stu-id="52745-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md)


[<span data-ttu-id="52745-136">使用自动发现</span><span class="sxs-lookup"><span data-stu-id="52745-136">Working with Autodiscover</span></span>](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

