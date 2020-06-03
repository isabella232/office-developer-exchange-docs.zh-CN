---
title: 域（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Domain 元素表示在 GetDomainSettings 操作（SOAP）中返回的域集合、组织在 GetFederationInformation 操作（SOAP）中进行了联合的域，或者由 GetOrganizationRelationshipSettings 操作（SOAP）返回的具有组织关系关系的域。
ms.openlocfilehash: c56fb72841776c0060c1300b52b2f6a06b1ec0ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526303"
---
# <a name="domains-soap"></a>域（SOAP）

Domain**元素表示**在[GETDOMAINSETTINGS 操作（soap）](getdomainsettings-operation-soap.md)中返回的域集合、组织在[GetFederationInformation 操作（soap）](getfederationinformation-operation-soap.md)中进行了联合的域，或者由[GetOrganizationRelationshipSettings 操作（soap）](getorganizationrelationshipsettings-operation-soap.md)返回的具有组织关系关系的域。
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **域**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域（SOAP）](domain-soap.md) <br/> |代表单个域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsRequest （SOAP）](getdomainsettingsrequest-soap.md) <br/> |表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求。  <br/> |
|[响应（GetFederationInformation）（SOAP）](response-getfederationinformationsoap.md) <br/> |包含[GetFederationInformation 操作（SOAP）](getfederationinformation-operation-soap.md)响应信息。  <br/> |
|[GetOrganizationRelationshipSettingsRequest （SOAP）](getorganizationrelationshipsettingsrequest-soap.md) <br/> |表示[GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)请求。  <br/> |
   
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

- [GetDomainSettingsRequest （SOAP）](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse （SOAP）](getfederationinformationresponse-soap.md)

