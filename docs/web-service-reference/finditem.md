---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: FindItem 元素定义查找邮箱中的项目的请求。
ms.openlocfilehash: 6664cd91007f1d39db7e8d446e0135f47d5ab932
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353922"
---
# <a name="finditem"></a>FindItem

**FindItem**元素定义查找邮箱中的项目的请求。 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


**FindItemType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**遍历** <br/> |定义搜索是否查找文件夹或文件夹的垃圾站中的项目。 此属性是必需的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |返回文件夹中的项的标识。  <br/> |
|带有 SoftDeleted  <br/> |返回仅的文件夹中的项的标识转储程序。 注意与搜索限制组合软删除遍历将导致返回零项即使有与搜索条件匹配项。  <br/> |
|关联  <br/> |返回文件夹中仅的相关联的项的标识。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识项目属性和[FindItem 操作](finditem-operation.md)响应中包括的内容。  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何分页的项信息**FindItem**请求返回。 此元素是可选的。  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |介绍其中分页的视图启动和**FindItem**请求中返回的最大项目数。 通过一小部分介绍了从找到项集开头的分页的视图偏移量。 此元素是可选的。  <br/> |
|[CalendarView](calendarview.md) <br/> |提供时间跨越限制以定义搜索的日历项目。 此元素是可选的。  <br/> |
|[ContactsView](contactsview.md) <br/> |定义搜索联系人项目基于按字母顺序排列的显示名称。 此元素是可选的。  <br/> |
|[GroupBy](groupby.md) <br/> |指定**FindItem**查询的任意分组。 此元素是可选的。  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |提供用于**FindItem**查询标准分组。 此元素是可选的。  <br/> |
|[限制](restriction.md) <br/> |定义的限制或用于筛选项目或**FindItem**中的文件夹的查询/ **FindFolder**和搜索文件夹的操作。 此元素是可选的。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义项 FindItem 请求中的排序方式。 此元素是可选的。  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识要搜索的 FindItem 和 FindFolder 操作的文件夹。  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |包含基于上高级查询语法 (AQS) 邮箱查询字符串。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

只有一个[IndexedPageItemView](indexedpageitemview.md)、 [FractionalPageItemView](fractionalpageitemview.md)、 [CalendarView](calendarview.md)，或[ContactsView](contactsview.md)元素可以包含在**FindItem**请求。 只有一个[GroupBy](groupby.md)或[DistinguishedGroupBy](distinguishedgroupby.md)元素可以包含在**FindItem**请求。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindItem 操作](finditem-operation.md)
- [查找项目](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

