---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: EmailAddress 元素指定站点邮箱或关联人员完全解析的 SMTP 地址。
ms.openlocfilehash: 76b279a82f6f277d9f231866437359ceae46df59
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545256"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

**EmailAddress** 元素指定站点邮箱或关联人员完全解析的 SMTP 地址。 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Name (string)](name-string.md) <br/> |指定搜索精简条件名称或密钥或电子邮件用户的名称。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的主 SMTP 地址。  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |指定电子邮件地址的路由类型。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |表示由电子邮件地址表示的邮箱的类型。  <br/> |
|[ItemId](itemid.md) <br/> |包含项目在项目存储中的唯一标识符Exchange项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[角色](persona.md) <br/> |指定由 **GetPersona** 请求返回的一组人员数据。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

此元素为可选。
  
**EmailAddress** 元素适用于从 Exchange 2013 Exchange Online 2013 Microsoft Exchange Server版本的客户端。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

