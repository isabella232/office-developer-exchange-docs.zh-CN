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
description: 请求元素包含一个请求可返回域设置。
ms.openlocfilehash: 71a6072d476fd665dad8b0c0fe388a40db56e059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827135"
---
# <a name="request-getdomainsettings-soap"></a><span data-ttu-id="92abf-103">请求 (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92abf-103">Request (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="92abf-104">**请求**元素包含一个请求可返回域设置。</span><span class="sxs-lookup"><span data-stu-id="92abf-104">The **Request** element contains a request to return domain settings.</span></span> 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 <span data-ttu-id="92abf-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="92abf-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92abf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92abf-106">Attributes and elements</span></span>

<span data-ttu-id="92abf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92abf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92abf-108">属性</span><span class="sxs-lookup"><span data-stu-id="92abf-108">Attributes</span></span>

<span data-ttu-id="92abf-109">无。</span><span class="sxs-lookup"><span data-stu-id="92abf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92abf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="92abf-110">Child elements</span></span>

|<span data-ttu-id="92abf-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="92abf-111">**Element**</span></span>|<span data-ttu-id="92abf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="92abf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92abf-113">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92abf-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="92abf-114">代表[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)以返回为其配置的域或组织具有联合[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中的域。</span><span class="sxs-lookup"><span data-stu-id="92abf-114">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md).</span></span>  <br/> |
|[<span data-ttu-id="92abf-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92abf-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="92abf-116">包含请求的配置设置的名称。</span><span class="sxs-lookup"><span data-stu-id="92abf-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92abf-117">父元素</span><span class="sxs-lookup"><span data-stu-id="92abf-117">Parent elements</span></span>

|<span data-ttu-id="92abf-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="92abf-118">**Element**</span></span>|<span data-ttu-id="92abf-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="92abf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92abf-120">GetDomainSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92abf-120">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="92abf-121">代表[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="92abf-121">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md)request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="92abf-122">文本值</span><span class="sxs-lookup"><span data-stu-id="92abf-122">Text value</span></span>

<span data-ttu-id="92abf-123">无。</span><span class="sxs-lookup"><span data-stu-id="92abf-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92abf-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="92abf-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92abf-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="92abf-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="92abf-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="92abf-126">Schema Name</span></span>  <br/> |<span data-ttu-id="92abf-127">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="92abf-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="92abf-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="92abf-128">Validation File</span></span>  <br/> |<span data-ttu-id="92abf-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="92abf-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="92abf-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="92abf-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="92abf-131">True</span><span class="sxs-lookup"><span data-stu-id="92abf-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92abf-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92abf-132">See also</span></span>



[<span data-ttu-id="92abf-133">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="92abf-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

