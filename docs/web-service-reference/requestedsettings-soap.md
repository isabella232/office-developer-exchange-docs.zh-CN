---
title: RequestedSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: RequestedSettings 元素包含请求的配置设置的名称。
ms.openlocfilehash: b8f3beabdd231d964cb5661a7cdd06f3860f0e06
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542825"
---
# <a name="requestedsettings-soap"></a>RequestedSettings (SOAP)

**RequestedSettings** 元素包含请求的配置设置的名称。 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 **RequestedSettings**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Setting (SOAP)](setting-soap.md) <br/> |表示要返回的配置设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |表示检索一个或多个用户的指定设置的请求。  <br/> |
|[请求 (SOAP)](request-soap.md) <br/> |包含请求的配置设置和目标用户。  <br/> |
|[GetDomainSettingsRequest (SOAP)](getdomainsettingsrequest-soap.md) <br/> |表示 [SOAP 请求 (GetDomainSettings) ](getdomainsettings-operation-soap.md) 操作。  <br/> |
   
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
  
[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

