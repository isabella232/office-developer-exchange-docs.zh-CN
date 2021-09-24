---
title: PlayOnPhoneResponse（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 42b16880-1271-4690-abd0-0072d95b04b7
description: PlayOnPhoneResponse 元素定义对 UM Web 服务请求 (PlayOnPhone) 的响应。
ms.openlocfilehash: 9c2893837a1bc9c4836dc3cab6fb14e0d1fd611b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516522"
---
# <a name="playonphoneresponse-um-web-service"></a>PlayOnPhoneResponse（UM Web 服务）

**PlayOnPhoneResponse** 元素定义对 UM Web 服务请求 ([PlayOnPhone](playonphone-operation-um-web-service.md)) 的响应。 
  
[PlayOnPhoneResponse（UM Web 服务）](playonphoneresponse-um-web-service.md)
  
```xml
<PlayOnPhoneResponse />
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

文本值是必需的。 文本值是调用标识符，用于[GetCallInfo](getcallinfo-operation-um-web-service.md)操作 () UM Web 服务)  (请求或 Disconnect 操作 (UM Web 服务) 请求中的[CallId](callid-um-web-service.md) [ (UM Web 服务) ](disconnect-operation-um-web-service.md)的值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[PlayOnPhone 操作（UM Web 服务）](playonphone-operation-um-web-service.md)

