---
title: 使用自动发现查找连接点
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03896542-549b-4c45-973c-98f9025ea26c
description: 了解如何使用自动发现服务来定向客户端应用程序，到正确的 Exchange 服务器。
ms.openlocfilehash: eb3fb3664e5789638c097a43cf48f757bb0713ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353978"
---
# <a name="use-autodiscover-to-find-connection-points"></a>使用自动发现查找连接点

了解如何使用自动发现服务来定向客户端应用程序，到正确的 Exchange 服务器。
  
Exchange 自动发现服务客户端应用程序提供承载的电子邮件帐户配置设置 Exchange Online、 Exchange Online 作为 Office 365 的一部分或运行的 Exchange 版本的 Exchange 服务器上启动与 Exchange2013。 自动发现服务是一种 web 服务，提供配置设置。 自动发现服务是一种 web 服务，提供 Exchange 服务器到客户端应用程序的配置信息。 客户端应用程序使用自动发现可确定特定邮箱的自动发现服务的终结点。 本文介绍如何执行从 Exchange 服务器以查找正确的终结点的响应。 
  
有关如何获取电子邮件地址配置设置的信息，请参阅[获取使用自动发现 Exchange 中的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)和[获取从 Exchange 服务器的域设置](how-to-get-domain-settings-from-an-exchange-server.md)。
  
> [!NOTE]
> 查找正确的终结点的过程的用户或域设置请求的一部分。 自动发现服务使用的重定向响应的一系列发送电子邮件地址的正确终结点将客户端应用程序。 
  
您可以使用以下 Exchange 开发技术之一访问自动发现服务：

- Exchange Web Services (EWS) 托管的 API
    
- EWS
    
如果您使用 EWS，您可以使用以下方法检索用户设置：
    
- 基于 SOAP 的自动发现服务
    
- XML (POX) 自动发现服务
    
- 生成从 SOAP 或 XML 自动发现服务自动生成代理
    
有关这些方法的详细信息，请参阅[exchange 自动发现](autodiscover-for-exchange.md)。

有关这些 Exchange 开发技术的详细信息，请参阅[在 Exchange 浏览 EWS 托管 API 和 EWS，web services](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)。 

EWS 托管 API 以检索用户设置提供基于对象的接口。 如果您的客户端应用程序使用托管的代码，我们建议您使用 EWS 托管 API。 EWS 托管 API 界面更好地专为一个简单的对象模型比典型的自动生成 web 服务代理。 
  
如果您使用 EWS，我们建议您使用 SOAP 自动发现服务，因为它支持比 POX 自动发现服务更丰富的功能。
  
## <a name="prerequisites-for-finding-an-endpoint"></a>查找终结点的先决条件
<a name="bk_Prereq"> </a>

您可以创建使用自动发现服务的客户端应用程序之前，您需要有权访问以下：
  
- Exchange Online 或正在运行的 Exchange 版本开始 Exchange 2007 sp1 的服务器。 如果您使用基于 SOAP 的自动发现服务、 Exchange Online 或 Exchange 启动与 Exchange 2010 的版本。
    
- Exchange 服务器配置为接受来自客户端应用程序的连接。 有关如何配置您的 Exchange 服务器的信息，请参阅[在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)。
    
- 有权使用 EWS 帐户。 有关如何配置帐户的信息，请参阅[在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)。
    
> [!NOTE]
> 如果您使用 EWS 托管 API，您必须提供在某些情况下证书验证回调。 您可能还需要使用某些生成的代理库，如那些通过 Visual Studio 创建的证书验证回调。 有关详细信息，请参阅[验证 EWS 托管 API 服务器证书](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
### <a name="core-concepts-for-finding-an-endpoint"></a>查找终结点的核心概念
<a name="bk_Core"> </a>

您使用自动发现查找终结点之前，您应熟悉以下表中列出的概念。
  
|**概念**|**说明**|
|:-----|:-----|
|[Exchange 自动发现](autodiscover-for-exchange.md) <br/> |提供自动发现服务的工作原理的概述。  <br/> |
   
如果您使用 EWS 托管 API，您使用[Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类[Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/dd633907%28v=exchg.80%29.aspx)命名空间中管理与 EWS 的连接。 要使用本文中的 EWS 托管 API 代码示例，您需要以引用您的代码中的以下命名空间： 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="find-the-correct-endpoint-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 来查找正确的终结点
<a name="bk_Managed"> </a>

如果您使用 EWS 托管 API，由**ExchangeService**类处理对自动发现服务的调用。 若要确定正确的终结点的电子邮件帐户，请 **[ExchangeService]** 对象上调用**AutodiscoverUrl**方法。 下面的代码示例演示如何使用 EWS 托管 API Exchange.asmx 文件正确的客户端访问服务器上设置电子邮件地址的 EWS web 服务终结点。 
  
```cs
NetworkCredential credentials = new NetworkCredential(securelyStoredEmail, securelyStoredPassword);
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2013);
service.Credentials = credentials;
service.AutodiscoverUrl("User1@contoso.com");
```

## <a name="find-the-correct-endpoint-by-using-ews"></a>使用 EWS 查找正确的终结点
<a name="bk_SOAP"> </a>

SOAP 自动发现服务可能使用的请求和响应的一系列定向到正确的终结点 EWS 的应用程序。 有关确定的电子邮件帐户的正确终结点的过程的信息，请参阅[exchange 自动发现](autodiscover-for-exchange.md)。 下面的 XML 示例演示请求和响应，您可以预期发出 SOAP 自动发现请求以查找正确的终结点时的系列。
  
### <a name="soap-autodiscover-endpoint-request"></a>SOAP 自动发现终结点请求

下面的示例演示发送到自动发现服务以查找正确的终结点的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://mail.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

自动发现服务会使用两种重定向响应之一响应： HTTP 302 重定向或 SOAP 重定向响应。 如果从 Exchange 服务器响应 HTTP 302 重定向，客户端应用程序应验证重定向地址是可以接受，然后按照重定向响应。
  
> [!IMPORTANT]
> 用于验证重定向响应的条件，请参阅[exchange 自动发现](autodiscover-for-exchange.md)。 
  
如果自动发现服务将返回一个重定向响应，指示[错误代码](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx)元素**用户回音**元素的客户端应用程序应使用**RedirectTarget**元素来构建是新设置请求发送到指定的重定向响应中的服务器。 下面的示例显示服务器的重定向响应。 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>682</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

后重定向，客户端使用的重定向 URL 准备另一个请求。 下面的代码演示的请求重定向响应中创建的示例。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

当客户端应用程序具有已定向到的正确的终结点的自动发现服务时，服务器将发送与[ErrorCode](http://msdn.microsoft.com/library/0bb00cee-c66b-4f34-b99d-355458f5e83b%28Office.15%29.aspx)元素**用户回音**元素设置为**NoError**和包含请求的响应用户设置。 仅请求的用户设置， **InternalEwsUrl**和**ExternalEwsUrl**，则返回。 下面的示例显示来自服务器的响应。 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
        Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>15</h:MajorVersion>
      <h:MinorVersion>0</h:MinorVersion>
      <h:MajorBuildNumber>160</h:MajorBuildNumber>
      <h:MinorBuildNumber>4</h:MinorBuildNumber>
      <h:Version>Exchange2013</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

按照自动发现过程查找终结点返回请求的域或用户设置。 有关发出请求的特定设置的信息，请参阅以下文章：
  
- [从 Exchange 服务器获取域设置](how-to-get-domain-settings-from-an-exchange-server.md)    
- [通过使用自动发现 Exchange 中获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)   
- [Exchange 自动发现](autodiscover-for-exchange.md)    
- [Exchange 的自动发现 web 服务引用](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)    
- [Exchange 的 EWS 引用](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

