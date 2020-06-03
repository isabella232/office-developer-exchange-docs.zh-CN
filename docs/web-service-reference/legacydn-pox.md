---
title: LegacyDN （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: LegacyDN 元素通过旧版可分辨名称标识用户的邮箱。
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526380"
---
# <a name="legacydn-pox"></a>LegacyDN （POX）

**LegacyDN**元素通过旧版可分辨名称标识用户的邮箱。 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[请求（POX）](request-pox.md) <br/> |包含对自动发现服务的请求。  <br/> |
|[User （POX）](user-pox.md) <br/> |提供用户特定的信息。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示用户的旧电子邮件地址。
  
## <a name="remarks"></a>备注

[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)元素是自动发现请求的替代元素。 当运行 Microsoft Exchange Server 2007 的计算机上存在邮箱时，将使用此方法。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

