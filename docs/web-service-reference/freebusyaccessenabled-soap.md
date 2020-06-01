---
title: FreeBusyAccessEnabled （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: FreeBusyAccessEnabled 元素表示 FreeBusyAccessEnabled （）标志。 FreeBusyAccessEnabled 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: c148d8fa1301339f8579884dc02b6c9e452f3035
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461294"
---
# <a name="freebusyaccessenabled-soap"></a><span data-ttu-id="01b3d-105">FreeBusyAccessEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="01b3d-105">FreeBusyAccessEnabled (SOAP)</span></span>

<span data-ttu-id="01b3d-106">**FreeBusyAccessEnabled**元素表示**FreeBusyAccessEnabled （）** 标志。</span><span class="sxs-lookup"><span data-stu-id="01b3d-106">The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag.</span></span> <span data-ttu-id="01b3d-107">**FreeBusyAccessEnabled**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="01b3d-107">The **FreeBusyAccessEnabled** element is for internal use only.</span></span> <span data-ttu-id="01b3d-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="01b3d-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 <span data-ttu-id="01b3d-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="01b3d-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01b3d-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="01b3d-110">Attributes and elements</span></span>

<span data-ttu-id="01b3d-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="01b3d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01b3d-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="01b3d-112">Attributes</span></span>

<span data-ttu-id="01b3d-113">无。</span><span class="sxs-lookup"><span data-stu-id="01b3d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01b3d-114">子元素</span><span class="sxs-lookup"><span data-stu-id="01b3d-114">Child elements</span></span>

<span data-ttu-id="01b3d-115">无。</span><span class="sxs-lookup"><span data-stu-id="01b3d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01b3d-116">父元素</span><span class="sxs-lookup"><span data-stu-id="01b3d-116">Parent elements</span></span>

|<span data-ttu-id="01b3d-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="01b3d-117">**Element**</span></span>|<span data-ttu-id="01b3d-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="01b3d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01b3d-119">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="01b3d-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="01b3d-120">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="01b3d-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01b3d-121">文本值</span><span class="sxs-lookup"><span data-stu-id="01b3d-121">Text value</span></span>

<span data-ttu-id="01b3d-122">如果**FreeBusyAccessEnabled**元素的文本值为**true** ，则表示应使用共享关系从组织中的用户检索忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="01b3d-122">A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization.</span></span> <span data-ttu-id="01b3d-123">**如果值为 false** ，则表示应取消共享关系。</span><span class="sxs-lookup"><span data-stu-id="01b3d-123">A value of **false** indicates that the sharing relationship should be suppressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01b3d-124">备注</span><span class="sxs-lookup"><span data-stu-id="01b3d-124">Remarks</span></span>

<span data-ttu-id="01b3d-125">使用此元素可允许或禁止显示服务器中的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="01b3d-125">Use this element to allow or suppress free/busy information from the server.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="01b3d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="01b3d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01b3d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="01b3d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="01b3d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="01b3d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="01b3d-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="01b3d-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="01b3d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="01b3d-130">Validation File</span></span>  <br/> |<span data-ttu-id="01b3d-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="01b3d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="01b3d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="01b3d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="01b3d-133">True</span><span class="sxs-lookup"><span data-stu-id="01b3d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01b3d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="01b3d-134">See also</span></span>



[<span data-ttu-id="01b3d-135">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="01b3d-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

