---
title: TTL （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: TTL 元素指定设置保持有效的生存时间（以小时为单位）。
ms.openlocfilehash: 9a17cbe4e669d1afe9f3ef4a24f2a9a2889a7d52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467380"
---
# <a name="ttl-pox"></a>TTL （POX）

**TTL**元素指定设置保持有效的生存时间（以小时为单位）。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[TTL （POX）](ttl-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到安装了客户端访问服务器角色的 Exchange Server 2007 计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值表示设置保持有效的生存时间（以小时为单位）。 0值表示不需要重新发现。 如果未指定任何值，则此元素的默认值为1小时。
  
## <a name="remarks"></a>备注

**TTL**元素所表示的时间过后，应使用自动发现请求 rediscovered 这些设置。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

