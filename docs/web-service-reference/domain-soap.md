---
title: 域 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: 域元素包含 GetFederationInformation 响应中的联盟的域或包含 GetDomainSettings 请求中请求为其配置设置的域。
ms.openlocfilehash: 411ca866800322ef06eeecc2ab92adc6f711917c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753971"
---
# <a name="domain-soap"></a><span data-ttu-id="2798d-103">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2798d-103">Domain (SOAP)</span></span>

<span data-ttu-id="2798d-104">**域**元素包含**GetFederationInformation**响应中的联盟的域或包含**GetDomainSettings**请求中请求为其配置设置的域。</span><span class="sxs-lookup"><span data-stu-id="2798d-104">The **Domain** element contains a federated domain in a **GetFederationInformation** response or contains a domain the configuration settings for which are requested in a **GetDomainSettings** request.</span></span> 
  
```XML
<Domain/> 
```

 <span data-ttu-id="2798d-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2798d-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2798d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2798d-106">Attributes and elements</span></span>

<span data-ttu-id="2798d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2798d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2798d-108">属性</span><span class="sxs-lookup"><span data-stu-id="2798d-108">Attributes</span></span>

<span data-ttu-id="2798d-109">无。</span><span class="sxs-lookup"><span data-stu-id="2798d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2798d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2798d-110">Child elements</span></span>

<span data-ttu-id="2798d-111">无。</span><span class="sxs-lookup"><span data-stu-id="2798d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2798d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2798d-112">Parent elements</span></span>

|<span data-ttu-id="2798d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2798d-113">**Element**</span></span>|<span data-ttu-id="2798d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2798d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2798d-115">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2798d-115">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="2798d-116">代表**GetDomainSettings**操作中返回的配置设置的域或组织具有联合**GetFederationInformation**操作中的域。</span><span class="sxs-lookup"><span data-stu-id="2798d-116">Represents the domains the configuration settings for which are returned in a **GetDomainSettings** operation or the domains that the organization has federated in a **GetFederationInformation** operation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2798d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2798d-117">Text value</span></span>

<span data-ttu-id="2798d-118">**域**元素的文本值表示的域名。</span><span class="sxs-lookup"><span data-stu-id="2798d-118">The text value of the **Domain** element represents a domain name.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2798d-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="2798d-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2798d-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="2798d-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2798d-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="2798d-121">Schema Name</span></span>  <br/> |<span data-ttu-id="2798d-122">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="2798d-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2798d-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="2798d-123">Validation File</span></span>  <br/> |<span data-ttu-id="2798d-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2798d-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2798d-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="2798d-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="2798d-126">True</span><span class="sxs-lookup"><span data-stu-id="2798d-126">True</span></span>  <br/> |
   

