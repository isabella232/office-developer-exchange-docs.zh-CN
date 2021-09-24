---
title: Response (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: Response 元素包含对 GetUserSettings 操作的响应 (SOAP) 、GetDomainSettings 操作 (SOAP) 或 GetFederationInformation 操作 (SOAP) 请求。
ms.openlocfilehash: d42014991db8e93f88b80bed97970f043290cfb1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512357"
---
# <a name="response-soap"></a>Response (SOAP)

**Response** 元素包含对 [GetUserSettings](getusersettings-operation-soap.md)操作的响应 (SOAP) 、GetDomainSettings [操作 (SOAP)](getdomainsettings-operation-soap.md)或 [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求。 
  
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
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |包含每个请求的用户的配置设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsResponseMessage (SOAP)](getusersettingsresponsemessage-soap.md) <br/> |定义对 SOAP ([GetUserSettingsRequest](getusersettingsrequest-soap.md))  <br/> |
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |定义对 [GETDomainSettingsRequest ](getdomainsettingsrequest-soap.md) (SOAP) 的响应。  <br/> |
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |定义对 SOAP ([GetFederationInformationRequest) 的响应 ](getfederationinformationrequest-soap.md)。  <br/> |
   
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


[自动发现 Web 服务引用Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)

