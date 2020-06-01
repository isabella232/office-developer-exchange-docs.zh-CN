---
title: 响应（GetDomainSettings）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: Response 元素表示对单个域的 GetDomainSettings 调用的响应。
ms.openlocfilehash: 67fe7aea4533058fa0df972e49a2069749dc258b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455581"
---
# <a name="response-getdomainsettings-soap"></a>响应（GetDomainSettings）（SOAP）

**Response**元素表示对单个域的**GetDomainSettings**调用的响应。 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainResponses （SOAP）](domainresponses-soap.md) <br/> |包含对**GetDomainSettings**请求中请求的每个域的响应。  <br/> |
|[ErrorCode （SOAP）](errorcode-soap.md) <br/> |包含与响应关联的错误代码（如果适用）。  <br/> |
|[ErrorMessage （SOAP）](errormessage-soap.md) <br/> |包含与响应关联的错误消息（如果适用）。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsResponseMessage （SOAP）](getdomainsettingsresponsemessage-soap.md) <br/> |返回到调用方的域配置设置。  <br/> |
   
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

