---
title: Attributions (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: Attributions 元素指定与其关联的 Value 元素的属性数组。
ms.openlocfilehash: e5483e8e7ef4745e8025106ae1f1c52e91987183
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529326"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Attributions (ArrayOfValueAttributionsType)

**Attributions** 元素指定与其关联的 **Value** 元素的属性数组。 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Attribution (string)](attribution-string.md) <br/> |指定用于标识属性的字符串。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |指定项目的正文内容。  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |指定电子邮件地址数组及其关联属性的实例。  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |指定一个人物的扩展属性。  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |指定电话号码数组及其关联属性的实例。  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |指定一个邮政地址数组及其关联属性的实例。  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |指定 persona 元素的字符串数据数组的实例。  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |指定与 persona 元素关联的属性数组中的实例。  <br/> |
   
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

