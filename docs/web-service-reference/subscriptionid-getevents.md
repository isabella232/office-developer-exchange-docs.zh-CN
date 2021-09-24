---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: SubscriptionId 元素表示订阅的标识符。
ms.openlocfilehash: c24ae8dc61fa98716efc38d7a2500cab503760b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522584"
---
# <a name="subscriptionid-getevents"></a>SubscriptionId (GetEvents)

**SubscriptionId** 元素表示订阅的标识符。 
  
```xml
<SubscriptionId/>
```

 **SubscriptionIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetEvents](getevents.md) <br/> |表示拉取客户端用于从服务器请求通知的操作。  <br/> |
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含 Subscribe 请求的状态和结果。  <br/> |
|[取消订阅](unsubscribe.md) <br/> |包含用于取消订阅的属性。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值为 GUID。
  
## <a name="remarks"></a>注解

表示订阅标识符的 GUID 由客户端访问服务器创建订阅时生成。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)

