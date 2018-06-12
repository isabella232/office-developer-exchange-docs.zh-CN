---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: RedirectTarget (SOAP) 元素包含目标的重定向 URL 或电子邮件地址。
ms.openlocfilehash: 3a8a0c39c6889730c9d17778c6a26f84fcbcd4a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827019"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="09481-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="09481-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="09481-104">[RedirectTarget (SOAP)](redirecttarget-soap.md)元素包含目标的重定向 URL 或电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="09481-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="09481-105">**string**</span><span class="sxs-lookup"><span data-stu-id="09481-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09481-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="09481-106">Attributes and elements</span></span>

<span data-ttu-id="09481-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="09481-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09481-108">属性</span><span class="sxs-lookup"><span data-stu-id="09481-108">Attributes</span></span>

<span data-ttu-id="09481-109">无。</span><span class="sxs-lookup"><span data-stu-id="09481-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09481-110">子元素</span><span class="sxs-lookup"><span data-stu-id="09481-110">Child elements</span></span>

<span data-ttu-id="09481-111">无。</span><span class="sxs-lookup"><span data-stu-id="09481-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09481-112">父元素</span><span class="sxs-lookup"><span data-stu-id="09481-112">Parent elements</span></span>

|<span data-ttu-id="09481-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="09481-113">**Element**</span></span>|<span data-ttu-id="09481-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="09481-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09481-115">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="09481-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="09481-116">代表对单个用户 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="09481-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="09481-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="09481-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="09481-118">包含指定的域的请求的设置。</span><span class="sxs-lookup"><span data-stu-id="09481-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09481-119">文本值</span><span class="sxs-lookup"><span data-stu-id="09481-119">Text value</span></span>

<span data-ttu-id="09481-120">文本值包含目标的后续 GetUserSettings 应使用的重定向 URL 或电子邮件地址或 GetDomainSettings 请求。</span><span class="sxs-lookup"><span data-stu-id="09481-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09481-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="09481-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09481-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="09481-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="09481-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="09481-123">Schema Name</span></span>  <br/> |<span data-ttu-id="09481-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="09481-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="09481-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="09481-125">Validation File</span></span>  <br/> |<span data-ttu-id="09481-126">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="09481-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="09481-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="09481-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="09481-128">True</span><span class="sxs-lookup"><span data-stu-id="09481-128">True</span></span>  <br/> |
   

