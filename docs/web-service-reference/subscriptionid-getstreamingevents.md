---
title: SubscriptionId (GetStreamingEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f86c178-2311-4844-82db-c2a0e469d116
description: SubscriptionId 元素表示流式订阅的标识符。
ms.openlocfilehash: 8931fda5087fa985c646da328a0cb27fa2c2a708
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540375"
---
# <a name="subscriptionid-getstreamingevents"></a>SubscriptionId (GetStreamingEvents)

**SubscriptionId** 元素表示流式订阅的标识符。 
  
```XML
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
|[GetStreamingEvents](getstreamingevents.md) <br/> |表示客户端用于从服务器请求流式处理通知的操作。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值为 GUID。
  
## <a name="remarks"></a>注解

表示订阅标识符的 GUID 由客户端访问服务器创建订阅时生成。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetStreamingEvents 操作](getstreamingevents-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

