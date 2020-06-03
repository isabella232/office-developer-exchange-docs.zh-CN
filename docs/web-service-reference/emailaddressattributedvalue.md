---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: EmailAddressAttributedValue 元素指定电子邮件地址数组的实例及其关联的归属。
ms.openlocfilehash: 09fdd5921cef3d70a6da4b6d4d38f08834c5d482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530689"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

**EmailAddressAttributedValue**元素指定电子邮件地址数组的实例及其关联的归属。 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Value （EmailAddressType）](value-emailaddresstype.md) <br/> |指定与归属数组相关联的**EmailAddress**的值。  <br/> |
|[归属（ArrayOfValueAttributionsType）](attributions-arrayofvalueattributionstype.md) <br/> |为其关联的**Value**元素指定归属的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |为关联角色的电子邮件值和其源归属的标识符指定一个数组。  <br/> |
|[Emails2](emails2.md) <br/> |为关联角色的电子邮件值和其源归属的标识符指定一个数组。  <br/> |
|[Emails3](emails3.md) <br/> |为关联角色的电子邮件值和其源归属的标识符指定一个数组。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

