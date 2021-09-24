---
title: GetUMPropertiesResponse（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: GetUMPropertiesResponse 元素定义对 UM Web 服务请求 (GetUMProperties) 的响应。
ms.openlocfilehash: 97c3850d46369d4ab533629a8b24e199db3dd44a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522962"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse（UM Web 服务）

**GetUMPropertiesResponse** 元素定义对 UM Web 服务请求 ([GetUMProperties](getumproperties-operation-um-web-service.md)) 的响应。 
  
[GetUMPropertiesResponse（UM Web 服务）](getumpropertiesresponse-um-web-service.md)
  
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
|[MissedCallNotificationEnabled（UM Web 服务）](missedcallnotificationenabled-um-web-service.md) <br/> |指示是否启用未接来电通知。  <br/> |
|[PlayOnPhoneDialString（UM Web 服务）](playonphonedialstring-um-web-service.md) <br/> |包含用于 UM Web 服务 ([PlayOnPhone](playonphone-operation-um-web-service.md)操作的默认拨号字符串) Um Web 服务 ([PlayOnPhoneGreeting) 。 ](playonphonegreeting-operation-um-web-service.md)  <br/> |
|[TelephoneAccessNumbers（UM Web 服务）](telephoneaccessnumbers-um-web-service.md) <br/> |包含用户可用于通过电话访问统一消息的电话号码列表。  <br/> |
|[TelephoneAccessFolderEmail（UM Web 服务）](telephoneaccessfolderemail-um-web-service.md) <br/> |包含统一消息将通过电话读取邮件的电子邮件文件夹的标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUMProperties 操作（UM Web 服务）](getumproperties-operation-um-web-service.md)

