---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: FindPeople 元素指定 FindPeople 请求中使用的一组数据。 数据包括零个或多个以下元素：人员形状 (可选) 、索引页项视图、限制 (可选) 、聚合限制 (可选) 、排序顺序 (可选) 、父文件夹 ID 和查询字符串 (可选) 。
ms.openlocfilehash: 44070c79ad5d1615929a6169d1808cf365b7cab4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535161"
---
# <a name="findpeople"></a>FindPeople

**FindPeople** 元素指定 FindPeople 请求中使用的一组数据。 数据包括零个或多个以下元素：人员形状 (可选) 、索引页项视图、限制 (可选) 、聚合限制 (可选) 、排序顺序 (可选) 、父文件夹 ID 和查询字符串 (可选) 。 
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[PersonaShape](personashape.md)  | [IndexedPageItemView](indexedpageitemview.md)  | [限制](restriction.md)  | [AggregationRestriction](aggregationrestriction.md)  | [SortOrder](sortorder.md)  | [ParentFolderId (TargetFolderIdType) ](parentfolderid-targetfolderidtype.md)  | [QueryString (QueryStringType) ](querystring-querystringtype.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

