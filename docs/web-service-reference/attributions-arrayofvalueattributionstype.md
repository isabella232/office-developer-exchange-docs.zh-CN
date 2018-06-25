---
title: 归属 (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: 归属元素指定其关联的值元素的归属的数组。
ms.openlocfilehash: a64510cacb9923682418ca8a9b203c765a129bdd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753297"
---
# <a name="attributions-arrayofvalueattributionstype"></a>归属 (ArrayOfValueAttributionsType)

**归属**元素指定其关联的**值**元素的归属的数组。 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[归属 （字符串）](attribution-string.md) <br/> |指定用于标识属性的字符串。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |指定项目的正文内容。  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |指定一个电子邮件地址和其关联的归属的数组的实例。  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |指定角色扩展的的属性。  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |指定一个电话号码和其关联的归属的数组的实例。  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |指定的邮政地址和其关联的归属声明数组的实例。  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |指定个人元素的字符串数据类型数组的实例。  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |数组中的关联的个人元素的属性中指定的实例。  <br/> |
   
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

