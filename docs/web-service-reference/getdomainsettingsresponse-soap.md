---
title: GetDomainSettingsResponse （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: GetDomainSettingsResponse 元素表示对 GetDomainSettings 操作（SOAP）的响应，该操作返回域设置。
ms.openlocfilehash: 94cb202948e6a0d5a34f5547132c052d1d1b6a40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461875"
---
# <a name="getdomainsettingsresponse-soap"></a>GetDomainSettingsResponse （SOAP）

**GetDomainSettingsResponse**元素表示对[GETDOMAINSETTINGS 操作（SOAP）](getdomainsettings-operation-soap.md)的响应，该操作返回域设置。
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainResponses （SOAP）](domainresponses-soap.md) <br/> |包含每个请求域的设置的响应数组。  <br/> |
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |表示自动发现服务返回的错误代码。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |表示与自动发现服务返回的错误代码相关联的消息。  <br/> |
   
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

