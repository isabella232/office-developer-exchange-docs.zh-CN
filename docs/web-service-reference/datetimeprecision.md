---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: DateTimePrecision 元素指定返回的日期/时间值的精度。
ms.openlocfilehash: 075e37bfdd2c61f56352e000ef6cc5810dd81bbb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535708"
---
# <a name="datetimeprecision"></a>DateTimePrecision

**DateTimePrecision** 元素指定返回的日期/时间值的精度。 
  
```XML
<DateTimePrecision />
```

**DateTimePrecisionType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

**DateTimePrecision** 元素位于 SOAP 标头中。 
  
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 秒
    
- 毫秒
    
## <a name="remarks"></a>注解

当使用 **DateTimePrecision** 元素设置为"Seconds"的 SOAP 标头时，日期/时间值将返回到最接近的秒数 (00：00：00) 。 使用"毫秒"时，日期/时间值将返回到最接近的毫秒 (00：00：00.00000) 。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   

