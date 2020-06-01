---
title: MissedCallNotificationEnabled （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- MissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 8e6bf0b1-ff76-474c-ac0f-621b6ab89212
description: MissedCallNotificationEnabled 元素包含一个值，该值指示是否在对 GetUMProperties 操作（UM web 服务）请求的响应中启用未接来电通知。
ms.openlocfilehash: e2f18027c56be1408c27d5f687fe90f8ffd724db
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468654"
---
# <a name="missedcallnotificationenabled-um-web-service"></a>MissedCallNotificationEnabled （UM web 服务）

**MissedCallNotificationEnabled**元素包含一个值，该值指示是否在对[GETUMPROPERTIES 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应中启用未接来电通知。 
  
[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md)
  
[MissedCallNotificationEnabled （UM web 服务）](missedcallnotificationenabled-um-web-service.md)
  
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
|[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md) <br/> |定义对[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

布尔文本值是必需的。 以下是可能的值：
  
- True
    
- False
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)
  
[SetMissedCallNotificationEnabled 操作（UM web 服务）](setmissedcallnotificationenabled-operation-um-web-service.md)

