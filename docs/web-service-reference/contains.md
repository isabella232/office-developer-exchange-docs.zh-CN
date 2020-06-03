---
title: Contains
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: Contains 元素表示一个搜索表达式，用于确定给定属性是否包含提供的常量字符串值。
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527115"
---
# <a name="contains"></a>Contains

**Contains**元素表示一个搜索表达式，用于确定给定属性是否包含提供的常量字符串值。 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


**ContainsExpressionType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**ContainmentMode** <br/> |标识搜索的边界。  <br/> |
|**ContainmentComparison** <br/> |确定搜索是否忽略大小写和空格。  <br/> |
   
#### <a name="containmentmode-attribute-values"></a>ContainmentMode 属性值

|**值**|**说明**|
|:-----|:-----|
|FullString  <br/> |在完整字符串和常量之间进行比较。 属性值和提供的常量完全相同。  <br/> |
|作  <br/> |在字符串前缀和常量之间进行比较。  <br/> |
|取  <br/> |在字符串的子字符串和常量之间进行比较。  <br/> |
|PrefixOnWords  <br/> |在字符串中单个词的前缀和常量之间进行比较。  <br/> |
|ExactPhrase  <br/> |在字符串中的精确短语和常量之间进行比较。  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a>ContainmentComparison 属性值

|**值**|**说明**|
|:-----|:-----|
|混杂  <br/> |比较必须准确。  <br/> |
|IgnoreCase  <br/> |比较将忽略大小写。  <br/> |
|IgnoreNonSpacingCharacters  <br/> |比较将忽略非空格字符。  <br/> |
|稀疏  <br/> |要删除的。  <br/> |
|IgnoreCaseAndNonSpacingCharacters  <br/> |比较将忽略大小写和非空格字符。  <br/> |
|LooseAndIgnoreCase  <br/> |要删除的。  <br/> |
|LooseAndIgnoreNonSpace  <br/> |要删除的。  <br/> |
|LooseAndIgnoreCaseAndIgnoreNonSpace  <br/> |要删除的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**描述**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识 MAPI 属性。  <br/> |
|[常量](constant.md) <br/> |标识限制中的常量值。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |表示允许您在两个或多个搜索表达式之间执行布尔 And 运算的搜索表达式。 如果和中包含的所有搜索表达式均**为 true**，则 and 操作的结果为**true** 。  <br/> |
|[或](or.md) <br/> |表示在其包含的搜索表达式上执行逻辑 OR 的搜索表达式。 如果其任何子级返回**true**，则[或](or.md)元素将返回**true** 。  <br/> |
   
## <a name="remarks"></a>备注

属性用于确定元素的匹配方式。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

