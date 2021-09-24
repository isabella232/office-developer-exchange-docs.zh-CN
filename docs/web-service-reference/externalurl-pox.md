---
title: ExternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: ExternalUrl 元素包含用于通过使用 MAPI/HTTP 协议从用户组织外部将客户端连接到通讯簿服务器或用户邮箱的 URL。
ms.openlocfilehash: 90aaf9cabedba4ea89e0ed47da010245006407ba
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510070"
---
# <a name="externalurl-pox"></a>ExternalUrl (POX)

**ExternalUrl** 元素包含用于通过使用 MAPI/HTTP 协议从用户组织外部将客户端连接到通讯簿服务器或用户邮箱的 URL。 
  
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
|[AddressBook (POX)](addressbook-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到通讯簿服务器的规范。  <br/> |
|[MailStore (POX)](mailstore-pox.md) <br/> |包含使用 MAPI/HTTP 协议将客户端连接到用户邮箱的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示可用于从用户组织外部访问通讯簿服务器或用户邮箱的 URL。
  
## <a name="remarks"></a>注解

**ExternalUrl** 元素可以存在于具有 [Protocol (POX](protocol-pox.md)) Type 属性值为"mapiHttp"的响应中。 
  
**ExternalUrl** 元素可用于从内部版本 15.00.0847.032 (Exchange Server 2013 SP1) 开始，实现 MAPI/HTTP 协议和目标 Exchange Online、Exchange Online 作为 Office 365 一部分的 Exchange 本地版本的客户端。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

