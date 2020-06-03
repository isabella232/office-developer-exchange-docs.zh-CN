---
title: 归属（ArrayOfValueAttributionsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: 归属元素为其关联的 Value 元素指定归属的数组。
ms.openlocfilehash: 9fd552670c529009838125063869f65e130c1e63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463991"
---
# <a name="attributions-arrayofvalueattributionstype"></a>归属（ArrayOfValueAttributionsType）

**归属**元素为其关联的**Value**元素指定归属的数组。 
  
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
|[特性（string）](attribution-string.md) <br/> |指定用于标识属性的字符串。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |指定项目的正文内容。  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |指定电子邮件地址数组的实例及其关联的归属。  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |指定角色的扩展属性。  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |指定电话号码数组的实例及其关联的归属。  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |指定邮政地址数组的实例及其关联的归属。  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |指定一个 persona 元素的字符串数据数组的实例。  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |指定与 persona 元素相关联的属性数组中的实例。  <br/> |
   
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

