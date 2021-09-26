---
title: Request (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Request 元素包含对自动发现服务的请求。
ms.openlocfilehash: 91bc9cad6df976e8a8500eecc997f573a7df7289
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542831"
---
# <a name="request-pox"></a>Request (POX)

**Request** 元素包含对自动发现服务的请求。 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Request (POX)](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |标识自动发现响应的架构。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |标识用户的电子邮件地址。  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |按旧版可分辨名称标识用户的邮箱。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AutoDiscover (POX)](autodiscover-pox.md) <br/> |自动发现请求中的根元素。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

