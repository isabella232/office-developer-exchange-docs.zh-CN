---
title: GetAppManifests 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: 查找有关 GetAppManifests EWS 操作的信息。
ms.openlocfilehash: 979a09d24d0c9365a92e589aa169bebf2340411b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509915"
---
# <a name="getappmanifests-operation"></a>GetAppManifests 操作

查找有关 **GetAppManifests** EWS 操作的信息。 
  
**GetAppManifests** 操作检索应用程序清单。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-getappmanifests-operation"></a>使用 GetAppManifests 操作

**GetAppManifests** 操作不获取任何参数来请求邮箱的应用程序清单。 该响应将包含邮箱中安装的每个应用的 base64 编码的 XML 清单文件。 
  
### <a name="getappmanifests-operation-soap-headers"></a>GetAppManifests 操作 SOAP 标头

**GetAppManifests** 操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a>GetAppManifests 操作请求示例：获取邮箱的应用程序清单

**GetAppManifests** 操作请求的以下示例显示如何获取邮箱的应用程序清单。 [ApiVersionSupported](apiversionsupported.md)元素和[SchemaVersionSupported](schemaversionsupported.md)元素是可选的。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

请求 SOAP 正文包含以下元素：
  
- [GetAppManifests](getappmanifests.md)
    
- [ApiVersionSupported](apiversionsupported.md)
    
- [SchemaVersionSupported](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a>成功的 GetAppManifests 操作响应

以下示例显示成功响应 **GetAppManifests** 操作请求，以获取邮箱的应用程序清单。 
  
> [!NOTE]
> 所有 base64 应用清单已被任意截断，以保持可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [GetAppManifestsResponse](getappmanifestsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [应用](apps.md)
    
- [应用](app.md)
    
- [清单](manifest.md)
    
响应 SOAP 正文还可以包含以下元素：
  
- [清单](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a>GetAppManifests 操作错误响应

此操作返回的错误与输入参数格式无效或常规 EWS 错误有关。 有关 EWS 通用且特定于此操作的错误代码，请参阅 [ResponseCode](responsecode.md)。
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)
    
- [DisableApp 操作](disableapp-operation.md)
    
- [InstallApp 操作](installapp-operation.md)
    
- [UninstallApp 操作](uninstallapp-operation.md)
    
- [GetAppMarketplaceUrl 操作](getappmarketplaceurl-operation.md)
    

