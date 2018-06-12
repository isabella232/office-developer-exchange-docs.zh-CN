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
description: MoreEvents 元素指示队列传送到客户端中是否有多个事件。
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826489"
---
# <a name="moreevents"></a>MoreEvents

**MoreEvents**元素指示队列传送到客户端中是否有多个事件。 
  
```xml
<MoreEvents/>
```

 **Boolean**
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

文本值表示的布尔值。 值为**true**指示多个事件队列中。 如果值为**false**指示的多个事件不会在队列中。 此属性是只读的。 
  
## <a name="remarks"></a>备注

对于出现通知，此元素中的一个**true**值指示客户端应发出另一个 GetEvents 请求以获取剩余的事件。 假定客户端规范需要事件通知的最小的延迟，GetEvents 请求应继续连续连续，直到**false** **MoreEvents**值返回。 
  
对于推送通知**MoreEvents** **true**值指示客户端，另一个通知请求将发送到客户端提供剩余的事件。 类似于出现通知，这些后续请求将继续连续连续直到客户端访问服务器上的事件队列为空。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

