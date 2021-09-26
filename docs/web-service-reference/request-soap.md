---
title: Request (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: Request 元素包含请求的配置设置和目标用户。
ms.openlocfilehash: 533419d6e622bb1d415f739868aaf30c79c41635
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542803"
---
# <a name="request-soap"></a>Request (SOAP)

**Request** 元素包含请求的配置设置和目标用户。 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 **GetUserSettingsRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Users (SOAP)](users-soap.md) <br/> |表示应检索其设置的用户的电子邮件地址的集合。  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |包含请求的配置设置的名称。  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |指定提供程序希望使用的特定服务器版本。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsRequestMessage (SOAP)](getusersettingsrequestmessage-soap.md) <br/> |表示 [SOAP 请求 (GetUserSettings) ](getusersettings-operation-soap.md) 操作。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)

