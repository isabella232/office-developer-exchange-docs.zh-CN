---
title: Request (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: Request 元素包含返回域设置的请求。
ms.openlocfilehash: fbee6479b844ac9026b0cfc0218cdc542ea0f2fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540543"
---
# <a name="request-getdomainsettings-soap"></a>Request (GetDomainSettings) (SOAP)

**Request** 元素包含返回域设置的请求。 
  
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
|[Domains (SOAP)](domains-soap.md) <br/> |表示在 [GetDomainSettings ](getdomainsettings-operation-soap.md) 操作 (SOAP) 中返回的配置或组织在 [GetFederationInformation ](getfederationinformation-operation-soap.md)操作 (SOAP) 中联合的域。  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |包含请求的配置设置的名称。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md) <br/> |表示 SOAP 请求 [ (GetDomainSettings) ](getdomainsettings-operation-soap.md)操作。  <br/> |
   
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

