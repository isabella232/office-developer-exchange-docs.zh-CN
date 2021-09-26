---
title: DictionaryEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DictionaryEntry
api_type:
- schema
ms.assetid: 531ea96a-d411-43e6-9fec-11fa2c959a30
description: DictionaryEntry 元素指定单个词典条目属性的内容。
ms.openlocfilehash: 4a9e481f3b9d6fc2d0ef739031042354ed717bee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545319"
---
# <a name="dictionaryentry"></a>DictionaryEntry

**DictionaryEntry** 元素指定单个词典条目属性的内容。 
  
```xml
<DictionaryEntry>
   <DictionaryKey/>
   <DictionaryValue/>
</DictionaryEntry>
```

 **UserConfigurationDictionaryEntryType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DictionaryKey](dictionarykey.md) <br/> |指定字典属性的字典键。  <br/> |
|[DictionaryValue](dictionaryvalue.md) <br/> |指定字典属性的字典值。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|"词典" <br/> |定义用户配置对象的一组字典属性条目。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

