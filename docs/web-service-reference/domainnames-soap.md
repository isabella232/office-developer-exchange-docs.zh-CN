---
title: DomainNames (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 79ffc3f9-25c4-40b5-84ce-09a3c5f892fa
description: DomainNames 元素表示域名集合。 DomainNames 元素供内部使用。 此元素不由客户端使用。
ms.openlocfilehash: 7697b05d7432051b9048837cb41894684f52be15
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526414"
---
# <a name="domainnames-soap"></a>DomainNames (SOAP)

**DomainNames** 元素表示域名集合。 **DomainNames** 元素供内部使用。 此元素不由客户端使用。 
  
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
|[Domains (SOAP)](domains-soap.md) <br/> |表示从 [GetDomainSettings ](getdomainsettings-operation-soap.md)操作 (SOAP [) 、GetFederationInformation 操作 (SOAP) ](getfederationinformation-operation-soap.md)或 [GetOrganizationRelationshipSettings ](getorganizationrelationshipsettings-operation-soap.md)操作 (SOAP) 返回的域的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[OrganizationRelationshipSettings (SOAP)](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

此元素表示外部组织的 SMTP 域。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)

