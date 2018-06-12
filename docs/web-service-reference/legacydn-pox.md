---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: LegacyDN 元素标识用户的邮箱的旧的可分辨名称。
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826243"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

**LegacyDN**元素标识用户的邮箱的旧的可分辨名称。 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[请求 (POX)](request-pox.md) <br/> |包含对自动发现服务的请求。  <br/> |
|[用户 (POX)](user-pox.md) <br/> |提供特定于用户的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的旧的电子邮件地址。
  
## <a name="remarks"></a>备注

[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)元素是自动发现请求的其他元素。 运行 Microsoft Exchange Server 2007 的计算机上存在的邮箱时使用它。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

