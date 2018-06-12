---
title: FreeBusyAccessEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8d2d3276-b180-424e-a707-7256d14a1776
description: FreeBusyAccessEnabled 元素均表示 FreeBusyAccessEnabled() 标志。 FreeBusyAccessEnabled 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 4727e7054c02a4b5d454cb880691ecc01a075327
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754425"
---
# <a name="freebusyaccessenabled-soap"></a><span data-ttu-id="a224a-105">FreeBusyAccessEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a224a-105">FreeBusyAccessEnabled (SOAP)</span></span>

<span data-ttu-id="a224a-106">**FreeBusyAccessEnabled**元素均表示**FreeBusyAccessEnabled()** 标志。</span><span class="sxs-lookup"><span data-stu-id="a224a-106">The **FreeBusyAccessEnabled** element represents the **FreeBusyAccessEnabled()** flag.</span></span> <span data-ttu-id="a224a-107">**FreeBusyAccessEnabled**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="a224a-107">The **FreeBusyAccessEnabled** element is for internal use only.</span></span> <span data-ttu-id="a224a-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="a224a-108">This element is not used by clients.</span></span> 
  
```XML
<FreeBusyAccessEnabled>true | false</FreeBusyAccessEnabled>
```

 <span data-ttu-id="a224a-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a224a-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a224a-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a224a-110">Attributes and elements</span></span>

<span data-ttu-id="a224a-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a224a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a224a-112">属性</span><span class="sxs-lookup"><span data-stu-id="a224a-112">Attributes</span></span>

<span data-ttu-id="a224a-113">无。</span><span class="sxs-lookup"><span data-stu-id="a224a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a224a-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a224a-114">Child elements</span></span>

<span data-ttu-id="a224a-115">无。</span><span class="sxs-lookup"><span data-stu-id="a224a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a224a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a224a-116">Parent elements</span></span>

|<span data-ttu-id="a224a-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a224a-117">**Element**</span></span>|<span data-ttu-id="a224a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a224a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a224a-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a224a-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="a224a-120">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="a224a-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a224a-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a224a-121">Text value</span></span>

<span data-ttu-id="a224a-122">文本值为**true**的**FreeBusyAccessEnabled**元素指示共享关系应该用于检索忙/闲信息从组织中的用户。</span><span class="sxs-lookup"><span data-stu-id="a224a-122">A text value of **true** for the **FreeBusyAccessEnabled** element indicates that the sharing relationship should be used to retrieve free busy information from users in the organization.</span></span> <span data-ttu-id="a224a-123">如果值为**false**指示应禁止显示的共享的关系。</span><span class="sxs-lookup"><span data-stu-id="a224a-123">A value of **false** indicates that the sharing relationship should be suppressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a224a-124">备注</span><span class="sxs-lookup"><span data-stu-id="a224a-124">Remarks</span></span>

<span data-ttu-id="a224a-125">使用此元素以允许或禁止从服务器忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="a224a-125">Use this element to allow or suppress free/busy information from the server.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a224a-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="a224a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a224a-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="a224a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a224a-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="a224a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a224a-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="a224a-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a224a-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="a224a-130">Validation File</span></span>  <br/> |<span data-ttu-id="a224a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a224a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a224a-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="a224a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a224a-133">True</span><span class="sxs-lookup"><span data-stu-id="a224a-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a224a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a224a-134">See also</span></span>



[<span data-ttu-id="a224a-135">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a224a-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

