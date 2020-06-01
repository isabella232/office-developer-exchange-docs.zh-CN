---
title: Value （EmailAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: Value 元素指定与归属数组相关联的 EmailAddress 的值。
ms.openlocfilehash: 45af2aaab7d2475ae46ae24ed13b1435f5b352c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467597"
---
# <a name="value-emailaddresstype"></a>Value （EmailAddressType）

**Value**元素指定与归属数组相关联的**EmailAddress**的值。 
  
```XML
<Value>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
   <OriginalDisplayName/>
</Value>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[名称（字符串）](name-string.md)  | [EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)  | [RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)  | [MailboxType](mailboxtype.md)  | [ItemId](itemid.md)  | [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>父元素

[EmailAddressAttributedValue](emailaddressattributedvalue.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

