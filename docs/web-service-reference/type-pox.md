---
title: 类型（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Type 元素标识配置的邮件帐户的类型。
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465098"
---
# <a name="type-pox"></a><span data-ttu-id="c7d36-103">类型（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-103">Type (POX)</span></span>

<span data-ttu-id="c7d36-104">**Type**元素标识配置的邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="c7d36-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="c7d36-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c7d36-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c7d36-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c7d36-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c7d36-109">类型（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c7d36-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7d36-110">Attributes and elements</span></span>

<span data-ttu-id="c7d36-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7d36-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7d36-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="c7d36-112">Attributes</span></span>

<span data-ttu-id="c7d36-113">无。</span><span class="sxs-lookup"><span data-stu-id="c7d36-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7d36-114">子元素</span><span class="sxs-lookup"><span data-stu-id="c7d36-114">Child elements</span></span>

<span data-ttu-id="c7d36-115">无。</span><span class="sxs-lookup"><span data-stu-id="c7d36-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7d36-116">父元素</span><span class="sxs-lookup"><span data-stu-id="c7d36-116">Parent elements</span></span>

|<span data-ttu-id="c7d36-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7d36-117">**Element**</span></span>|<span data-ttu-id="c7d36-118">**描述**</span><span class="sxs-lookup"><span data-stu-id="c7d36-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7d36-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="c7d36-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c7d36-120">包含用于将客户端连接到 Exchange 服务器的规范。</span><span class="sxs-lookup"><span data-stu-id="c7d36-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7d36-121">文本值</span><span class="sxs-lookup"><span data-stu-id="c7d36-121">Text value</span></span>

<span data-ttu-id="c7d36-122">该文本值表示邮件帐户的类型。</span><span class="sxs-lookup"><span data-stu-id="c7d36-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="c7d36-123">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="c7d36-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="c7d36-124">**值**</span><span class="sxs-lookup"><span data-stu-id="c7d36-124">**Value**</span></span>|<span data-ttu-id="c7d36-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7d36-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7d36-126">EXCH</span><span class="sxs-lookup"><span data-stu-id="c7d36-126">EXCH</span></span>  <br/> |<span data-ttu-id="c7d36-127">用于连接到服务器的协议为 Exchange RPC。</span><span class="sxs-lookup"><span data-stu-id="c7d36-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="c7d36-128">EXHTTP</span><span class="sxs-lookup"><span data-stu-id="c7d36-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="c7d36-129">用于连接到服务器 RPC/HTTP 连接的协议。</span><span class="sxs-lookup"><span data-stu-id="c7d36-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="c7d36-130">表达式</span><span class="sxs-lookup"><span data-stu-id="c7d36-130">EXPR</span></span>  <br/> |<span data-ttu-id="c7d36-131">用于连接到服务器的协议是 Exchange RPC over HTTP （使用 RPC 代理服务器）。</span><span class="sxs-lookup"><span data-stu-id="c7d36-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="c7d36-132">仅当[AccountType （POX）](accounttype-pox.md)元素设置为 "电子邮件" 时，此设置才适用。</span><span class="sxs-lookup"><span data-stu-id="c7d36-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="c7d36-133">网络</span><span class="sxs-lookup"><span data-stu-id="c7d36-133">WEB</span></span>  <br/> |<span data-ttu-id="c7d36-134">通过使用在[服务器（POX）](server-pox.md)元素中指定的 URL，可以从 Web 浏览器访问电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c7d36-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="c7d36-135">仅当[AccountType （POX）](accounttype-pox.md)元素设置为 "电子邮件" 时，此设置才适用。</span><span class="sxs-lookup"><span data-stu-id="c7d36-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="c7d36-136">版本差异</span><span class="sxs-lookup"><span data-stu-id="c7d36-136">Version differences</span></span>

<span data-ttu-id="c7d36-137">如果将服务器配置为接受 RPC/HTTP 连接，并且客户端包含包含 "ExHttpInfo" 的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头，则 Office 365、exchange Online 和本地 exchange （从 build 15.00.0995.014 开始）将返回值 "EXHTTP"。</span><span class="sxs-lookup"><span data-stu-id="c7d36-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7d36-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7d36-138">See also</span></span>



[<span data-ttu-id="c7d36-139">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="c7d36-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

