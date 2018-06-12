---
title: TokenType (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: TokenType 元素标识将 GetClientAccessToken 响应中返回的客户端访问令牌的类型。
ms.openlocfilehash: c9adb60acf76fefebd58e2fd3bc899332a63dbee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838261"
---
# <a name="tokentype-clientaccesstokentype"></a>TokenType (ClientAccessTokenType)

**TokenType**元素标识将**GetClientAccessToken**响应中返回的客户端访问令牌的类型。 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[TokenRequest](tokenrequest.md) | [令牌 (ClientAccessTokenType)](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>文本值

**CallerIdentity**文本值意味着返回呼叫者标识客户端访问令牌。 文本值的**ExtensionCallback**表明返回扩展回调客户端访问令牌。 **ScopedToken**文本值指示客户端访问令牌的作用域的令牌。 
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

