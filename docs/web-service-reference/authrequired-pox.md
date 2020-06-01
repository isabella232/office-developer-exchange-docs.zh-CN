---
title: Resolver.rst.authrequired （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 241a23ee-d2a2-4724-b794-d0d523d480a2
description: Resolver.rst.authrequired 元素指定是否需要身份验证。
ms.openlocfilehash: 25e3aff6a6db719c7f466e30fd6166e602f2d418
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461623"
---
# <a name="authrequired-pox"></a>Resolver.rst.authrequired （POX）

**Resolver.rst.authrequired**元素指定是否需要身份验证。 
  
- [自动发现（POX）](autodiscover-pox.md)
  
- [响应（POX）](response-pox.md)
  
- [帐户（POX）](account-pox.md)
  
- [协议（POX）](protocol-pox.md)
  
- [Resolver.rst.authrequired （POX）](authrequired-pox.md)
  
```xml
<AuthRequired>on or off</AuthRequired>
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到运行 Microsoft Exchange Server 2007 且安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值指定是否需要身份验证。 可能的值为 **"开" 或 "** **关**"。 如果未指定值，则默认值为**on**。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

