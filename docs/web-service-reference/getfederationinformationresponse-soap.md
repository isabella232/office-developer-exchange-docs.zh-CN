---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: GetFederationInformationResponse 元素包含 GetFederationInformation 操作 (SOAP) 响应。
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754556"
---
# <a name="getfederationinformationresponse-soap"></a><span data-ttu-id="a67e1-103">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-103">GetFederationInformationResponse (SOAP)</span></span>

<span data-ttu-id="a67e1-104">**GetFederationInformationResponse**元素包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应。</span><span class="sxs-lookup"><span data-stu-id="a67e1-104">The **GetFederationInformationResponse** element contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span> 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 <span data-ttu-id="a67e1-105">**GetFederationInformationResponse**</span><span class="sxs-lookup"><span data-stu-id="a67e1-105">**GetFederationInformationResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a67e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a67e1-106">Attributes and elements</span></span>

<span data-ttu-id="a67e1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a67e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a67e1-108">属性</span><span class="sxs-lookup"><span data-stu-id="a67e1-108">Attributes</span></span>

<span data-ttu-id="a67e1-109">无。</span><span class="sxs-lookup"><span data-stu-id="a67e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a67e1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a67e1-110">Child elements</span></span>

|<span data-ttu-id="a67e1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a67e1-111">**Element**</span></span>|<span data-ttu-id="a67e1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a67e1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a67e1-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="a67e1-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a67e1-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a67e1-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="a67e1-116">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="a67e1-116">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="a67e1-117">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-117">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md) <br/> |<span data-ttu-id="a67e1-118">定义应用程序的位置。</span><span class="sxs-lookup"><span data-stu-id="a67e1-118">Defines the location of an application.</span></span>  <br/> |
|[<span data-ttu-id="a67e1-119">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-119">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="a67e1-120">表示安全令牌，其中包含安全令牌服务标识符和终结点的集合。</span><span class="sxs-lookup"><span data-stu-id="a67e1-120">Represents a collection of security tokens, which contain security token service identifiers and endpoints.</span></span>  <br/> |
|[<span data-ttu-id="a67e1-121">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-121">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="a67e1-122">代表为其配置[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings**操作中返回的域或组织具有联合[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中的域**GetFederationInformation**操作。</span><span class="sxs-lookup"><span data-stu-id="a67e1-122">Represents the domains the configurations for which are returned in a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** operation or the domains the organization has federated in a [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a67e1-123">父元素</span><span class="sxs-lookup"><span data-stu-id="a67e1-123">Parent elements</span></span>

<span data-ttu-id="a67e1-124">无。</span><span class="sxs-lookup"><span data-stu-id="a67e1-124">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a67e1-125">文本值</span><span class="sxs-lookup"><span data-stu-id="a67e1-125">Text value</span></span>

<span data-ttu-id="a67e1-126">无。</span><span class="sxs-lookup"><span data-stu-id="a67e1-126">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a67e1-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="a67e1-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a67e1-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="a67e1-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a67e1-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="a67e1-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a67e1-130">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="a67e1-130">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a67e1-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="a67e1-131">Validation File</span></span>  <br/> |<span data-ttu-id="a67e1-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a67e1-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a67e1-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="a67e1-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a67e1-134">True</span><span class="sxs-lookup"><span data-stu-id="a67e1-134">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a67e1-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a67e1-135">See also</span></span>



[<span data-ttu-id="a67e1-136">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a67e1-136">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

