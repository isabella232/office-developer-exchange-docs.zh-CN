---
title: Excludes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: Excludes 元素执行指定属性和提供的值的按位掩码。
ms.openlocfilehash: 7923c31a4a1fea0270c9a4372072d7b0a3b79c76
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510139"
---
# <a name="excludes"></a>Excludes

**Excludes** 元素执行指定属性和提供的值的按位掩码。 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <ExtendedFieldURI/> 
   <Bitmask/>
</Excludes>
```

```xml
<Excludes>
   <IndexedFieldURI/> 
   <Bitmask/>
</Excludes>
```

**ExcludesType**

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
|[Bitmask](bitmask.md) <br/> |表示在排除限制操作期间使用的十六进制或 [十进制掩码](excludes.md) 。 如果位掩码代表十六进制数，则必须以 0x 或 0X 作为前缀。 否则，它将被视为十进制数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |表示允许您在两个或多个搜索表达式之间执行布尔 And 操作搜索表达式。 如果 And 中包含的所有搜索表达式都 **为 true，** 则 And 操作的结果 **为 true。**  <br/> |
|[或](or.md) <br/> |表示对包含的搜索表达式执行逻辑 OR 的搜索表达式。 如果 [Or](or.md)元素的任何子元素返回 **true，** 则其返回 **true。**  <br/> |
   
## <a name="remarks"></a>注解

**如果对** 以下内容执行的 AND **操作解析** 为 0，则排除将解析为 true： 
  
1. 属性的位值
    
2. 属性的位掩码值
    
**排除** 只能应用于具有整数值的属性。 如果属性类型不是整数，响应中将返回 **ErrorUnsupportedPathForQuery** 的错误代码。 
  
可以通过调用 Not (排除) 。
  
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

