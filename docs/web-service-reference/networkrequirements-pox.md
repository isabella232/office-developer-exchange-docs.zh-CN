---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: NetworkRequirements 元素包含用于确定客户端计算机是否满足 Internet 服务提供程序 (ISP) 的要求连接到服务器的网络上的条件。
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826529"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

**NetworkRequirements**元素包含用于确定客户端计算机是否满足 Internet 服务提供程序 (ISP) 的要求连接到服务器的网络上的条件。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[NetworkRequirements (POX)](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |标识的范围内的 IP 版本 4 (IPv4) 开始用于标识网络上的计算机的地址。  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |标识的末尾的范围内的 IP 版本 4 (IPv4) 用于标识网络上的计算机的地址。  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |标识的范围内的 IP 版本 6 (IPv6) 开始用于标识网络上的计算机的地址。  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |标识的末尾的范围内的 IP 版本 6 (IPv6) 用于标识网络上的计算机的地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="remarks"></a>备注

如果电子邮件客户端不匹配的网络要求，它应尝试其他协议类型。 Isp 可以提供一组具有[协议 (POX)](protocol-pox.md)标记不需要身份验证但所需的 ISP 网络上的服务器。 Isp 可以列出服务器要求身份验证，但不是需要位于特定的网络上的另一的组。 
  
**NetworkRequirements**元素是可选的。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

