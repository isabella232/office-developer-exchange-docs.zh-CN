---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: RedirectTarget (SOAP) 元素包含目标的重定向 URL 或电子邮件地址。
ms.openlocfilehash: 3a8a0c39c6889730c9d17778c6a26f84fcbcd4a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827019"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

[RedirectTarget (SOAP)](redirecttarget-soap.md)元素包含目标的重定向 URL 或电子邮件地址。 
  
```XML
<RedirectTarget/>
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
|[用户回音 (SOAP)](userresponse-soap.md) <br/> |代表对单个用户 GetUserSettings 请求的响应。  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |包含指定的域的请求的设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值包含目标的后续 GetUserSettings 应使用的重定向 URL 或电子邮件地址或 GetDomainSettings 请求。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

