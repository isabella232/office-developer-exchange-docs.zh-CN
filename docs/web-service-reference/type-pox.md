---
title: 类型 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Type 元素标识配置的邮件帐户的类型。
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838295"
---
# <a name="type-pox"></a><span data-ttu-id="a3ea2-103">类型 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-103">Type (POX)</span></span>

<span data-ttu-id="a3ea2-104">**Type**元素标识配置的邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="a3ea2-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a3ea2-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a3ea2-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a3ea2-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a3ea2-109">类型 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a3ea2-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a3ea2-110">Attributes and elements</span></span>

<span data-ttu-id="a3ea2-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3ea2-112">属性</span><span class="sxs-lookup"><span data-stu-id="a3ea2-112">Attributes</span></span>

<span data-ttu-id="a3ea2-113">无。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3ea2-114">子元素</span><span class="sxs-lookup"><span data-stu-id="a3ea2-114">Child elements</span></span>

<span data-ttu-id="a3ea2-115">无。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3ea2-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a3ea2-116">Parent elements</span></span>

|<span data-ttu-id="a3ea2-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a3ea2-117">**Element**</span></span>|<span data-ttu-id="a3ea2-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3ea2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3ea2-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="a3ea2-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a3ea2-120">包含客户端连接到 Exchange 服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a3ea2-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a3ea2-121">Text value</span></span>

<span data-ttu-id="a3ea2-122">文本值表示的邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="a3ea2-123">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="a3ea2-124">**值**</span><span class="sxs-lookup"><span data-stu-id="a3ea2-124">**Value**</span></span>|<span data-ttu-id="a3ea2-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3ea2-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3ea2-126">EXCH</span><span class="sxs-lookup"><span data-stu-id="a3ea2-126">EXCH</span></span>  <br/> |<span data-ttu-id="a3ea2-127">用于连接到服务器的协议是 Exchange RPC。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="a3ea2-128">EXHTTP</span><span class="sxs-lookup"><span data-stu-id="a3ea2-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="a3ea2-129">用于连接到服务器的 RPC/HTTP 连接协议。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="a3ea2-130">EXPR</span><span class="sxs-lookup"><span data-stu-id="a3ea2-130">EXPR</span></span>  <br/> |<span data-ttu-id="a3ea2-131">用于连接到服务器的协议是 Exchange RPC over HTTP，使用 RPC 代理服务器。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="a3ea2-132">[AccountType (POX)](accounttype-pox.md)元素设置为电子邮件时，这是仅适用。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="a3ea2-133">WEB</span><span class="sxs-lookup"><span data-stu-id="a3ea2-133">WEB</span></span>  <br/> |<span data-ttu-id="a3ea2-134">电子邮件从 Web 浏览器访问使用[服务器 (POX)](server-pox.md)元素中指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="a3ea2-135">[AccountType (POX)](accounttype-pox.md)元素设置为电子邮件时，这是仅适用。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="a3ea2-136">版本差异</span><span class="sxs-lookup"><span data-stu-id="a3ea2-136">Version differences</span></span>

<span data-ttu-id="a3ea2-137">Office 365 和 Exchange Online 中，在本地版本的 Exchange 开头构建 15.00.0995.014 返回的值为"EXHTTP"才将服务器配置为接受 RPC/HTTP 连接和客户端包括[X ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头的包含"ExHttpInfo"。</span><span class="sxs-lookup"><span data-stu-id="a3ea2-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3ea2-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3ea2-138">See also</span></span>



[<span data-ttu-id="a3ea2-139">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="a3ea2-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

