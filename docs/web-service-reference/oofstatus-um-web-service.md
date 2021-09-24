---
title: OofStatus（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: OofStat Office us 元素包含一个值，该值指示在 UM Web 服务请求中执行 GetUMProperties (操作的用户的"统一消息外出) 状态。
ms.openlocfilehash: 4e899317defdb4ac4c27c3fdc17d7b7222dff6a7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539267"
---
# <a name="oofstatus-um-web-service"></a>OofStatus（UM Web 服务）

**OofStatus** 元素包含一个值，该值指示在 UM Web 服务 Office请求中执行 [GetUMProperties](getumproperties-operation-um-web-service.md) (操作的用户的"统一消息外出) 状态。 
  
[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md)
  
[OofStatus（UM Web 服务）](oofstatus-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
    <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
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
  
[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md)

