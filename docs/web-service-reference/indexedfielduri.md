---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: IndexedFieldURI 元素标识字典中的各个成员。
ms.openlocfilehash: f794d9970590417d916925f7258b28d4f0920d0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467016"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

**IndexedFieldURI**元素标识字典中的各个成员。 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识包含要返回的成员的词典。 此特性是必需的。  <br/> |
|**FieldIndex** <br/> |标识要返回的字典的成员。 此特性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|项： InternetMessageHeader  <br/> |表示项目的邮件头。  <br/> |
|联系人： ImAddress  <br/> |表示联系人的即时消息地址。  <br/> |
|联系人： PhysicalAddress：街道  <br/> |表示联系人的街道地址。  <br/> |
|联系人： PhysicalAddress： City  <br/> |表示联系人所在的城市。  <br/> |
|联系人： PhysicalAddress： State  <br/> |表示联系人的状态。  <br/> |
|联系人： PhysicalAddress：国家/地区  <br/> |表示联系人所在的国家/地区。  <br/> |
|联系人： PhysicalAddress：邮政编码  <br/> |表示联系人的邮政编码。  <br/> |
|联系人： PhoneNumber  <br/> |表示联系人的电话号码。  <br/> |
|联系人： EmailAddress  <br/> |表示联系人的电子邮件地址。  <br/> |
|distributionlist： Members： Member  <br/> |表示一个通讯组列表的成员。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |标识要获取、设置或创建的其他属性。  <br/> |
|[AggregateOn](aggregateon.md) <br/> |表示一个属性，该属性用于确定分组的 FindItem 结果集的分组项的顺序。  <br/> |
|[GroupBy](groupby.md) <br/> |指定 FindItem 查询的任意分组。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

