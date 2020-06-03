---
title: 域（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Domain 元素在 GetFederationInformation 响应中包含一个联合域，或者包含一个域，在 GetDomainSettings 请求中请求的配置设置。
ms.openlocfilehash: f90c608ee1fc3356a227bca6411eaeff0c1e8b22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456981"
---
# <a name="domain-soap"></a><span data-ttu-id="cf720-103">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="cf720-103">Domain (SOAP)</span></span>

<span data-ttu-id="cf720-104">**Domain**元素在**GetFederationInformation**响应中包含一个联合域，或者包含一个域，在**GetDomainSettings**请求中请求的配置设置。</span><span class="sxs-lookup"><span data-stu-id="cf720-104">The **Domain** element contains a federated domain in a **GetFederationInformation** response or contains a domain the configuration settings for which are requested in a **GetDomainSettings** request.</span></span> 
  
```XML
<Domain/> 
```

 <span data-ttu-id="cf720-105">**string**</span><span class="sxs-lookup"><span data-stu-id="cf720-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf720-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf720-106">Attributes and elements</span></span>

<span data-ttu-id="cf720-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf720-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf720-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cf720-108">Attributes</span></span>

<span data-ttu-id="cf720-109">无。</span><span class="sxs-lookup"><span data-stu-id="cf720-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf720-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cf720-110">Child elements</span></span>

<span data-ttu-id="cf720-111">无。</span><span class="sxs-lookup"><span data-stu-id="cf720-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cf720-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cf720-112">Parent elements</span></span>

|<span data-ttu-id="cf720-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf720-113">**Element**</span></span>|<span data-ttu-id="cf720-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf720-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf720-115">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="cf720-115">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="cf720-116">表示在**GetDomainSettings**操作中返回的配置设置或组织在**GetFederationInformation**操作中联合的域的域。</span><span class="sxs-lookup"><span data-stu-id="cf720-116">Represents the domains the configuration settings for which are returned in a **GetDomainSettings** operation or the domains that the organization has federated in a **GetFederationInformation** operation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf720-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cf720-117">Text value</span></span>

<span data-ttu-id="cf720-118">**Domain**元素的文本值表示一个域的名称。</span><span class="sxs-lookup"><span data-stu-id="cf720-118">The text value of the **Domain** element represents a domain name.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cf720-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf720-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf720-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf720-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cf720-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf720-121">Schema Name</span></span>  <br/> |<span data-ttu-id="cf720-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="cf720-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cf720-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf720-123">Validation File</span></span>  <br/> |<span data-ttu-id="cf720-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf720-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf720-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf720-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf720-126">True</span><span class="sxs-lookup"><span data-stu-id="cf720-126">True</span></span>  <br/> |
   

