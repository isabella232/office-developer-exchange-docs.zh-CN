---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: GetFederationInformationResponse 元素包含 GetFederationInformation 操作 (SOAP) 响应。
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754556"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

**GetFederationInformationResponse**元素包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应。 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 **GetFederationInformationResponse**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |代表由自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |代表相关联的自动发现服务返回的错误代码的邮件。  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |定义应用程序的位置。  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |表示安全令牌，其中包含安全令牌服务标识符和终结点的集合。  <br/> |
|[域 (SOAP)](domains-soap.md) <br/> |代表为其配置[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings**操作中返回的域或组织具有联合[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中的域**GetFederationInformation**操作。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

