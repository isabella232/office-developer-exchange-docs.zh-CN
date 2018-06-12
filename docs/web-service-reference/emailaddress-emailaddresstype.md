---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: EmailAddress 元素指定站点邮箱或相关联的角色的完全解析的 SMTP 地址。
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754042"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

**EmailAddress**元素指定站点邮箱或相关联的角色的完全解析的 SMTP 地址。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[名称 （字符串）](name-string.md) <br/> |指定搜索精简条件名称或键或电子邮件用户的名称。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |定义邮箱用户的主 SMTP 的地址。  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |指定传送的电子邮件地址类型。  <br/> |
|[MailboxType](mailboxtype.md) <br/> |表示由的电子邮件地址的邮箱的类型。  <br/> |
|[ItemId](itemid.md) <br/> |包含在 Exchange 存储中的项目的唯一标识符和更改的键。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[角色](persona.md) <br/> |指定一组个人**GetPersona**请求返回的数据。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

此元素为可选。
  
适用于 Exchange Online 和版本的开头 Exchange 2013 的 Microsoft Exchange Server 的目标设定的客户端的**EmailAddress**元素。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

