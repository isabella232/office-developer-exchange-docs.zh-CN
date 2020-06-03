---
title: Action （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a3462c6b-453c-462a-830d-f29ee4a2babb
description: Action 元素提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。
ms.openlocfilehash: f6d542b908948d09020b850b60ca1bdb025dd342
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529691"
---
# <a name="action-pox"></a>Action （POX）

**Action**元素提供用于确定是否需要其他自动发现请求来返回用户配置信息的信息。 
  
- [自动发现（POX）](autodiscover-pox.md)
  
- [响应（POX）](response-pox.md)
  
- [帐户（POX）](account-pox.md)
  
- [Action （POX）](action-pox.md)
  
```xml
<Action>redirectUrl or redirectAddr or settings</Action>
```

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**描述**|
|:-----|:-----|
|[帐户（POX）](account-pox.md) <br/> |指定用户的帐户设置。  <br/> |
   
## <a name="text-value"></a>文本值

Text 值表示检索用户的配置信息是否需要其他自动发现请求。 下表列出了可能的值。
  
|**值**|**说明**|
|:-----|:-----|
|redirectUrl  <br/> |如果指定此值， [RedirectUrl （POX）](redirecturl-pox.md)元素将指定要在后续自动发现请求中使用的客户端访问服务器 URL。 客户端应用程序应在10次重定向后停止重定向。  <br/> |
|redirectAddr  <br/> |如果指定此值， [RedirectAddr （POX）](redirectaddr-pox.md)元素将指定应用于后续自动发现请求的电子邮件地址。  <br/> |
|settings  <br/> |如果指定此值，自动发现响应将包含用于配置帐户的设置。 大部分设置都将在[Protocol （POX）](protocol-pox.md)元素中找到。  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)

