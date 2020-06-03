---
title: 获取来自 Exchange 服务器的域设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 2f9acb81-5135-4f72-94e8-65c235d725e6
description: 了解如何使用自动发现服务从 Exchange 服务器获取域设置。
localization_priority: Priority
ms.openlocfilehash: e77810089b77f614f6bca064b2e5cf6bde2bff7c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455805"
---
# <a name="get-domain-settings-from-an-exchange-server"></a>获取来自 Exchange 服务器的域设置

了解如何使用自动发现服务从 Exchange 服务器获取域设置。
  
您可以使用自动发现服务检索电子邮件域的配置信息。 自动发现服务向应用程序提供连接到特定域的正确服务终结点的过程。
  
您可以使用以下一种开发技术来访问自动发现服务：
  
- Exchange Web 服务（EWS）托管 API
    
- EWS
    
    如果您使用 EWS，则可以使用以下方法来检索用户设置：
    
  - 基于 SOAP 的自动发现服务
    
  - XML （POX）自动发现服务
    
  - 从 SOAP 或 XML 自动发现服务生成的自动生成的代理
    
    有关这些方法的详细信息，请参阅[Exchange 的自动发现](autodiscover-for-exchange.md)。
    
EWS 托管 API 提供了用于检索用户设置的基于对象的接口。 如果客户端应用程序使用托管代码，建议使用 EWS 托管 API。 对简单对象模型而言，EWS 托管 API 接口比典型的自动生成 web 服务代理更好地优化。 
  
如果使用 EWS，则建议您使用 SOAP 自动发现服务，因为它支持的功能集比 POX 自动发现服务更丰富。
  
自动发现服务仅返回请求的配置设置。 下表列出了自动发现服务可以返回的域配置设置。
  
**表1：域配置设置**

|**配置设置**|**说明**|
|:-----|:-----|
|ExternalEwsUrl  <br/> |EWS 的外部 URL。  <br/> |
|ExternalEwsVersion  <br/> |承载 EWS URL 的 Exchange 服务器的版本。  <br/> |
   
## <a name="prerequisites-for-getting-domain-settings"></a>获取域设置的先决条件
<a name="bk_Prereq"> </a>

在创建连接到自动发现服务的应用程序以获取域设置之前，请确保您有权访问以下内容：
  
- Exchange Online、作为 Office 365 的一部分的 Exchange Online 或运行 Exchange 2007 的 Exchange 版本的服务器。 如果使用的是基于 EWS SOAP 的自动发现服务，则运行从 Exchange 2010 开始的 Exchange 版本的服务器。
    
- 一种配置为接受来自客户端应用程序的连接的 Exchange 服务器。 有关如何配置 Exchange server 的信息，请参阅[控制 exchange 中对 EWS 的客户端应用程序访问](controlling-client-application-access-to-ews-in-exchange.md)。
    
- 有权使用 EWS 的帐户。 有关如何配置帐户的信息，请参阅[控制 Exchange 中的客户端应用程序对 EWS 的访问](controlling-client-application-access-to-ews-in-exchange.md)。
    
> [!NOTE]
> 如果使用 EWS 托管 API，则必须在某些情况下提供证书验证回调。 您可能还需要具有一些生成的代理库（如由 Visual Studio 创建的代理库）的证书验证回调。 有关详细信息，请参阅[验证 EWS 托管 API 的服务器证书](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 
  
### <a name="core-concepts-for-getting-domain-settings"></a>用于获取域设置的核心概念
<a name="bk_Core"> </a>

在使用自动发现来获取域设置之前，您应该先熟悉下表中列出的概念。
  
|**概念**|**说明**|
|:-----|:-----|
|[Exchange 自动发现](autodiscover-for-exchange.md) <br/> |提供自动发现服务的工作原理的概述。  <br/> |
|[使用自动发现查找连接点](how-to-use-autodiscover-to-find-connection-points.md) <br/> |描述自动发现服务用于将客户端应用程序重定向到正确的服务终结点的过程。  <br/> |
   
如果使用的是 EWS 托管 API，请使用 WebServices 命名空间中的 ExchangeService 类来管理到 EWS 的[连接的名称](https://msdn.microsoft.com/library/exchange/dd633907%28v=exchg.80%29.aspx)的[Microsoft.Exchange.WebServices.Data.ExchangeService](https://msdn.microsoft.com/library/exchange/dd635811%28v=exchg.80%29.aspx) 。 本节中的代码示例假定您在代码中引用了以下命名空间： 
  
- **System.Net**
    
- **WebServices。 ExchangeService 的**
    
## <a name="get-domain-settings-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取域设置
<a name="bk_Managed"> </a>

如果使用的是 EWS 托管 API，则可以使用 WebServices 对象的 AutodiscoverSettings 方法来生成检索域的配置信息的请求，如下面的示例所示，您可以使用对象的[GetUserSettings](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) [方法。](https://msdn.microsoft.com/library/exchange/dd634321%28v=exchg.80%29.aspx) 在此示例中，仅请求某些可能的域设置，并且仅从服务器返回请求的设置。 
  
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

您可以分析返回的集合，以访问每个键/值对。 下面的示例演示如何分析每个返回的元素并显示每个键/值对的名称和值。
  
```cs
// Display each retrieved value. The settings are part of a key/value pair.
foreach (KeyValuePair<DomainSettingName, Object> domainsetting in domainresponse.Settings)
{
    Console.WriteLine(domainsetting.Key.ToString() + ": " + domainsetting.Value.ToString());
}
```

或者，您可以获取特定设置的值。 在下面的示例中，将显示**ExternalEwsUrl**设置。 
  
```cs
// Display a specific setting, such as ExternalEwsUrl.
Console.WriteLine(domainresponse.Settings[DomainSettingName.ExternalEwsUrl]);
```

## <a name="get-user-settings-by-using-ews-soap-autodiscover"></a>使用 EWS SOAP 自动发现获取用户设置
<a name="bk_SOAP"> </a>

下面的示例演示了从自动发现服务中获取两个域设置的 SOAP XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:wsa="http://www.w3.org/2005/08/addressing" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
        xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2013</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetDomainSettings</wsa:Action>
    <wsa:To>https://autodiscover.exchange.microsoft.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetDomainSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
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

下面的示例演示在分析来自客户端的请求之后，服务器返回的 XML 响应。
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">https://schemas.microsoft.com/exchange/2010/
          Autodiscover/Autodiscover/GetDomainSettingsResponse</a:Action>
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

域设置提供了客户端连接到 EWS 所需的基本信息。 您可以使用此信息连接到 EWS，也可以从服务器检索电子邮件帐户的其他配置设置。 有关详细信息，请参阅以下文章：
  
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
## <a name="see-also"></a>另请参阅


- [设置 EWS 应用程序](setting-up-your-ews-application.md)
    
- [Exchange 的自动发现 web 服务参考](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)
    
- [Exchange 的 EWS 引用](https://msdn.microsoft.com/library/2a873474-1bb2-4cb1-a556-40e8c4159f4a%28Office.15%29.aspx)
    

