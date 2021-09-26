---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: Previous Watermarkmark 元素表示已成功与订阅的客户端通信的最新事件水印。
ms.openlocfilehash: c46e18c7a58405fe2149666531cb2af773110816
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543021"
---
# <a name="previouswatermark"></a>PreviousWatermark

**Previous Watermarkmark** 元素表示已成功与订阅的客户端通信的最新事件水印。 
  
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
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示最新的水印。 文本值不能为空字符串。
  
## <a name="remarks"></a>注解

**Previous一mark** 属性对客户端用于确定最后一个成功通知非常有用。 例如，如果订阅有三个带有水印 1、2 和 3 的事件，并且下一个通知的 **Previous Watermarkmark** 值为 3，则客户端可以将此值与上次收到通知的 Watermark 值进行比较。 这使客户端可以确保事件的连续性。 
  
对于推送客户端 **，Previous Watermarkmark** 与客户端上一个已知本地水印进行比较。 如果值不同，客户端会错过事件通知，应该使用最新的本地水印重新建立订阅。 例如，如果推送客户端收到具有水印 1、2 和 3 的订阅的三个事件，并且下一个通知附带 **Previous Watermarkmark** 值 5，则客户端已至少错过一个通知，应创建新订阅，将 3 作为水印传递。 
  
对于拉客户端 **，Previous Watermarkmark** 的值将和客户端在 GetEvents 调用中包括的 [Watermark](watermark.md) 相同。 
  
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
  
[Unsubscribe 操作](unsubscribe-operation.md)

