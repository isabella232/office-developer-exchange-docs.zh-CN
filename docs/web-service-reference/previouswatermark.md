---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: PreviousWatermark 元素均表示水印成功传到用于订阅的客户端的最新事件。
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826886"
---
# <a name="previouswatermark"></a>PreviousWatermark

**PreviousWatermark**元素均表示水印成功传到用于订阅的客户端的最新事件。 
  
```xml
<PreviousWatermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来发生的事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示最新的水印。 文本值不能为空字符串。
  
## <a name="remarks"></a>备注

**PreviousWatermark**属性可确定上次成功通知客户端。 例如，如果订阅具有三个事件水印 1、 2 和 3，并将下一个通知发送**PreviousWatermark**值为 3，客户端可以进行比较此值为水印值接收的最后一个通知。 这样，客户端以确保事件的连续性。 
  
对于推送客户端， **PreviousWatermark**将与本地、 客户端的最后一个已知水印进行比较。 如果值不同，客户端错过了事件通知，以及如何应使用最新的本地水印重建订阅。 例如，如果推送客户端接收水印 1、 2 和 3，与订阅的三个事件和下一个通知附带**PreviousWatermark**值 5，则客户端将错过了至少一个通知，应创建新的订阅，将作为水印传递 3。 
  
对于提取客户端的**PreviousWatermark**值将由客户端 GetEvents 呼叫中包含[水印](watermark.md)相同。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消操作](unsubscribe-operation.md)

