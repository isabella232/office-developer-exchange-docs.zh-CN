---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: TTL 元素指定的时间生存，以小时，在此期间设置一直保持有效。
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838293"
---
# <a name="ttl-pox"></a>TTL (POX)

**TTL**元素指定的时间生存，以小时，在此期间设置一直保持有效。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到在其安装客户端访问服务器角色的 Exchange Server 2007 计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示生存时间中的设置期间保持有效的时间。 值为零表示该重新发现功能，则不需要。 如果未不指定任何值，此元素的默认值为 1 小时。
  
## <a name="remarks"></a>备注

**TTL**元素表示的时间过后，应使用自动发现请求重新发现设置。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

