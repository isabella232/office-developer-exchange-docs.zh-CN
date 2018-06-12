---
title: DomainSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bad5399c-0762-4979-9c15-58cf4b7b6278
description: DomainSetting 元素包含由 GetDomainSettings 操作 (SOAP) 操作请求返回的域设置。
ms.openlocfilehash: f1c7a30ee221c5f3ca1358d0f3c3aca5c3467159
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753987"
---
# <a name="domainsetting-soap"></a><span data-ttu-id="f2d79-103">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2d79-103">DomainSetting (SOAP)</span></span>

<span data-ttu-id="f2d79-104">**DomainSetting**元素包含由[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)操作请求返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="f2d79-104">The **DomainSetting** element contains domain settings that are returned by the [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<DomainSetting>
   <Name/>
</DomainSetting>
```

 <span data-ttu-id="f2d79-105">**DomainSetting**</span><span class="sxs-lookup"><span data-stu-id="f2d79-105">**DomainSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2d79-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2d79-106">Attributes and elements</span></span>

<span data-ttu-id="f2d79-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2d79-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2d79-108">属性</span><span class="sxs-lookup"><span data-stu-id="f2d79-108">Attributes</span></span>

<span data-ttu-id="f2d79-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2d79-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2d79-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2d79-110">Child elements</span></span>

|<span data-ttu-id="f2d79-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2d79-111">**Element**</span></span>|<span data-ttu-id="f2d79-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2d79-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d79-113">名称 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2d79-113">Name (SOAP)</span></span>](name-soap.md) <br/> |<span data-ttu-id="f2d79-114">代表设置的名称。</span><span class="sxs-lookup"><span data-stu-id="f2d79-114">Represents the name of a setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2d79-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f2d79-115">Parent elements</span></span>

|<span data-ttu-id="f2d79-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2d79-116">**Element**</span></span>|<span data-ttu-id="f2d79-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2d79-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2d79-118">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2d79-118">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="f2d79-119">表示已提交的自动发现请求中或由自动发现响应返回的域设置。</span><span class="sxs-lookup"><span data-stu-id="f2d79-119">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2d79-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f2d79-120">Text value</span></span>

<span data-ttu-id="f2d79-121">无。</span><span class="sxs-lookup"><span data-stu-id="f2d79-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2d79-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2d79-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2d79-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2d79-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f2d79-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2d79-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f2d79-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f2d79-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f2d79-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2d79-126">Validation File</span></span>  <br/> |<span data-ttu-id="f2d79-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2d79-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2d79-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2d79-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2d79-129">True</span><span class="sxs-lookup"><span data-stu-id="f2d79-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2d79-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2d79-130">See also</span></span>

- [<span data-ttu-id="f2d79-131">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f2d79-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

