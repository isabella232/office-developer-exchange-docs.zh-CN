---
title: Value (Message Tracking)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: Value 元素表示邮件跟踪报告的属性值。
ms.openlocfilehash: c8aa4f3cc41e76b633ee1b244371de2f5410c944
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513960"
---
# <a name="value-message-tracking"></a>Value (Message Tracking)

**Value** 元素表示邮件跟踪报告的属性值。 
  
```xml
<Value/>
```

**String**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |表示用于创建邮件跟踪报告的属性的字符串的名称和值对。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是可选的。
  
## <a name="remarks"></a>注解

此元素可在 [TrackingPropertyType](trackingpropertytype.md) 元素中最多出现一次。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

