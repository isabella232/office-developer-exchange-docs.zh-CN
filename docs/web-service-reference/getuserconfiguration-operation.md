---
title: GetUserConfiguration 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 71d50e3c-92bd-435f-8118-b28bb85f8138
description: GetUserConfiguration 操作从文件夹中获取用户配置对象。
ms.openlocfilehash: be6c662cf49a7c2441f94084dd909e86fe703e20
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516844"
---
# <a name="getuserconfiguration-operation"></a>GetUserConfiguration 操作

**GetUserConfiguration** 操作从文件夹中获取用户配置对象。 
  
## <a name="getuserconfiguration-request-example"></a>GetUserConfiguration 请求示例

### <a name="description"></a>Description

**GetUserConfiguration** 请求的以下示例显示如何形成请求，以在"草稿"文件夹中获取用户配置对象。 
  
### <a name="code"></a>代码

```XML
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
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts"/>
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>Dictionary</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="getuserconfiguration-response-example"></a>GetUserConfiguration 响应示例

### <a name="description"></a>Description

以下示例显示了对 **GetUserConfiguration** 请求的成功响应。 
  
### <a name="code"></a>代码

```XML
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
    <m:GetUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:UserConfiguration>
            <t:UserConfigurationName Name="TestConfig">
              <t:DistinguishedFolderId Id="drafts">
              </t:DistinguishedFolderId>
            </t:UserConfigurationName>
            <t:Dictionary>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>PhoneNumber</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>String</t:Type>
                  <t:Value>555-555-1111</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
            </t:Dictionary>
          </m:UserConfiguration>
        </m:GetUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:GetUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>另请参阅



[EWS 操作在Exchange](ews-operations-in-exchange.md)
  
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

