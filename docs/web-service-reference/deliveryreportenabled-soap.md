---
title: DeliveryReportEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: DeliveryReportEnabled 元素均表示 DeliveryReportEnabled() 标志。 DeliveryReportEnabled 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 089256a5f75ad92a4f11c5aaf3d175382eeee456
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753833"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="3fa10-105">DeliveryReportEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3fa10-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="3fa10-106">**DeliveryReportEnabled**元素均表示**DeliveryReportEnabled()** 标志。</span><span class="sxs-lookup"><span data-stu-id="3fa10-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="3fa10-107">**DeliveryReportEnabled**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="3fa10-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="3fa10-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="3fa10-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="3fa10-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3fa10-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3fa10-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3fa10-110">Attributes and elements</span></span>

<span data-ttu-id="3fa10-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3fa10-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fa10-112">属性</span><span class="sxs-lookup"><span data-stu-id="3fa10-112">Attributes</span></span>

<span data-ttu-id="3fa10-113">无。</span><span class="sxs-lookup"><span data-stu-id="3fa10-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fa10-114">子元素</span><span class="sxs-lookup"><span data-stu-id="3fa10-114">Child elements</span></span>

<span data-ttu-id="3fa10-115">无。</span><span class="sxs-lookup"><span data-stu-id="3fa10-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3fa10-116">父元素</span><span class="sxs-lookup"><span data-stu-id="3fa10-116">Parent elements</span></span>

|<span data-ttu-id="3fa10-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="3fa10-117">**Element**</span></span>|<span data-ttu-id="3fa10-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="3fa10-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fa10-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3fa10-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="3fa10-120">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="3fa10-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3fa10-121">文本值</span><span class="sxs-lookup"><span data-stu-id="3fa10-121">Text value</span></span>

<span data-ttu-id="3fa10-122">True DeliveryReportEnabled 元素的文本值指示可从组织中的用户的送达报告。</span><span class="sxs-lookup"><span data-stu-id="3fa10-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="3fa10-123">值为 false 指示应取消送达报告。</span><span class="sxs-lookup"><span data-stu-id="3fa10-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3fa10-124">注解</span><span class="sxs-lookup"><span data-stu-id="3fa10-124">Remarks</span></span>

<span data-ttu-id="3fa10-125">使用此元素以允许或禁止从服务器的送达报告。</span><span class="sxs-lookup"><span data-stu-id="3fa10-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fa10-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="3fa10-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fa10-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="3fa10-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3fa10-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="3fa10-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3fa10-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="3fa10-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3fa10-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="3fa10-130">Validation File</span></span>  <br/> |<span data-ttu-id="3fa10-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3fa10-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3fa10-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="3fa10-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fa10-133">True</span><span class="sxs-lookup"><span data-stu-id="3fa10-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fa10-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3fa10-134">See also</span></span>

- [<span data-ttu-id="3fa10-135">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3fa10-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

