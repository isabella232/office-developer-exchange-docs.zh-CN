---
title: InternalUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: InternalUrl 元素包含通过 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱内部的 URL。
ms.openlocfilehash: 9c6ba621a681ec54d88089de6b7ae1eefdebc679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465574"
---
# <a name="internalurl-pox"></a>InternalUrl （POX）

**InternalUrl**元素包含通过 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱内部的 URL。 
  
```XML
<InternalUrl/>
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
|[AddressBook （POX）](addressbook-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。  <br/> |
|[MailStore （POX）](mailstore-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示可用于从用户的组织中访问通讯簿服务器或用户邮箱的 URL。
  
## <a name="remarks"></a>备注

**InternalUrl**元素可以出现在具有**Type**属性值为 "mapi" 的[Protocol （POX）](protocol-pox.md)元素的响应中。 
  
**InternalUrl**元素可用于实现 MAPI/HTTP 协议和目标 exchange online 的客户端、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 build 15.00.0847.032 （exchange SERVER 2013 SP1）开始。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

