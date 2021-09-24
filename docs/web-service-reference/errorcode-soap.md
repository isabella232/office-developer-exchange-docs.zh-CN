---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: ErrorCode 元素表示自动发现服务返回的错误代码。
ms.openlocfilehash: fa40cb8b7a2ec80ecf752058f540969013748d39
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530771"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

**ErrorCode** 元素表示自动发现服务返回的错误代码。 
  
```XML
<ErrorCode/>
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
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |包含对 SOAP ([GetFederationInformation ](getfederationinformation-operation-soap.md)) 的响应。  <br/> |
|[Response (SOAP)](response-soap.md) <br/> |包含 SOAP 请求中对 [GetUserSettings () ](getusersettings-operation-soap.md)的响应。  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |表示检索用户设置时返回的错误。  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |表示对针对单个用户 ([SOAP) GetUserSettings ](getusersettings-operation-soap.md) 操作的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示自动发现错误响应的错误代码。 下表列出了 **ErrorCode** 元素的可能文本值。 
  
|**错误代码文本值**|**说明**|
|:-----|:-----|
|NoError  <br/> |没有错误。  <br/> |
|RedirectAddress  <br/> |呼叫者必须遵循自动发现返回的电子邮件地址重定向。  <br/> |
|RedirectUrl  <br/> |调用方必须遵循自动发现返回的 URL 重定向。  <br/> |
|InvalidUser  <br/> |请求中传递的用户无效。  <br/> |
|InvalidRequest  <br/> |请求无效。  <br/> |
|InvalidSetting  <br/> |指定的设置无效。  <br/> |
|SettingIsNotAvailable  <br/> |指定的设置不可用。  <br/> |
|ServerBusy  <br/> |服务器太忙，无法处理请求。  <br/> |
|InvalidDomain  <br/> |请求的域无效。  <br/> |
|NotFederated  <br/> |组织未联合。  <br/> |
|InternalServerError  <br/> |存在内部服务器错误。  <br/> |
   
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

