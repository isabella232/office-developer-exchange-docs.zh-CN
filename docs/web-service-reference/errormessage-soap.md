---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: ErrorMessage 元素均表示一条消息，与错误代码返回的自动发现服务相关联。
ms.openlocfilehash: 888eedc9c7cbbd1aad5cba21e76d999699c7ed02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754156"
---
# <a name="errormessage-soap"></a>ErrorMessage (SOAP)

**ErrorMessage**元素均表示一条消息，与错误代码返回的自动发现服务相关联。 
  
```XML
<ErrorMessage/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |代表由自动发现服务返回的所有响应的基类型。  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |包含指定的域的请求的设置。  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |包含对各个域[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)呼叫的响应。  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |包含对[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。  <br/> |
|[响应 (SOAP)](response-soap.md) <br/> |包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |代表在检索用户设置时返回的错误。  <br/> |
|[用户回音 (SOAP)](userresponse-soap.md) <br/> |代表对单个用户[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示的错误消息。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

