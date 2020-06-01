---
title: 响应（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Response 元素包含对 GetUserSettings 操作（SOAP）、GetDomainSettings 操作（SOAP）或 GetFederationInformation 操作（SOAP）请求的响应。
ms.openlocfilehash: 90cb29dd4ce4026211a5b592f149c8190dc81d29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456414"
---
# <a name="response-soap"></a>响应（SOAP）

**Response**元素包含对[GETUSERSETTINGS 操作（soap）](getusersettings-operation-soap.md)、 [GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)或[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md)请求的响应。 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 **GetUserSettingsResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[UserResponses （SOAP）](userresponses-soap.md) <br/> |包含每个请求的用户的配置设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsResponseMessage （SOAP）](getusersettingsresponsemessage-soap.md) <br/> |定义对[GetUserSettingsRequest （SOAP）](getusersettingsrequest-soap.md)的响应 <br/> |
|[GetDomainSettingsResponseMessage （SOAP）](getdomainsettingsresponsemessage-soap.md) <br/> |定义对[GetDomainSettingsRequest （SOAP）](getdomainsettingsrequest-soap.md)的响应。  <br/> |
|[GetFederationInformationResponseMessage （SOAP）](getfederationinformationresponsemessage-soap.md) <br/> |定义对[GetFederationInformationRequest （SOAP）](getfederationinformationrequest-soap.md)的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)


[Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

