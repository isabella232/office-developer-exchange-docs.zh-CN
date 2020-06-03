---
title: 类型（POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Type 元素标识配置的邮件帐户的类型。
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465098"
---
# <a name="type-pox"></a>类型（POX）

**Type**元素标识配置的邮件帐户的类型。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[协议（POX）](protocol-pox.md)
  
[类型（POX）](type-pox.md)
  
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

|**元素**|**描述**|
|:-----|:-----|
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到 Exchange 服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示邮件帐户的类型。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|EXCH  <br/> |用于连接到服务器的协议为 Exchange RPC。  <br/> |
|EXHTTP  <br/> |用于连接到服务器 RPC/HTTP 连接的协议。  <br/> |
|表达式  <br/> |用于连接到服务器的协议是 Exchange RPC over HTTP （使用 RPC 代理服务器）。  <br/> 仅当[AccountType （POX）](accounttype-pox.md)元素设置为 "电子邮件" 时，此设置才适用。  <br/> |
|网络  <br/> |通过使用在[服务器（POX）](server-pox.md)元素中指定的 URL，可以从 Web 浏览器访问电子邮件。  <br/> 仅当[AccountType （POX）](accounttype-pox.md)元素设置为 "电子邮件" 时，此设置才适用。  <br/> |
   
### <a name="version-differences"></a>版本差异

如果将服务器配置为接受 RPC/HTTP 连接，并且客户端包含包含 "ExHttpInfo" 的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头，则 Office 365、exchange Online 和本地 exchange （从 build 15.00.0995.014 开始）将返回值 "EXHTTP"。 
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

