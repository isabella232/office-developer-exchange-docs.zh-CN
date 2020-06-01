---
title: TargetApplicationUri （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e13c0edd-2ab1-49bb-a993-54a8db2dfbb9
description: TargetApplicationUri 元素定义目标应用程序 URI。 TargetApplicationUri 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 88968aac604b77cd057dbc69c396227a489ac9a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457086"
---
# <a name="targetapplicationuri-soap"></a><span data-ttu-id="be018-105">TargetApplicationUri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="be018-105">TargetApplicationUri (SOAP)</span></span>

<span data-ttu-id="be018-106">**TargetApplicationUri**元素定义目标应用程序 URI。</span><span class="sxs-lookup"><span data-stu-id="be018-106">The **TargetApplicationUri** element defines the target application URI.</span></span> <span data-ttu-id="be018-107">**TargetApplicationUri**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="be018-107">The **TargetApplicationUri** element is for internal use only.</span></span> <span data-ttu-id="be018-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="be018-108">This element is not used by clients.</span></span> 
  
```XML
<TargetApplicationUri/>
```

 <span data-ttu-id="be018-109">**anyURI**</span><span class="sxs-lookup"><span data-stu-id="be018-109">**anyURI**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be018-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be018-110">Attributes and elements</span></span>

<span data-ttu-id="be018-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be018-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be018-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="be018-112">Attributes</span></span>

<span data-ttu-id="be018-113">无。</span><span class="sxs-lookup"><span data-stu-id="be018-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be018-114">子元素</span><span class="sxs-lookup"><span data-stu-id="be018-114">Child elements</span></span>

<span data-ttu-id="be018-115">无。</span><span class="sxs-lookup"><span data-stu-id="be018-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be018-116">父元素</span><span class="sxs-lookup"><span data-stu-id="be018-116">Parent elements</span></span>

|<span data-ttu-id="be018-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="be018-117">**Element**</span></span>|<span data-ttu-id="be018-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="be018-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be018-119">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="be018-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="be018-120">表示单个组织的组织关系列表</span><span class="sxs-lookup"><span data-stu-id="be018-120">Represents a list of organization relationships for a single organization</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be018-121">备注</span><span class="sxs-lookup"><span data-stu-id="be018-121">Remarks</span></span>

<span data-ttu-id="be018-122">此元素定义外部组织的目标 URI。</span><span class="sxs-lookup"><span data-stu-id="be018-122">This element defines the target URI of the external organization.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be018-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="be018-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be018-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="be018-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="be018-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="be018-125">Schema Name</span></span>  <br/> |<span data-ttu-id="be018-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="be018-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="be018-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="be018-127">Validation File</span></span>  <br/> |<span data-ttu-id="be018-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="be018-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="be018-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="be018-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="be018-130">True</span><span class="sxs-lookup"><span data-stu-id="be018-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be018-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be018-131">See also</span></span>



[<span data-ttu-id="be018-132">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="be018-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

