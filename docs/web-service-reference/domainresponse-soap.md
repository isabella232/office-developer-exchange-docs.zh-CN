---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: DomainResponse 元素包含指定的域的请求的设置。
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753975"
---
# <a name="domainresponse-soap"></a>DomainResponse (SOAP)

**DomainResponse**元素包含指定的域的请求的设置。 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 **DomainResponse**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |包含错误未能返回的设置的信息。  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |表示已提交的自动发现请求中或由自动发现响应返回的域设置。  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |标识目标的重定向。 URL 或电子邮件地址可以是目标。  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |指定与特定的请求相关联的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |指定与特定的请求相关联的错误消息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |包含**DomainResponse**元素的数组。 每个**DomainResponse**元素包含指定的用户的请求的设置。  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |包含为每个域的响应。  <br/> |
   
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

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

