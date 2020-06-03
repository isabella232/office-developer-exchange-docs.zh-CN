---
title: DomainResponses （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: DomainResponses 元素包含每个请求的域的设置的响应数组。
ms.openlocfilehash: 2c76b9691fe88657a65130ef6829e5af64380d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526317"
---
# <a name="domainresponses-soap"></a>DomainResponses （SOAP）

**DomainResponses**元素包含每个请求的域的设置的响应数组。 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 **ArrayOfDomainResponse**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainResponse （SOAP）](domainresponse-soap.md) <br/> |包含指定域的请求的设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetDomainSettingsResponse （SOAP）](getdomainsettingsresponse-soap.md) <br/> |表示对域的[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求的响应，并返回域设置。  <br/> |
|[响应（GetDomainSettings）（SOAP）](response-getdomainsettingssoap.md) <br/> |表示对单个域的[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)调用的响应。  <br/> |
   
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

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)

