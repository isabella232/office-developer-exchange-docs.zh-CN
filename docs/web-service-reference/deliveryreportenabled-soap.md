---
title: DeliveryReportEnabled （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ab522bc-40ea-4e43-aa57-6d2562db35e9
description: DeliveryReportEnabled 元素表示 DeliveryReportEnabled （）标志。 DeliveryReportEnabled 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 2a163b3e6ceaa169cc8f76f395b7d501419a31ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458472"
---
# <a name="deliveryreportenabled-soap"></a><span data-ttu-id="47770-105">DeliveryReportEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="47770-105">DeliveryReportEnabled (SOAP)</span></span>

<span data-ttu-id="47770-106">**DeliveryReportEnabled**元素表示**DeliveryReportEnabled （）** 标志。</span><span class="sxs-lookup"><span data-stu-id="47770-106">The **DeliveryReportEnabled** element represents the **DeliveryReportEnabled()** flag.</span></span> <span data-ttu-id="47770-107">**DeliveryReportEnabled**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="47770-107">The **DeliveryReportEnabled** element is for internal use only.</span></span> <span data-ttu-id="47770-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="47770-108">This element is not used by clients.</span></span> 
  
```XML
<DeliveryReportEnabled>true | false</DeliveryReportEnabled>
```

 <span data-ttu-id="47770-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="47770-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47770-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="47770-110">Attributes and elements</span></span>

<span data-ttu-id="47770-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="47770-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47770-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="47770-112">Attributes</span></span>

<span data-ttu-id="47770-113">无。</span><span class="sxs-lookup"><span data-stu-id="47770-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47770-114">子元素</span><span class="sxs-lookup"><span data-stu-id="47770-114">Child elements</span></span>

<span data-ttu-id="47770-115">无。</span><span class="sxs-lookup"><span data-stu-id="47770-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="47770-116">父元素</span><span class="sxs-lookup"><span data-stu-id="47770-116">Parent elements</span></span>

|<span data-ttu-id="47770-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="47770-117">**Element**</span></span>|<span data-ttu-id="47770-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="47770-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47770-119">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="47770-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="47770-120">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="47770-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="47770-121">文本值</span><span class="sxs-lookup"><span data-stu-id="47770-121">Text value</span></span>

<span data-ttu-id="47770-122">如果 DeliveryReportEnabled 元素的文本值为 true，则表示可以使用来自组织中的用户的送达报告。</span><span class="sxs-lookup"><span data-stu-id="47770-122">A text value of true for the DeliveryReportEnabled element indicates that the delivery reports from users in the organization can be used.</span></span> <span data-ttu-id="47770-123">如果值为 false，则表示应禁止送达报告。</span><span class="sxs-lookup"><span data-stu-id="47770-123">A value of false indicates that the delivery reports should suppressed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47770-124">备注</span><span class="sxs-lookup"><span data-stu-id="47770-124">Remarks</span></span>

<span data-ttu-id="47770-125">使用此元素可允许或禁止来自服务器的送达报告。</span><span class="sxs-lookup"><span data-stu-id="47770-125">Use this element to allow or suppress delivery reports from the server.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47770-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="47770-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47770-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="47770-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="47770-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="47770-128">Schema Name</span></span>  <br/> |<span data-ttu-id="47770-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="47770-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="47770-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="47770-130">Validation File</span></span>  <br/> |<span data-ttu-id="47770-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="47770-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="47770-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="47770-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="47770-133">True</span><span class="sxs-lookup"><span data-stu-id="47770-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47770-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47770-134">See also</span></span>

- [<span data-ttu-id="47770-135">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="47770-135">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

