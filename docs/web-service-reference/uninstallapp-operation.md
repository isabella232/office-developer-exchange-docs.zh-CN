---
title: UninstallApp 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: 查找信息 UninstallApp EWS 操作。
ms.openlocfilehash: 4f44224651993023336eef5540ec29b7f6a6e32e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838320"
---
# <a name="uninstallapp-operation"></a>UninstallApp 操作

查找有关**UninstallApp** EWS 操作的信息。 
  
**UninstallApp**操作卸载 outlook 邮件应用程序。 
  
Exchange Server 2013 中引入了此操作。
  
## <a name="using-the-uninstallapp-operation"></a>使用 UninstallApp 操作

**UninstallApp**操作请求中的标识邮件应用程序卸载采用一个参数。 
  
### <a name="uninstallapp-operation-soap-headers"></a>UninstallApp 操作 SOAP 标头

**UninstallApp**操作可以使用下表中列出的 SOAP 标头。 
  
|**标头名称**|**元素**|**说明**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。 适用于请求此标头。  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。 适用于响应此标头。  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a>UninstallApp 操作请求示例： 卸载邮箱中的邮件应用程序

下面的示例**UninstallApp**操作的请求显示如何向卸载邮件应用程序使用的应用程序标识符。 可以由[GetAppManifests 操作](getappmanifests-operation.md)返回应用程序清单中找到应用程序标识符。
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:UninstallApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
      </m:UninstallApp>
   </soap:Body>
</soap:Envelope>
```

请求 SOAP 正文包含以下元素：
  
- [UninstallApp](uninstallapp.md)
    
- [ID （字符串）](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a>成功 UninstallApp 操作响应

下面的示例演示对**UninstallApp**操作请求卸载邮件应用程序的成功响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

响应 SOAP 正文中包含以下元素：
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a>UninstallApp 操作错误响应

下面的示例演示**UninstallApp**操作请求错误响应。 这是卸载已卸载的邮件应用程序请求的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

错误响应 SOAP 正文包含以下元素：
  
- [UninstallAppResponse](uninstallappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
通用到 EWS 且特定于此操作的其他错误代码，请参阅[ResponseCode](responsecode.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
    
- [InstallApp 操作](installapp-operation.md)
    
- [DisableApp 操作](disableapp-operation.md)
    
- [GetAppManifests](getappmanifests.md)
    
- [GetAppMarketplaceUrl 操作](getappmarketplaceurl-operation.md)
    

