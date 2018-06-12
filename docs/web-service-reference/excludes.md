---
title: 排除
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
description: 排除元素执行指定的属性和提供的值的按位掩码。
ms.openlocfilehash: 73e4eb782a4f54c113ea9a9b67fcf185a9028153
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754191"
---
# <a name="excludes"></a>排除

**排除**元素执行指定的属性和提供的值的按位掩码。 
  
```xml
<Excludes>
   <FieldURI/>
   <Bitmask/>
</Excludes>
```

 **ExcludesType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识 MAPI 属性。  <br/> |
|[位掩码](bitmask.md) <br/> |代表用于[排除](excludes.md)限制操作过程中使用十六进制或小数的掩码。 如果位掩码表示的十六进制数，它必须由 0 x 或 0x 作为前缀。 否则，它将被视为十进制数。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |代表一个搜索表达式，使您可以执行两个或多个搜索表达式之间 Boolean 和操作。 如果 And 中包含的搜索表达式都**为真**，和操作的结果为**true** 。  <br/> |
|[或](or.md) <br/> |表示对它所包含的搜索表达式执行逻辑或搜索表达式。 如果任何其子返回**true**，则将返回**true** [或](or.md)元素。  <br/> |
   
## <a name="remarks"></a>备注

 如果执行下面的 AND 操作将解析为 0，**排除**将解析为**true** : 
  
1. 属性的按位值
    
2. 属性的位掩码值
    
 **排除**可只能应用于该属性的整数值。 属性类型是一个整数之外的任何内容，如果是响应中返回的错误代码为**ErrorUnsupportedPathForQuery** 。 
  
您可以通过调用 Not(Excludes) 执行还原操作。
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

