---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: RedirectTarget (SOAP) 元素包含重定向 URL 或电子邮件地址的目标。
ms.openlocfilehash: 0e09529f62dfde66f1ef05875bb0b0a0886db452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513540"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

[RedirectTarget (SOAP) ](redirecttarget-soap.md)元素包含重定向 URL 或电子邮件地址的目标。 
  
```XML
<RedirectTarget/>
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
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |表示对单个用户的 GetUserSettings 请求的响应。  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |包含指定域的请求设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值包含应用于后续 GetUserSettings 或 GetDomainSettings 请求的重定向 URL 或电子邮件地址的目标。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|架构名称  <br/> |自动发现架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |True  <br/> |
   

