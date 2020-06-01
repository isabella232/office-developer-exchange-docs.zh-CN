---
title: SMTPLast （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: SMTPLast 元素指定简单邮件传输协议（SMTP）服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。
ms.openlocfilehash: 7019da28ffa196a9abc8798aa75aff2756198da3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468430"
---
# <a name="smtplast-pox"></a>SMTPLast （POX）

**SMTPLast**元素指定简单邮件传输协议（SMTP）服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。 
  
- [自动发现（POX）](autodiscover-pox.md)
  
- [响应（POX）](response-pox.md)
  
- [帐户（POX）](account-pox.md)
  
- [协议（POX）](protocol-pox.md)
  
- [SMTPLast （POX）](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
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

该文本值指定 SMTP 服务器是否要求先下载电子邮件，然后再使用 SMTP 服务器发送电子邮件。 可能的值为 **"开" 或 "** **关**"。 默认值为**off**。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

