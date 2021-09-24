---
title: IsGreaterThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsGreaterThan
api_type:
- schema
ms.assetid: a6e9d462-cfa7-40ec-903e-128c95050352
description: IsGreaterThan 元素表示搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果第一个属性更大，则返回 true。
ms.openlocfilehash: 975b63be8dce414131dfbfef9851f7540fbd1b89
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523025"
---
# <a name="isgreaterthan"></a>IsGreaterThan

**IsGreaterThan** 元素表示搜索表达式，该表达式将属性与常量值或其他属性进行比较，如果第一个属性更大，则返回 true。 
  
```xml
<IsGreaterThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

**IsGreaterThanType**

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
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |表示与另一个属性比较时所使用的属性或常量值。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[限制](restriction.md) <br/> |表示用于在 FindItem/FindFolder 中筛选项目或文件夹和搜索文件夹操作的限制或查询。  <br/> |
|[not](not.md) <br/> |表示对其包含的搜索表达式的布尔值求反的搜索表达式。  <br/> |
|[And](and.md) <br/> |表示能够使您在两个或多个搜索表达式之间执行布尔 And 操作的搜索表达式。如果 And 中包含的搜索表达式为 **true**，则 And 操作的结果为 **true**。  <br/> |
|[或](or.md) <br/> |表示对包含的搜索表达式执行逻辑 OR 的搜索表达式。 如果其任何子级返回 [true](or.md)，则 **或** 将返回 **true**。  <br/> |
   
## <a name="remarks"></a>说明

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

