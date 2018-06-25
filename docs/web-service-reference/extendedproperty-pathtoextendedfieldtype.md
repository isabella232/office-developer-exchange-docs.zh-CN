---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: ExtendedProperty 元素指定的统一联系人存储库的扩展的属性。
ms.openlocfilehash: 7541fa6330ee96f7791febfabc672dbcf0e95b54
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754245"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty (PathToExtendedFieldType)

**ExtendedProperty**元素指定的统一联系人存储库的扩展的属性。 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |指示的可分辨的属性集标识符。 此属性是可选的。  <br/> |
|PropertySetId  <br/> |指示 GUID 属性集标识符。 此属性是可选的。  <br/> |
|PropertyTag  <br/> | 代表减去的类型部分的属性标记。<br/><br/>有两个选项的表示形式：  <br/><br/>-十六进制： 0x3fa4  <br/>-Decimal: 0-65535<br/><br/>  此属性是可选的。  <br/> |
|PropertyName  <br/> |指示在属性名称的字符串。 此属性是可选的。  <br/> |
|PropertyId  <br/> |指示属性标识符的整数。 此属性是可选的。  <br/> |
|PropertyType  <br/> |指示属性类型。 此属性是必需的。  <br/> |
|FieldURI  <br/> |指示字段统一资源标识符 (URI)。 此属性是必需的。 可能的值，请参阅[FieldURI](fielduri.md)元素。  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**值**|**说明**|
|:-----|:-----|
|会议  <br/> |指示会议。  <br/> |
|Appointment  <br/> |指示约会。  <br/> |
|Common  <br/> |指示常见属性集。  <br/> |
|PublicStrings  <br/> |指示公用的字符串。  <br/> |
|Address  <br/> |指示一个地址。  <br/> |
|InternetHeaders  <br/> |指示 Internet 邮件头。  <br/> |
|CalendarAssistant  <br/> |指示日历助理。  <br/> |
|UnifiedMessaging  <br/> |指示统一消息。  <br/> |
|任务  <br/> |表示的任务。  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**值**|**说明**|
|:-----|:-----|
|ApplicationTime  <br/> |指示应用程序的时间。  <br/> |
|ApplicationTimeArray  <br/> |指示应用程序的时间的数组。  <br/> |
|二进制  <br/> |指示二进制值。  <br/> |
|BinaryArray  <br/> |指示二进制值的数组。  <br/> |
|Boolean  <br/> |指示布尔值。  <br/> |
|CLSID  <br/> |指示 CLSID。  <br/> |
|CLSIDArray  <br/> |指示 Clsid 的数组。  <br/> |
|货币  <br/> |表示货币值。  <br/> |
|CurrencyArray  <br/> |指示的货币值的数组。  <br/> |
|双精度数  <br/> |指示**双**。  <br/> |
|DoubleArray  <br/> |指示**双精度**值的数组。  <br/> |
|错误  <br/> |指示错误。 这是错误报告的目的。 限制或获取或设置值不能使用它。  <br/> |
|Float  <br/> |指示**float**。  <br/> |
|FloatArray  <br/> |指示的**浮点**值的数组。  <br/> |
|整数  <br/> |指示整数。  <br/> |
|IntegerArray  <br/> |指示包含整数的数组。  <br/> |
|Long  <br/> |指示**长**。  <br/> |
|LongArray  <br/> |指示**长整型**值的数组。  <br/> |
|Null  <br/> |指示空值。 这是错误报告的目的。 限制或获取或设置值不能使用它。  <br/> |
|对象  <br/> |指示一个对象。 这是错误报告的目的。 限制或获取或设置值不能使用它。  <br/> |
|ObjectArray  <br/> |指示对象的数组。 这是错误报告的目的。 限制或获取或设置值不能使用它。  <br/> |
|短  <br/> |指示**短**。  <br/> |
|ShortArray  <br/> |指示的**简短**的值的数组。  <br/> |
|SystemTime  <br/> |指示系统时间值。  <br/> |
|SystemTimeArray  <br/> |指示系统时间值的数组。  <br/> |
|String  <br/> |指示字符串。  <br/> |
|StringArray  <br/> |指示一个字符串数组。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识扩展的 MAPI 属性。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |types.xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

