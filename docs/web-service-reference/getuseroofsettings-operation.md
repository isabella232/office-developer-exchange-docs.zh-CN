---
title: GetUserOofSettings 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetUserOofSettings
api_type:
- schema
ms.assetid: 153e4440-495b-4972-9811-2fbea740142a
description: GetUserOofSettings 操作获取邮箱用户的 Out of Office (OOF) 设置和邮件。
ms.openlocfilehash: 9298681bff1cce5be37e8bee978ddeb0431bacdc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533408"
---
# <a name="getuseroofsettings-operation"></a>GetUserOofSettings 操作

**GetUserOofSettings** 操作获取邮箱用户的 Out of Office (OOF) 设置和邮件。 
  
## <a name="soap-headers"></a>SOAP 标头

**GetUserOofSettings** 操作可以使用下表中列出和描述的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序正在模拟的用户。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。  <br/> |
   
## <a name="using-the-getuseroofsettings-operation"></a>使用 GetUserOofSettings 操作

**GetUserOofSettings** 操作提供对用户的 OOF 设置的访问权限。 用户由用户的电子邮件地址标识。 如果 OOF 邮件为 null 并且启用了 OOF，则不发送 OOF 邮件。 
  
> [!IMPORTANT]
> 如果 OOF 邮件由 MicrosoftOfficeOutlook 设置，则此操作将返回 HTML 格式的 OOF 邮件。 
  
## <a name="getuseroofsettings-request-example"></a>GetUserOofSettings 请求示例

### <a name="description"></a>说明

下面的示例展示了获取单个用户的 OOF 信息的 **GetUserOofSettings** 请求。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns ="https://schemas.microsoft.com/exchange/services/2006/types">
        <Address>User1@example.com</Address>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [GetUserOofSettingsRequest](getuseroofsettingsrequest.md)
    
- [Mailbox (Availability)](mailbox-availability.md)
    
- [Address (string)](address-string.md)
    
## <a name="successful-getuseroofsettings-response-example"></a>成功的 GetUserOofSettings 响应示例

### <a name="description"></a>说明

以下示例显示 OOF 邮件处于禁用的 OOF 状态。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserOofSettingsResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessage ResponseClass="Success">
        <ResponseCode>NoError</ResponseCode>
      </ResponseMessage>
      <OofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Disabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2006-11-03T23:00:00</StartTime>
          <EndTime>2006-11-04T23:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office. This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </OofSettings>
      <AllowExternalOof>All</AllowExternalOof>
    </GetUserOofSettingsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-getuseroofsettings-response-elements"></a>成功的 GetUserOofSettings 响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
    
- [ResponseMessage](responsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [OofSettings](oofsettings.md)
    
- [OofState](oofstate.md)
    
- [ExternalAudience](externalaudience.md)
    
- [Duration (UserOofSettings)](duration-useroofsettings.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
- [InternalReply](internalreply.md)
    
- [ExternalReply](externalreply.md)
    
- [消息](message-ex15websvcsotherref.md)
    
- [AllowExternalOof](allowexternaloof.md)
    
## <a name="getuseroofsettings-error-response-example"></a>GetUserOofSettings 错误响应示例

### <a name="description"></a>说明

以下示例显示尝试访问其他用户的 OOF 信息导致的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <soap:Fault>
      <faultcode>soap:Client</faultcode>
      <faultstring>Microsoft.Exchange.Data.Storage.AccessDeniedException: User is not mailbox owner. User = S-1-5-21-3642464542-282065186-3871681729-1155, MailboxGuid = S-1-5-21-3642464542-282065186-3871681729-1156 ---> User is not mailbox owner. </faultstring>
      <faultactor>https://CAS01.example.com/EWS/Exchange.asmx</faultactor>
      <detail>
        <ErrorCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">-2146233088</ErrorCode>
      </detail>
    </soap:Fault>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

