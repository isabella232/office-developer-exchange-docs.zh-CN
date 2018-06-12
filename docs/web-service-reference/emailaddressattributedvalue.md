---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: EmailAddressAttributedValue 元素指定实例及其关联的归属和数组的电子邮件地址。
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754059"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

**EmailAddressAttributedValue**元素指定实例及其关联的归属和数组的电子邮件地址。 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[值 (EmailAddressType)](value-emailaddresstype.md) <br/> |指定与归属数组关联的**电子邮件地址**的值。  <br/> |
|[归属 (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |指定其关联的**值**元素的归属的数组。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |指定的电子邮件值的数组和为相关联的角色其源归属的标识符。  <br/> |
|[Emails2](emails2.md) <br/> |指定的电子邮件值的数组和为相关联的角色其源归属的标识符。  <br/> |
|[Emails3](emails3.md) <br/> |指定的电子邮件值的数组和为相关联的角色其源归属的标识符。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

