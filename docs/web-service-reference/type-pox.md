---
title: 类型 (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Type 元素标识配置的邮件帐户的类型。
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838295"
---
# <a name="type-pox"></a>类型 (POX)

**Type**元素标识配置的邮件帐户的类型。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[协议 (POX)](protocol-pox.md)
  
[类型 (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示的邮件帐户的类型。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|EXCH  <br/> |用于连接到服务器的协议是 Exchange RPC。  <br/> |
|EXHTTP  <br/> |用于连接到服务器的 RPC/HTTP 连接协议。  <br/> |
|EXPR  <br/> |用于连接到服务器的协议是 Exchange RPC over HTTP，使用 RPC 代理服务器。  <br/> [AccountType (POX)](accounttype-pox.md)元素设置为电子邮件时，这是仅适用。  <br/> |
|WEB  <br/> |电子邮件从 Web 浏览器访问使用[服务器 (POX)](server-pox.md)元素中指定的 URL。  <br/> [AccountType (POX)](accounttype-pox.md)元素设置为电子邮件时，这是仅适用。  <br/> |
   
### <a name="version-differences"></a>版本差异

Office 365 和 Exchange Online 中，在本地版本的 Exchange 开头构建 15.00.0995.014 返回的值为"EXHTTP"才将服务器配置为接受 RPC/HTTP 连接和客户端包括[X ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头的包含"ExHttpInfo"。 
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

