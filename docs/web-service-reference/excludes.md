---
title: 不包括
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Excludes
api_type:
- schema
ms.assetid: bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1
description: 排除元素执行指定属性的按位掩码和提供的值。
ms.openlocfilehash: d5fcd8b86b454aa731bd43974b5b7d674fe76ed6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530612"
---
# <a name="excludes"></a>不包括

**排除**元素执行指定属性的按位掩码和提供的值。 
  
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
|[位掩码](bitmask.md) <br/> |表示在不[包括](excludes.md)的限制操作期间要使用的十六进制或小数掩码。 如果位掩码代表十六进制数，则它的前缀必须为0x 或0X。 否则，它将被视为十进制数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |表示允许您在两个或多个搜索表达式之间执行布尔 And 运算的搜索表达式。 如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。  <br/> |
|[或](or.md) <br/> |表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。 如果其任何子级返回**true**，则[或](or.md)元素将返回**true** 。  <br/> |
   
## <a name="remarks"></a>备注

如果对以下项执行的 AND 操作解析为0，则**排除**将解析为**true** ： 
  
1. 属性的按位值
    
2. 属性的位掩码值
    
"**排除**" 仅可应用于具有整数值的属性。 如果属性类型不是整数，则会在响应中返回**ErrorUnsupportedPathForQuery**的错误代码。 
  
您可以通过不调用（不包括）执行反向操作。
  
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

