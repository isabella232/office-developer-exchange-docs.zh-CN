---
title: 请求（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Request 元素包含对自动发现服务的请求。
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459544"
---
# <a name="request-pox"></a>请求（POX）

**Request**元素包含对自动发现服务的请求。 
  
- [自动发现（POX）](autodiscover-pox.md) 
- [请求（POX）](request-pox.md)
  
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
|[AcceptableResponseSchema （POX）](acceptableresponseschema-pox.md) <br/> |标识自动发现响应的架构。  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |标识用户的电子邮件地址。  <br/> |
|[LegacyDN （POX）](legacydn-pox.md) <br/> |通过旧版可分辨名称标识用户的邮箱。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[自动发现（POX）](autodiscover-pox.md) <br/> |自动发现请求中的根元素。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

