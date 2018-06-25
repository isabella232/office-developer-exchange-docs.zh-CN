---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: CertPrincipalName 元素指定需要使用 SSL 连接到 Microsoft Exchange Server 2007 组织的安全套接字层 (SSL) 证书主体名称。
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753444"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

**CertPrincipalName**元素指定需要使用 SSL 连接到 Microsoft Exchange Server 2007 组织的安全套接字层 (SSL) 证书主体名称。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到计算机上运行安装了客户端访问服务器角色的 Exchange 2007 的技术指标。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定使用 SSL 连接到 Microsoft Exchange 组织所需的 SSL 证书主体名称。
  
## <a name="remarks"></a>注解

如果未指定**CertPrincipalName**元素，则默认设置为 msstd:SERVER，其中的 SERVER 是[服务器 (POX)](server-pox.md)元素中指定的值。 例如，如果服务器指定为 example.com 和**CertPrincipalName**与开启[SSL (POX)](ssl-pox.md)保留为空，则**CertPrincipalName**的默认值将为 msstd:example.com。 
  
如果**未**指定，Windows 将验证根据在 MSDN 上的[主体名称](http://go.microsoft.com/fwlink/?LinkId=93417)主题中找到的信息的证书主体名称。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

