---
title: QueryString （String）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: QueryString 元素指定要返回的一组要返回的值，这些值与 FindPeople 操作请求中的查询字符串相匹配。 未指定 QueryString 的搜索将返回指定文件夹中的所有项目。
ms.openlocfilehash: ec025f86d3e6fb74810e9c539eba102d05adbb93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465322"
---
# <a name="querystring-string"></a>QueryString （String）

**QueryString**元素指定要返回的一组要返回的值，这些值与[FindPeople 操作](findpeople-operation.md)请求中的查询字符串相匹配。 未指定**QueryString**的搜索将返回指定文件夹中的所有项目。 
  
```XML
<QueryString/> 
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |包含[FindPeople 操作](findpeople-operation.md)搜索的参数。  <br/> |
   
## <a name="text-value"></a>文本值

**QueryString** text 值代表使用[高级查询语法（AQS）](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)的子集进行的邮箱查询。 有关此元素的语法的信息，请参阅[QueryString （QueryStringType）](querystring-querystringtype.md)。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindPeople 操作](findpeople-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

