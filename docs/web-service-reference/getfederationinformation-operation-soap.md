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
description: GetFederationInformation 操作提供的组织，如的目标 URI 用于请求令牌，并针对此组织和组织还具有其他域联盟状态的信息联盟。
ms.openlocfilehash: bf38b2f2b3db3e38b9b0157d1677efe4fc274e1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754560"
---
# <a name="getfederationinformation-operation-soap"></a><span data-ttu-id="d47f6-103">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-103">GetFederationInformation operation (SOAP)</span></span>

<span data-ttu-id="d47f6-104">**GetFederationInformation**操作提供组织的联合身份验证状态的信息，如目标 URI 用于请求令牌的了面向此组织和其他域的组织具有还联盟。</span><span class="sxs-lookup"><span data-stu-id="d47f6-104">The **GetFederationInformation** operation provides information about the federation status of the organization, such as the target URI to be used when requesting tokens that are targeted at this organization, and the other domains that the organization has also federated.</span></span> 
  
<span data-ttu-id="d47f6-105">仅联盟的组织可以共享日历、 联系人和外部用户的邮件。</span><span class="sxs-lookup"><span data-stu-id="d47f6-105">Only federated organizations can share calendar, contacts, and messages to external users.</span></span>
  
## <a name="getfederationinformation-request-example"></a><span data-ttu-id="d47f6-106">GetFederationInformation 请求示例</span><span class="sxs-lookup"><span data-stu-id="d47f6-106">GetFederationInformation request example</span></span>

### <a name="description"></a><span data-ttu-id="d47f6-107">说明</span><span class="sxs-lookup"><span data-stu-id="d47f6-107">Description</span></span>

<span data-ttu-id="d47f6-108">**GetFederationInformation**请求的下面的示例演示请求用户的联合身份验证信息。</span><span class="sxs-lookup"><span data-stu-id="d47f6-108">The following example of a **GetFederationInformation** request shows a request for a user's federation information.</span></span> <span data-ttu-id="d47f6-109">客户端向服务器发送此请求。</span><span class="sxs-lookup"><span data-stu-id="d47f6-109">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d47f6-110">代码</span><span class="sxs-lookup"><span data-stu-id="d47f6-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:exm="http://schemas.microsoft.com/exchange/services/2006/messages"
           xmlns:ext="http://schemas.microsoft.com/exchange/services/2006/types"
           xmlns:a="http://www.w3.org/2005/08/addressing"
           xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema"> 
    <soap:Header> 
        <a:MessageID>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:MessageID> 
        <a:Action soap:mustUnderstand="1">http://schemas.microsoft.com/
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
            xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Request> 
                <Domain>contoso.com</Domain> 
            </Request> 
        </GetFederationInformationRequestMessage>
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="d47f6-111">请求元素</span><span class="sxs-lookup"><span data-stu-id="d47f6-111">Request elements</span></span>

<span data-ttu-id="d47f6-112">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d47f6-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="d47f6-113">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-113">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md)
    
- [<span data-ttu-id="d47f6-114">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-114">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="d47f6-115">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-115">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a><span data-ttu-id="d47f6-116">GetFederationInformation 响应示例</span><span class="sxs-lookup"><span data-stu-id="d47f6-116">GetFederationInformation response example</span></span>

### <a name="description"></a><span data-ttu-id="d47f6-117">说明</span><span class="sxs-lookup"><span data-stu-id="d47f6-117">Description</span></span>

<span data-ttu-id="d47f6-118">下面的示例演示对**GetFederationInformation**请求服务器发送到客户端的成功响应。</span><span class="sxs-lookup"><span data-stu-id="d47f6-118">The following example shows a successful response to the **GetFederationInformation** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="d47f6-119">代码</span><span class="sxs-lookup"><span data-stu-id="d47f6-119">Code</span></span>

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
xmlns:a="http://www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">
            http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetFederationInformationResponse
        </a:Action> 
        <a:RelatesTo>urn:uuid:6389558d-9e05-465e-ade9-aae14c4bcd10</a:RelatesTo> 
    </s:Header> 
    <s:Body> 
        <GetFederationInformationResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover"> 
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

### <a name="response-elements"></a><span data-ttu-id="d47f6-120">响应元素</span><span class="sxs-lookup"><span data-stu-id="d47f6-120">Response elements</span></span>

<span data-ttu-id="d47f6-121">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="d47f6-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d47f6-122">GetFederationInformationResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-122">GetFederationInformationResponseMessage (SOAP)</span></span>](getfederationinformationresponsemessage-soap.md)
    
- [<span data-ttu-id="d47f6-123">响应 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-123">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="d47f6-124">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-124">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="d47f6-125">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-125">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="d47f6-126">ApplicationUri (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-126">ApplicationUri (SOAP)</span></span>](applicationuri-soap.md)
    
- [<span data-ttu-id="d47f6-127">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-127">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="d47f6-128">域 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-128">Domain (SOAP)</span></span>](domain-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="d47f6-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d47f6-129">See also</span></span>

- [<span data-ttu-id="d47f6-130">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="d47f6-131">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d47f6-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

