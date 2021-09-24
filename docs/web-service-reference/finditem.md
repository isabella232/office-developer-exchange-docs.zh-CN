---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: FindItem 元素定义查找邮箱中的项目的请求。
ms.openlocfilehash: 7005b4a837c61ffa00a49b687e729de7ed769bcf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541313"
---
# <a name="finditem"></a>FindItem

**FindItem** 元素定义查找邮箱中的项目的请求。 
  
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
|**遍历** <br/> |定义搜索是否在文件夹或文件夹的垃圾站中查找项目。 此特性是必需的。  <br/> |
   
#### <a name="traversal-attribute-values"></a>遍历属性值

|**值**|**说明**|
|:-----|:-----|
|浅  <br/> |仅返回文件夹中项目的标识。  <br/> |
|SoftDeleted  <br/> |仅返回文件夹垃圾站中项目的标识。 请注意，软删除遍历与搜索限制相结合将导致返回零项，即使存在符合搜索条件的项目。  <br/> |
|关联  <br/> |仅返回文件夹中关联项目的标识。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |标识要包括在 [FindItem](finditem-operation.md) 操作响应中的项目属性和内容。  <br/> |
|[IndexedPageItemView](indexedpageitemview.md) <br/> |介绍如何为 **FindItem** 请求返回分页项信息。 此元素为可选。  <br/> |
|[FractionalPageItemView](fractionalpageitemview.md) <br/> |描述分页视图的起始位置以及 **FindItem** 请求中返回的最大项目数。 从找到的项目集的开头分页的视图偏移量由分数描述。 此元素为可选。  <br/> |
|[CalendarView](calendarview.md) <br/> |提供用于定义日历项目搜索的时间限制。 此元素为可选。  <br/> |
|[ContactsView](contactsview.md) <br/> |根据显示名称的字母顺序定义联系人项目的搜索。 此元素为可选。  <br/> |
|[GroupBy](groupby.md) <br/> |指定 **FindItem** 查询的任意分组。 此元素为可选。  <br/> |
|[DistinguishedGroupBy](distinguishedgroupby.md) <br/> |为 **FindItem 查询提供标准** 分组。 此元素是可选的。  <br/> |
|[限制](restriction.md) <br/> |定义用于筛选 **FindItem** FindFolder 和搜索文件夹操作中的项目或文件夹 /  的限制或查询。 此元素为可选。  <br/> |
|[SortOrder](sortorder.md) <br/> |定义如何在 FindItem 请求中对项目进行排序。 此元素是可选的。  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |标识要搜索 FindItem 和 FindFolder 操作的文件夹。  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |包含基于高级查询语法的邮箱查询字符串 (AQS) 。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

**FindItem** 请求中只能包含 [IndexedPageItemView、FractionalPageItemView、CalendarView](fractionalpageitemview.md)或 [ContactsView](contactsview.md)元素之一。 [](indexedpageitemview.md) [](calendarview.md) **FindItem** 请求中只能包含一个 [GroupBy](groupby.md)或 [DistinguishedGroupBy](distinguishedgroupby.md)元素。 
  
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

