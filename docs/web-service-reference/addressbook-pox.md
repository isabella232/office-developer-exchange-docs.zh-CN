---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: AddressBook 元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。
ms.openlocfilehash: 28de1d41146b082c8b7f82c868fbbed1ce2c483e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546796"
---
# <a name="addressbook-pox"></a>AddressBook (POX)

**AddressBook** 元素包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[AddressBook (POX)](addressbook-pox.md)
  
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
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |包含应该用于通过使用 MAPI/HTTP 协议从组织网络外部访问通讯簿的 URL。  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |包含应该用于通过使用 MAPI/HTTP 协议从组织网络内部访问通讯簿的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="remarks"></a>注解

**AddressBook** 元素存在于响应中，该响应具有 Type 属性值为"mapiHttp"的 Protocol  [ (POX)](protocol-pox.md)元素。 
  
**AddressBook** 元素可用于从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 开始，实现 MAPI/HTTP 协议和目标 Exchange Online、Exchange Online 作为 Office 365 一部分的 Exchange 本地版本的客户端。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

