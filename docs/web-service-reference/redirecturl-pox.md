---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: RedirectUrl 元素包含的计算机的运行 Microsoft Exchange Server 2007 的客户端访问服务器安装了角色，用于获取自动发现设置的 URL。
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827027"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

**RedirectUrl**元素包含的计算机的运行 Microsoft Exchange Server 2007 的客户端访问服务器安装了角色，用于获取自动发现设置的 URL。 
  
[自动发现 (POX)](autodiscover-pox.md)
  
[响应 (POX)](response-pox.md)
  
[帐户 (POX)](account-pox.md)
  
[RedirectUrl (POX)](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
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
|[帐户 (POX)](account-pox.md) <br/> |指定用户帐户的设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示用于获取自动发现设置客户端访问服务器的 URL。
  
## <a name="remarks"></a>备注

客户端应用程序应停止 10 次重定向后重定向。
  
## <a name="see-also"></a>另请参阅



[Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

