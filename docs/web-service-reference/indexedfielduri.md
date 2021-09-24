---
title: IndexedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IndexedFieldURI
api_type:
- schema
ms.assetid: 5c9cd0b5-7eca-480a-8730-fe98b1779afa
description: IndexedFieldURI 元素标识字典的单个成员。
ms.openlocfilehash: 851d0d4296e926ab21e5bd1b842d5a215c27308a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539624"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

**IndexedFieldURI** 元素标识字典的单个成员。 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识包含要返回的成员的字典。 此特性是必需的。  <br/> |
|**FieldIndex** <br/> |标识要返回的词典的成员。 此特性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|item：InternetMessageHeader  <br/> |表示项目的邮件头。  <br/> |
|contacts：ImAddress  <br/> |表示联系人的即时消息地址。  <br/> |
|contacts：PhysicalAddress：Street  <br/> |表示联系人的街道地址。  <br/> |
|contacts：PhysicalAddress：City  <br/> |表示联系人的城市。  <br/> |
|contacts：PhysicalAddress：State  <br/> |表示联系人的状态。  <br/> |
|contacts：PhysicalAddress：Country  <br/> |表示联系人的国家/地区。  <br/> |
|contacts：PhysicalAddress：PostalCode  <br/> |表示联系人的邮政编码。  <br/> |
|contacts：PhoneNumber  <br/> |表示联系人的电话号码。  <br/> |
|contacts：EmailAddress  <br/> |表示联系人的电子邮件地址。  <br/> |
|distributionlist：Members：Member  <br/> |表示一个通讯组列表的成员。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |标识要获取、设置或创建的其他属性。  <br/> |
|[AggregateOn](aggregateon.md) <br/> |代表用于确定分组的 FindItem 项目的分组顺序的属性结果集。  <br/> |
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

