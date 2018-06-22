---
title: AbsoluteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDate
api_type:
- schema
ms.assetid: 8bc59a26-6fe1-42e9-968c-69a94a3fb0ae
description: AbsoluteDate 元素均表示从标准版或夏时制时间的更改时的日期。
ms.openlocfilehash: d14cafb08297e5be3c8620c441f8b84b46ffe53e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753186"
---
# <a name="absolutedate"></a>AbsoluteDate

**AbsoluteDate**元素均表示从标准版或夏时制时间的更改时的日期。 
  
```xml
<AbsoluteDate/>
```

**日期**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[标准](standard.md) <br/> |表示当时间从夏令时更改为标准时间时的日期和时间。  <br/> |
|[夏时制](daylight.md) <br/> |表示的日期和时间更改时从标准时间到夏时制的时间。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示当之间标准版或夏时制 shift 发生的日期。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)




