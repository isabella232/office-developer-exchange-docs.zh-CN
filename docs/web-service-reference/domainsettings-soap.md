---
title: DomainSettings （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f3d37f5a-c9ea-4ed9-a011-94d33bda64d1
description: DomainSettings 元素表示在自动发现请求中提交或由自动发现响应返回的域设置。
ms.openlocfilehash: 67e3753b0cf5c7c653664ff087f697ce7ae2b7a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530696"
---
# <a name="domainsettings-soap"></a>DomainSettings （SOAP）

**DomainSettings**元素表示在自动发现请求中提交或由自动发现响应返回的域设置。 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 **DomainSettings**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainSetting （SOAP）](domainsetting-soap.md) <br/> |包含由[GetDomainSettings 操作（SOAP）](getdomainsettings-operation-soap.md)请求返回的域设置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[DomainResponse （SOAP）](domainresponse-soap.md) <br/> |包含指定域的请求的设置。  <br/> |
   
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

