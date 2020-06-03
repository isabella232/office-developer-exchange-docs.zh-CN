---
title: DomainResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: DomainResponse 元素包含指定域的请求的设置。
ms.openlocfilehash: dea6e36c51ceea53201b668cfba616c03a44df86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456960"
---
# <a name="domainresponse-soap"></a>DomainResponse （SOAP）

**DomainResponse**元素包含指定域的请求的设置。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSettingErrors （SOAP）](domainsettingerrors-soap.md) <br/> |包含无法返回的设置的错误消息。  <br/> |
|[DomainSettings （SOAP）](domainsettings-soap.md) <br/> |表示在自动发现请求中提交或由自动发现响应返回的域设置。  <br/> |
|[RedirectTarget （SOAP）](redirecttarget-soap.md) <br/> |标识重定向的目标。 目标可以是 URL，也可以是电子邮件地址。  <br/> |
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |指定与特定请求相关联的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |指定与特定请求相关联的错误消息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ArrayOfDomainResponse （SOAP）](arrayofdomainresponse-soap.md) <br/> |包含**DomainResponse**元素的数组。 每个**DomainResponse**元素都包含指定用户的请求的设置。  <br/> |
|[DomainResponses （SOAP）](domainresponses-soap.md) <br/> |包含每个域的响应。  <br/> |
   
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

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

