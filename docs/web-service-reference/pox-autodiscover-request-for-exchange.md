---
title: Exchange POX 自动发现请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: 自动发现请求包含用户的客户端访问配置的查询。
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826865"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="4bfd6-103">Exchange POX 自动发现请求</span><span class="sxs-lookup"><span data-stu-id="4bfd6-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="4bfd6-104">自动发现请求包含用户的客户端访问配置的查询。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="4bfd6-105">自动发现请求示例</span><span class="sxs-lookup"><span data-stu-id="4bfd6-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="4bfd6-106">说明</span><span class="sxs-lookup"><span data-stu-id="4bfd6-106">Description</span></span>

<span data-ttu-id="4bfd6-107">下面的 XML 示例演示了自动发现请求正文。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="4bfd6-108">代码</span><span class="sxs-lookup"><span data-stu-id="4bfd6-108">Code</span></span>

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="4bfd6-109">请求标头</span><span class="sxs-lookup"><span data-stu-id="4bfd6-109">Request Headers</span></span>

<span data-ttu-id="4bfd6-110">发送自动发现请求时，以下 HTTP 标头是可选的。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="4bfd6-111">**表 1。HTTP 请求标头**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="4bfd6-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-112">**Header**</span></span>|<span data-ttu-id="4bfd6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4bfd6-114">X MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="4bfd6-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="4bfd6-115">如果存在此参数，并且已设置为"1"，指示客户端的请求可用于连接到服务器使用 MAPI/HTTP 协议的信息。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="4bfd6-116">适用于客户端实现 MAPI/HTTP 协议的此标头。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="4bfd6-117">X ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="4bfd6-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="4bfd6-118">此标头中包含客户端支持的功能的以逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="4bfd6-119">表 2 中指定的可能值。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="4bfd6-120">**表 2。X ClientCanHandle 标头值**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="4bfd6-121">**X ClientCanHandle 值 （不区分大小写）**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="4bfd6-122">**服务器的最低版本**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-122">**Minimum server version**</span></span>|<span data-ttu-id="4bfd6-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="4bfd6-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4bfd6-124">协商</span><span class="sxs-lookup"><span data-stu-id="4bfd6-124">Negotiate</span></span>  <br/> |<span data-ttu-id="4bfd6-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="4bfd6-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="4bfd6-126">如果存在此值时，服务器将[AuthPackage (POX)](authpackage-pox.md)元素中返回的值为"协商"，如果服务器配置为接受协商身份验证。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="4bfd6-127">如果此值不存在，则服务器不会**AuthPackage**元素中返回的值为"协商"。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="4bfd6-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="4bfd6-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="4bfd6-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="4bfd6-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="4bfd6-130">如果存在此值时，服务器将返回与[类型 (POX)](type-pox.md)元素设置为"EXHTTP"，如果将服务器配置为接受 RPC/HTTP 连接[协议 (POX)](protocol-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="4bfd6-131">如果此值不存在，则服务器不会返回**协议**具有元素的**类型**元素设置为"EXHTTP"。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="4bfd6-132">请求元素</span><span class="sxs-lookup"><span data-stu-id="4bfd6-132">Request elements</span></span>

<span data-ttu-id="4bfd6-133">在请求正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="4bfd6-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="4bfd6-134">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="4bfd6-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="4bfd6-135">请求 (POX)</span><span class="sxs-lookup"><span data-stu-id="4bfd6-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="4bfd6-136">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="4bfd6-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="4bfd6-137">EMailAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="4bfd6-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="4bfd6-138">[LegacyDN (POX)](legacydn-pox.md)元素可用于代替的[电子邮件地址 (POX)](emailaddress-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="4bfd6-139">版本差异</span><span class="sxs-lookup"><span data-stu-id="4bfd6-139">Version differences</span></span>

<span data-ttu-id="4bfd6-140">X MapiHttpCapability 标头位于 Office 365，Exchange Online 和本地开头的 Exchange 版本生成 15.00.0847.032 (Exchange Server 2013 SP1)。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="4bfd6-141">X ClientCanHandle 标头位于 Office 365，Exchange Online 和本地开头的 Exchange 版本生成 15.00.0995.014。</span><span class="sxs-lookup"><span data-stu-id="4bfd6-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4bfd6-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4bfd6-142">See also</span></span>



[<span data-ttu-id="4bfd6-143">Exchange POX 自动发现响应</span><span class="sxs-lookup"><span data-stu-id="4bfd6-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="4bfd6-144">Exchange POX 自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="4bfd6-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="4bfd6-145">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="4bfd6-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

