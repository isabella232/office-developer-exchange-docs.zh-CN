---
title: GetFederationInformationResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: GetFederationInformationResponse 元素包含 GetFederationInformation 操作（SOAP）响应。
ms.openlocfilehash: c9e65a2b1759946b8493b3c730f08df6fe353fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460041"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse （SOAP）

**GetFederationInformationResponse**元素包含[GETFEDERATIONINFORMATION 操作（SOAP）](getfederationinformation-operation-soap.md)响应。 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
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
|[TokenIssuers （SOAP）](tokenissuers-soap.md) <br/> |表示安全令牌的集合，其中包含安全令牌服务标识符和终结点。  <br/> |
|[域（SOAP）](domains-soap.md) <br/> |代表域在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md) **GetDomainSettings**操作中返回的配置或组织在[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md) **GetFederationInformation**操作中进行了联合的域。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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



[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)

