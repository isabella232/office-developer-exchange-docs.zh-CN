---
title: 响应 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Response 元素包含对 GetUserSettings 操作 (SOAP)、 GetDomainSettings 操作 (SOAP) 或 GetFederationInformation 操作 (SOAP) 请求的响应。
ms.openlocfilehash: 240c8e1f904ad685b51c1f657b2bc18e14fd985e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827179"
---
# <a name="response-soap"></a>响应 (SOAP)

**Response**元素包含对[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)、 [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)或[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 **GetUserSettingsResponse**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |代表由自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |代表相关联的自动发现服务返回的错误代码的邮件。  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |包含为每个请求的用户的配置设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsResponseMessage (SOAP)](getusersettingsresponsemessage-soap.md) <br/> |定义对[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md)的响应 <br/> |
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |定义对[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)的响应。  <br/> |
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |定义对[GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md)的响应。  <br/> |
   
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



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)


[Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

