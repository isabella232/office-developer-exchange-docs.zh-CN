---
title: Exists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exists
api_type:
- schema
ms.assetid: 55d568bd-8dbc-4d50-b9d7-54b74a54d4b5
description: Exists 元素表示搜索表达式，如果某个项目上存在，则该表达式会返回 true。
ms.openlocfilehash: b5e7a24c5214574ef385cd6ffca87ed5f861c188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456946"
---
# <a name="exists"></a>Exists

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Exists** 元素表示搜索表达式，如果某个项目上存在，则该表达式会返回 **true**。 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 **ExistsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识 MAPI 属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。如果 And 中包含的搜索表达式为 **true**，则 And 操作的结果为 **true**。  <br/> |
|[或](or.md) <br/> |表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。如果其任何子级返回 [true](or.md)，则 **或** 将返回 **true**。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

