---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: CertPrincipalName 元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层 (SSL) 证书主体名称。
ms.openlocfilehash: 69ee49cdad09032c269ffbbcc918044daf61cb9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523249"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

**CertPrincipalName** 元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层 (SSL) 证书主体名称。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行 2007 Exchange客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定使用 SSL 连接到 Microsoft Exchange所需的 SSL 证书主体名称。
  
## <a name="remarks"></a>注解

如果 **未指定 CertPrincipalName** 元素，则默认设置为 msstd：SERVER，其中 SERVER 是 [Server (POX) 元素中指定的](server-pox.md) 值。 例如，如果将 SERVER 指定为 example.com 且 **CertPrincipalName** 留空，同时 [启用 SSL (POX) ，](ssl-pox.md)**则 CertPrincipalName** 的默认值为 msstd：example.com。 
  
如果 **未指定**，Windows MSDN 上的主体名称主题中的信息 [验证](https://go.microsoft.com/fwlink/?LinkId=93417)证书主体名称。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

