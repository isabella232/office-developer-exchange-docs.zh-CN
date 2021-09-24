---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: RedirectUrl 元素包含运行 Microsoft Exchange Server 2007（已安装客户端访问服务器角色）的计算机的 URL，该角色应该用于获取自动发现设置。
ms.openlocfilehash: d515f3f79f2370dc496614bab0a3f77300ad4e30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513526"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

**RedirectUrl** 元素包含运行 Microsoft Exchange Server 2007（已安装客户端访问服务器角色）的计算机的 URL，该角色应该用于获取自动发现设置。 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[RedirectUrl (POX)](redirecturl-pox.md)
  
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
|[Account (POX)](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示客户端访问服务器的 URL，该 URL 应该用于获取自动发现设置。
  
## <a name="remarks"></a>注解

客户端应用程序应在 10 次重定向后停止重定向。
  
## <a name="see-also"></a>另请参阅



[用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)

