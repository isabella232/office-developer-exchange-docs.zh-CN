---
title: AuthRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 241a23ee-d2a2-4724-b794-d0d523d480a2
description: AuthRequired 元素指定是否需要身份验证。
ms.openlocfilehash: b747f53766b6b914955c5e41b63462b9b44bff4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753299"
---
# <a name="authrequired-pox"></a>AuthRequired (POX)

**AuthRequired**元素指定是否需要身份验证。 
  
- [自动发现 (POX)](autodiscover-pox.md)
  
- [响应 (POX)](response-pox.md)
  
- [帐户 (POX)](account-pox.md)
  
- [协议 (POX)](protocol-pox.md)
  
- [AuthRequired (POX)](authrequired-pox.md)
  
```xml
<AuthRequired>on or off</AuthRequired>
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
|[协议 (POX)](protocol-pox.md) <br/> |包含客户端连接到运行 Microsoft Exchange Server 2007 的安装了客户端访问服务器角色的计算机的规格。  <br/> |
   
## <a name="text-value"></a>文本值

文本值指定是否需要身份验证。 可能的值为**在**打开和**关闭**。 如果不指定一个值，则默认值是**在上**。 
  
## <a name="see-also"></a>另请参阅

- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

