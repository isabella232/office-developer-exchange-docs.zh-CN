---
title: 名称（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: dce6d823-dc33-4a47-babe-6370a15ac7b4
description: Name 元素表示设置的名称。
ms.openlocfilehash: 74e6d6b59d972d7230c23b38cd3f4a8591401bbd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466883"
---
# <a name="name-soap"></a>名称（SOAP）

**Name**元素表示设置的名称。 
  
```XML
<Name/>
```

**string**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSetting （SOAP）](domainsetting-soap.md) <br/> |包含由[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求返回的域设置。  <br/> |
|[DomainStringSetting （SOAP）](domainstringsetting-soap.md) <br/> |表示域设置的值的类型为 string 类型。  <br/> |
|[OrganizationRelationshipSettings （SOAP）](organizationrelationshipsettings-soap.md) <br/> |表示单个组织的组织关系列表。  <br/> |
|[UserSetting （SOAP）](usersetting-soap.md) <br/> |代表单个用户设置。  <br/> |
|[ProtocolConnectionCollectionSetting （SOAP）](protocolconnectioncollectionsetting-soap.md) <br/> |表示服务器协议连接设置的集合。  <br/> |
|[StringSetting （SOAP）](stringsetting-soap.md) <br/> |表示用户设置的值的类型为 string 类型。  <br/> |
|[WebClientUrlCollectionSetting （SOAP）](webclienturlcollectionsetting-soap.md) <br/> |表示一个用户设置，它是 Exchange Web 客户端 Url 的集合。  <br/> |
|[AlternateMailboxCollectionSetting （SOAP）](alternatemailboxcollectionsetting-soap.md) <br/> |包含备用邮箱设置的集合。  <br/> |
   
## <a name="text-value"></a>文本值

**Name**元素的文本值是设置的名称。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
- [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)
- [GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)

