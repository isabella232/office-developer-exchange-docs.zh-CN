---
title: CertPrincipalName （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: CertPrincipalName 元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层（SSL）证书主体名称。
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463340"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName （POX）

**CertPrincipalName**元素指定使用 SSL 连接到 Microsoft Exchange Server 2007 组织所需的安全套接字层（SSL）证书主体名称。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[CertPrincipalName （POX）](certprincipalname-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到运行 Exchange 2007 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值指定使用 SSL 连接到 Microsoft Exchange 组织所需的 SSL 证书主体名称。
  
## <a name="remarks"></a>备注

如果未指定**CertPrincipalName**元素，则默认设置为 MSSTD： server，其中的 server 是在[服务器（POX）](server-pox.md)元素中指定的值。 例如，如果将 SERVER 指定为 example.com，并将**CertPrincipalName**保留为空，并且[SSL （POX）](ssl-pox.md)打开，则**CertPrincipalName**的默认值为 msstd:example .com。 
  
如果**未指定，则 Windows**将根据 MSDN 上的[主体名称](https://go.microsoft.com/fwlink/?LinkId=93417)主题中的信息来验证证书主体名称。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

