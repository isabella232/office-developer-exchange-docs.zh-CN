---
title: Server (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 0ce51644-7f3a-408c-a398-814439b658dc
description: Server 元素指定邮件服务器的名称。
ms.openlocfilehash: 13673364aff111e1f330121283738119bc6041a2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517789"
---
# <a name="server-pox"></a>Server (POX)

**Server** 元素指定邮件服务器的名称。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Server (POX)](server-pox.md)
  
```xml
<Server/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行 2007 Microsoft Exchange Server安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值标识服务器。 对于 POP3、SMTP、IMAP 或 NNTP 等协议，此值将为主机名或 IP 地址。 对于 DAV 或 WEB 等协议，这将是 URL。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

