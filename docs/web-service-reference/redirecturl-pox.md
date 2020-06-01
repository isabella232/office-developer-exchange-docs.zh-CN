---
title: RedirectUrl （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: RedirectUrl 元素包含运行 Microsoft Exchange Server 2007 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。
ms.openlocfilehash: 5400b1e7a4bb7ebebc58b6a0f1fc9bf37f5a2e22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468087"
---
# <a name="redirecturl-pox"></a>RedirectUrl （POX）

**RedirectUrl**元素包含运行 Microsoft Exchange server 2007 且安装了应用于获取自动发现设置的客户端访问服务器角色的计算机的 URL。 
  
[自动发现（POX）](autodiscover-pox.md)
  
[响应（POX）](response-pox.md)
  
[帐户（POX）](account-pox.md)
  
[RedirectUrl （POX）](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
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
|[帐户（POX）](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值表示应用于获取自动发现设置的客户端访问服务器的 URL。
  
## <a name="remarks"></a>备注

客户端应用程序应在10次重定向后停止重定向。
  
## <a name="see-also"></a>另请参阅



[Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

