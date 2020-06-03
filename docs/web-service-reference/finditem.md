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
description: FindItem 元素定义一个请求，以查找邮箱中的项目。
ms.openlocfilehash: 3aeda1cffc03292734a91bc3fff3289d51c9b445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460993"
---
# <a name="finditem"></a>FindItem

**FindItem**元素定义一个请求，以查找邮箱中的项目。 
  
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
|**遍历** <br/> |定义搜索是查找文件夹中的项目还是文件夹的 dumpsters。 此特性是必需的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |仅返回文件夹中项的标识。  <br/> |
|SoftDeleted  <br/> |仅返回文件夹的转储程序中项的标识。 请注意，与搜索限制组合在一起的软删除的遍历将导致返回零个项目，即使存在与搜索条件匹配的项目也是如此。  <br/> |
|相应  <br/> |仅返回文件夹中关联项的标识。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识要包括在[FindItem 操作](finditem-operation.md)响应中的项目属性和内容。  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何为**FindItem**请求返回分页项目信息。 此元素为可选。  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |介绍分页视图的起始位置和**FindItem**请求中返回的最大项目数。 从一组找到的项目开始的分页视图偏移量按分数进行描述。 此元素为可选。  <br/> |
|[CalendarView](calendarview.md) <br/> |提供用于定义对日历项目的搜索的时间跨度限制。 此元素为可选。  <br/> |
|[ContactsView](contactsview.md) <br/> |根据字母显示名称定义对联系人项目的搜索。 此元素为可选。  <br/> |
|[GroupBy](groupby.md) <br/> |指定**FindItem**查询的任意分组。 此元素为可选。  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |提供**FindItem**查询的标准分组。 此元素为可选。  <br/> |
|[限制](restriction.md) <br/> |定义用于筛选**FindItem** /  **FindFolder**和 search folder 操作中的项或文件夹的限制或查询。 此元素为可选。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义如何在 FindItem 请求中对项目进行排序。 此元素是可选的。  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识用于搜索 FindItem 和 FindFolder 操作的文件夹。  <br/> |
|[QueryString （QueryStringType）](querystring-querystringtype.md) <br/> |包含基于高级查询语法（AQS）的邮箱查询字符串。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

**FindItem**请求中只能包含[IndexedPageItemView](indexedpageitemview.md)、 [FractionalPageItemView](fractionalpageitemview.md)、 [CalendarView](calendarview.md)或[ContactsView](contactsview.md)元素中的一个。 只有一个[GroupBy](groupby.md)或[DistinguishedGroupBy](distinguishedgroupby.md)元素可以包含在**FindItem**请求中。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [FindItem 操作](finditem-operation.md)
- [查找项目](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

