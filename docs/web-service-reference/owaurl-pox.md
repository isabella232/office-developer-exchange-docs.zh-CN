---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: OWAUrl 元素描述 URL 并用于访问特定的正在运行 Microsoft Exchange Server 2007 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826673"
---
# <a name="owaurl-pox"></a><span data-ttu-id="4e6b2-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-103">OWAUrl (POX)</span></span>

<span data-ttu-id="4e6b2-104">**OWAUrl**元素描述 URL 并用于访问特定的正在运行 Microsoft Exchange Server 2007 的计算机的身份验证架构了客户端访问服务器角色安装承载 Outlook Web Access。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="4e6b2-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4e6b2-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4e6b2-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4e6b2-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="4e6b2-109">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="4e6b2-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4e6b2-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e6b2-111">Attributes and elements</span></span>

<span data-ttu-id="4e6b2-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e6b2-113">属性</span><span class="sxs-lookup"><span data-stu-id="4e6b2-113">Attributes</span></span>

|<span data-ttu-id="4e6b2-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-114">**Attribute**</span></span>|<span data-ttu-id="4e6b2-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e6b2-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="4e6b2-117">介绍用于访问 Outlook Web Access 的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="4e6b2-118">AuthenticationMethod 属性</span><span class="sxs-lookup"><span data-stu-id="4e6b2-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="4e6b2-119">**值**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-119">**Value**</span></span>|<span data-ttu-id="4e6b2-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e6b2-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="4e6b2-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="4e6b2-122">集成的 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="4e6b2-123">FBA</span><span class="sxs-lookup"><span data-stu-id="4e6b2-123">FBA</span></span>  <br/> |<span data-ttu-id="4e6b2-124">基于表单的身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="4e6b2-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="4e6b2-125">NTLM</span></span>  <br/> |<span data-ttu-id="4e6b2-126">NTLM 身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="4e6b2-127">摘要式</span><span class="sxs-lookup"><span data-stu-id="4e6b2-127">Digest</span></span>  <br/> |<span data-ttu-id="4e6b2-128">摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="4e6b2-129">基本</span><span class="sxs-lookup"><span data-stu-id="4e6b2-129">Basic</span></span>  <br/> |<span data-ttu-id="4e6b2-130">基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e6b2-131">子元素</span><span class="sxs-lookup"><span data-stu-id="4e6b2-131">Child elements</span></span>

<span data-ttu-id="4e6b2-132">无。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e6b2-133">父元素</span><span class="sxs-lookup"><span data-stu-id="4e6b2-133">Parent elements</span></span>

|<span data-ttu-id="4e6b2-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-134">**Element**</span></span>|<span data-ttu-id="4e6b2-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e6b2-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e6b2-136">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="4e6b2-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="4e6b2-137">包含客户端可以连接到内部防火墙时的 Outlook Web Access Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4e6b2-138">文本值</span><span class="sxs-lookup"><span data-stu-id="4e6b2-138">Text value</span></span>

<span data-ttu-id="4e6b2-139">文本值表示的客户端访问服务器上的 Outlook Web Access 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="4e6b2-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e6b2-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e6b2-140">See also</span></span>



[<span data-ttu-id="4e6b2-141">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="4e6b2-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

