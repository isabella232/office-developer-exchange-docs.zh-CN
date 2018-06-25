---
title: 查询字符串 （字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: QueryString 元素指定一组值的匹配 FindPeople 操作请求中的查询字符串返回。 使用没有指定的查询字符串搜索返回从指定的文件夹的所有项。
ms.openlocfilehash: 9c5c733adcec1496e36986fd720b56b0a0274593
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826935"
---
# <a name="querystring-string"></a>查询字符串 （字符串）

**QueryString**元素指定一组值的匹配[FindPeople 操作](findpeople-operation.md)请求中的查询字符串返回。 使用没有指定的**查询字符串**搜索返回从指定的文件夹的所有项。 
  
```XML
<QueryString/> 
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindPeople](findpeople.md) <br/> |包含[FindPeople 操作](findpeople-operation.md)搜索参数。  <br/> |
   
## <a name="text-value"></a>文本值

**QueryString**文本值表示邮箱查询使用[高级查询语法 (AQS)](http://msdn.microsoft.com/en-us/library/aa965711%28VS.85%29.aspx)的子集。 有关此元素的语法的信息，请参阅[QueryString (QueryStringType)](querystring-querystringtype.md)。
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindPeople 操作](findpeople-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

