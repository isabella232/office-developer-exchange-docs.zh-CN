---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: FindPeople 元素指定一的组 FindPeople 请求中使用的数据。 将数据包含零个或多个以下元素： 个人形状 （可选）、 索引的页面项视图、 （可选） 限制、 聚合限制 （可选）、 排序顺序 （可选）、 父文件夹 Id 和 （可选） 查询字符串。
ms.openlocfilehash: 79c8a4324cd217232442b781c33223296d8015e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754357"
---
# <a name="findpeople"></a>FindPeople

**FindPeople**元素指定一的组 FindPeople 请求中使用的数据。 将数据包含零个或多个以下元素： 个人形状 （可选）、 索引的页面项视图、 （可选） 限制、 聚合限制 （可选）、 排序顺序 （可选）、 父文件夹 Id 和 （可选） 查询字符串。 
  
```XML
<FindPeople>
   <PersonaShape/>
   <IndexedPageItemView/>
   <Restriction/>
   <AggregationRestriction/>
   <SortOrder/>
   <ParentFolderId/>
   <QueryString/>
</FindPeople>
```

 **FindPeopleType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [限制](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [查询字符串 (QueryStringType)](querystring-querystringtype.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

