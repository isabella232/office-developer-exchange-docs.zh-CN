---
title: Type (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Type 元素标识已配置的邮件帐户的类型。
ms.openlocfilehash: bb92913071509fec46736341bce56b1a00730f6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517523"
---
# <a name="type-pox"></a>Type (POX)

**Type** 元素标识已配置的邮件帐户的类型。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Type (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示邮件帐户的类型。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|EXCH  <br/> |用于连接到服务器的协议由 RPC Exchange。  <br/> |
|EXHTTP  <br/> |用于连接到服务器 RPC/HTTP 连接的协议。  <br/> |
|EXPR  <br/> |用于连接到服务器的协议通过 HTTP Exchange RPC over HTTP。  <br/> This is only applicable when the [AccountType (POX) ](accounttype-pox.md) element is set to email.  <br/> |
|WEB  <br/> |通过使用 Server (POX) 元素中指定的 URL，从 Web [浏览器访问 ](server-pox.md) 电子邮件。  <br/> This is only applicable when the [AccountType (POX) ](accounttype-pox.md) element is set to email.  <br/> |
   
### <a name="version-differences"></a>版本差异

Office 365版本 15.00.0995.014 的 Exchange、Exchange Online 和本地版本仅在服务器配置为接受 RPC/HTTP 连接并且客户端包含包含"ExHttpInfo"的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头时，才返回"EXHTTP"值。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

