---
title: GetPhoneCallInformation 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetPhoneCallInformation
api_type:
- schema
ms.assetid: 418bd6ca-39d9-49a9-841e-7a71ede1fa51
description: GetPhoneCallInformation 操作返回有关指定电话呼叫的信息。
ms.openlocfilehash: 7cb9ecbb30e6cdd4d85b60215f40e0be5f4aaa84
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539955"
---
# <a name="getphonecallinformation-operation"></a>GetPhoneCallInformation 操作

**GetPhoneCallInformation** 操作返回有关指定电话呼叫的信息。 
  
## <a name="getphonecallinformation-request-example"></a>GetPhoneCallInformation 请求示例

### <a name="description"></a>说明

**GetPhoneCallInformation** 请求的以下示例显示如何形成请求，以获取有关特定电话呼叫的信息。 
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetPhoneCallInformation>
      <m:PhoneCallId Id="NDDY5uY29y9t"/>
    </m:GetPhoneCallInformation>
  </soap:Body>
</soap:Envelope>
```

## <a name="getphonecallinformation-response-example"></a>GetPhoneCallInformation 响应示例

### <a name="description"></a>说明

以下示例显示了对 **GetPhoneCallInformation** 请求的成功响应。 该响应表示当前已连接的电话呼叫。 
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetPhoneCallInformationResponse ResponseClass="Success" 
                                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <m:PhoneCallInformation xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
        <t:PhoneCallState xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">Connected</t:PhoneCallState>
        <t:ConnectionFailureCause xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">None</t:ConnectionFailureCause>
      </m:PhoneCallInformation>
    </GetPhoneCallInformationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

