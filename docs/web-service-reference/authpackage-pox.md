---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: AuthPackage 元素指定针对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753294"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

**AuthPackage**元素指定针对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。 
  
- [自动发现 (POX)](autodiscover-pox.md)
  
- [响应 (POX)](response-pox.md)
  
- [帐户 (POX)](account-pox.md)
  
- [协议 (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定对邮箱服务器进行身份验证时使用的身份验证方案。 以下是可能的值：
  
- 基本
- kerb
- kerbntlm
- ntlm
- certificate
- 协商
- nego2
    
## <a name="remarks"></a>注解

[类型 (POX)](type-pox.md)元素的文本值为 EXCH 或 EXPR 时才使用**AuthPackage**元素。 
  
### <a name="version-differences"></a>版本差异

Office 365 和 Exchange Online 中，在本地版本的 Exchange 开头构建 15.00.0995.014 返回的值为"协商"才将服务器配置为使用协商身份验证和客户端包括[X ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头的包含"协商"。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

