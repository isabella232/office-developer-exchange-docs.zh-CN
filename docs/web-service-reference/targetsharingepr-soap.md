---
title: TargetSharingEpr （SOAP）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0115a740-9264-4e57-a410-197bb39e6c81
description: TargetSharingEpr 元素表示 TargetSharingEpr 属性。 TargetSharingEpr 元素仅供内部使用。
ms.openlocfilehash: 8cb8d114ae43dfc8ad76aebe87e0e920c16477f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457079"
---
# <a name="targetsharingepr-soap"></a><span data-ttu-id="3213d-104">TargetSharingEpr （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3213d-104">TargetSharingEpr (SOAP)</span></span>
 
<span data-ttu-id="3213d-105">**TargetSharingEpr**元素表示**TargetSharingEpr**属性。</span><span class="sxs-lookup"><span data-stu-id="3213d-105">The **TargetSharingEpr** element represents the **TargetSharingEpr** property.</span></span> <span data-ttu-id="3213d-106">**TargetSharingEpr**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="3213d-106">The **TargetSharingEpr** element is for internal use only.</span></span> <span data-ttu-id="3213d-107">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="3213d-107">This element is not used by clients.</span></span> 
  
```XML
<TargetSharingEpr/>
```

<span data-ttu-id="3213d-108">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="3213d-108">**anyURI**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3213d-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3213d-109">Attributes and elements</span></span>

<span data-ttu-id="3213d-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3213d-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3213d-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="3213d-111">Attributes</span></span>

<span data-ttu-id="3213d-112">无。</span><span class="sxs-lookup"><span data-stu-id="3213d-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3213d-113">子元素</span><span class="sxs-lookup"><span data-stu-id="3213d-113">Child elements</span></span>

<span data-ttu-id="3213d-114">无。</span><span class="sxs-lookup"><span data-stu-id="3213d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3213d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="3213d-115">Parent elements</span></span>

|<span data-ttu-id="3213d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3213d-116">**Element**</span></span>|<span data-ttu-id="3213d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3213d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3213d-118">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="3213d-118">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="3213d-119">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="3213d-119">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3213d-120">备注</span><span class="sxs-lookup"><span data-stu-id="3213d-120">Remarks</span></span>

<span data-ttu-id="3213d-121">此元素指定外部组织的目标服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="3213d-121">This element specifies the URL of the target server for the external organization.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3213d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="3213d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3213d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="3213d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3213d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="3213d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="3213d-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="3213d-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3213d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="3213d-126">Validation File</span></span>  <br/> |<span data-ttu-id="3213d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3213d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3213d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="3213d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="3213d-129">True</span><span class="sxs-lookup"><span data-stu-id="3213d-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3213d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3213d-130">See also</span></span>

- [<span data-ttu-id="3213d-131">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="3213d-131">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

