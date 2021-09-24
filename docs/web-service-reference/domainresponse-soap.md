---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: DomainResponse 元素包含指定域的请求设置。
ms.openlocfilehash: fb7288b55452d8499596ce09c3ada9cec4b88d5b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517201"
---
# <a name="domainresponse-soap"></a>DomainResponse (SOAP)

**DomainResponse** 元素包含指定域的请求设置。 
  
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
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |包含无法返回的设置的错误信息。  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |表示在自动发现请求中提交或由自动发现响应返回的域设置。  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |标识重定向的目标。 目标可以是 URL 或电子邮件地址。  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |指定与特定请求关联的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |指定与特定请求关联的错误消息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |包含 **DomainResponse 元素** 的数组。 每个 **DomainResponse** 元素都包含指定用户的请求设置。  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |包含每个域的响应。  <br/> |
   
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

