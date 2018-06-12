---
title: OofStatus （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- OofStatus
api_type:
- schema
ms.assetid: 0ba4225a-784e-4e6e-bd20-be45f0f7597c
description: OofStatus 元素包含一个值，该 indicaties 发出 GetUMProperties 操作 （UM web 服务） 请求的用户的统一消息外出状态。
ms.openlocfilehash: 1fe358a8bfea3c509220d6705a238ae832de37e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826650"
---
# <a name="oofstatus-um-web-service"></a>OofStatus （UM web 服务）

**OofStatus**元素包含一个值，该 indicaties 发出[GetUMProperties 操作 （UM web 服务）](getumproperties-operation-um-web-service.md)请求的用户的统一消息外出状态。 
  
[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md)
  
[OofStatus （UM web 服务）](oofstatus-um-web-service.md)
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md) <br/> |定义[GetUMProperties 操作 （UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

Boolean 的文本值为 required。 以下是可能的值：
  
- True
    
- False
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作 （UM web 服务）](getumproperties-operation-um-web-service.md)
  
[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md)

