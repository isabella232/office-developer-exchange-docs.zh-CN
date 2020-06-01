---
title: OWAUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: OWAUrl 元素描述用于访问运行 Microsoft Exchange Server 2007 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457261"
---
# <a name="owaurl-pox"></a><span data-ttu-id="0eb99-103">OWAUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-103">OWAUrl (POX)</span></span>

<span data-ttu-id="0eb99-104">**OWAUrl**元素描述用于访问运行 Microsoft Exchange server 2007 的特定计算机的 URL 和身份验证架构，该计算机安装了承载 Outlook Web Access 的客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="0eb99-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="0eb99-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0eb99-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0eb99-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0eb99-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0eb99-109">Internal （POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="0eb99-110">OWAUrl （POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0eb99-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0eb99-111">Attributes and elements</span></span>

<span data-ttu-id="0eb99-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0eb99-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0eb99-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="0eb99-113">Attributes</span></span>

|<span data-ttu-id="0eb99-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="0eb99-114">**Attribute**</span></span>|<span data-ttu-id="0eb99-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="0eb99-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0eb99-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="0eb99-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="0eb99-117">介绍用于访问 Outlook Web Access 的身份验证方法。</span><span class="sxs-lookup"><span data-stu-id="0eb99-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="0eb99-118">AuthenticationMethod 属性</span><span class="sxs-lookup"><span data-stu-id="0eb99-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="0eb99-119">**值**</span><span class="sxs-lookup"><span data-stu-id="0eb99-119">**Value**</span></span>|<span data-ttu-id="0eb99-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="0eb99-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0eb99-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="0eb99-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="0eb99-122">集成的 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="0eb99-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="0eb99-123">FBA</span><span class="sxs-lookup"><span data-stu-id="0eb99-123">FBA</span></span>  <br/> |<span data-ttu-id="0eb99-124">基于表单的身份验证。</span><span class="sxs-lookup"><span data-stu-id="0eb99-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="0eb99-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="0eb99-125">NTLM</span></span>  <br/> |<span data-ttu-id="0eb99-126">NTLM 身份验证。</span><span class="sxs-lookup"><span data-stu-id="0eb99-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="0eb99-127">Digest</span><span class="sxs-lookup"><span data-stu-id="0eb99-127">Digest</span></span>  <br/> |<span data-ttu-id="0eb99-128">摘要式身份验证。</span><span class="sxs-lookup"><span data-stu-id="0eb99-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="0eb99-129">基本</span><span class="sxs-lookup"><span data-stu-id="0eb99-129">Basic</span></span>  <br/> |<span data-ttu-id="0eb99-130">基本身份验证。</span><span class="sxs-lookup"><span data-stu-id="0eb99-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0eb99-131">子元素</span><span class="sxs-lookup"><span data-stu-id="0eb99-131">Child elements</span></span>

<span data-ttu-id="0eb99-132">无。</span><span class="sxs-lookup"><span data-stu-id="0eb99-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0eb99-133">父元素</span><span class="sxs-lookup"><span data-stu-id="0eb99-133">Parent elements</span></span>

|<span data-ttu-id="0eb99-134">**元素**</span><span class="sxs-lookup"><span data-stu-id="0eb99-134">**Element**</span></span>|<span data-ttu-id="0eb99-135">**描述**</span><span class="sxs-lookup"><span data-stu-id="0eb99-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0eb99-136">Internal （POX）</span><span class="sxs-lookup"><span data-stu-id="0eb99-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="0eb99-137">包含当客户端在防火墙内部时可连接到的 Outlook Web Access Url 的集合。</span><span class="sxs-lookup"><span data-stu-id="0eb99-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0eb99-138">文本值</span><span class="sxs-lookup"><span data-stu-id="0eb99-138">Text value</span></span>

<span data-ttu-id="0eb99-139">该文本值表示客户端访问服务器上的 Outlook Web Access 服务的 URL。</span><span class="sxs-lookup"><span data-stu-id="0eb99-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0eb99-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0eb99-140">See also</span></span>



[<span data-ttu-id="0eb99-141">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="0eb99-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

