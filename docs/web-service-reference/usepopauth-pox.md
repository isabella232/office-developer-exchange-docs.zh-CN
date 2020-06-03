---
title: UsePOPAuth （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: UsePOPAuth 元素指示为 POP3 帐户类型提供的身份验证信息是否也用于简单邮件传输协议（SMTP）。
ms.openlocfilehash: 8d5bfffaab31c382ad43915e18b8a7a2b2737c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466505"
---
# <a name="usepopauth-pox"></a>UsePOPAuth （POX）

**UsePOPAuth**元素指示为 POP3 帐户类型提供的身份验证信息是否也用于简单邮件传输协议（SMTP）。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[UsePOPAuth （POX）](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
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

Text 值指示为 POP3 帐户提供的身份验证信息是否也用于 SMTP。 可能的值为 **"开" 或 "** **关**"。
  
## <a name="remarks"></a>备注

仅当[Type （POX）](type-pox.md)为 SMTP 时，才使用**UsePOPAuth**元素。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

