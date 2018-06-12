---
title: 响应 (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Response 元素包含 GetFederationInformation 操作 (SOAP) 响应的信息。
ms.openlocfilehash: 946cba56d7503a0e20ec59640f4f1258c00a844e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827171"
---
# <a name="response-getfederationinformation-soap"></a>响应 (GetFederationInformation) (SOAP)

**Response**元素包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应的信息。 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <ApplicationUri/>
   <Domains/>
</Response>
```

 **GetFederationInformationResponse**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |代表由自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |代表相关联的自动发现服务返回的错误代码的邮件。  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |定义应用程序的位置。  <br/> |
|[域 (SOAP)](domains-soap.md) <br/> |代表为其配置返回在[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)或组织具有联合[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中的域的域集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |定义[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

