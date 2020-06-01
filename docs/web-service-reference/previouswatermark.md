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
description: PreviousWatermark 元素表示成功传递给订阅客户端的最新事件的水印。
ms.openlocfilehash: 1b26a645a5ec6dbbd2874b118f968866aadc32af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461651"
---
# <a name="previouswatermark"></a>PreviousWatermark

**PreviousWatermark**元素表示成功传递给订阅客户端的最新事件的水印。 
  
```xml
<PreviousWatermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅以及上次通知之后发生的事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值表示最新的水印。 文本值不能为空字符串。
  
## <a name="remarks"></a>备注

**PreviousWatermark**属性对确定最后一个成功通知的客户端很有用。 例如，如果订阅包含具有水印1、2和3的三个事件，并且下一个通知发送的**PreviousWatermark**值为3，则客户端可以将此值与接收到的最后一条通知的水位线值进行比较。 这使客户端能够确保事件的连续性。 
  
对于推送客户端，将**PreviousWatermark**与本地的客户端最后一个已知的水印进行比较。 如果值不同，客户端将错过事件通知，应使用最新的本地水印重新建立订阅。 例如，如果推送客户端接收到具有水印1、2和3的订阅的三个事件，并且下一个通知的**PreviousWatermark**值为5，则客户端已错过至少一次通知，应创建一个新的订阅，并将3作为水印进行传递。 
  
对于 pull 客户端， **PreviousWatermark**的值将与 GetEvents 调用中的客户端所包含的[水印](watermark.md)相同。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)

