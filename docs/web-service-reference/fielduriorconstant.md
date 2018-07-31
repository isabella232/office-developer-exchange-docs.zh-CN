---
title: FieldURIOrConstant
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldURIOrConstant
api_type:
- schema
ms.assetid: 89d7a87e-7c93-49b8-83ec-8798e08c1052
description: FieldURIOrConstant 元素表示的属性或常量值用于比较与另一个属性。
ms.openlocfilehash: a24c2fa044e03d0ac6f900625e325600903df8d0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354223"
---
# <a name="fielduriorconstant"></a>FieldURIOrConstant

**FieldURIOrConstant**元素表示的属性或常量值用于比较与另一个属性。 
  
```xml
<FieldURIOrConstant>
   <Constant/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
    <IndexedFieldURI/> 
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <FieldURI/>
</FieldURIOrConstant>
```

```xml
<FieldURIOrConstant>
   <ExtendedFieldURI/> 
</FieldURIOrConstant>
```

**FieldURIOrConstantType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[常量](constant.md) <br/> |标识限制中的以常量值。  <br/> |
|[FieldURI](fielduri.md) <br/> |标识由 URI 频繁引用的属性。  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |标识词典中的各个成员。  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识 MAPI 属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[IsEqualTo](isequalto.md) <br/> |代表一个搜索表达式的比较一个常数值的属性或另一个属性，并计算结果为 true，如果二者相等。  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为更高版本时为 true。  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为大于或等于第二个值或属性时为 true。  <br/> |
|[IsLessThan](islessthan.md) <br/> |代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为小于第二个值或属性时为 true。  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |代表一个搜索表达式，将一个常数值的属性或其他属性进行比较，并返回的第一个属性为小于或等于第二个值或属性时为 true。  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |代表一个搜索表达式的比较一个常数值的属性或另一个属性，并返回 true 如果值不相同。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

下面的 XML 示例演示用于常量和字段 URI FieldURIOrConstant 元素。
  
```xml
<Restriction>
  <Or xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <IsEqualTo>
      <FieldURI FieldURI="item:DateTimeCreated"/>
      <FieldURIOrConstant>
        <FieldURI FieldURI="item:DateTimeReceived"/>
      </FieldURIOrConstant>
    </IsEqualTo>
    <IsEqualTo>
      <FieldURI FieldURI="item:Subject"/>
      <FieldURIOrConstant>
        <Constant Value="Here is a test message"/>
      </FieldURIOrConstant>
    </IsEqualTo>
  </Or>
</Restriction>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

