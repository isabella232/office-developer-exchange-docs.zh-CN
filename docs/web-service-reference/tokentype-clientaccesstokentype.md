---
title: TokenType （ClientAccessTokenType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: TokenType 元素标识将在 GetClientAccessToken 响应中返回的客户端访问令牌的类型。
ms.openlocfilehash: 49ba2973967b12396e0c7f56129c89c40ccbcf97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466050"
---
# <a name="tokentype-clientaccesstokentype"></a>TokenType （ClientAccessTokenType）

**TokenType**元素标识将在**GetClientAccessToken**响应中返回的客户端访问令牌的类型。 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[TokenRequest](tokenrequest.md)  | [令牌（ClientAccessTokenType）](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>文本值

**CallerIdentity**的文本值表示返回调用方标识客户端访问令牌。 **ExtensionCallback**的文本值表示返回一个扩展回调客户端访问令牌。 **ScopedToken**的文本值指示客户端访问令牌是作用域内的令牌。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

