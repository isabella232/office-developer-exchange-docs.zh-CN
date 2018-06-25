---
title: 域 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: 域元素均表示返回 GetDomainSettings 操作 (SOAP)、 组织具有联合 GetFederationInformation 操作 (SOAP) 中的域或与组织关系作为域中的域集合返回由 GetOrganizationRelationshipSettings 操作 (SOAP)。
ms.openlocfilehash: 7a21a3a09516de2d1c38021ca3ccd2161d9cdd1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753982"
---
# <a name="domains-soap"></a>域 (SOAP)

**域**元素均表示返回[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)、 组织已在[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)中，联合域或域中的域集合返回由[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)的组织关系。
  
```XML
<Domains>
   <Domain/>
</Domains>
```

 **域**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域 (SOAP)](domain-soap.md) <br/> |代表单个域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |代表[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)请求。  <br/> |
|[响应 (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |包含[GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)响应的信息。  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |代表[GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)请求。  <br/> |
   
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

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

