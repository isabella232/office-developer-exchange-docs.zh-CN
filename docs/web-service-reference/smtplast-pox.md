---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: SMTPLast 元素指定的简单邮件传输协议 (SMTP) 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。
ms.openlocfilehash: 5359f20b33855f4ef48566058bc46bd618e3b2ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827505"
---
# <a name="smtplast-pox"></a>SMTPLast (POX)

**SMTPLast**元素指定的简单邮件传输协议 (SMTP) 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。 
  
- [自动发现 (POX)](autodiscover-pox.md)
  
- [响应 (POX)](response-pox.md)
  
- [帐户 (POX)](account-pox.md)
  
- [协议 (POX)](protocol-pox.md)
  
- [SMTPLast (POX)](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定 SMTP 服务器是否要求使用 SMTP 服务器发送电子邮件之前下载的电子邮件。 可能的值为**在**打开和**关闭**。 默认值已**关闭**。
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

