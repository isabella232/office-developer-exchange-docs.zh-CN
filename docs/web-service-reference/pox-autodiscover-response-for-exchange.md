---
title: Exchange POX 自动发现响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 08c6c5a2-a67a-4141-a8bd-1b5d560b90a7
description: 自动发现响应中包含对包含用于建立与 Exchange Web Services (EWS) 的绑定的 Url 的列表的自动发现请求的响应。
ms.openlocfilehash: d9f8a5cc86efaa4dceda7385164872ecc5409252
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826863"
---
# <a name="pox-autodiscover-response-for-exchange"></a><span data-ttu-id="5f89c-103">Exchange POX 自动发现响应</span><span class="sxs-lookup"><span data-stu-id="5f89c-103">POX Autodiscover response for Exchange</span></span>

<span data-ttu-id="5f89c-104">自动发现响应中包含对包含用于建立与 Exchange Web Services (EWS) 的绑定的 Url 的列表的自动发现请求的响应。</span><span class="sxs-lookup"><span data-stu-id="5f89c-104">The Autodiscover response contains a response to an Autodiscover request that includes a list of URLs that are used to establish a binding with Exchange Web Services (EWS).</span></span>
  
## <a name="autodiscover-response-example"></a><span data-ttu-id="5f89c-105">自动发现响应示例</span><span class="sxs-lookup"><span data-stu-id="5f89c-105">Autodiscover response example</span></span>

### <a name="description"></a><span data-ttu-id="5f89c-106">说明</span><span class="sxs-lookup"><span data-stu-id="5f89c-106">Description</span></span>

<span data-ttu-id="5f89c-107">下面的示例演示了成功的自动发现响应。</span><span class="sxs-lookup"><span data-stu-id="5f89c-107">The following example shows a successful Autodiscover response.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f89c-108">代码</span><span class="sxs-lookup"><span data-stu-id="5f89c-108">Code</span></span>

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>First Last</DisplayName>
      <LegacyDN>/o=contoso/ou=First Administrative Group/cn=Recipients/cn=iuser885646</LegacyDN>
      <DeploymentId>644560b8-a1ce-429c-8ace-23395843f701</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>MBX-SERVER.mail.internal.contoso.com</Server>
        <ServerDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER</ServerDN>
        <ServerVersion>72008287</ServerVersion>
        <MdbDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER/cn=Microsoft Private MDB</MdbDN>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>Exchange.contoso.com</Server>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-01-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-02-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Basic">https://cas-04-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-05-server.mail.internal.contoso.com/owa</OWAUrl>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

### <a name="comments"></a><span data-ttu-id="5f89c-109">注释</span><span class="sxs-lookup"><span data-stu-id="5f89c-109">Comments</span></span>

<span data-ttu-id="5f89c-110">若要将绑定到 Exchange Web 服务，使用标识[ASUrl (POX)](asurl-pox.md)元素的 URL。</span><span class="sxs-lookup"><span data-stu-id="5f89c-110">To bind to Exchange Web Services, use the URL identified by the [ASUrl (POX)](asurl-pox.md) element.</span></span> 
  
### <a name="response-element"></a><span data-ttu-id="5f89c-111">Response 元素</span><span class="sxs-lookup"><span data-stu-id="5f89c-111">Response Element</span></span>

<span data-ttu-id="5f89c-112">响应正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f89c-112">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="5f89c-113">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-113">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="5f89c-114">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-114">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="5f89c-115">用户 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-115">User (POX)</span></span>](user-pox.md)
    
- [<span data-ttu-id="5f89c-116">DisplayName (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-116">DisplayName (POX)</span></span>](displayname-pox.md)
    
- [<span data-ttu-id="5f89c-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-117">LegacyDN (POX)</span></span>](legacydn-pox.md)
    
- [<span data-ttu-id="5f89c-118">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-118">DeploymentId (POX)</span></span>](deploymentid-pox.md)
    
- [<span data-ttu-id="5f89c-119">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-119">Account (POX)</span></span>](account-pox.md)
    
- [<span data-ttu-id="5f89c-120">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-120">AccountType (POX)</span></span>](accounttype-pox.md)
    
- [<span data-ttu-id="5f89c-121">操作 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-121">Action (POX)</span></span>](action-pox.md)
    
- [<span data-ttu-id="5f89c-122">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-122">Protocol (POX)</span></span>](protocol-pox.md)
    
- [<span data-ttu-id="5f89c-123">类型 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-123">Type (POX)</span></span>](type-pox.md)
    
- [<span data-ttu-id="5f89c-124">服务器 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-124">Server (POX)</span></span>](server-pox.md)
    
- [<span data-ttu-id="5f89c-125">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-125">ServerDN (POX)</span></span>](serverdn-pox.md)
    
- [<span data-ttu-id="5f89c-126">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-126">ServerVersion (POX)</span></span>](serverversion-pox.md)
    
- [<span data-ttu-id="5f89c-127">MdbDN (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-127">MdbDN (POX)</span></span>](mdbdn-pox.md)
    
- [<span data-ttu-id="5f89c-128">ASUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-128">ASUrl (POX)</span></span>](asurl-pox.md)
    
- [<span data-ttu-id="5f89c-129">OOFUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-129">OOFUrl (POX)</span></span>](oofurl-pox.md)
    
- [<span data-ttu-id="5f89c-130">UMUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-130">UMUrl (POX)</span></span>](umurl-pox.md)
    
- [<span data-ttu-id="5f89c-131">OABUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-131">OABUrl (POX)</span></span>](oaburl-pox.md)
    
- [<span data-ttu-id="5f89c-132">内部 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-132">Internal (POX)</span></span>](internal-pox.md)
    
- [<span data-ttu-id="5f89c-133">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-133">OWAUrl (POX)</span></span>](owaurl-pox.md)
    
## <a name="autodiscover-error-response-example"></a><span data-ttu-id="5f89c-134">自动发现错误响应示例</span><span class="sxs-lookup"><span data-stu-id="5f89c-134">Autodiscover Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5f89c-135">说明</span><span class="sxs-lookup"><span data-stu-id="5f89c-135">Description</span></span>

<span data-ttu-id="5f89c-136">下面的示例演示了自动发现错误响应。</span><span class="sxs-lookup"><span data-stu-id="5f89c-136">The following example shows an Autodiscover error response.</span></span>
  
### <a name="code"></a><span data-ttu-id="5f89c-137">代码</span><span class="sxs-lookup"><span data-stu-id="5f89c-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
    <Error Time="21:25:04.8897083" Id="4130155072">
      <ErrorCode>600</ErrorCode>
      <Message>Invalid Request</Message>
      <DebugData />
    </Error>
  </Response>
</Autodiscover>
```

### <a name="error-response-element"></a><span data-ttu-id="5f89c-138">错误的 response 元素</span><span class="sxs-lookup"><span data-stu-id="5f89c-138">Error response element</span></span>

<span data-ttu-id="5f89c-139">响应正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="5f89c-139">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="5f89c-140">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-140">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="5f89c-141">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-141">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="5f89c-142">错误 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-142">Error (POX)</span></span>](error-pox.md)
    
- [<span data-ttu-id="5f89c-143">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-143">ErrorCode (POX)</span></span>](errorcode-pox.md)
    
- [<span data-ttu-id="5f89c-144">消息 (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-144">Message (POX)</span></span>](message-pox.md)
    
- [<span data-ttu-id="5f89c-145">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="5f89c-145">DebugData (POX)</span></span>](debugdata-pox.md)
    
## <a name="see-also"></a><span data-ttu-id="5f89c-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f89c-146">See also</span></span>

- [<span data-ttu-id="5f89c-147">Exchange POX 自动发现请求</span><span class="sxs-lookup"><span data-stu-id="5f89c-147">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
- [<span data-ttu-id="5f89c-148">Exchange POX 自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="5f89c-148">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md) 
- [<span data-ttu-id="5f89c-149">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f89c-149">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

