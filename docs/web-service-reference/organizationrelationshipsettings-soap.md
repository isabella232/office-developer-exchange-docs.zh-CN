---
title: OrganizationRelationshipSettings （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 917481bb-46fc-4b88-8683-4cf812dcb0ab
description: OrganizationRelationshipSettings 元素表示单个组织的组织关系列表。 OrganizationRelationshipSettings 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 383b3635e1435c6597ccf793a7990c411c02d36d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462456"
---
# <a name="organizationrelationshipsettings-soap"></a><span data-ttu-id="41399-105">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-105">OrganizationRelationshipSettings (SOAP)</span></span>

<span data-ttu-id="41399-106">**OrganizationRelationshipSettings**元素表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="41399-106">The **OrganizationRelationshipSettings** element represents a list of organization relationships for a single organization.</span></span> <span data-ttu-id="41399-107">**OrganizationRelationshipSettings**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="41399-107">The **OrganizationRelationshipSettings** element is for internal use only.</span></span> <span data-ttu-id="41399-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="41399-108">This element is not used by clients.</span></span> 
  
```XML
<OrganizationRelationshipSettings>
    <DeliveryReportEnabled/>
    <DomainNames/>
    <FreeBusyAccessEnabled/>
    <FreeBusyAccessLevel/>
    <MailTipsAccessEnabled/>
    <MailTipsAccessLevel/>
    <MailboxMoveEnabled/>
    <Name/>
    <TargetApplicationUri/>
    <TargetAudodiscoverEpr/>
    <TargetSharingEpr/>
</OrganizationRelationshipSettings>
```

 <span data-ttu-id="41399-109">**OrganizationRelationshipSettings**</span><span class="sxs-lookup"><span data-stu-id="41399-109">**OrganizationRelationshipSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41399-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41399-110">Attributes and elements</span></span>

<span data-ttu-id="41399-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41399-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41399-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="41399-112">Attributes</span></span>

<span data-ttu-id="41399-113">无。</span><span class="sxs-lookup"><span data-stu-id="41399-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41399-114">子元素</span><span class="sxs-lookup"><span data-stu-id="41399-114">Child elements</span></span>

|<span data-ttu-id="41399-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="41399-115">**Element**</span></span>|<span data-ttu-id="41399-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="41399-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41399-117">DeliveryReportEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-117">DeliveryReportEnabled (SOAP)</span></span>](deliveryreportenabled-soap.md) <br/> |<span data-ttu-id="41399-118">代表 " [DeliveryReportEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx)标志。</span><span class="sxs-lookup"><span data-stu-id="41399-118">Represents the [DeliveryReportEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.DeliveryReportEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="41399-119">DomainNames （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-119">DomainNames (SOAP)</span></span>](domainnames-soap.md) <br/> |<span data-ttu-id="41399-120">表示域名集合。</span><span class="sxs-lookup"><span data-stu-id="41399-120">Represents the domain names collection.</span></span>  <br/> |
|[<span data-ttu-id="41399-121">FreeBusyAccessEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-121">FreeBusyAccessEnabled (SOAP)</span></span>](freebusyaccessenabled-soap.md) <br/> |<span data-ttu-id="41399-122">代表 " [FreeBusyAccessEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx)标志。</span><span class="sxs-lookup"><span data-stu-id="41399-122">Represents the [FreeBusyAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.FreeBusyAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="41399-123">FreeBusyAccessLevel （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-123">FreeBusyAccessLevel (SOAP)</span></span>](freebusyaccesslevel-soap.md) <br/> |<span data-ttu-id="41399-124">表示[FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="41399-124">Represents the [FreeBusyAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.FreeBusyAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="41399-125">MailTipsAccessEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-125">MailTipsAccessEnabled (SOAP)</span></span>](mailtipsaccessenabled-soap.md) <br/> |<span data-ttu-id="41399-126">代表 " [MailTipsAccessEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx)标志。</span><span class="sxs-lookup"><span data-stu-id="41399-126">Represents the [MailTipsAccessEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailTipsAccessEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="41399-127">MailTipsAccessLevel （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-127">MailTipsAccessLevel (SOAP)</span></span>](mailtipsaccesslevel-soap.md) <br/> |<span data-ttu-id="41399-128">表示[MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="41399-128">Represents the [MailTipsAccessLevel](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.MailTipsAccessLevel.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="41399-129">MailboxMoveEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-129">MailboxMoveEnabled (SOAP)</span></span>](mailboxmoveenabled-soap.md) <br/> |<span data-ttu-id="41399-130">代表 " [MailboxMoveEnabled" （）](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx)标志。</span><span class="sxs-lookup"><span data-stu-id="41399-130">Represents the [MailboxMoveEnabled()](https://msdn.microsoft.com/library/Microsoft.Exchange.SoapWebClient.AutoDiscover.OrganizationRelationshipSettings.MailboxMoveEnabled.aspx) flag.</span></span>  <br/> |
|[<span data-ttu-id="41399-131">名称（SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-131">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="41399-132">表示组织关系的名称。</span><span class="sxs-lookup"><span data-stu-id="41399-132">Represents the name of the organization relationship.</span></span>  <br/> |
|[<span data-ttu-id="41399-133">TargetApplicationUri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-133">TargetApplicationUri (SOAP)</span></span>](targetapplicationuri-soap.md) <br/> |<span data-ttu-id="41399-134">定义目标应用程序 URI。</span><span class="sxs-lookup"><span data-stu-id="41399-134">Defines the target application URI.</span></span>  <br/> |
|[<span data-ttu-id="41399-135">TargetAutodiscoverEpr （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-135">TargetAutodiscoverEpr (SOAP)</span></span>](targetautodiscoverepr-soap.md) <br/> |<span data-ttu-id="41399-136">表示[TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="41399-136">Represents the [TargetAutodiscoverEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetAutodiscoverEpr.aspx) property.</span></span>  <br/> |
|[<span data-ttu-id="41399-137">TargetSharingEpr （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-137">TargetSharingEpr (SOAP)</span></span>](targetsharingepr-soap.md) <br/> |<span data-ttu-id="41399-138">表示[TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="41399-138">Represents the [TargetSharingEpr](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.OrganizationRelationship.TargetSharingEpr.aspx) property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41399-139">父元素</span><span class="sxs-lookup"><span data-stu-id="41399-139">Parent elements</span></span>

|<span data-ttu-id="41399-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="41399-140">**Element**</span></span>|<span data-ttu-id="41399-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="41399-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41399-142">OrganizationRelationshipSettingsCollection （SOAP）</span><span class="sxs-lookup"><span data-stu-id="41399-142">OrganizationRelationshipSettingsCollection (SOAP)</span></span>](organizationrelationshipsettingscollection-soap.md) <br/> |<span data-ttu-id="41399-143">表示与查询匹配的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="41399-143">Represents a list of organization relationships that match the query.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41399-144">文本值</span><span class="sxs-lookup"><span data-stu-id="41399-144">Text value</span></span>

<span data-ttu-id="41399-145">无。</span><span class="sxs-lookup"><span data-stu-id="41399-145">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41399-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="41399-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41399-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="41399-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="41399-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="41399-148">Schema Name</span></span>  <br/> |<span data-ttu-id="41399-149">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="41399-149">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="41399-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="41399-150">Validation File</span></span>  <br/> |<span data-ttu-id="41399-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="41399-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="41399-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="41399-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="41399-153">True</span><span class="sxs-lookup"><span data-stu-id="41399-153">True</span></span>  <br/> |
   

