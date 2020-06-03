---
title: Exchange 的 POX 自动发现响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 08c6c5a2-a67a-4141-a8bd-1b5d560b90a7
description: 自动发现响应包含对自动发现请求的响应，其中包含用于建立与 Exchange Web 服务（EWS）的绑定的 Url 的列表。
ms.openlocfilehash: 0d903d9829fa6dc1273d8b25a1eeb0b68700d5da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462281"
---
# <a name="pox-autodiscover-response-for-exchange"></a>Exchange 的 POX 自动发现响应

自动发现响应包含对自动发现请求的响应，其中包含用于建立与 Exchange Web 服务（EWS）的绑定的 Url 的列表。
  
## <a name="autodiscover-response-example"></a>自动发现响应示例

### <a name="description"></a>Description

下面的示例展示了一个成功的自动发现响应。
  
### <a name="code"></a>代码

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
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

### <a name="comments"></a>备注

若要绑定到 Exchange Web 服务，请使用由[ASUrl （POX）](asurl-pox.md)元素标识的 URL。 
  
### <a name="response-element"></a>Response 元素

响应正文中使用以下元素：
  
- [自动发现（POX）](autodiscover-pox.md)
    
- [响应（POX）](response-pox.md)
    
- [User （POX）](user-pox.md)
    
- [DisplayName （POX）](displayname-pox.md)
    
- [LegacyDN （POX）](legacydn-pox.md)
    
- [DeploymentId （POX）](deploymentid-pox.md)
    
- [帐户（POX）](account-pox.md)
    
- [AccountType （POX）](accounttype-pox.md)
    
- [Action （POX）](action-pox.md)
    
- [协议（POX）](protocol-pox.md)
    
- [类型（POX）](type-pox.md)
    
- [服务器（POX）](server-pox.md)
    
- [ServerDN （POX）](serverdn-pox.md)
    
- [ServerVersion （POX）](serverversion-pox.md)
    
- [MdbDN （POX）](mdbdn-pox.md)
    
- [ASUrl （POX）](asurl-pox.md)
    
- [OOFUrl （POX）](oofurl-pox.md)
    
- [UMUrl （POX）](umurl-pox.md)
    
- [OABUrl （POX）](oaburl-pox.md)
    
- [Internal （POX）](internal-pox.md)
    
- [OWAUrl （POX）](owaurl-pox.md)
    
## <a name="autodiscover-error-response-example"></a>自动发现错误响应示例

### <a name="description"></a>Description

以下示例显示了自动发现错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
    <Error Time="21:25:04.8897083" Id="4130155072">
      <ErrorCode>600</ErrorCode>
      <Message>Invalid Request</Message>
      <DebugData />
    </Error>
  </Response>
</Autodiscover>
```

### <a name="error-response-element"></a>Error response 元素

响应正文中使用以下元素：
  
- [自动发现（POX）](autodiscover-pox.md)
    
- [响应（POX）](response-pox.md)
    
- [错误（POX）](error-pox.md)
    
- [ErrorCode （POX）](errorcode-pox.md)
    
- [Message （POX）](message-pox.md)
    
- [DebugData （POX）](debugdata-pox.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现请求](pox-autodiscover-request-for-exchange.md)
- [Exchange 的 POX 自动发现 web 服务参考](pox-autodiscover-web-service-reference-for-exchange.md) 
- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

