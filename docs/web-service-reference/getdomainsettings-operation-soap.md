---
title: GetDomainSettings 操作 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a6f4a53d-d7f6-4ad1-8afb-78745c500eaa
description: GetDomainSettings 操作为用户检索域的指定设置。 自动发现将返回要发现的域以及这些域的请求设置。
ms.openlocfilehash: fd655e088b73372bc1dd68a740ebc2b516d1804a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460965"
---
# <a name="getdomainsettings-operation-soap"></a><span data-ttu-id="a18eb-104">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a18eb-104">GetDomainSettings operation (SOAP)</span></span>

<span data-ttu-id="a18eb-105">**GetDomainSettings**操作为用户检索域的指定设置。</span><span class="sxs-lookup"><span data-stu-id="a18eb-105">The **GetDomainSettings** operation retrieves the specified settings of the domain for the user.</span></span> <span data-ttu-id="a18eb-106">自动发现将返回要发现的域以及这些域的请求设置。</span><span class="sxs-lookup"><span data-stu-id="a18eb-106">Autodiscover returns the domains that are to be discovered and the requested settings of those domains.</span></span> 
  
## <a name="getdomainsettings-request-example"></a><span data-ttu-id="a18eb-107">GetDomainSettings 请求示例</span><span class="sxs-lookup"><span data-stu-id="a18eb-107">GetDomainSettings request example</span></span>

### <a name="description"></a><span data-ttu-id="a18eb-108">说明</span><span class="sxs-lookup"><span data-stu-id="a18eb-108">Description</span></span>

<span data-ttu-id="a18eb-109">以下示例的**GetDomainSettings**请求显示了对用户的**ExternalEWSUrl**域设置的请求。</span><span class="sxs-lookup"><span data-stu-id="a18eb-109">The following example of a **GetDomainSettings** request shows a request for a user's **ExternalEWSUrl** domain settings.</span></span> <span data-ttu-id="a18eb-110">客户端将此请求发送到服务器。</span><span class="sxs-lookup"><span data-stu-id="a18eb-110">The client sends this request to the server.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a18eb-111">代码</span><span class="sxs-lookup"><span data-stu-id="a18eb-111">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?> 
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soap:Header> 
        <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
        <wsa:Action>https://schemas.microsoft.com/exchange/2010/
            Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
        <wsa:To>
            https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc
        </wsa:To>
    </soap:Header> 
    <soap:Body> 
        <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com
            /exchange/2010/Autodiscover"> 
            <a:Request> 
                <a:Domains> 
                    <a:Domain>contoso.com<</a:Domain> 
                </a:Domains> 
                <a:RequestedSettings> 
                    <a:Setting>ExternalEwsUrl</a:Setting> 
                </a:RequestedSettings> 
            </a:Request> 
        </a:GetDomainSettingsRequestMessage> 
    </soap:Body> 
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="a18eb-112">Request 元素</span><span class="sxs-lookup"><span data-stu-id="a18eb-112">Request elements</span></span>

<span data-ttu-id="a18eb-113">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a18eb-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="a18eb-114">GetDomainSettingsRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-114">GetDomainSettingsRequestMessage (SOAP)</span></span>](getdomainsettingsrequestmessage-soap.md)
    
- [<span data-ttu-id="a18eb-115">请求 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a18eb-115">Request (SOAP)</span></span>](request-soap.md)
    
- [<span data-ttu-id="a18eb-116">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-116">Domains (SOAP)</span></span>](domains-soap.md)
    
- [<span data-ttu-id="a18eb-117">域（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-117">Domain (SOAP)</span></span>](domain-soap.md)
    
- [<span data-ttu-id="a18eb-118">RequestedSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-118">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md)
    
- [<span data-ttu-id="a18eb-119">设置（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-119">Setting (SOAP)</span></span>](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a><span data-ttu-id="a18eb-120">GetDomainSettings 响应示例</span><span class="sxs-lookup"><span data-stu-id="a18eb-120">GetDomainSettings response example</span></span>

### <a name="description"></a><span data-ttu-id="a18eb-121">说明</span><span class="sxs-lookup"><span data-stu-id="a18eb-121">Description</span></span>

<span data-ttu-id="a18eb-122">下面的示例演示对服务器发送到客户端的**GetDomainSettings**请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a18eb-122">The following example shows a successful response to the **GetDomainSettings** request that the server sends to the client.</span></span> 
  
### <a name="code"></a><span data-ttu-id="a18eb-123">代码</span><span class="sxs-lookup"><span data-stu-id="a18eb-123">Code</span></span>

```XML
//www.w3.org/2005/08/addressing"> 
    <s:Header> 
        <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/ 
            Autodiscover/Autodiscover/GetDomainSettingsResponse
        </a:Action> 
        <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
            xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
        <h:MajorVersion>14</h:MajorVersion> 
        <h:MinorVersion>0</h:MinorVersion> 
        <h:MajorBuildNumber>639</h:MajorBuildNumber> 
        <h:MinorBuildNumber>20</h:MinorBuildNumber> 
        <h:Version>Exchange2010</h:Version> 
        </h:ServerVersionInfo>
    </s:Header> 
    <s:Body> 
        <GetDomainSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover"> 
            <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance"> 
                <ErrorCode>NoError</ErrorCode> 
                <ErrorMessage /> 
                <DomainResponses> 
                    <DomainResponse> 
                        <ErrorCode>NoError</ErrorCode> 
                        <ErrorMessage>No error.</ErrorMessage> 
                        <DomainSettingErrors /> 
                        <DomainSettings> 
                            <DomainSetting i:type="DomainStringSetting"> 
                                <Name>ExternalEwsUrl</Name> 
                                <Value>https://emea.mail.microsoft.com/EWS/Exchange.asmx</Value> 
                            </DomainSetting> 
                        </DomainSettings> 
                        <RedirectTarget i:nil="true" /> 
                    </DomainResponse> 
                </DomainResponses> 
            </Response> 
        </GetDomainSettingsResponseMessage> 
    </s:Body> 
</s:Envelope>
```

### <a name="response-elements"></a><span data-ttu-id="a18eb-124">Response 元素</span><span class="sxs-lookup"><span data-stu-id="a18eb-124">Response elements</span></span>

<span data-ttu-id="a18eb-125">响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="a18eb-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="a18eb-126">GetDomainSettingsResponseMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-126">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md)
    
- [<span data-ttu-id="a18eb-127">响应（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-127">Response (SOAP)</span></span>](response-soap.md)
    
- [<span data-ttu-id="a18eb-128">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-128">ErrorCode (SOAP)</span></span>](errorcode-soap.md)
    
- [<span data-ttu-id="a18eb-129">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-129">ErrorMessage (SOAP)</span></span>](errormessage-soap.md)
    
- [<span data-ttu-id="a18eb-130">DomainResponses （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md)
    
- [<span data-ttu-id="a18eb-131">DomainResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-131">DomainResponse (SOAP)</span></span>](domainresponse-soap.md)
    
- [<span data-ttu-id="a18eb-132">DomainSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-132">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md)
    
- [<span data-ttu-id="a18eb-133">DomainSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-133">DomainSettings (SOAP)</span></span>](domainsettings-soap.md)
    
- [<span data-ttu-id="a18eb-134">DomainSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-134">DomainSetting (SOAP)</span></span>](domainsetting-soap.md)
    
- [<span data-ttu-id="a18eb-135">名称（SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-135">Name (SOAP)</span></span>](name-soap.md)
    
- [<span data-ttu-id="a18eb-136">Value （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-136">Value (SOAP)</span></span>](value-soap.md)
    
- [<span data-ttu-id="a18eb-137">RedirectTarget （SOAP）</span><span class="sxs-lookup"><span data-stu-id="a18eb-137">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md)
    
## <a name="see-also"></a><span data-ttu-id="a18eb-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a18eb-138">See also</span></span>



[<span data-ttu-id="a18eb-139">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a18eb-139">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="a18eb-140">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a18eb-140">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)

