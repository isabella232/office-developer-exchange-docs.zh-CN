---
title: Response (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: ca48a4b3-5006-4bb7-973e-d9137ce67e16
description: Response 元素包含 SOAP 响应 (GetFederationInformation) 操作。
ms.openlocfilehash: b5618dc1d2c862e504ea3134b28edca39c71f62c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523522"
---
# <a name="response-getfederationinformation-soap"></a>Response (GetFederationInformation) (SOAP)

**Response** 元素包含 SOAP 响应 ([GetFederationInformation)](getfederationinformation-operation-soap.md)操作。 
  
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
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |定义应用程序的位置。  <br/> |
|[Domains (SOAP)](domains-soap.md) <br/> |表示域集合 [GetDomainSettings ](getdomainsettings-operation-soap.md)操作 (SOAP) 中返回的配置，或组织在 [GetFederationInformation ](getfederationinformation-operation-soap.md)操作 (SOAP) 中联合的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |定义 SOAP 请求中 [对 GetFederationInformation () ](getfederationinformation-operation-soap.md) 的响应。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

