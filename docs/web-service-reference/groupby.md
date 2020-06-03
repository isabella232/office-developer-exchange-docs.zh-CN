---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: GroupBy 元素指定 FindItem 查询的任意分组。
ms.openlocfilehash: 0d681e5376e4dd71921cc97f270211e49179db85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530097"
---
# <a name="groupby"></a>GroupBy

**GroupBy**元素指定 FindItem 查询的任意分组。 
  
- [FindItem](finditem.md)
- [GroupBy](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

**GroupByType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Order** <br/> | 确定在响应中返回的分组项数组中组的顺序。 此属性的类型为 SortDirectionType。  <br/> |
   
#### <a name="order-attribute-values"></a>顺序属性值

|**值**|**说明**|
|:-----|:-----|
|升序  <br/> |组按升序排列。  <br/> |
|降序  <br/> |组按降序排列。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识要获取、设置或创建的扩展 MAPI 属性。  <br/> |
|[AggregateOn](aggregateon.md) <br/> |表示用于确定响应中的组顺序的字段。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |定义在邮箱中查找项目的请求。  <br/><br/> 下面是此元素的 XPath 表达式:  `/FindItem` <br/> |
   
## <a name="remarks"></a>备注

FindItem 响应将包含组的集合。 每个组将包含具有**GroupBy**属性的匹配值的所有项目。 确定分组的属性在[FieldURI](fielduri.md)、 [IndexedFieldURI](indexedfielduri.md)或[ExtendedFieldURI](extendedfielduri.md)元素中进行标识。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindItem 操作](finditem-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

