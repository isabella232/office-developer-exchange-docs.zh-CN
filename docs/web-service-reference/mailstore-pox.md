---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: MailStore 元素包含客户端连接到用户的邮箱，使用 MAPI/HTTP 协议的规范。
ms.openlocfilehash: 4c82c7b61752cf7d91287a3968f6c642f4943855
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826301"
---
# <a name="mailstore-pox"></a>MailStore (POX)

**MailStore**元素包含客户端连接到用户的邮箱，使用 MAPI/HTTP 协议的规范。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[MailStore (POX)](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[ExternalUrl (POX)](externalurl-pox.md) <br/> |包含用于访问用户的邮箱从组织的网络外部通过 MAPI/HTTP 协议的 URL。  <br/> |
|[InternalUrl (POX)](internalurl-pox.md) <br/> |包含用于通过 MAPI/HTTP 协议访问从组织的网络内的用户的邮箱的 URL。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="remarks"></a>注解

与**Type**属性值为"mapiHttp"[协议 (POX)](protocol-pox.md)元素的响应中存在的**MailStore**元素。 
  
**MailStore**元素是可用于实现 MAPI/HTTP 协议和目标 Exchange Online、 Exchange Online 作为 Office 365 的一部分的客户端和 Exchange 开头的本地版本构建 15.00.0847.032 (Exchange Server 2013 SP1)。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

