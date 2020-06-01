---
title: AddressBook （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: AddressBook 元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。
ms.openlocfilehash: 0967ac123cd3bb0086fd004ea0d0d37c08d2e037
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463634"
---
# <a name="addressbook-pox"></a>AddressBook （POX）

**AddressBook**元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[AddressBook （POX）](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ExternalUrl （POX）](externalurl-pox.md) <br/> |包含从组织网络外部使用 MAPI/HTTP 协议访问通讯簿时应使用的 URL。  <br/> |
|[InternalUrl （POX）](internalurl-pox.md) <br/> |包含从组织的网络中使用 MAPI/HTTP 协议访问通讯簿时应使用的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="remarks"></a>备注

**AddressBook**元素存在于具有**Type**属性值为 "mapi" 的[Protocol （POX）](protocol-pox.md)元素的响应中。 
  
**AddressBook**元素可用于实现 MAPI/HTTP 协议和目标 exchange online 的客户端、exchange online （作为 Office 365 的一部分）和 exchange online 版本（从 build 15.00.0847.032 （exchange SERVER 2013 SP1）开始。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

