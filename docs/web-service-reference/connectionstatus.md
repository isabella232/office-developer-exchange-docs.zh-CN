---
title: ConnectionStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionStatus
api_type:
- schema
ms.assetid: 4300f9d6-8bf9-48c2-9f07-d80197864e17
description: ConnectionStatus 元素提供流式订阅状态的文本说明。
ms.openlocfilehash: 05ff80ac3e6c3c8bf1341a179a14c9d052c9947f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536849"
---
# <a name="connectionstatus"></a>ConnectionStatus

**ConnectionStatus** 元素提供流式订阅状态的文本说明。 
  
```xml
<ConnectionStatus>OK or Closed</ConnectionStatus>
```

 **ConnectionStatusType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |包含单个 [GetStreamingEvents](getstreamingevents-operation.md) 操作请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是此元素的可能文本值：
  
- 确定
    
- 已结束
    
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



[GetStreamingEvents 操作](getstreamingevents-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

