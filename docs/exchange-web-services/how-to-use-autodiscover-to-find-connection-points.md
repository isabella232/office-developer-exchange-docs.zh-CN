---
title: 使用自动发现查找连接点
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: 了解如何使用自动发现服务将客户端应用程序定向到正确的 Exchange 服务器。
localization_priority: Priority
ms.openlocfilehash: c1895fa0d2cce489467a726614e9457052624ef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527591"
---
# <a name="use-autodiscover-to-find-connection-points"></a>使用自动发现查找连接点

了解如何使用自动发现服务将客户端应用程序定向到正确的 Exchange 服务器。
  
Exchange 自动发现服务为您的客户端应用程序提供了托管在 Exchange Online 上的电子邮件帐户、作为 Office 365 的一部分的 Exchange Online 或从 Exchange 2013 开始运行 Exchange 版本的 Exchange 服务器的配置设置。 自动发现服务是一种提供配置设置的 web 服务。 自动发现服务是向客户端应用程序提供 Exchange server 配置信息的 web 服务。 客户端应用程序使用自动发现来确定特定邮箱的自动发现服务的终结点。 本文介绍如何跟踪来自 Exchange 服务器的响应以查找正确的终结点。 
  
有关如何获取电子邮件地址配置设置的信息，请参阅使用自动发现和从[exchange 服务器获取域设置](how-to-get-domain-settings-from-an-exchange-server.md)中的[从 exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。
  
> [!NOTE]
> 查找正确终结点的过程是用户或域设置请求的一部分。 自动发现服务使用一系列重定向响应将客户端应用程序发送到电子邮件地址的正确终结点。 
  
您可以使用以下 Exchange 开发技术之一来访问自动发现服务：

- Exchange Web 服务（EWS）托管 API
    
- EWS
    
如果您使用 EWS，则可以使用以下方法来检索用户设置：
    
- 基于 SOAP 的自动发现服务
    
- XML （POX）自动发现服务
    
- 从 SOAP 或 XML 自动发现服务生成的自动生成的代理
    
有关这些方法的详细信息，请参阅[Exchange 的自动发现](autodiscover-for-exchange.md)。

有关这些 Exchange 开发技术的详细信息，请参阅[在 exchange 中浏览 EWS 托管 API、ews 和 web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)。 

EWS 托管 API 提供了用于检索用户设置的基于对象的接口。 如果客户端应用程序使用托管代码，建议使用 EWS 托管 API。 对简单对象模型而言，EWS 托管 API 接口比典型的自动生成 web 服务代理更好地优化。 
  
如果使用 EWS，则建议您使用 SOAP 自动发现服务，因为它支持的功能集比 POX 自动发现服务更丰富。
  
## <a name="prerequisites-for-finding-an-endpoint"></a>查找终结点的先决条件
<a name="bk_Prereq"> </a>

在创建使用自动发现服务的客户端应用程序之前，您需要具有以下权限：
  
- Exchange Online 或运行 Exchange 版本（从 Exchange 2007 SP1 开始）的服务器。 如果使用基于 SOAP 的自动发现服务，则 Exchange Online 或从 Exchange 2010 开始的 Exchange 版本。
    
- 一种配置为接受来自客户端应用程序的连接的 Exchange 服务器。 有关如何配置 Exchange server 的信息，请参阅[控制 exchange 中对 EWS 的客户端应用程序访问](controlling-client-application-access-to-ews-in-exchange.md)。
    
- 有权使用 EWS 的帐户。 有关如何配置帐户的信息，请参阅[控制 Exchange 中的客户端应用程序对 EWS 的访问](controlling-client-application-access-to-ews-in-exchange.md)。
    
> [!NOTE]
> 如果使用 EWS 托管 API，则必须在某些情况下提供证书验证回调。 您可能还需要具有一些生成的代理库（如由 Visual Studio 创建的代理库）的证书验证回调。 有关详细信息，请参阅[验证 EWS 托管 API 的服务器证书](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>查找终结点的核心概念
<a name="bk_Core"> </a>

在使用自动发现查找终结点之前，应该先熟悉下表中列出的概念。
  
|**概念**|**说明**|
|:-----|:-----|
|[Exchange 自动发现](autodiscover-for-exchange.md) <br/> |提供自动发现服务的工作原理的概述。  <br/> |
   
如果使用的是 EWS 托管 API，请使用 WebServices 命名空间中的 ExchangeService 类来管理到 EWS 的[连接的名称](https://msdn.microsoft.com/library/dd633907%28v=exchg.80%29.aspx)的[Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 。 若要使用本文中的 EWS 托管 API 代码示例，您需要在代码中引用以下命名空间： 
  
- **System.Net**
    
- **WebServices。 ExchangeService 的**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 查找正确的终结点
<a name="bk_Managed"> </a>

如果使用 EWS 托管 API，则对自动发现服务的调用由**ExchangeService**类处理。 若要确定电子邮件帐户的正确终结点，请对 **[ExchangeService]** 对象调用**AutodiscoverUrl**方法。 下面的代码示例演示如何使用 EWS 托管 API 将电子邮件地址的 EWS web 服务终结点设置为正确的客户端访问服务器上的 Exchange .asmx 文件。 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>使用 EWS 查找正确的终结点
<a name="bk_SOAP"> </a>

SOAP 自动发现服务可能使用一系列请求和响应将应用程序定向到 EWS 的正确终结点。 有关确定电子邮件帐户的正确终结点的过程的信息，请参阅[Exchange 的自动发现](autodiscover-for-exchange.md)。 下面的 XML 示例显示在建立 SOAP 自动发现请求查找正确的终结点时，您可以预料到的请求和响应系列。
  
### <a name="soap-autodiscover-endpoint-request"></a>SOAP 自动发现终结点请求

下面的示例演示发送到自动发现服务以查找正确终结点的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

### <a name="soap-autodiscover-redirection-response"></a>SOAP 自动发现重定向响应

自动发现服务可能会通过以下两个重定向响应之一进行响应： HTTP 302 重定向或 SOAP 重定向响应。 如果来自 Exchange 服务器的响应是 HTTP 302 重定向，则客户端应用程序应验证重定向地址是否可接受，然后遵循重定向响应。
  
> [!IMPORTANT]
> 有关验证重定向响应的条件，请参阅[Exchange 的自动发现](autodiscover-for-exchange.md)。 
  
如果自动发现服务返回一个重定向响应（由**UserResponse**元素的[ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx)元素指示），则客户端应用程序应使用**RedirectTarget**元素构建一个新的设置请求，该请求将发送到重定向响应中指定的服务器。 以下示例显示来自服务器的重定向响应。 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>User1@mail.Contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>

```

重定向后，客户端使用重定向 URL 准备另一个请求。 以下代码显示了您通过重定向响应创建的请求的示例。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>User1@mail.Contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>InternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsUrl</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>

```

当客户端应用程序定向到自动发现服务的正确终结点时，服务器将向 NoError 发送响应，并将**UserResponse**元素的[ErrorCode](https://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx)元素设置为**NoError** ，并包含请求的用户设置。 仅返回请求的用户设置**InternalEwsUrl**和**ExternalEwsUrl**。 下面的示例演示来自服务器的响应。 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
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
                <Name>InternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
              <UserSetting i:type="StringSetting">
                <Name>ExternalEwsUrl</Name>
                <Value>https://server.Contoso.com/ews/exchange.asmx</Value>
              </UserSetting>
            </UserSettings>
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a>后续步骤
<a name="bk_Next"> </a>

按照自动发现过程查找终结点将返回请求的域或用户设置。 有关为特定设置发出请求的信息，请参阅以下文章：
  
- [获取来自 Exchange 服务器的域设置](how-to-get-domain-settings-from-an-exchange-server.md)    
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)   
- [Exchange 自动发现](autodiscover-for-exchange.md)    
- [Exchange 的自动发现 web 服务参考](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [Exchange 的 EWS 引用](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

