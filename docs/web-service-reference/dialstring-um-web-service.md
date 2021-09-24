---
title: dialString（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- dialString
api_type:
- schema
ms.assetid: d1e3cd23-48fe-4ebc-a5c5-2226d223f800
description: dialString 元素包含要拨打的电话号码的值。
ms.openlocfilehash: dc5643f5aedfb128cf207b895fe96812e9a69496
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528868"
---
# <a name="dialstring-um-web-service"></a>dialString（UM Web 服务）

**dialString** 元素包含要拨打的电话号码的值。 
  
- [PlayOnPhone（UM Web 服务）](playonphone-um-web-service.md) 
- [dialString（UM Web 服务）](dialstring-um-web-service.md) 
- [PlayOnPhoneGreeting（UM Web 服务）](playonphonegreeting-um-web-service.md) 
- [dialString（UM Web 服务）](dialstring-um-web-service.md)
  
```xml
<dialString/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PlayOnPhone（UM Web 服务）](playonphone-um-web-service.md) <br/> |定义在电话上播放消息的请求。  <br/> |
|[PlayOnPhoneGreeting（UM Web 服务）](playonphonegreeting-um-web-service.md) <br/> |定义在电话上播放问候语的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值必须包含有效的拨号号码。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [PlayOnPhone（UM Web 服务）](playonphone-um-web-service.md)  
- [PlayOnPhone 操作（UM Web 服务）](playonphone-operation-um-web-service.md)  
- [PlayOnPhoneGreeting（UM Web 服务）](playonphonegreeting-um-web-service.md)  
- [PlayOnPhoneGreeting 操作（UM Web 服务）](playonphonegreeting-operation-um-web-service.md)

