---
title: CallState（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: CallState 元素包含一个值，该值指示呼叫的状态。
ms.openlocfilehash: 9435124e98cfb75beab5917c1e832096ca193e0c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519966"
---
# <a name="callstate-um-web-service"></a>CallState（UM Web 服务）

**CallState** 元素包含一个值，该值指示呼叫的状态。 
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)
  
[CallState（UM Web 服务）](callstate-um-web-service.md)
  
```xml
<CallState/>
```

 **UMCallState**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md) <br/> |定义对 UM Web 服务 ([GetCallInfo 操作) 。 ](getcallinfo-operation-um-web-service.md)  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 空闲
    
- 正在连接
    
- 警报
    
- 已连接
    
- 已断开连接
    
- 传入
    
- 正在转移
    
- 转发
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM Web 服务）](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)

