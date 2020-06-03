---
title: AuthPackage （POX）
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: AuthPackage 元素指定在对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459102"
---
# <a name="authpackage-pox"></a>AuthPackage （POX）

**AuthPackage**元素指定在对安装了邮箱服务器角色的 Exchange 服务器进行身份验证时使用的身份验证方案。 
  
- [自动发现（POX）](autodiscover-pox.md)
  
- [响应（POX）](response-pox.md)
  
- [帐户（POX）](account-pox.md)
  
- [协议（POX）](protocol-pox.md)
  
- [AuthPackage （POX）](authpackage-pox.md)
  
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
|[协议（POX）](protocol-pox.md) <br/> |包含用于将客户端连接到客户端访问服务器的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定在对邮箱服务器进行身份验证时使用的身份验证方案。 以下是可能的值：
  
- vba
- kerb
- kerbntlm
- ntlm
- 证书
- 沟通
- nego2
    
## <a name="remarks"></a>备注

仅当[Type （POX）](type-pox.md)元素的 text 值为 EXCH 或 EXPR 时，才使用**AuthPackage**元素。 
  
### <a name="version-differences"></a>版本差异

如果将服务器配置为使用协商身份验证，并且客户端包含包含 "协商" 的[X-ClientCanHandle](pox-autodiscover-request-for-exchange.md)标头，则从生成15.00.0995.014 开始的 Office 365、exchange Online 和本地版本将返回 "negotiate" 值。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

