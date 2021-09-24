---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: NetworkRequirements 元素包含用于确定客户端计算机是否位于满足 Internet 服务提供商 (ISP) 要求以连接到服务器的网络上的条件。
ms.openlocfilehash: 07a258ad48b74c614ce367db0f893ed884cf3f75
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509510"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

**NetworkRequirements** 元素包含用于确定客户端计算机是否位于满足 Internet 服务提供商 (ISP) 要求的网络以连接到服务器的条件。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |标识用于标识网络上计算机的 IP 版本 4 (IPv4) 范围的起始位置。  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |标识用于标识网络上计算机的 IP 版本 4 (IPv4) 地址的末尾。  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |标识用于标识网络上计算机的 IP 版本 6 (IPv6) 范围的起始位置。  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |标识用于标识网络上计算机的 IP 版本 6 (IPv6) 地址的末尾。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行 2007 Microsoft Exchange Server安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="remarks"></a>注解

如果电子邮件客户端不符合网络要求，则它应尝试其他协议类型。 ISP 可能会为一组服务器提供协议 [ (POX ](protocol-pox.md)) 标记，这些标记不需要身份验证，但需要位于 ISP 网络上。 ISP 可能会列出另一组需要身份验证但不要求位于特定网络的服务器。 
  
**NetworkRequirements** 元素是可选的。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

