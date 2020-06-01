---
title: 域（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Domain 元素在 GetFederationInformation 响应中包含一个联合域，或者包含一个域，在 GetDomainSettings 请求中请求的配置设置。
ms.openlocfilehash: f90c608ee1fc3356a227bca6411eaeff0c1e8b22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456981"
---
# <a name="domain-soap"></a>域（SOAP）

**Domain**元素在**GetFederationInformation**响应中包含一个联合域，或者包含一个域，在**GetDomainSettings**请求中请求的配置设置。 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[域（SOAP）](domains-soap.md) <br/> |表示在**GetDomainSettings**操作中返回的配置设置或组织在**GetFederationInformation**操作中联合的域的域。  <br/> |
   
## <a name="text-value"></a>文本值

**Domain**元素的文本值表示一个域的名称。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

