---
title: DomainNames （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: DomainNames 元素表示域名集合。 DomainNames 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 0b425b3cd4c0e7cb2427920d61feb04010a3b123
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458416"
---
# <a name="domainnames-soap"></a>DomainNames （SOAP）

**DomainNames**元素表示域名集合。 **DomainNames**元素仅供内部使用。 客户端不使用此元素。 
  
```XML
<DomainNames>
    <Domains/>
</DomainNames>
```

 **DomainNames**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域（SOAP）](domains-soap.md) <br/> |表示从[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)、 [GETFEDERATIONINFORMATION 操作（Soap）](getfederationinformation-operation-soap.md)或[GetOrganizationRelationshipSettings 操作（soap）](getorganizationrelationshipsettings-operation-soap.md)返回的域的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettings （SOAP）](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

此元素表示外部组织的 SMTP 域。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

