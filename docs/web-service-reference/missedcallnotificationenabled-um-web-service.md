---
title: MissedCallNotificationEnabled（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- MissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 8e6bf0b1-ff76-474c-ac0f-621b6ab89212
description: MissedCallNotificationEnabled 元素包含一个值，该值指示在响应 UM Web 服务请求的 GetUMProperties 操作时是否 (未接) 通知。
ms.openlocfilehash: 0566312db672b3795e5f163a35e4c31ae6b26af4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542041"
---
# <a name="missedcallnotificationenabled-um-web-service"></a>MissedCallNotificationEnabled（UM Web 服务）

**MissedCallNotificationEnabled** 元素包含一个值，该值指示在响应 UM Web 服务请求的 [GetUMProperties](getumproperties-operation-um-web-service.md)操作时是否 (未接) 通知。 
  
[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md)
  
[MissedCallNotificationEnabled（UM Web 服务）](missedcallnotificationenabled-um-web-service.md)
  
```xml
<MissedCallNotificationEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md) <br/> |定义对 UM Web 服务请求 ([GetUMProperties) ](getumproperties-operation-um-web-service.md) 的响应。  <br/> |
   
## <a name="text-value"></a>文本值

Boolean 文本值是必需的。 以下是可能的值：
  
- True
    
- 错误
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM Web 服务）](getumproperties-operation-um-web-service.md)
  
[SetMissedCallNotificationEnabled 操作（UM Web 服务）](setmissedcallnotificationenabled-operation-um-web-service.md)

