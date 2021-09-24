---
title: Timeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Timeout
api_type:
- schema
ms.assetid: c2e1ca5a-6667-4f6f-aac4-89de33bddc54
description: Timeout 元素表示订阅在没有来自客户端的 GetEvents 请求的情况下可以保持空闲的持续时间（分钟）。
ms.openlocfilehash: d0b5945f5d116e0ebb7a24a23970e785761fb0c9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534165"
---
# <a name="timeout"></a>Timeout

**Timeout** 元素表示订阅在没有来自客户端的 GetEvents 请求的情况下可以保持空闲的持续时间（分钟）。 
  
```xml
<Timeout/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于拉取的事件通知订阅的订阅。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则代表整数的文本值是必需的。 此元素的可能值为 1 到 1440（包括 1 和 1440）。 此元素是必需的。
  
## <a name="remarks"></a>注解

订阅的超时计时器由成功的 GetEvents 请求重置。
  
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

