---
title: GetUMPropertiesResponse （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: GetUMPropertiesResponse 元素定义对 GetUMProperties 操作（UM web 服务）请求的响应。
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459123"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse （UM web 服务）

**GetUMPropertiesResponse**元素定义对[GETUMPROPERTIES 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。 
  
[GetUMPropertiesResponse （UM web 服务）](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **UMProperties**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[MissedCallNotificationEnabled （UM web 服务）](missedcallnotificationenabled-um-web-service.md) <br/> |指示是否启用未接来电通知。  <br/> |
|[PlayOnPhoneDialString （UM web 服务）](playonphonedialstring-um-web-service.md) <br/> |包含用于[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)的默认拨号字符串。  <br/> |
|[TelephoneAccessNumbers （UM web 服务）](telephoneaccessnumbers-um-web-service.md) <br/> |包含用户通过电话访问统一消息时可使用的电话号码列表。  <br/> |
|[TelephoneAccessFolderEmail （UM web 服务）](telephoneaccessfolderemail-um-web-service.md) <br/> |包含电子邮件文件夹的标识符，统一消息将通过电话读取邮件。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM web 服务）](getumproperties-operation-um-web-service.md)

