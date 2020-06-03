---
title: 响应（GetFederationInformation）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Response 元素包含 GetFederationInformation 操作（SOAP）响应信息。
ms.openlocfilehash: 0b9a2c518b968faa6ef86b7c1f544eac40f8e5c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530584"
---
# <a name="response-getfederationinformation-soap"></a>响应（GetFederationInformation）（SOAP）

**Response**元素包含[GETFEDERATIONINFORMATION 操作（SOAP）](getfederationinformation-operation-soap.md)响应信息。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[ApplicationUri （SOAP）](applicationuri-soap.md) <br/> |定义应用程序的位置。  <br/> |
|[域（SOAP）](domains-soap.md) <br/> |代表域集合在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)中返回的配置，或组织在[GETFEDERATIONINFORMATION 操作（soap）](getfederationinformation-operation-soap.md)中联合的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationResponseMessage （SOAP）](getfederationinformationresponsemessage-soap.md) <br/> |定义对[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

