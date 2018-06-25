---
title: 从 Exchange 服务器获取域设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2f9acb81-5135-4f72-94e8-65c235d725e6
description: 了解如何使用自动发现服务获取从 Exchange 服务器的域设置。
ms.openlocfilehash: 0dd990cc82762936e7827115685ce0178eafb5ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752780"
---
# <a name="get-domain-settings-from-an-exchange-server"></a>从 Exchange 服务器获取域设置

了解如何使用自动发现服务获取从 Exchange 服务器的域设置。
  
您可以通过使用自动发现服务来检索配置信息的电子邮件域。 自动发现服务提供您的应用程序与连接到特定域的正确的服务终结点的过程。
  
您可以使用以下开发技术之一访问自动发现服务：
  
- Exchange Web Services (EWS) 托管的 API
    
- EWS
    
    如果您使用 EWS，您可以使用以下方法检索用户设置：
    
  - 基于 SOAP 的自动发现服务
    
  - XML (POX) 自动发现服务
    
  - 生成从 SOAP 或 XML 自动发现服务自动生成代理
    
    有关这些方法的详细信息，请参阅[exchange 自动发现](autodiscover-for-exchange.md)。
    
EWS 托管 API 以检索用户设置提供基于对象的接口。 如果您的客户端应用程序使用托管的代码，我们建议您使用 EWS 托管 API。 EWS 托管 API 界面更好地专为一个简单的对象模型比典型的自动生成 web 服务代理。 
  
如果您使用 EWS，我们建议您使用 SOAP 自动发现服务，因为它支持比 POX 自动发现服务更丰富的功能。
  
自动发现服务返回仅请求的配置设置。 下表列出了可返回自动发现服务的域配置设置。
  
**表 1： 域配置设置**

|**配置设置**|**说明**|
|:-----|:-----|
|ExternalEwsUrl  <br/> |EWS 的外部 URL。  <br/> |
|ExternalEwsVersion  <br/> |Exchange server 承载 EWS URL 的版本。  <br/> |
   
## <a name="prerequisites-for-getting-domain-settings"></a>获取域设置的先决条件
<a name="bk_Prereq"> </a>

创建的应用程序连接到自动发现服务获取域设置之前，请确保您有权访问以下：
  
- Exchange Online、 Exchange Online 作为 Office 365 的一部分或运行的开头 Exchange 2007 的 Exchange 版本的服务器。 如果您使用的基于 EWS SOAP 的自动发现服务，运行的开头 Exchange 2010 的 Exchange 版本的服务器。
    
- Exchange 服务器配置为接受来自客户端应用程序的连接。 有关如何配置您的 Exchange 服务器的信息，请参阅[在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)。
    
- 有权使用 EWS 帐户。 有关如何配置帐户的信息，请参阅[在 Exchange 控制客户端应用程序访问 EWS](controlling-client-application-access-to-ews-in-exchange.md)。
    
> [!NOTE]
> 如果您使用 EWS 托管 API，您必须提供在某些情况下证书验证回调。 您可能还需要使用某些生成的代理库，如那些通过 Visual Studio 创建的证书验证回调。 有关详细信息，请参阅[验证 EWS 托管 API 服务器证书](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
### <a name="core-concepts-for-getting-domain-settings"></a>用于获取域设置的核心概念
<a name="bk_Core"> </a>

您可以使用自动发现来获取域设置之前，您应熟悉以下表中列出的概念。
  
|**概念**|**说明**|
|:-----|:-----|
|[Exchange 自动发现](autodiscover-for-exchange.md) <br/> |提供自动发现服务的工作原理的概述。  <br/> |
|[使用 Autodiscover 以查找连接点](how-to-use-autodiscover-to-find-connection-points.md) <br/> |描述自动发现服务用于将重定向到正确的服务终结点的客户端应用程序的过程。  <br/> |
   
如果您使用 EWS 托管 API，您使用[Microsoft.Exchange.WebServices.Data.ExchangeService](http://msdn.microsoft.com/en-us/library/exchange/dd635811%28v=exchg.80%29.aspx)类[Microsoft.Exchange.WebServices.Data](http://msdn.microsoft.com/en-us/library/exchange/dd633907%28v=exchg.80%29.aspx)命名空间中管理与 EWS 的连接。 本节中的代码示例假定您在您的代码中引用的以下命名空间： 
  
- **System.Net**
    
- **Microsoft.Exchange.WebServices.Data.ExchangeService**
    
## <a name="get-domain-settings-by-using-the-ews-managed-api"></a>通过使用 EWS 托管 API 获取域设置
<a name="bk_Managed"> </a>

如果您使用 EWS 托管 API，您可以使用[Microsoft.Exchange.WebServices.Data.AutodiscoverService](http://msdn.microsoft.com/en-us/library/exchange/dd634321%28v=exchg.80%29.aspx)对象的[Microsoft.Exchange.WebServices.Data.AutodiscoverSettings.GetUserSettings](http://msdn.microsoft.com/en-us/library/exchange/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx)方法生成请求下面的示例中所示的检索一个域，配置信息。 本示例中，只将某些可能域设置请求，并从服务器返回请求的设置。 
  
```cs
AutodiscoverService autodiscoverService = new AutodiscoverService("domain.contoso.com");
autodiscoverService.Credentials = new NetworkCredential("User1", "password", "domain.contoso.com");
// Submit a request and get the settings. The response contains only the
// settings that are requested, if they exist.
GetDomainSettingsResponse domainresponse = autodiscoverService.GetDomainSettings(
    "domain",
    ExchangeVersion.Exchang2013,
    DomainSettingName.ExternalEwsUrl,
    DomainSettingName.ExternalEwsVersion);
```

您可以分析返回访问每个键/值对的集合。 下面的示例演示如何返回的每个元素通过分析和显示名称和每个键/值对的值。
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
foreach (KeyValuePair<DomainSettingName, Object> domainsetting in domainresponse.Settings)
{
    Console.WriteLine(domainsetting.Key.ToString() + ": " + domainsetting.Value.ToString());
}
```

此外，您可以获取特定设置的值。 以下示例中，在**ExternalEwsUrl**设置是显示。 
  
```cs
// Display a specific setting, such as ExternalEwsUrl.
Console.WriteLine(domainresponse.Settings[DomainSettingName.ExternalEwsUrl]);
```

## <a name="get-user-settings-by-using-ews-soap-autodiscover"></a>通过使用 EWS SOAP 自动发现获取用户设置
<a name="bk_SOAP"> </a>

下面的示例演示 XML SOAP 请求从自动发现服务获取两个域设置。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetDomainSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Domains>
          <a:Domain>domain</a:Domain>
        </a:Domains>
        <a:RequestedSettings>
          <a:Setting>ExternalEwsUrl</a:Setting>
          <a:Setting>ExternalEwsVersion</a:Setting>
        </a:RequestedSettings>
        <a:RequestedVersion>Exchange2013</a:RequestedVersion>
      </a:Request>
    </a:GetDomainSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

下面的示例演示后分析来自客户端的请求服务器返回的 XML 响应。
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/
          Autodiscover/Autodiscover/GetDomainSettingsResponse</a:Action>
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
    <GetDomainSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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
                <Value>https://failover.exchange.microsoft.com/ews/exchange.asmx</Value>
              </DomainSetting>
              <DomainSetting i:type="DomainStringSetting">
                <Name>ExternalEwsVersion</Name>
                <Value>15.00.0085.000</Value>
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

## <a name="next-steps"></a>后续步骤
<a name="bk_Next"> </a>

域设置提供了您的客户端需要连接到 EWS 的基本信息。 您可以使用此信息连接到 EWS，也可以从服务器中检索的电子邮件帐户的额外的配置设置。 有关详细信息，请参阅以下文章：
  
- [通过使用自动发现 Exchange 中获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>另请参阅


- [EWS 应用程序设置](setting-up-your-ews-application.md)
    
- [Exchange 的自动发现 web 服务引用](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [Exchange 的 EWS 引用](http://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

