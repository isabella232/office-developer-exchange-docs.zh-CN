---
title: DomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f3d37f5a-c9ea-4ed9-a011-94d33bda64d1
description: DomainSettings 元素表示已提交的自动发现请求中或由自动发现响应返回的域设置。
ms.openlocfilehash: 961051399dc8babd8cba6eeaf43456071d0f40a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753992"
---
# <a name="domainsettings-soap"></a><span data-ttu-id="bc5d0-103">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bc5d0-103">DomainSettings (SOAP)</span></span>

<span data-ttu-id="bc5d0-104">**DomainSettings**元素表示已提交的自动发现请求中或由自动发现响应返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-104">The **DomainSettings** element represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span> 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 <span data-ttu-id="bc5d0-105">**DomainSettings**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-105">**DomainSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc5d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bc5d0-106">Attributes and elements</span></span>

<span data-ttu-id="bc5d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc5d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="bc5d0-108">Attributes</span></span>

<span data-ttu-id="bc5d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc5d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bc5d0-110">Child elements</span></span>

|<span data-ttu-id="bc5d0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-111">**Element**</span></span>|<span data-ttu-id="bc5d0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc5d0-113">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bc5d0-113">DomainSetting (SOAP)</span></span>](domainsetting-soap.md) <br/> |<span data-ttu-id="bc5d0-114">包含由[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-114">Contains domain settings that are returned by a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc5d0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="bc5d0-115">Parent elements</span></span>

|<span data-ttu-id="bc5d0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-116">**Element**</span></span>|<span data-ttu-id="bc5d0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="bc5d0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc5d0-118">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bc5d0-118">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="bc5d0-119">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-119">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc5d0-120">文本值</span><span class="sxs-lookup"><span data-stu-id="bc5d0-120">Text value</span></span>

<span data-ttu-id="bc5d0-121">无。</span><span class="sxs-lookup"><span data-stu-id="bc5d0-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc5d0-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="bc5d0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc5d0-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="bc5d0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bc5d0-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="bc5d0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bc5d0-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="bc5d0-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bc5d0-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="bc5d0-126">Validation File</span></span>  <br/> |<span data-ttu-id="bc5d0-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bc5d0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bc5d0-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="bc5d0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc5d0-129">True</span><span class="sxs-lookup"><span data-stu-id="bc5d0-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc5d0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc5d0-130">See also</span></span>

- [<span data-ttu-id="bc5d0-131">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bc5d0-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

