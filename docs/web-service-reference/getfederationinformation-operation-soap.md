---
title: GetFederationInformation 操作 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6666a42-a18f-4e4b-beb6-b25ff62cfcc5
description: GetFederationInformation 操作提供有关组织的联合身份验证状态的信息，例如，在请求此组织的目标令牌时要使用的目标 URI，以及组织同时也是联合的其他域。
ms.openlocfilehash: 533b2f6d282e3287f4945df56b169f5bc93ff445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455623"
---
# <a name="getfederationinformation-operation-soap"></a><span data-ttu-id="bd961-103">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd961-103">GetFederationInformation operation (SOAP)</span></span>

<span data-ttu-id="bd961-104">**GetFederationInformation**操作提供有关组织的联合身份验证状态的信息，例如，在请求此组织的目标令牌时要使用的目标 URI，以及组织同时也是联合的其他域。</span><span class="sxs-lookup"><span data-stu-id="bd961-104">The **GetFederationInformation** operation provides information about the federation status of the organization, such as the target URI to be used when requesting tokens that are targeted at this organization, and the other domains that the organization has also federated.</span></span> 
  
<span data-ttu-id="bd961-105">只有联合组织可以将日历、联系人和邮件共享给外部用户。</span><span class="sxs-lookup"><span data-stu-id="bd961-105">Only federated organizations can share calendar, contacts, and messages to external users.</span></span>
  
## <a name="getfederationinformation-request-example"></a><span data-ttu-id="bd961-106">GetFederationInformation 请求示例</span><span class="sxs-lookup"><span data-stu-id="bd961-106">GetFederationInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="bd961-107">Description</span><span class="sxs-lookup"><span data-stu-id="bd961-107">Description</span></span>

<span data-ttu-id="bd961-108">以下示例的**GetFederationInformation**请求显示了用户的联合身份验证信息的请求。</span><span class="sxs-lookup"><span data-stu-id="bd961-108">The following example of a **GetFederationInformation** request shows a request for a user's federation information.</span></span> <span data-ttu-id="bd961-109">客户端将此请求发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="bd961-109">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bd961-110">代码</span><span class="sxs-lookup"><span data-stu-id="bd961-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="https://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="https://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">https://schemas.microsoft.com/
            exchange/2010/Autodiscover/Autodiscover/GetFederationInformation
        </a:Action> 
        <a:To soap:mustUnderstand="1">https://autodiscover.byfcxu-
            dom.extest.microsoft.com/autodiscover/autodiscover.svc</a:To> 
        <a:ReplyTo>
            <a:Address>http://www.w3.org/2005/08/addressing/anonymous</a:Address> 
        </a:ReplyTo> 
    </soap:Header> 
    <soap:Body> 
        <GetFederationInformationRequestMessage 
            xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="bd961-111">Request 元素</span><span class="sxs-lookup"><span data-stu-id="bd961-111">Request elements</span></span>

<span data-ttu-id="bd961-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="bd961-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bd961-113">GetFederationInformationRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-113">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md)
    
- [<span data-ttu-id="bd961-114">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd961-114">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="bd961-115">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-115">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a><span data-ttu-id="bd961-116">GetFederationInformation 响应示例</span><span class="sxs-lookup"><span data-stu-id="bd961-116">GetFederationInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="bd961-117">Description</span><span class="sxs-lookup"><span data-stu-id="bd961-117">Description</span></span>

<span data-ttu-id="bd961-118">下面的示例演示对服务器发送到客户端的**GetFederationInformation**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="bd961-118">The following example shows a successful response to the **GetFederationInformation** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="bd961-119">代码</span><span class="sxs-lookup"><span data-stu-id="bd961-119">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage/> 
                <ApplicationUri>BYFCXU-DOM.EXTEST.MICROSOFT.COM</ApplicationUri> 
                <Domains> 
                    <Domain>contoso.com</Domain> 
                    <Domain>europe.contoso.com</Domain> 
                    <Domain>americas.contoso.com</Domain> 
                    <Domain>contosolive.com</Domain> 
                </Domains> 
            </Response> 
        </GetFederationInformationResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="bd961-120">Response 元素</span><span class="sxs-lookup"><span data-stu-id="bd961-120">Response elements</span></span>

<span data-ttu-id="bd961-121">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="bd961-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bd961-122">GetFederationInformationResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-122">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md)
    
- [<span data-ttu-id="bd961-123">响应（SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-123">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="bd961-124">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-124">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="bd961-125">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-125">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="bd961-126">ApplicationUri （SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-126">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md)
    
- [<span data-ttu-id="bd961-127">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-127">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="bd961-128">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="bd961-128">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="bd961-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd961-129">See also</span></span>

- [<span data-ttu-id="bd961-130">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd961-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="bd961-131">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bd961-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

