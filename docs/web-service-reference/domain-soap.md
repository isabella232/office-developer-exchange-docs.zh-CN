---
title: Domain (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: Domain 元素包含 GetFederationInformation 响应中的联合域，或包含 GetDomainSettings 请求中请求其配置设置的域。
ms.openlocfilehash: a2e69dc845f9841931263fe90e39550bceb81ab8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520820"
---
# <a name="domain-soap"></a>Domain (SOAP)

**Domain** 元素包含 **GetFederationInformation** 响应中的联合域，或包含 **GetDomainSettings** 请求中请求其配置设置的域。 
  
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
|[Domains (SOAP)](domains-soap.md) <br/> |表示在 **GetDomainSettings** 操作中返回的配置设置的域或组织在 **GetFederationInformation** 操作中联合的域。  <br/> |
   
## <a name="text-value"></a>文本值

**Domain** 元素的文本值表示域名。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

