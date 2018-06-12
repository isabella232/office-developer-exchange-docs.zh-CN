---
title: 域 (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: 域元素包含 GetFederationInformation 响应中的联盟的域或包含 GetDomainSettings 请求中请求为其配置设置的域。
ms.openlocfilehash: 411ca866800322ef06eeecc2ab92adc6f711917c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753971"
---
# <a name="domain-soap"></a>域 (SOAP)

**域**元素包含**GetFederationInformation**响应中的联盟的域或包含**GetDomainSettings**请求中请求为其配置设置的域。 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[域 (SOAP)](domains-soap.md) <br/> |代表**GetDomainSettings**操作中返回的配置设置的域或组织具有联合**GetFederationInformation**操作中的域。  <br/> |
   
## <a name="text-value"></a>文本值

**域**元素的文本值表示的域名。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

