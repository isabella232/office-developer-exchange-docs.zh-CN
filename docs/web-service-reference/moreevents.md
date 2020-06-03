---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: MoreEvents 元素指示队列中是否存在要传递到客户端的更多事件。
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462729"
---
# <a name="moreevents"></a>MoreEvents

**MoreEvents**元素指示队列中是否存在要传递到客户端的更多事件。 
  
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
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅以及上次通知之后发生的事件的信息。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示一个布尔值。 **如果值为 true，则**表示队列中有更多事件。 **如果值为 false** ，则表示队列中没有其他事件。 此属性是只读的。 
  
## <a name="remarks"></a>备注

在请求通知的情况下，此元素中的**true**值指示客户端应发出另一个 GetEvents 请求，以获取剩余事件。 假定客户端规范要求的事件通知的最低延迟，则 GetEvents 请求应持续持续连续，直到返回**false** **MoreEvents**值。 
  
在推送通知的情况下， **MoreEvents**的**true**值向客户端指明将向客户端发送另一个通知请求，以传递其余事件。 与 Pull 通知类似，这些后续请求将继续连续持续连续，直到客户端访问服务器上的事件队列为空。 
  
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
  
[取消订阅操作](unsubscribe-operation.md)

