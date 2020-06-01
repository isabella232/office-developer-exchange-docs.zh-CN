---
title: MailStore （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: MailStore 元素包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。
ms.openlocfilehash: 635228fcfeb3ad791c845050b82666a6e060b229
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459789"
---
# <a name="mailstore-pox"></a>MailStore （POX）

**MailStore**元素包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[MailStore （POX）](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ExternalUrl （POX）](externalurl-pox.md) <br/> |包含用于通过 MAPI/HTTP 协议从组织的网络外部访问用户邮箱的 URL。  <br/> |
|[InternalUrl （POX）](internalurl-pox.md) <br/> |包含用于通过 MAPI/HTTP 协议从组织的网络中访问用户邮箱的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="remarks"></a>备注

**MailStore**元素存在于具有**Type**属性值为 "mapi" 的[Protocol （POX）](protocol-pox.md)元素的响应中。 
  
**MailStore**元素可用于实现 MAPI/HTTP 协议和目标 exchange online 的客户端、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 build 15.00.0847.032 （exchange SERVER 2013 SP1）开始。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

