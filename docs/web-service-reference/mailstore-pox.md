---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: MailStore 元素包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。
ms.openlocfilehash: 543bcb8df84904f2b70d6feeabf16d1cc021f3e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511120"
---
# <a name="mailstore-pox"></a>MailStore (POX)

**MailStore** 元素包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[MailStore (POX)](mailstore-pox.md)
  
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
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |包含应该用于通过 MAPI/HTTP 协议从组织网络外部访问用户邮箱的 URL。  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |包含应该用于通过 MAPI/HTTP 协议从组织网络内部访问用户邮箱的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="remarks"></a>注解

**MailStore** 元素存在于具有 Protocol ([POX](protocol-pox.md)) Type 属性值为"mapiHttp"的响应中。  
  
**MailStore** 元素可用于从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 起实现 MAPI/HTTP 协议和目标 Exchange Online、Exchange Online 作为 Office 365 一部分的 Exchange 本地版本的客户端。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

