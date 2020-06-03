---
title: 请求 (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: Request 元素包含一个返回域设置的请求。
ms.openlocfilehash: c5f666102be8aaeee001a23706732e9e6c44b560
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459586"
---
# <a name="request-getdomainsettings-soap"></a>请求 (GetDomainSettings) (SOAP)

**Request**元素包含一个返回域设置的请求。 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 **GetDomainSettingsRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[域（SOAP）](domains-soap.md) <br/> |表示在[GetDomainSettings 操作（soap）](getdomainsettings-operation-soap.md)或组织在[GETFEDERATIONINFORMATION 操作（soap）](getfederationinformation-operation-soap.md)中进行了联合的域中返回的配置的域。  <br/> |
|[RequestedSettings （SOAP）](requestedsettings-soap.md) <br/> |包含所请求的配置设置的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsRequestMessage （SOAP）](getdomainsettingsrequestmessage-soap.md) <br/> |表示[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求。  <br/> |
   
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

