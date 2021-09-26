---
title: GetDomainSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: GetDomainSettingsRequest 元素表示 SOAP (请求) GetDomainSettings 操作。
ms.openlocfilehash: 4c222c6832b5be7da598de3390d13123749f8b0f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544990"
---
# <a name="getdomainsettingsrequest-soap"></a>GetDomainSettingsRequest (SOAP)

**GetDomainSettingsRequest** 元素表示 SOAP (请求) [GetDomainSettings](getdomainsettings-operation-soap.md)操作。 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 **GetDomainSettingsRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |表示域标识符的集合。  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |包含请求的域配置设置的名称。  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |指定提供程序将使用的服务器版本。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
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



[GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

