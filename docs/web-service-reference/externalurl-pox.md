---
title: ExternalUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: ExternalUrl 元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱外部的 URL。
ms.openlocfilehash: 94265051be68ed06d1dab8d46dd4ce29d8694c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457954"
---
# <a name="externalurl-pox"></a>ExternalUrl （POX）

**ExternalUrl**元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器或用户邮箱外部的 URL。 
  
```XML
<ExternalUrl/>
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

文本值表示可用于从用户组织外部访问通讯簿服务器或用户邮箱的 URL。
  
## <a name="remarks"></a>备注

**ExternalUrl**元素可以出现在具有**Type**属性值为 "mapi" 的[Protocol （POX）](protocol-pox.md)元素的响应中。 
  
**ExternalUrl**元素可用于实现 MAPI/HTTP 协议和目标 exchange online 的客户端、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 build 15.00.0847.032 （exchange SERVER 2013 SP1）开始。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

