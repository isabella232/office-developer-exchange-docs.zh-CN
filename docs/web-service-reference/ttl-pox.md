---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: TTL 元素指定生存时间（以小时表示）的设置保持有效。
ms.openlocfilehash: 6850f104fe90ae941f9d1d522fa3d3641e433c5f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515101"
---
# <a name="ttl-pox"></a>TTL (POX)

**TTL** 元素指定生存时间（以小时表示）的设置保持有效。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到安装了客户端访问Exchange Server 2007 计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示生存时间（以小时表示，在此期间设置仍然有效）。 值为零表示不需要重新发现。 如果未指定任何值，则此元素的默认值为 1 小时。
  
## <a name="remarks"></a>注解

TTL 元素表示的时间过后，应该使用自动发现请求重新发现设置。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

