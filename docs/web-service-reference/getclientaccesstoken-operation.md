---
title: GetClientAccessToken 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 086876cc-e22c-4e89-89f9-19e78af51217
description: 查找有关 GetClientAccessToken EWS 操作的信息。
ms.openlocfilehash: 2d49d675fcedb0e7e8312a9715f095c47fcf3d77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462036"
---
# <a name="getclientaccesstoken-operation"></a><span data-ttu-id="f3068-103">GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="f3068-103">GetClientAccessToken operation</span></span>

<span data-ttu-id="f3068-104">查找有关**GetClientAccessToken** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="f3068-104">Find information about the **GetClientAccessToken** EWS operation.</span></span> 
  
<span data-ttu-id="f3068-105">**GetClientAccessToken**操作获取适用于 Outlook 的邮件应用程序的客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="f3068-105">The **GetClientAccessToken** operation gets a client access token for a mail app for Outlook.</span></span> 
  
<span data-ttu-id="f3068-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="f3068-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getclientaccesstoken-operation"></a><span data-ttu-id="f3068-107">使用 GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="f3068-107">Using the GetClientAccessToken operation</span></span>

<span data-ttu-id="f3068-108">**GetClientAccessToken**操作请求采用两个必需参数：应用程序的标识符和令牌类型。</span><span class="sxs-lookup"><span data-stu-id="f3068-108">The **GetClientAccessToken** operation request takes two required arguments: the identifier of the app, and the token type.</span></span> <span data-ttu-id="f3068-109">您可以使用[getappmanifests 已操作](getappmanifests-operation.md)来请求应用程序标识符。</span><span class="sxs-lookup"><span data-stu-id="f3068-109">You can use the [GetAppManifests operation](getappmanifests-operation.md) to request the app identifier.</span></span> 
  
### <a name="getclientaccesstoken-operation-soap-headers"></a><span data-ttu-id="f3068-110">GetClientAccessToken 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="f3068-110">GetClientAccessToken operation SOAP headers</span></span>

<span data-ttu-id="f3068-111">**GetClientAccessToken**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="f3068-111">The **GetClientAccessToken** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f3068-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="f3068-112">**Header name**</span></span>|<span data-ttu-id="f3068-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f3068-113">**Element**</span></span>|<span data-ttu-id="f3068-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f3068-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f3068-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f3068-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f3068-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f3068-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f3068-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="f3068-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f3068-118">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="f3068-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f3068-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f3068-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f3068-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f3068-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f3068-121">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="f3068-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f3068-122">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="f3068-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getclientaccesstoken-operation-request-example-get-a-caller-identity-token"></a><span data-ttu-id="f3068-123">GetClientAccessToken 操作请求示例：获取呼叫方标识令牌</span><span class="sxs-lookup"><span data-stu-id="f3068-123">GetClientAccessToken operation request example: Get a caller identity token</span></span>

<span data-ttu-id="f3068-124">以下示例的**GetClientAccessToken**操作请求显示如何获取应用程序的呼叫者标识令牌。</span><span class="sxs-lookup"><span data-stu-id="f3068-124">The following example of a **GetClientAccessToken** operation request shows how to get a caller identity token for an app.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetClientAccessToken>
         <m:TokenRequests>
            <t:TokenRequest>
               <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
               <t:TokenType>CallerIdentity</t:TokenType>
            </t:TokenRequest>
         </m:TokenRequests>
      </m:GetClientAccessToken>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f3068-125">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f3068-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3068-126">GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="f3068-126">GetClientAccessToken</span></span>](getclientaccesstoken.md)
    
- [<span data-ttu-id="f3068-127">TokenRequests</span><span class="sxs-lookup"><span data-stu-id="f3068-127">TokenRequests</span></span>](tokenrequests.md)
    
- [<span data-ttu-id="f3068-128">TokenRequest</span><span class="sxs-lookup"><span data-stu-id="f3068-128">TokenRequest</span></span>](tokenrequest.md)
    
- [<span data-ttu-id="f3068-129">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="f3068-129">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="f3068-130">TokenType</span><span class="sxs-lookup"><span data-stu-id="f3068-130">TokenType</span></span>](tokentype.md)
    
## <a name="successful-getclientaccesstoken-operation-response"></a><span data-ttu-id="f3068-131">成功的 GetClientAccessToken 操作响应</span><span class="sxs-lookup"><span data-stu-id="f3068-131">Successful GetClientAccessToken operation response</span></span>

<span data-ttu-id="f3068-132">下面的示例演示对**GetClientAccessToken**操作请求的成功响应，以获取应用程序的呼叫者标识令牌。</span><span class="sxs-lookup"><span data-stu-id="f3068-132">The following example shows a successful response to a **GetClientAccessToken** operation request to get a caller identity token for an app.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f3068-133">为了保持可读性，本文中的标记值已缩短。</span><span class="sxs-lookup"><span data-stu-id="f3068-133">The token values in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Success">
               <m:ResponseCode>NoError</m:ResponseCode>
               <m:Token>
                  <t:Id>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</t:Id>
                  <t:TokenType>CallerIdentity</t:TokenType>
                  <t:TokenValue>eyJ0eXAmv0QitaJg</t:TokenValue>
                  <t:TTL>479</t:TTL>
               </m:Token>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f3068-134">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f3068-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3068-135">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="f3068-135">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="f3068-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f3068-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f3068-137">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f3068-137">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="f3068-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3068-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f3068-139">令牌（ClientAccessTokenType）</span><span class="sxs-lookup"><span data-stu-id="f3068-139">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md)
    
- [<span data-ttu-id="f3068-140">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="f3068-140">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="f3068-141">TokenType （ClientAccessTokenType）</span><span class="sxs-lookup"><span data-stu-id="f3068-141">TokenType (ClientAccessTokenType)</span></span>](tokentype-clientaccesstokentype.md)
    
- [<span data-ttu-id="f3068-142">TokenValue</span><span class="sxs-lookup"><span data-stu-id="f3068-142">TokenValue</span></span>](tokenvalue.md)
    
- [<span data-ttu-id="f3068-143">TTL （ClientAccessTokenTypeType）</span><span class="sxs-lookup"><span data-stu-id="f3068-143">TTL (ClientAccessTokenTypeType)</span></span>](ttl-clientaccesstokentypetype.md)
    
## <a name="getclientaccesstoken-operation-error-response"></a><span data-ttu-id="f3068-144">GetClientAccessToken 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="f3068-144">GetClientAccessToken operation error response</span></span>

<span data-ttu-id="f3068-145">下面的示例演示对**GetClientAccessToken**操作请求的错误响应。</span><span class="sxs-lookup"><span data-stu-id="f3068-145">The following example shows an error response to a **GetClientAccessToken** operation request.</span></span> <span data-ttu-id="f3068-146">这是对在没有适当权限的情况下获取扩展回调令牌的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f3068-146">This is a response to a request to get an extension callback token without the appropriate permissions.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
         <m:ResponseMessages>
            <m:GetClientAccessTokenResponseMessage ResponseClass="Error">
               <m:MessageText>The caller does not have enough permission for this token request.</m:MessageText>
               <m:ResponseCode>ErrorInvalidClientAccessTokenRequest</m:ResponseCode>
               <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
            </m:GetClientAccessTokenResponseMessage>
         </m:ResponseMessages>
      </m:GetClientAccessTokenResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f3068-147">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="f3068-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f3068-148">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="f3068-148">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="f3068-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f3068-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f3068-150">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f3068-150">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="f3068-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="f3068-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f3068-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f3068-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f3068-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f3068-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f3068-154">有关对 EWS 通用的其他错误代码以及特定于此操作的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="f3068-154">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3068-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f3068-155">See also</span></span>

- [<span data-ttu-id="f3068-156">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="f3068-156">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f3068-157">Getappmanifests 已操作</span><span class="sxs-lookup"><span data-stu-id="f3068-157">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    
- [<span data-ttu-id="f3068-158">Outlook 外接程序</span><span class="sxs-lookup"><span data-stu-id="f3068-158">Outlook add-ins</span></span>](https://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

