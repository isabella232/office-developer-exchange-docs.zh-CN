---
title: 请求 (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: Request 元素包含一个返回域设置的请求。
ms.openlocfilehash: c5f666102be8aaeee001a23706732e9e6c44b560
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459586"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="d8892-103">请求 (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d8892-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="d8892-104">**Request**元素包含一个返回域设置的请求。</span><span class="sxs-lookup"><span data-stu-id="d8892-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="d8892-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="d8892-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8892-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d8892-106">Attributes and elements</span></span>

<span data-ttu-id="d8892-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d8892-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8892-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d8892-108">Attributes</span></span>

<span data-ttu-id="d8892-109">无。</span><span class="sxs-lookup"><span data-stu-id="d8892-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8892-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d8892-110">Child elements</span></span>

|<span data-ttu-id="d8892-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d8892-111">**Element**</span></span>|<span data-ttu-id="d8892-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8892-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8892-113">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="d8892-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="d8892-114">表示在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)或组织在[GETFEDERATIONINFORMATION 操作（soap）](getfederationinformation-operation-soap.md)中进行了联合的域中返回的配置的域。</span><span class="sxs-lookup"><span data-stu-id="d8892-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="d8892-115">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d8892-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="d8892-116">包含所请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="d8892-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d8892-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d8892-117">Parent elements</span></span>

|<span data-ttu-id="d8892-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d8892-118">**Element**</span></span>|<span data-ttu-id="d8892-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8892-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8892-120">GetDomainSettingsRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="d8892-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="d8892-121">表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="d8892-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8892-122">文本值</span><span class="sxs-lookup"><span data-stu-id="d8892-122">Text value</span></span>

<span data-ttu-id="d8892-123">无。</span><span class="sxs-lookup"><span data-stu-id="d8892-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8892-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d8892-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8892-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d8892-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d8892-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d8892-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d8892-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="d8892-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d8892-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d8892-128">Validation File</span></span>  <br/> |<span data-ttu-id="d8892-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d8892-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d8892-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d8892-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8892-131">True</span><span class="sxs-lookup"><span data-stu-id="d8892-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8892-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d8892-132">See also</span></span>



[<span data-ttu-id="d8892-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d8892-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

