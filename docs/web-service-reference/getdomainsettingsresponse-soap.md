---
title: GetDomainSettingsResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: GetDomainSettingsResponse 元素表示对 GetDomainSettings 操作（SOAP）的响应，该操作返回域设置。
ms.openlocfilehash: 94cb202948e6a0d5a34f5547132c052d1d1b6a40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461875"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="f11db-103">GetDomainSettingsResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f11db-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="f11db-104">**GetDomainSettingsResponse**元素表示对[GETDOMAINSETTINGS 操作（SOAP）](getdomainsettings-operation-soap.md)的响应，该操作返回域设置。</span><span class="sxs-lookup"><span data-stu-id="f11db-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="f11db-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="f11db-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f11db-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f11db-106">Attributes and elements</span></span>

<span data-ttu-id="f11db-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f11db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f11db-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f11db-108">Attributes</span></span>

<span data-ttu-id="f11db-109">无。</span><span class="sxs-lookup"><span data-stu-id="f11db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f11db-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f11db-110">Child elements</span></span>

|<span data-ttu-id="f11db-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f11db-111">**Element**</span></span>|<span data-ttu-id="f11db-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f11db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f11db-113">DomainResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f11db-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="f11db-114">包含每个请求域的设置的响应数组。</span><span class="sxs-lookup"><span data-stu-id="f11db-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="f11db-115">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f11db-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="f11db-116">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f11db-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="f11db-117">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f11db-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="f11db-118">表示与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="f11db-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f11db-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f11db-119">Parent elements</span></span>

<span data-ttu-id="f11db-120">无。</span><span class="sxs-lookup"><span data-stu-id="f11db-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f11db-121">文本值</span><span class="sxs-lookup"><span data-stu-id="f11db-121">Text value</span></span>

<span data-ttu-id="f11db-122">无。</span><span class="sxs-lookup"><span data-stu-id="f11db-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f11db-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f11db-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f11db-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f11db-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f11db-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f11db-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f11db-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f11db-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f11db-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f11db-127">Validation File</span></span>  <br/> |<span data-ttu-id="f11db-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f11db-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f11db-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f11db-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f11db-130">True</span><span class="sxs-lookup"><span data-stu-id="f11db-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f11db-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f11db-131">See also</span></span>



[<span data-ttu-id="f11db-132">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f11db-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

