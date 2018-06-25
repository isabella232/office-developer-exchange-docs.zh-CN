---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: GetDomainSettingsResponse 元素均表示对 GetDomainSettings 操作 (SOAP)，其返回域设置的响应。
ms.openlocfilehash: c4984c2c6c532fcbd45c1a75733e578f6d9491fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754526"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="7af14-103">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7af14-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="7af14-104">**GetDomainSettingsResponse**元素均表示一个[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)，其返回域设置响应。</span><span class="sxs-lookup"><span data-stu-id="7af14-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="7af14-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="7af14-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7af14-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7af14-106">Attributes and elements</span></span>

<span data-ttu-id="7af14-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7af14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7af14-108">属性</span><span class="sxs-lookup"><span data-stu-id="7af14-108">Attributes</span></span>

<span data-ttu-id="7af14-109">无。</span><span class="sxs-lookup"><span data-stu-id="7af14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7af14-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7af14-110">Child elements</span></span>

|<span data-ttu-id="7af14-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7af14-111">**Element**</span></span>|<span data-ttu-id="7af14-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7af14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7af14-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7af14-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="7af14-114">包含数组的每个请求的域设置的响应。</span><span class="sxs-lookup"><span data-stu-id="7af14-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="7af14-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7af14-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="7af14-116">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="7af14-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="7af14-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7af14-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="7af14-118">代表相关联的自动发现服务返回的错误代码的邮件。</span><span class="sxs-lookup"><span data-stu-id="7af14-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7af14-119">父元素</span><span class="sxs-lookup"><span data-stu-id="7af14-119">Parent elements</span></span>

<span data-ttu-id="7af14-120">无。</span><span class="sxs-lookup"><span data-stu-id="7af14-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7af14-121">文本值</span><span class="sxs-lookup"><span data-stu-id="7af14-121">Text value</span></span>

<span data-ttu-id="7af14-122">无。</span><span class="sxs-lookup"><span data-stu-id="7af14-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7af14-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="7af14-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7af14-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="7af14-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7af14-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="7af14-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7af14-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="7af14-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7af14-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="7af14-127">Validation File</span></span>  <br/> |<span data-ttu-id="7af14-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7af14-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7af14-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="7af14-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="7af14-130">True</span><span class="sxs-lookup"><span data-stu-id="7af14-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7af14-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7af14-131">See also</span></span>



[<span data-ttu-id="7af14-132">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7af14-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

