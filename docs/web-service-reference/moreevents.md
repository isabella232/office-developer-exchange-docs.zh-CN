---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: MoreEvents 元素指示队列中是否有更多事件要传递到客户端。
ms.openlocfilehash: 7a19349e406a7e55e52c8a8cf0c3febba0a7301b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521807"
---
# <a name="moreevents"></a>MoreEvents

**MoreEvents** 元素指示队列中是否有更多事件要传递到客户端。 
  
```xml
<MoreEvents/>
```

 **Boolean**
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

文本值表示一个布尔值。 true **值表示** 队列中有更多事件。 false **值表示** 队列中不再有事件。 此属性是只读的。 
  
## <a name="remarks"></a>注解

对于 Pull 通知，此元素中的 **true** 值向客户端指示应发出另一个 GetEvents 请求以获取其余事件。 假定客户端规范需要事件通知的最小延迟，GetEvents 请求应继续连续，直到返回 **false** **MoreEvents** 值。 
  
对于推送通知 **，MoreEvents** 的 **true** 值指示向客户端发送另一个通知请求以传递剩余事件。 与"拉取通知"类似，这些后续请求将继续连续进行，直到客户端访问服务器上的事件队列为空。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

