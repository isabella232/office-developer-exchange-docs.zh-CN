---
title: GetUserSettings 操作 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 758d965c-ef63-4de4-9120-e293abf14ff8
description: GetUserSettings 操作包含对用户的客户端访问配置的查询。
ms.openlocfilehash: e274fd4e1ca954ea25ea91a52e363c9a434b290a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466141"
---
# <a name="getusersettings-operation-soap"></a>GetUserSettings 操作 (SOAP)

**GetUserSettings**操作包含对用户的客户端访问配置的查询。 
  
## <a name="getusersettings-request-example"></a>GetUserSettings 请求示例

### <a name="description"></a>说明

以下 XML 示例显示了自动发现请求正文，该正文请求用户的显示名称、可分辨名称、部署 ID、邮箱服务器、邮箱可分辨名称、Active Directory 服务器、客户端访问服务器版本和受支持的 Exchange Web 服务架构。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"      
               xmlns:wsa="http://www.w3.org/2005/08/addressing" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"      
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2010</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://myserver.contoso.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>UserName@domain.contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>UserDisplayName</a:Setting>
          <a:Setting>UserDN</a:Setting>
          <a:Setting>UserDeploymentId</a:Setting>
          <a:Setting>InternalMailboxServer</a:Setting>
          <a:Setting>MailboxDN</a:Setting>
          <a:Setting>ActiveDirectoryServer</a:Setting>
          <a:Setting>CasVersion</a:Setting>
          <a:Setting>EwsSupportedSchemas</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a>Request 元素

请求正文中使用以下元素：
  
- [GetUserSettingsRequestMessage （SOAP）](getusersettingsrequestmessage-soap.md)
    
- [邮箱（SOAP）](mailbox-soap.md)
    
- [请求 (SOAP)](request-soap.md)
    
- [RequestedServerVersion （SOAP）](requestedserverversion-soap.md)
    
- [RequestedSettings （SOAP）](requestedsettings-soap.md)
    
- [设置（SOAP）](setting-soap.md)
    
- [User （SOAP）](user-soap.md)
    
- [Users （SOAP）](users-soap.md)
    
## <a name="getusersettings-response-example"></a>GetUserSettings 响应示例

### <a name="description"></a>说明

下面的示例展示了一个成功的**GetUserSettings**响应。 
  
### <a name="code"></a>代码

```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
  </s:Header>
  <s:Body>
  <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>NoError</ErrorCode>
            <ErrorMessage>No error.</ErrorMessage>
            <RedirectTarget i:nil="true" />
            <UserSettingErrors />
            <UserSettings>
              <UserSetting i:type="StringSetting">
                <Name>UserDisplayName</Name>
                <Value>UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Recipients/cn=UserDisplayName</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>UserDeploymentId</Name>
                <Value>a40E2742-21c6-4050-8Ed2-d41f100c22b8</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>CasVersion</Name>
                <Value>14.00.0478.000</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>EwsSupportedSchemas</Name>
                <Value>Exchange2007,  Exchange2010</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>InternalMailboxServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ActiveDirectoryServer</Name>
                <Value>machinename.domain.contoso.com</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>MailboxDN</Name>
                <Value>/o=First Organization/ou=Exchange Administrative Group (SDASDASDJ)/cn=Configuration/cn=Servers/cn=server/cn=Contoso Pri MDB</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

### <a name="response-elements"></a>Response 元素

响应正文中使用以下元素：
  
- [ErrorCode （SOAP）](errorcode-soap.md)
    
- [ErrorMessage （SOAP）](errormessage-soap.md)
    
- [GetUserSettingsResponseMessage （SOAP）](getusersettingsresponsemessage-soap.md)
    
- [名称（SOAP）](name-soap.md)
    
- [RedirectTarget （SOAP）](redirecttarget-soap.md)
    
- [响应（SOAP）](response-soap.md)
    
- [UserResponse （SOAP）](userresponse-soap.md)
    
- [UserResponses （SOAP）](userresponses-soap.md)
    
- [UserSetting （SOAP）](usersetting-soap.md)
    
- [UserSettingErrors （SOAP）](usersettingerrors-soap.md)
    
- [UserSettings （SOAP）](usersettings-soap.md)
    
- [Value （SOAP）](value-soap.md)
    
## <a name="see-also"></a>另请参阅



[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)


[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

