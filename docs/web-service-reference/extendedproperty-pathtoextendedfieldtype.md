---
title: ExtendedProperty （PathToExtendedFieldType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: ExtendedProperty 元素指定统一联系人存储区的扩展属性。
ms.openlocfilehash: f6c283d5cce3bc927662ad0d9c796c0589e7054c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460139"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty （PathToExtendedFieldType）

**ExtendedProperty**元素指定统一联系人存储区的扩展属性。 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |指示可分辨属性集标识符。 此特性是可选的。  <br/> |
|PropertySetId  <br/> |指示 GUID 属性集标识符。 此特性是可选的。  <br/> |
|PropertyTag  <br/> | 表示属性标记减去类型部分。<br/><br/>有两种方法可供选择：  <br/><br/>-十六进制：0x3fa4  <br/>-十进制：0-65535<br/><br/>  此特性是可选的。  <br/> |
|PropertyName  <br/> |指示属性名称的字符串。 此特性是可选的。  <br/> |
|PropertyId  <br/> |指示属性标识符的整数。 此特性是可选的。  <br/> |
|Recordtype  <br/> |指示属性类型。 此特性是必需的。  <br/> |
|FieldURI  <br/> |指示字段统一资源标识符（URI）。 此特性是必需的。 有关可能的值，请参阅[FieldURI](fielduri.md)元素。  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**值**|**说明**|
|:-----|:-----|
|要求  <br/> |表示会议。  <br/> |
|Appointment  <br/> |指示约会。  <br/> |
|常见  <br/> |指示通用属性集。  <br/> |
|PublicStrings  <br/> |指示公共字符串。  <br/> |
|地址  <br/> |指示地址。  <br/> |
|InternetHeaders  <br/> |指示 Internet 标头。  <br/> |
|CalendarAssistant  <br/> |指示日历助理。  <br/> |
|UnifiedMessaging  <br/> |指示统一消息。  <br/> |
|任务  <br/> |指示任务。  <br/> |
   
#### <a name="propertytype"></a>Recordtype

|**值**|**说明**|
|:-----|:-----|
|ApplicationTime  <br/> |指示应用程序的时间。  <br/> |
|ApplicationTimeArray  <br/> |指示应用程序的时间数组。  <br/> |
|Binary  <br/> |指示二进制值。  <br/> |
|BinaryArray  <br/> |指示二进制值数组。  <br/> |
|Boolean  <br/> |指示布尔值。  <br/> |
|CLSID  <br/> |指示 CLSID。  <br/> |
|CLSIDArray  <br/> |指示一个 Clsid 数组。  <br/> |
|货币  <br/> |指示货币值。  <br/> |
|CurrencyArray  <br/> |指示货币值的数组。  <br/> |
|双精度  <br/> |指示**双精度型**。  <br/> |
|DoubleArray  <br/> |指示**双精度**值的数组。  <br/> |
|错误  <br/> |指示错误。 这是出于错误报告目的。 它不能在限制中使用，也不能用于获取或设置值。  <br/> |
|浮点  <br/> |指示**float**。  <br/> |
|FloatArray  <br/> |指示**float**值数组。  <br/> |
|Integer  <br/> |指示一个整数。  <br/> |
|IntegerArray  <br/> |指示一个整数数组。  <br/> |
|长型  <br/> |指示**长**。  <br/> |
|LongArray  <br/> |指示**long**值的数组。  <br/> |
|NULL  <br/> |指示 null 值。 这是出于错误报告目的。 它不能在限制中使用，也不能用于获取或设置值。  <br/> |
|对象  <br/> |指示对象。 这是出于错误报告目的。 它不能在限制中使用，也不能用于获取或设置值。  <br/> |
|ObjectArray  <br/> |指示对象的数组。 这是出于错误报告目的。 它不能在限制中使用，也不能用于获取或设置值。  <br/> |
|短  <br/> |指示**短整型**。  <br/> |
|ShortArray  <br/> |指示一个**短**值数组。  <br/> |
|SystemTime  <br/> |指示系统时间值。  <br/> |
|SystemTimeArray  <br/> |指示系统时间值的数组。  <br/> |
|String  <br/> |指示字符串。  <br/> |
|StringArray  <br/> |指示一个字符串数组。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |标识扩展 MAPI 属性。  <br/> |
   
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |类型 .xsd  <br/> |
|可以为空  <br/> ||
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

