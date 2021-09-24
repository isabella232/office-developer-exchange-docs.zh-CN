---
title: Domains (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5f81d1b7-c6a4-456f-9935-13d04a3d92d7
description: Domains 元素表示 GetDomainSettings 操作 (SOAP) 中返回的域集合、组织在 GetFederationInformation 操作 (SOAP) 中联合的域，或由 GetOrganizationRelationshipSettings 操作 (SOAP) 返回的具有组织关系的域。
ms.openlocfilehash: 667b2611ce8b393252f9bdda6dd7ec201b605047
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538321"
---
# <a name="domains-soap"></a>Domains (SOAP)

**Domains** 元素表示 [GetDomainSettings](getdomainsettings-operation-soap.md)操作 (SOAP) 中返回的域集合、组织在 [GetFederationInformation](getfederationinformation-operation-soap.md)操作 (SOAP) 中联合的域，或 [由 GetOrganizationRelationshipSettings](getorganizationrelationshipsettings-operation-soap.md)操作 (SOAP) 返回的具有组织关系的域。
  
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
|[Domain (SOAP)](domain-soap.md) <br/> |表示单个域。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |表示 [SOAP 请求 (GetDomainSettings) ](getdomainsettings-operation-soap.md) 操作。  <br/> |
|[Response (GetFederationInformation) (SOAP)](response-getfederationinformationsoap.md) <br/> |包含 [SOAP 响应 (GetFederationInformation) ](getfederationinformation-operation-soap.md) 操作。  <br/> |
|[GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) <br/> |表示 [SOAP 请求 (GetOrganizationRelationshipSettings) ](getorganizationrelationshipsettings-operation-soap.md) 操作。  <br/> |
   
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

- [GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md)  
- [GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md)

