---
title: ErrorMessage (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: b84dd664-4c49-42c9-a49f-2ec4a9f7588b
description: ErrorMessage 元素表示与自动发现服务返回的错误代码相关联的消息。
ms.openlocfilehash: ebaa20f796787862ce3438bd496e29f88cb6ec6a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517075"
---
# <a name="errormessage-soap"></a>ErrorMessage (SOAP)

**ErrorMessage** 元素表示与自动发现服务返回的错误代码相关联的消息。 
  
```XML
<ErrorMessage/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |表示自动发现服务返回的所有响应的基本类型。  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |包含指定域的请求设置。  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |包含对单个域的 SOAP ([调用) GetDomainSettings ](getdomainsettings-operation-soap.md) 操作的响应。  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |包含 SOAP 请求对[GetFederationInformation (的响应) 。](getfederationinformation-operation-soap.md)  <br/> |
|[Response (SOAP)](response-soap.md) <br/> |包含 SOAP 请求中对 [GetUserSettings () ](getusersettings-operation-soap.md) 的响应。  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |表示检索用户设置时返回的错误。  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |表示对针对单个用户 ([SOAP) GetUserSettings ](getusersettings-operation-soap.md) 操作的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示错误消息。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
  
[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

