---
title: FreeBusyAccessLevel （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a287b9c3-7fb6-4f2f-a8dc-15d4bc32394c
description: FreeBusyAccessLevel 元素表示 FreeBusyAccessLevel 属性。 FreeBusyAccessLevel 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 7ff0c6c72f924a2f1f8eee0dd152d19f6a8745e9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460048"
---
# <a name="freebusyaccesslevel-soap"></a><span data-ttu-id="84d31-105">FreeBusyAccessLevel （SOAP）</span><span class="sxs-lookup"><span data-stu-id="84d31-105">FreeBusyAccessLevel (SOAP)</span></span>

<span data-ttu-id="84d31-106">**FreeBusyAccessLevel**元素表示**FreeBusyAccessLevel**属性。</span><span class="sxs-lookup"><span data-stu-id="84d31-106">The **FreeBusyAccessLevel** element represents the **FreeBusyAccessLevel** property.</span></span> <span data-ttu-id="84d31-107">**FreeBusyAccessLevel**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="84d31-107">The **FreeBusyAccessLevel** element is for internal use only.</span></span> <span data-ttu-id="84d31-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="84d31-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessLevel/>
```

 <span data-ttu-id="84d31-109">**string**</span><span class="sxs-lookup"><span data-stu-id="84d31-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84d31-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84d31-110">Attributes and elements</span></span>

<span data-ttu-id="84d31-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84d31-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84d31-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="84d31-112">Attributes</span></span>

<span data-ttu-id="84d31-113">无。</span><span class="sxs-lookup"><span data-stu-id="84d31-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84d31-114">子元素</span><span class="sxs-lookup"><span data-stu-id="84d31-114">Child elements</span></span>

<span data-ttu-id="84d31-115">无。</span><span class="sxs-lookup"><span data-stu-id="84d31-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="84d31-116">父元素</span><span class="sxs-lookup"><span data-stu-id="84d31-116">Parent elements</span></span>

|<span data-ttu-id="84d31-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="84d31-117">**Element**</span></span>|<span data-ttu-id="84d31-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="84d31-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84d31-119">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="84d31-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="84d31-120">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="84d31-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84d31-121">备注</span><span class="sxs-lookup"><span data-stu-id="84d31-121">Remarks</span></span>

<span data-ttu-id="84d31-122">此元素指定响应中将返回的最大忙/闲详细信息量，并指示外部共享的忙/闲数据的级别。</span><span class="sxs-lookup"><span data-stu-id="84d31-122">This element specifies the maximum amount of free/busy detail that will be returned in the response and indicates the level of free/busy data that is externally shared.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="84d31-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="84d31-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84d31-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="84d31-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="84d31-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="84d31-125">Schema Name</span></span>  <br/> |<span data-ttu-id="84d31-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="84d31-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="84d31-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="84d31-127">Validation File</span></span>  <br/> |<span data-ttu-id="84d31-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="84d31-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="84d31-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="84d31-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="84d31-130">True</span><span class="sxs-lookup"><span data-stu-id="84d31-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84d31-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84d31-131">See also</span></span>



[<span data-ttu-id="84d31-132">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="84d31-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

