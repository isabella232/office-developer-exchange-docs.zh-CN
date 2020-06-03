---
title: NetworkRequirements （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: NetworkRequirements 元素包含用于确定客户端计算机是否在满足 Internet 服务提供商（ISP）的要求以连接到服务器的网络上的条件。
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462722"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements （POX）

**NetworkRequirements**元素包含用于确定客户端计算机是否在满足 Internet 服务提供商（ISP）的要求以连接到服务器的网络上的条件。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[NetworkRequirements （POX）](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IPv4Start （POX）](ipv4start-pox.md) <br/> |标识用于标识网络上的计算机的 IP 版本4（IPv4）地址范围的起始地址。  <br/> |
|[IPv4End （POX）](ipv4end-pox.md) <br/> |标识用于标识网络上的计算机的 IP 版本4（IPv4）地址范围的结束地址。  <br/> |
|[IPv6Start （POX）](ipv6start-pox.md) <br/> |标识用于标识网络上的计算机的 IP 版本6（IPv6）地址范围的起始地址。  <br/> |
|[IPv6End （POX）](ipv6end-pox.md) <br/> |标识用于标识网络上的计算机的 IP 版本6（IPv6）地址范围的结束。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="remarks"></a>备注

如果电子邮件客户端不符合网络要求，它应尝试其他协议类型。 Isp 可以为一组具有[协议（POX）](protocol-pox.md)标记的服务器提供不需要进行身份验证，但必须在 ISP 网络中进行身份验证的服务器。 Isp 可能列出了需要进行身份验证但不需要在特定网络上的另一组服务器。 
  
**NetworkRequirements**元素是可选的。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

