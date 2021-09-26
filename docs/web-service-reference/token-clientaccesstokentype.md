---
title: Token (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cddd6075-06b6-4858-9ffa-9db4d9d9b030
description: Token 元素指定客户端访问令牌。
ms.openlocfilehash: b9cd0887d082c2ddd9abe0505ebec993f0261fad
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545732"
---
# <a name="token-clientaccesstokentype"></a>Token (ClientAccessTokenType)

**Token** 元素指定客户端访问令牌。 
  
```XML
<Token>
   <Id/>
   <TokenType/>
   <TokenValue/>
   <TTL/>
</Token>
```

 **ClientAccessTokenType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[ID (String) ](id-string.md)  | [TokenType](tokentype.md)  | [TokenValue](tokenvalue.md)  | [TTL](ttl.md)
  
### <a name="parent-elements"></a>父元素

[GetClientAccessTokenResponseMessage](getclientaccesstokenresponsemessage.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

