---
title: Exchange 的 POX 自动发现请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: 自动发现请求包含对用户的客户端访问配置的查询。
ms.openlocfilehash: b2138f9813c7b75aef9afb90089b9b874aac7532
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461665"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="9e476-103">Exchange 的 POX 自动发现请求</span><span class="sxs-lookup"><span data-stu-id="9e476-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="9e476-104">自动发现请求包含对用户的客户端访问配置的查询。</span><span class="sxs-lookup"><span data-stu-id="9e476-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="9e476-105">自动发现请求示例</span><span class="sxs-lookup"><span data-stu-id="9e476-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="9e476-106">说明</span><span class="sxs-lookup"><span data-stu-id="9e476-106">Description</span></span>

<span data-ttu-id="9e476-107">以下 XML 示例显示了自动发现请求正文。</span><span class="sxs-lookup"><span data-stu-id="9e476-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="9e476-108">代码</span><span class="sxs-lookup"><span data-stu-id="9e476-108">Code</span></span>

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="9e476-109">请求标头</span><span class="sxs-lookup"><span data-stu-id="9e476-109">Request Headers</span></span>

<span data-ttu-id="9e476-110">在发送自动发现请求时，以下 HTTP 标头是可选的。</span><span class="sxs-lookup"><span data-stu-id="9e476-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="9e476-111">**表1。HTTP 请求标头**</span><span class="sxs-lookup"><span data-stu-id="9e476-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="9e476-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="9e476-112">**Header**</span></span>|<span data-ttu-id="9e476-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e476-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e476-114">X-MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="9e476-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="9e476-115">如果存在并设置为 "1"，则指示客户端正在请求可用于通过使用 MAPI/HTTP 协议连接到服务器的信息。</span><span class="sxs-lookup"><span data-stu-id="9e476-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="9e476-116">此标头适用于实现 MAPI/HTTP 协议的客户端。</span><span class="sxs-lookup"><span data-stu-id="9e476-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="9e476-117">X-ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="9e476-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="9e476-118">此标头包含客户端支持的功能的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="9e476-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="9e476-119">表2中指定了可能的值。</span><span class="sxs-lookup"><span data-stu-id="9e476-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="9e476-120">**表2。ClientCanHandle 标头值**</span><span class="sxs-lookup"><span data-stu-id="9e476-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="9e476-121">**X-ClientCanHandle 值（不区分大小写）**</span><span class="sxs-lookup"><span data-stu-id="9e476-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="9e476-122">**最低服务器版本**</span><span class="sxs-lookup"><span data-stu-id="9e476-122">**Minimum server version**</span></span>|<span data-ttu-id="9e476-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e476-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e476-124">沟通</span><span class="sxs-lookup"><span data-stu-id="9e476-124">Negotiate</span></span>  <br/> |<span data-ttu-id="9e476-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="9e476-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="9e476-126">如果此值存在，如果服务器配置为接受协商身份验证，则服务器将在[AuthPackage （POX）](authpackage-pox.md)元素中返回值 "Negotiate"。</span><span class="sxs-lookup"><span data-stu-id="9e476-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="9e476-127">如果此值不存在，则服务器将不会在**AuthPackage**元素中返回 "Negotiate" 值。</span><span class="sxs-lookup"><span data-stu-id="9e476-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="9e476-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="9e476-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="9e476-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="9e476-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="9e476-130">如果此值存在，则服务器将返回一个[Protocol （POX）](protocol-pox.md)元素，其中如果将服务器配置为接受 RPC/HTTP 连接，则该服务器会将[类型（POX）](type-pox.md)元素设置为 "EXHTTP"。</span><span class="sxs-lookup"><span data-stu-id="9e476-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="9e476-131">如果不存在此值，则服务器将不会返回**Type**元素设置为 "EXHTTP" 的**协议**元素。</span><span class="sxs-lookup"><span data-stu-id="9e476-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="9e476-132">Request 元素</span><span class="sxs-lookup"><span data-stu-id="9e476-132">Request elements</span></span>

<span data-ttu-id="9e476-133">请求正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="9e476-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="9e476-134">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="9e476-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="9e476-135">请求（POX）</span><span class="sxs-lookup"><span data-stu-id="9e476-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="9e476-136">AcceptableResponseSchema （POX）</span><span class="sxs-lookup"><span data-stu-id="9e476-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="9e476-137">EMailAddress （POX）</span><span class="sxs-lookup"><span data-stu-id="9e476-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="9e476-138">可以使用[LegacyDN （POX）](legacydn-pox.md)元素代替[EMailAddress （POX）](emailaddress-pox.md)元素。</span><span class="sxs-lookup"><span data-stu-id="9e476-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="9e476-139">版本差异</span><span class="sxs-lookup"><span data-stu-id="9e476-139">Version differences</span></span>

<span data-ttu-id="9e476-140">在 Office 365、Exchange Online 和内部部署版本中，MapiHttpCapability 标头适用于以 build 15.00.0847.032 （Exchange Server 2013 SP1）开头的 Exchange Online 和内部部署版本。</span><span class="sxs-lookup"><span data-stu-id="9e476-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="9e476-141">在 Office 365、Exchange Online 和内部部署版本中，ClientCanHandle 标头可从生成15.00.0995.014 开始。</span><span class="sxs-lookup"><span data-stu-id="9e476-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9e476-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e476-142">See also</span></span>



[<span data-ttu-id="9e476-143">Exchange 的 POX 自动发现响应</span><span class="sxs-lookup"><span data-stu-id="9e476-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="9e476-144">Exchange 的 POX 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="9e476-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="9e476-145">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="9e476-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

