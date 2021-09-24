---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: LegacyDN 元素按旧版可分辨名称标识用户的邮箱。
ms.openlocfilehash: bd65e18daf1b05f66ebd767635cbe6a3135f1abf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540830"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

**LegacyDN** 元素按旧版可分辨名称标识用户的邮箱。 
  
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
|[Request (POX)](request-pox.md) <br/> |包含对自动发现服务的请求。  <br/> |
|[User (POX)](user-pox.md) <br/> |提供特定于用户的信息。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用户的旧电子邮件地址。
  
## <a name="remarks"></a>注解

[EmailAddress (NonEmptyStringType) ](emailaddress-nonemptystringtype.md)元素是自动发现请求的备用元素。 当邮箱存在于运行 2007 年 2007 Microsoft Exchange Server使用。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

