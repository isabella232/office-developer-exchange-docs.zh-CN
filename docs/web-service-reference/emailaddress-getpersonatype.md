---
title: EmailAddress (GetPersonaType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: GetPersonaType (的 EmailAddress) 元素指定与人员相关联的电子邮件地址。
ms.openlocfilehash: 7d024234c66c2b90bdd5d04f25d67db54770bdb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520801"
---
# <a name="emailaddress-getpersonatype"></a>EmailAddress (GetPersonaType)

**EmailAddress (GetPersonaType)** 元素指定与人员相关联的电子邮件地址。 
  
```XML
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
    <OriginalDisplayName></OriginalDisplayName>
</EmailAddress>>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[名称 (字符串) ](name-string.md)  | [EmailAddress (NonEmptyStringType) ](emailaddress-nonemptystringtype.md)  | [RoutingType (EmailAddressType) ](routingtype-emailaddresstype.md)  | [MailboxType](mailboxtype.md)  | [ItemId](itemid.md)  | [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>父元素

[GetPersona](getpersona.md)
  
## <a name="remarks"></a>说明

Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetPersona](getpersona.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

