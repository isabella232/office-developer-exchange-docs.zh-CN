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
# <a name="getdomainsettings-operation-soap"></a>GetDomainSettings 操作 (SOAP)

**GetDomainSettings**操作为用户检索域的指定设置。 自动发现将返回要发现的域以及这些域的请求设置。 
  
## <a name="getdomainsettings-request-example"></a>GetDomainSettings 请求示例

### <a name="description"></a>说明

以下示例的**GetDomainSettings**请求显示了对用户的**ExternalEWSUrl**域设置的请求。 客户端将此请求发送到服务器。 
  
### <a name="code"></a>代码

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

### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [GetDomainSettingsRequestMessage （SOAP）](getdomainsettingsrequestmessage-soap.md)
    
- [请求 (SOAP)](request-soap.md)
    
- [域（SOAP）](domains-soap.md)
    
- [域（SOAP）](domain-soap.md)
    
- [RequestedSettings （SOAP）](requestedsettings-soap.md)
    
- [设置（SOAP）](setting-soap.md)
    
## <a name="getdomainsettings-response-example"></a>GetDomainSettings 响应示例

### <a name="description"></a>说明

下面的示例演示对服务器发送到客户端的**GetDomainSettings**请求的成功响应。 
  
### <a name="code"></a>代码

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

### <a name="response-elements"></a>Response 元素

响应中使用以下元素：
  
- [GetDomainSettingsResponseMessage （SOAP）](getdomainsettingsresponsemessage-soap.md)
    
- [响应（SOAP）](response-soap.md)
    
- [ErrorCode （SOAP）](errorcode-soap.md)
    
- [ErrorMessage （SOAP）](errormessage-soap.md)
    
- [DomainResponses （SOAP）](domainresponses-soap.md)
    
- [DomainResponse （SOAP）](domainresponse-soap.md)
    
- [DomainSettingErrors （SOAP）](domainsettingerrors-soap.md)
    
- [DomainSettings （SOAP）](domainsettings-soap.md)
    
- [DomainSetting （SOAP）](domainsetting-soap.md)
    
- [名称（SOAP）](name-soap.md)
    
- [Value （SOAP）](value-soap.md)
    
- [RedirectTarget （SOAP）](redirecttarget-soap.md)
    
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

