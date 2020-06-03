---
title: DomainResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: DomainResponse 元素包含指定域的请求的设置。
ms.openlocfilehash: dea6e36c51ceea53201b668cfba616c03a44df86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456960"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="f59d4-103">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="f59d4-104">**DomainResponse**元素包含指定域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="f59d4-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="f59d4-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="f59d4-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f59d4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f59d4-106">Attributes and elements</span></span>

<span data-ttu-id="f59d4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f59d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f59d4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f59d4-108">Attributes</span></span>

<span data-ttu-id="f59d4-109">无。</span><span class="sxs-lookup"><span data-stu-id="f59d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f59d4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f59d4-110">Child elements</span></span>

|<span data-ttu-id="f59d4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f59d4-111">**Element**</span></span>|<span data-ttu-id="f59d4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f59d4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f59d4-113">DomainSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="f59d4-114">包含无法返回的设置的错误消息。</span><span class="sxs-lookup"><span data-stu-id="f59d4-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="f59d4-115">DomainSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="f59d4-116">表示在自动发现请求中提交或由自动发现响应返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="f59d4-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="f59d4-117">RedirectTarget （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="f59d4-118">标识重定向的目标。</span><span class="sxs-lookup"><span data-stu-id="f59d4-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="f59d4-119">目标可以是 URL，也可以是电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f59d4-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="f59d4-120">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="f59d4-121">指定与特定请求相关联的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f59d4-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="f59d4-122">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="f59d4-123">指定与特定请求相关联的错误消息。</span><span class="sxs-lookup"><span data-stu-id="f59d4-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f59d4-124">父元素</span><span class="sxs-lookup"><span data-stu-id="f59d4-124">Parent elements</span></span>

|<span data-ttu-id="f59d4-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="f59d4-125">**Element**</span></span>|<span data-ttu-id="f59d4-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="f59d4-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f59d4-127">ArrayOfDomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="f59d4-128">包含**DomainResponse**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="f59d4-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="f59d4-129">每个**DomainResponse**元素都包含指定用户的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="f59d4-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="f59d4-130">DomainResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f59d4-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="f59d4-131">包含每个域的响应。</span><span class="sxs-lookup"><span data-stu-id="f59d4-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f59d4-132">文本值</span><span class="sxs-lookup"><span data-stu-id="f59d4-132">Text value</span></span>

<span data-ttu-id="f59d4-133">无。</span><span class="sxs-lookup"><span data-stu-id="f59d4-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f59d4-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="f59d4-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f59d4-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="f59d4-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f59d4-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="f59d4-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f59d4-137">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f59d4-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f59d4-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="f59d4-138">Validation File</span></span>  <br/> |<span data-ttu-id="f59d4-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f59d4-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f59d4-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="f59d4-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f59d4-141">True</span><span class="sxs-lookup"><span data-stu-id="f59d4-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f59d4-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f59d4-142">See also</span></span>

- [<span data-ttu-id="f59d4-143">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f59d4-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

