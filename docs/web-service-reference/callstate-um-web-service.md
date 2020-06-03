---
title: CallState （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallState
api_type:
- schema
ms.assetid: 88670707-12f7-41c5-ac81-dda0c354a2cb
description: CallState 元素包含一个值，该值指示呼叫的状态。
ms.openlocfilehash: 44614c460286ff49ebc2373263c1827c6be5cc08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454608"
---
# <a name="callstate-um-web-service"></a>CallState （UM web 服务）

**CallState**元素包含一个值，该值指示呼叫的状态。 
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)
  
[CallState （UM web 服务）](callstate-um-web-service.md)
  
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
|[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md) <br/> |定义对[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 待机
    
- 正在连接
    
- 收到
    
- 已连接
    
- 已断开连接
    
- 即将
    
- 传输
    
- 发送
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)

