---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: ErrorCode 元素均表示由自动发现服务返回的错误代码。
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754146"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

**ErrorCode**元素均表示由自动发现服务返回的错误代码。 
  
```XML
<ErrorCode/>
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

文本值表示的错误代码为自动发现错误响应。 下表列出了**ErrorCode**元素的可能的文本值。 
  
|**错误代码的文本值**|**说明**|
|:-----|:-----|
|NoError  <br/> |没有错误。  <br/> |
|RedirectAddress  <br/> |呼叫者必须遵循的电子邮件地址重定向返回的自动发现。  <br/> |
|RedirectUrl  <br/> |呼叫者必须遵循返回的自动发现 URL 重定向。  <br/> |
|InvalidUser  <br/> |无效的用户的请求中传递。  <br/> |
|InvalidRequest  <br/> |请求无效。  <br/> |
|InvalidSetting  <br/> |指定的设置无效。  <br/> |
|SettingIsNotAvailable  <br/> |指定的设置不可用。  <br/> |
|ServerBusy  <br/> |服务器太忙而无法处理请求。  <br/> |
|InvalidDomain  <br/> |所请求的域无效。  <br/> |
|NotFederated  <br/> |非联盟组织。  <br/> |
|InternalServerError  <br/> |没有内部服务器错误。  <br/> |
   
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

