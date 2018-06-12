---
title: GetClientAccessToken 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 086876cc-e22c-4e89-89f9-19e78af51217
description: 查找信息 GetClientAccessToken EWS 操作。
ms.openlocfilehash: afa9a315a8421f31c345c9547a5d80bed41e9fbc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754481"
---
# <a name="getclientaccesstoken-operation"></a><span data-ttu-id="c5531-103">GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="c5531-103">GetClientAccessToken operation</span></span>

<span data-ttu-id="c5531-104">查找有关**GetClientAccessToken** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="c5531-104">Find information about the **GetClientAccessToken** EWS operation.</span></span> 
  
<span data-ttu-id="c5531-105">**GetClientAccessToken**操作获取客户端访问 outlook 邮件应用程序令牌。</span><span class="sxs-lookup"><span data-stu-id="c5531-105">The **GetClientAccessToken** operation gets a client access token for a mail app for Outlook.</span></span> 
  
<span data-ttu-id="c5531-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="c5531-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getclientaccesstoken-operation"></a><span data-ttu-id="c5531-107">使用 GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="c5531-107">Using the GetClientAccessToken operation</span></span>

<span data-ttu-id="c5531-108">**GetClientAccessToken**操作请求采用两个必需的参数： 应用程序和标记类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="c5531-108">The **GetClientAccessToken** operation request takes two required arguments: the identifier of the app, and the token type.</span></span> <span data-ttu-id="c5531-109">您可以使用[GetAppManifests 操作](getappmanifests-operation.md)请求的应用程序标识符。</span><span class="sxs-lookup"><span data-stu-id="c5531-109">You can use the [GetAppManifests operation](getappmanifests-operation.md) to request the app identifier.</span></span> 
  
### <a name="getclientaccesstoken-operation-soap-headers"></a><span data-ttu-id="c5531-110">GetClientAccessToken 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="c5531-110">GetClientAccessToken operation SOAP headers</span></span>

<span data-ttu-id="c5531-111">**GetClientAccessToken**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="c5531-111">The **GetClientAccessToken** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="c5531-112">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="c5531-112">**Header name**</span></span>|<span data-ttu-id="c5531-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5531-113">**Element**</span></span>|<span data-ttu-id="c5531-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5531-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5531-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="c5531-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="c5531-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="c5531-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="c5531-117">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="c5531-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="c5531-118">适用于请求此标头。</span><span class="sxs-lookup"><span data-stu-id="c5531-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="c5531-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="c5531-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="c5531-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c5531-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="c5531-121">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="c5531-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="c5531-122">适用于响应此标头。</span><span class="sxs-lookup"><span data-stu-id="c5531-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getclientaccesstoken-operation-request-example-get-a-caller-identity-token"></a><span data-ttu-id="c5531-123">GetClientAccessToken 操作请求示例： 获取呼叫者标识令牌</span><span class="sxs-lookup"><span data-stu-id="c5531-123">GetClientAccessToken operation request example: Get a caller identity token</span></span>

<span data-ttu-id="c5531-124">**GetClientAccessToken**操作请求的下面的示例演示如何获取应用程序的呼叫者标识令牌。</span><span class="sxs-lookup"><span data-stu-id="c5531-124">The following example of a **GetClientAccessToken** operation request shows how to get a caller identity token for an app.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="c5531-125">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c5531-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c5531-126">GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="c5531-126">GetClientAccessToken</span></span>](getclientaccesstoken.md)
    
- [<span data-ttu-id="c5531-127">TokenRequests</span><span class="sxs-lookup"><span data-stu-id="c5531-127">TokenRequests</span></span>](tokenrequests.md)
    
- [<span data-ttu-id="c5531-128">TokenRequest</span><span class="sxs-lookup"><span data-stu-id="c5531-128">TokenRequest</span></span>](tokenrequest.md)
    
- [<span data-ttu-id="c5531-129">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="c5531-129">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="c5531-130">TokenType</span><span class="sxs-lookup"><span data-stu-id="c5531-130">TokenType</span></span>](tokentype.md)
    
## <a name="successful-getclientaccesstoken-operation-response"></a><span data-ttu-id="c5531-131">成功 GetClientAccessToken 操作响应</span><span class="sxs-lookup"><span data-stu-id="c5531-131">Successful GetClientAccessToken operation response</span></span>

<span data-ttu-id="c5531-132">下面的示例演示对**GetClientAccessToken**操作请求以获取应用程序的呼叫者标识令牌的成功响应。</span><span class="sxs-lookup"><span data-stu-id="c5531-132">The following example shows a successful response to a **GetClientAccessToken** operation request to get a caller identity token for an app.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c5531-133">本文中的令牌值具有已缩短要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c5531-133">The token values in this article have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="c5531-134">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c5531-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c5531-135">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="c5531-135">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="c5531-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c5531-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c5531-137">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c5531-137">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="c5531-138">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c5531-138">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c5531-139">令牌 (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="c5531-139">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md)
    
- [<span data-ttu-id="c5531-140">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="c5531-140">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="c5531-141">TokenType (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="c5531-141">TokenType (ClientAccessTokenType)</span></span>](tokentype-clientaccesstokentype.md)
    
- [<span data-ttu-id="c5531-142">TokenValue</span><span class="sxs-lookup"><span data-stu-id="c5531-142">TokenValue</span></span>](tokenvalue.md)
    
- [<span data-ttu-id="c5531-143">TTL (ClientAccessTokenTypeType)</span><span class="sxs-lookup"><span data-stu-id="c5531-143">TTL (ClientAccessTokenTypeType)</span></span>](ttl-clientaccesstokentypetype.md)
    
## <a name="getclientaccesstoken-operation-error-response"></a><span data-ttu-id="c5531-144">GetClientAccessToken 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="c5531-144">GetClientAccessToken operation error response</span></span>

<span data-ttu-id="c5531-145">下面的示例演示对**GetClientAccessToken**操作请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="c5531-145">The following example shows an error response to a **GetClientAccessToken** operation request.</span></span> <span data-ttu-id="c5531-146">这是要获取扩展回调令牌不适当的权限请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c5531-146">This is a response to a request to get an extension callback token without the appropriate permissions.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetClientAccessTokenResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="c5531-147">错误响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="c5531-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="c5531-148">GetClientAccessTokenResponse</span><span class="sxs-lookup"><span data-stu-id="c5531-148">GetClientAccessTokenResponse</span></span>](getclientaccesstokenresponse.md)
    
- [<span data-ttu-id="c5531-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c5531-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c5531-150">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c5531-150">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
    
- [<span data-ttu-id="c5531-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="c5531-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c5531-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c5531-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c5531-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c5531-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="c5531-154">通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="c5531-154">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5531-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5531-155">See also</span></span>

- [<span data-ttu-id="c5531-156">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="c5531-156">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="c5531-157">GetAppManifests 操作</span><span class="sxs-lookup"><span data-stu-id="c5531-157">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    
- [<span data-ttu-id="c5531-158">Outlook 外接程序</span><span class="sxs-lookup"><span data-stu-id="c5531-158">Outlook add-ins</span></span>](http://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

