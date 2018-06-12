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
ms.openlocfilehash: 6a75e8855ecabf15ca31bb1e05d569c258a43b0b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825909"
---
# <a name="indexedfielduri"></a>IndexedFieldURI

**IndexedFieldURI**元素标识字典中的各个成员。 
  
```xml
<IndexedFieldURI FieldURI="" FieldIndex="" />
```

 **PathToIndexedFieldType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**FieldURI** <br/> |标识字典，其中包含要返回的成员。 此属性是必需的。  <br/> |
|**FieldIndex** <br/> |标识要返回的词典的成员。 此属性是必需的。  <br/> |
   
#### <a name="fielduri-attribute"></a>FieldURI 属性

|**值**|**说明**|
|:-----|:-----|
|项目： InternetMessageHeader  <br/> |表示项目的邮件头。  <br/> |
|联系人： ImAddress  <br/> |代表即时消息联系人的地址。  <br/> |
|联系人： PhysicalAddress:Street  <br/> |表示联系人的街道地址。  <br/> |
|联系人： PhysicalAddress:City  <br/> |代表联系人的城市。  <br/> |
|联系人： PhysicalAddress:State  <br/> |表示联系人的状态。  <br/> |
|联系人： PhysicalAddress:Country  <br/> |代表国家/地区的联系人。  <br/> |
|联系人： PhysicalAddress:PostalCode  <br/> |代表联系人的邮政编码。  <br/> |
|联系人： PhoneNumber  <br/> |代表联系人的电话号码。  <br/> |
|联系人： 电子邮件地址  <br/> |代表联系人的电子邮件地址。  <br/> |
|distributionlist:Members:Member  <br/> |表示一个通讯组列表的成员。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AdditionalProperties](additionalproperties.md) <br/> |标识要获取、 设置或创建的其他属性。  <br/> |
|[AggregateOn](aggregateon.md) <br/> |代表用于确定组合 FindItem 结果集的顺序分组的项目的属性。  <br/> |
|[GroupBy](groupby.md) <br/> |指定 FindItem 查询任意分组。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

