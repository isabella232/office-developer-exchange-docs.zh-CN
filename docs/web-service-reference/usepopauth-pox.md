---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: UsePOPAuth 元素指示为 POP3 类型的帐户提供的身份验证信息是否也用于简单邮件传输协议 (SMTP) 。
ms.openlocfilehash: 354c027bf40ddf30cda472eb4ca0d018dca64f9c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542622"
---
# <a name="usepopauth-pox"></a>UsePOPAuth (POX)

**UsePOPAuth** 元素指示为 POP3 类型的帐户提供的身份验证信息是否也用于简单邮件传输协议 (SMTP) 。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[UsePOPAuth (POX)](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
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
|[Protocol (POX)](protocol-pox.md) <br/> |包含用于将客户端连接到运行 2007 Microsoft Exchange Server安装了客户端访问服务器角色的计算机的规范。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指示为 POP3 类型的帐户提供的身份验证信息是否也用于 SMTP。 可能的值为 **on 和** **off。**
  
## <a name="remarks"></a>注解

**UsePOPAuth** 元素仅在类型为 [POX](type-pox.md) (为 SMTP) 使用。 
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

