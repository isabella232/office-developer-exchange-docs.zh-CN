---
title: DisableApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 211731a3-2470-49af-bda3-1ddfc15a8e46
description: 查找有关 DisableApp EWS 操作的信息。
ms.openlocfilehash: 7a4d3a13351042cc1a192388416381ebe28206bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510153"
---
# <a name="disableapp-operation"></a>DisableApp 操作

查找有关 **DisableApp** EWS 操作的信息。 
  
**DisableApp** 操作禁用邮件应用程序Outlook。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-disableapp-operation"></a>使用 DisableApp 操作

**DisableApp** 操作在请求中采用两个参数，用于标识要禁用的邮件应用程序以及禁用它的原因。 
  
### <a name="disableapp-operation-soap-headers"></a>DisableApp 操作 SOAP 标头

**DisableApp** 操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 此标头适用于请求。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。 此标头适用于响应。  <br/> |
   
## <a name="disableapp-operation-request-example-disable-a-mail-app-installed-in-a-mailbox"></a>DisableApp 操作请求示例：禁用邮箱中安装的邮件应用程序

DisableApp 操作请求的以下示例显示如何禁用邮件应用程序。 可在 [GetAppManifests](getappmanifests-operation.md) 操作响应中返回的应用清单中找到应用程序标识符。 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:DisableApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
         <m:DisableReason>NoReason</m:DisableReason>
      </m:DisableApp>
   </soap:Body>
</soap:Envelope>
```

请求 SOAP 正文包含以下元素：
  
- [DisableApp](disableapp.md)
    
- [ID (String)](id-string.md)
    
- [DisableReason](disablereason.md)
    
## <a name="successful-disableapp-operation-response"></a>成功的 DisableApp 操作响应

以下示例显示对禁用邮件应用程序的 **DisableApp** 操作请求的成功响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文包含以下元素：
  
- [DisableAppResponse](disableappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="disableapp-operation-error-response"></a>DisableApp 操作错误响应

以下示例显示对 **DisableApp** 操作请求的错误响应。 这是对禁用未安装在邮箱中的邮件应用程序的请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="14" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1C50226D-04B5-4AB2-9FCD-42E236B59E4A can't be found.</MessageText>
         <ResponseCode>ErrorExtensionNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [DisableAppResponse](disableappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
有关 EWS 通用且特定于此操作的其他错误代码，请参阅 [ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [EWS 操作在Exchange](ews-operations-in-exchange.md)   
- [InstallApp 操作](installapp-operation.md)   
- [UninstallApp 操作](uninstallapp-operation.md)   
- [GetAppManifests](getappmanifests.md)   
- [GetAppMarketplaceUrl 操作](getappmarketplaceurl-operation.md)   
- [Outlook 外接程序](https://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

