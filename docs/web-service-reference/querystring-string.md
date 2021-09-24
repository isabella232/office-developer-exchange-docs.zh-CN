---
title: QueryString (String)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f81b1b3d-9fe4-4ab3-b517-42e4207fa596
description: QueryString 元素指定一组要返回的值，这些值与 FindPeople 操作请求中的查询字符串匹配。 未指定 QueryString 的搜索返回指定文件夹中的所有项目。
ms.openlocfilehash: 6dfd4b5552511e2551baf5ce645f82d4f74e5499
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523732"
---
# <a name="querystring-string"></a>QueryString (String)

**QueryString** 元素指定一组要返回的值，这些值与 [FindPeople](findpeople-operation.md)操作请求中的查询字符串匹配。 未指定 **QueryString** 的搜索返回指定文件夹中的所有项目。 
  
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
|[FindPeople](findpeople.md) <br/> |包含 [FindPeople 操作搜索的参数](findpeople-operation.md) 。  <br/> |
   
## <a name="text-value"></a>文本值

**QueryString** 文本值表示通过使用高级查询语法或 [AQS](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx) (的一) 。 有关此元素的语法的信息，请参阅 [QueryString (QueryStringType) ](querystring-querystringtype.md)。
  
## <a name="remarks"></a>注解

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

