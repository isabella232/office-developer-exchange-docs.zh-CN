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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455623"
---
# <a name="getfederationinformation-operation-soap"></a>GetFederationInformation 操作 (SOAP)

**GetFederationInformation**操作提供有关组织的联合身份验证状态的信息，例如，在请求此组织的目标令牌时要使用的目标 URI，以及组织同时也是联合的其他域。 
  
只有联合组织可以将日历、联系人和邮件共享给外部用户。
  
## <a name="getfederationinformation-request-example"></a>GetFederationInformation 请求示例

### <a name="description"></a>说明

以下示例的**GetFederationInformation**请求显示了用户的联合身份验证信息的请求。 客户端将此请求发送到服务器。 
  
### <a name="code"></a>代码

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

### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [GetFederationInformationRequestMessage （SOAP）](getfederationinformationrequestmessage-soap.md)
    
- [请求 (SOAP)](request-soap.md)
    
- [域（SOAP）](domain-soap.md)
    
## <a name="getfederationinformation-response-example"></a>GetFederationInformation 响应示例

### <a name="description"></a>说明

下面的示例演示对服务器发送到客户端的**GetFederationInformation**请求的成功响应。 
  
### <a name="code"></a>代码

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

### <a name="response-elements"></a>Response 元素

响应中使用以下元素：
  
- [GetFederationInformationResponseMessage （SOAP）](getfederationinformationresponsemessage-soap.md)
    
- [响应（SOAP）](response-soap.md)
    
- [ErrorCode （SOAP）](errorcode-soap.md)
    
- [ErrorMessage （SOAP）](errormessage-soap.md)
    
- [ApplicationUri （SOAP）](applicationuri-soap.md)
    
- [域（SOAP）](domains-soap.md)
    
- [域（SOAP）](domain-soap.md)
    
## <a name="see-also"></a>另请参阅

- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

