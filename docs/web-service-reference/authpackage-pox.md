---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: AuthPackage 元素指定对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时所使用的身份验证方案。
ms.openlocfilehash: aff4e84cd44d76c2c5a913b6627e1b0c87bab4dc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513022"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

**AuthPackage** 元素指定对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时所使用的身份验证方案。 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Protocol (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定对邮箱服务器进行身份验证时所使用的身份验证方案。 以下是可能的值：
  
- basic
- kerb
- kerbntlm
- ntlm
- 证书
- negotiate
- nego2
    
## <a name="remarks"></a>注解

**AuthPackage** 元素仅在 TYPE ([POX](type-pox.md)) 具有 EXCH 或 EXPR 的文本值时使用。 
  
### <a name="version-differences"></a>版本差异

Office 365 15.00.0995.014 起，Exchange 的 Exchange、Exchange Online 和本地版本仅在服务器配置为使用协商身份验证且客户端包括包含"Negotiate"的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头时，才返回"negotiate"值。 
  
## <a name="see-also"></a>另请参阅

- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

