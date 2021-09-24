---
title: GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: GetStreamingEvents 元素表示客户端用于从服务器请求流通知的操作。
ms.openlocfilehash: 8a68b3edbb53b623e4dc709e0128c5b3ebc94f91
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523048"
---
# <a name="getstreamingevents"></a>GetStreamingEvents

**GetStreamingEvents** 元素表示客户端用于从服务器请求流通知的操作。 
  
[GetStreamingEvents](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 **GetStreamingEventsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) <br/> |表示查询事件的订阅的标识符。  <br/> |
|[ConnectionTimeout](connectiontimeout.md) <br/> |表示保持连接打开的分钟数。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

